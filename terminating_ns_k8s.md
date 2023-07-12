## Delete namespace stuck in termination state

To delete `namespace` stuck in termination state : open terminal

- `kubectl get namespace annoying-namespace-to-delete -o json > tmp.json`
- then edit tmp.json and remove "<b>kubernetes</b>" from <b>Finalizers</b>


edit the file `tmp.json` and remove the finalizers

it looks like this :
> }, "spec": { "finalizers": [ "kubernetes" ] },

after editing it should look like this
> }, "spec": { "finalizers": [ ] },

- `kubectl replace --raw "/api/v1/namespaces/<YOUR_NAMESPACE>/finalize" -f ./<YOUR_NAMESPACE>.json`

- `kubectl get ns <namespace-name>`
