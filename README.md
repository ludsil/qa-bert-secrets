# qa-bert-secrets

⚠️ **Plaintext Kubernetes Secrets — testing only.** Synced by Argo CD into a BYO AKS cluster for QA BERT experiments. Do NOT use this pattern in production; use SealedSecrets or External Secrets Operator instead.

Why this exists: spawned's `kubernetes` platform `Secret` component emits no actual `Secret` resource — only a `secretKeyRef` reference. Operators must materialize the Secret out-of-band. For QA BERT we use this public repo + a separate Argo CD `Application` per test namespace.

Filed as finding F068 in QA-BERT/KNOWN_FINDINGS.md.
