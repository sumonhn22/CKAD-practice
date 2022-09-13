# Exercise 12

In this exercise, you will create a Deployment with multiple replicas. After inspecting the Deployment, you will update its parameters. Furthermore, you will use the rollout history to roll back to a previous revision.

> **_NOTE:_** If you do not already have a cluster, you can create one by using minikube or you can use the Katacoda scenarios ["Creating and Manually Scaling a Deployment"](https://learning.oreilly.com/scenarios/6-5-ckad-deployments/9781098105235/) and ["Rolling Out a New Revision for a Deployment"](https://learning.oreilly.com/scenarios/6-6-ckad-deployments/9781098105242/).

## Performing Rolling Updates for a Deployment

1. Create a Deployment named `deploy` with 3 replicas. The Pods should use the `nginx` image and the name `nginx`. The Deployment uses the label `tier=backend`. The Pods should use the label `app=v1`.
2. List the Deployment and ensure that the correct number of replicas is running.
3. Update the image to `nginx:latest`.
4. Verify that the change has been rolled out to all replicas.
5. Scale the Deployment to 5 replicas.
6. Have a look at the Deployment rollout history.
7. Revert the Deployment to revision 1.
8. Ensure that the Pods use the image `nginx`.
9. (Optional) Discuss: Can you foresee potential issues with a rolling deployment? How do you configure a update process that first kills all existing containers with the current version before it starts containers with the new version?