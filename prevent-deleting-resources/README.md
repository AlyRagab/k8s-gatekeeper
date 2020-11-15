### We have to update the `ValidatingWebhookConfiguration` with the `DELETE` Operation :
```
k edit ValidatingWebhookConfiguration gatekeeper-validating-webhook-configuration
```
### Operations should be :
```
operations:
    - CREATE
    - UPDATE
    - DELETE
```