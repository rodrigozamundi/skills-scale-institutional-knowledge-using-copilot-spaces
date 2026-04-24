# 1. Crea una rama local
git checkout -b feat/add-docs-readme

# 2. Crea el archivo
cat > docs/README.md << 'EOF'
[pega el contenido del README.md arriba]
EOF

# 3. Commit y push
git add docs/README.md
git commit -m "docs: Add README for OctoAcme Project Management Docs

Adds centralized entry point and orientation for OctoAcme's project management playbook.
Includes overview of principles, roles, artifacts, lifecycle, and links to all process docs.

Closes #2"

git push origin feat/add-docs-readme

# 4. Crea el Pull Request con revisor
gh pr create \
  --title "docs: Add README for OctoAcme Project Management Docs" \
  --body "Closes #2" \
  --reviewer rodrigozamundi \
  --label documentation
