# pulumi_sample_codebuild

## How to reproduce the issue
### Borked
 - python3 -m venv .venv
 - source .venv/bin/activate
 - pip install -r requirements_borked.txt
 - pulumi up

 You should get the following error message:
 ```
 Diagnostics:
  aws:codebuild:Project (sample):
    error: aws:codebuild/project:Project resource 'sample' has a problem: Attribute must be a whole number, got 480
```

### Working
 - rm -rf .venv
 - python3 -m venv .venv
 - source .venv/bin/activate
 - pip install -r requirements_working.txt
 - pulumi up