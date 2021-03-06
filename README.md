# k8s-gatekeeper
Applying examples of Open Policy Agent - Gatekeeper into Kubernetes
- Normally we have two parts of Authorisations "User level" and "Resources level".
- User Level implemented by the RBAC permissions.
- Resources Level implemented by the OPA , So let's see how it works.

### Flow and Arch
- It is working as Admission Controller which let's the API Server validates the `kubectl`, `API Request` ...etc and checks if there is any policy applied against this related k8s-resource or no.
- OPA is deployed as a CRD.
- We create a Policy template by a `Rego` Language.
- Then we create a Constraint which will consume the previously created Policy template.

### OPA vs Gatekeeper ?
- OPA is a general Policy Agent which can be applied in many things.
- Gatekeeper is just specific for Kubernetes , and it actually uses OPA internally.
- Both OPA and Gatekeeper are using the `Rego` Policy Language.

### Setup of Gatekeeper :
```
kubectl apply -f gatekeeper-crd.yaml
```

#### Included in this repo policies examples of running OPA in Kubernetes.
