**Vote_CI_CD.yaml:** 

Step 1:
Trigger the pipeline from the main branch when relevant changes are detected. The pipeline is configured to run only if files or folders under main are modified, ensuring controlled and efficient executions.

Step 2:
Select the target Git repository where application or configuration changes need to be applied.

Step 3:
Provide Docker container registry details required for authentication, image tagging, and secure image storage.

Step 4:
Select the appropriate build agent based on pipeline requirements and workload.

Step 5:
Build the Docker image using the application source code and Dockerfile.

Step 6:
Push the newly built Docker image to the configured container registry with the latest version tag.

Step 7:
Perform an automated GitOps update using a Bash script to update the Kubernetes manifest repository with the latest Docker image tag.
This update triggers Argo CD to detect the change and automatically deploy the updated application to the Kubernetes cluster.
