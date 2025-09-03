# Contributing & Ownership Proof Instructions

Thank you for contributing. This file also includes instructions for the repository owner to create a GPG-signed proof of ownership.

Basic contribution guidelines:
- Fork the repository, create a branch, make changes, open a pull request.
- Follow conventional commit messages: type(scope): subject
- Add tests for bug fixes and features.

Creating a locally signed proof (for repository owner):

1) Ensure your git config uses an email address listed on your GitHub account:
   - git config user.name "Your Name"
   - git config user.email "your-primary-email@example.com"

2) Create a proof file (this repo includes proof.txt). Create a signed commit that adds the proof file:
   - git add proof.txt
   - git commit -S -m "chore(ownership): add signed ownership proof (proof.txt)"
   - git push origin main

3) Or create a signed tag (recommended) and push it:
   - git tag -s v0.1-ownership-proof -m "Ownership proof signed by Jayrobert77"
   - git push origin v0.1-ownership-proof

Notes:
- GPG signing requires a local GPG key. See GitHub docs: https://docs.github.com/en/authentication/managing-commit-signature-verification
- After pushing a signed tag, create a Release in GitHub from the tag to make it more visible.