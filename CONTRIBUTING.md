# Contributing

Start in the repository for the template or module you are changing. Describe the
member action that should work, the current behavior, and a small reproducible
example. Keep Platform identities, ownership, permissions and business state in
`freedom-platform`; a template consumes its versioned API and does not create a
second database or invent authority.

Use the pinned runtime and lockfile. Run the repository's tests and build, and
include the command results in your pull request. If API shapes change, update
the canonical Platform contract first, regenerate the pinned client, and verify
the affected consumers together. Do not fix a mismatch by silently editing a
generated vendor file.

Use synthetic fixtures. Never attach cookies, access tokens, private customer
records or provider credentials to an issue or commit. Public GitHub metadata
and source commits are useful evidence; a manually entered claim is not proof
of ownership, payment, publication or official release status.

A passing workflow is test evidence. Production deployment, paid resources and
external publication need their own authorized action. This bootstrap introduces
no contribution license agreement or new license grant.
