## Exercise 1

Set up a multi-node Kubernetes cluster using kubeadm. Ensure high availability by adding an additional control plane node.

### Requirements:
- At least 3 nodes
- kubeadm, kubectl, and container runtime installed

### Steps:
1. Initialize the control plane.
2. Add worker nodes.
3. Verify the cluster state.

<details>
  <summary><strong>Solution</strong></summary>

1. Run `kubeadm init` on the first control plane node.
2. Join worker nodes using the token provided by kubeadm.
3. Add additional control plane nodes using `kubeadm join --control-plane`.

</details>
