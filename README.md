# rd-fluxcd-lesson

# Етап 1

GITHUB_TOKEN=$(gh auth token) flux bootstrap github \
--owner=kyrylich \
--repository=rd-fluxcd-lesson \
--branch=main \
--path=./clusters/my-cluster \
--personal

# Eтап 2

