Q: $W_V$ shape
A: $(d_{\text{model}}, d_{\text{head}})$
#mechanistic-interpretability

Q: $W_O$ shape
A: $(d_{\text{head}}, d_{\text{model}})$
#mechanistic-interpretability

Q: $W_Q$ shape
A: $(d_{\text{model}}, d_{\text{head}})$
#mechanistic-interpretability

Q: $W_K$ shape
A: $(d_{\text{model}}, d_{\text{head}})$
#mechanistic-interpretability

Q: Denote the QK circuit
A: $W_E^T W_Q^T W_K W_E$
#mechanistic-interpretability #suspended

Q: Denote the OV circuit
A: $W_U W_O W_V W_E$
#mechanistic-interpretability #suspended

Q: In the token-token QK map you embed on both sides ($W_E^T \cdots W_E$); in the OV token map you embed in but unembed out ($W_U \cdots W_E$). Why the asymmetry?
A: QK is a bilinear form — we take two inputs (query and key) and return a scalar; OV is a linear map — we take one input (token) and return a distribution over output vocab logits.
#marked #mechanistic-interpretability #suspended

Q: What does the prev-token head do?
A: It writes the information about previous token's identity into the current token's residual stream.
#mechanistic-interpretability #suspended

Q: What does the induction head do?
A: It completes a pattern by composing based on the prev-token head's contribution: given `…[A][B]…[A]` predicts `[B]` (attends to the token after the previous occurrence of the current token, and copies it).
#mechanistic-interpretability #suspended

Q: What's the copying head?
A: A head with such OV circuit that copies the source token's identity to the destination's residual stream.
#mechanistic-interpretability #suspended

Q: Empirical signature of a copying head?
A: Diagonal token-map ($W_U W_{OV} W_E$ ≈ identity-like), and positive-real-part eigenvalues of the OV circuit.
#mechanistic-interpretability #suspended

Q: What's K-composition?
A: A composition where an earlier head's output is read as input to a later head's keys.
#mechanistic-interpretability #suspended

Q: Canonical example of K-composition?
A: Induction
#mechanistic-interpretability
