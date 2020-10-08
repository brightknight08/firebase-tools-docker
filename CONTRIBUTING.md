# CONTRIBUTING

I invite everyone to please feel free to contribute to the codes. You may also
review, suggest improvements, and request for additional packages that you may
require.

## git branching

Here's how (I think) we should do branching

### new issues = new branch

I just intend to use the `merge request` flow -- meaning, new issues should be
raised first. After discussions, we may submit new
[merge request](https://docs.gitlab.com/ee/user/project/merge_requests/)
and let it take care of creating new branches so that branching will be consistent.

### releases

to release, a particular commit should be tagged with any of the following:

- the basic version (major.minor.patch)
- release/major.minor.patch
- with v (e.g., release/v8.12.0, v8.10.0)
