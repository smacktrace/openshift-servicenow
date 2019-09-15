# Service Now Cluster Role to view OCP resources

	- https://docs.servicenow.com/bundle/london-it-operations-management/page/product/service-mapping/concept/kubernetes-discovery.html

	- Provide a user with the permissions to the following /api/v1 elements:
		* https://<url>/api/v1/namespaces/
		* https://<url>/api/v1/namespaces/<namespace>
		* https://<url>/api/v1/namespaces/kube-system/endpoints/kube-controller-manager
		* https://<url>/api/v1/services
		* https://<url>/api/v1/pods
		* https://<url>/api/v1/nodes


## Prereqs

1. Create namespace called "servicenow"

2. Create service account called "servicenow"
	- oc create sa servicenow


## Impliment Cluster role and Cluster Role Binding
	
	- oc apply -f servicenow-view-cluster-role.yml
	- oc apply -f servicenow-view-cluster-role-binding.yml  
