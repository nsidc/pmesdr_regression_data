# pmesdr_regression_data

This is the regression data for the PMESDR system at https://github.com/nsidc/pmesdr

There are 2 directories in the repo - one for v1 data (20180920) and one for v2 data (20230125)

## Steps to update or replace regression data

 1. Create new directory with today's date at the top level for the new files
 2. Populate the directory with the new files
 3. all .nc files are managed with git-lfs
 4. if a new file type is added then do
   - git lfs track "*.new"
 5. git add {new files}
 6. add new item to CHANGELOG.md
 7. git add CHANGELOG.md
 8. git commit -m "what this is for"
 9. git push
 10. Go to pmesdr repo and change the location of the regression data dir (PMESDR_REGRESS_DIR) in the set_pmesdr_environment.sh script to point to this new location