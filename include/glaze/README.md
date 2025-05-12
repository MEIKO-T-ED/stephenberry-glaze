# Preparation for internal usage

Only the content of the folder include/glaze is needed.

The following steps must be applied:

```bash
git clone https://github.com/DiehlControlsExternal/stephenberry-glaze
cd stephenberry-glaze
git switch -c diehl/main
git rm -rf .
git checkout main -- LICENSE include
git mv include/glaze/* .
rm -r include
git add .
git commit -m "mod: moved include/glaze/* to .; removed others"
git push -u origin diehl/main
```
The `diehl/main`branch contains now only the needed files.

The repo can be used now as a submodule in a parent repo.

`git submodule add -b diehl/main https://github.com/DiehlControlsExternal/stephenberry-glaze 3rd_party/glaze`
