# virtio

<p>int virtqueue_notify_enabled(struct virtqueue *vq)
{
	struct virtqueue_vring *vrq;

	UK_ASSERT(vq);
	vrq = to_virtqueue_vring(vq);

	return ((vrq->vring.used->flags & VRING_USED_F_NO_NOTIFY) == 0);
}</p>