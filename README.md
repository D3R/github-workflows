# Reusable GitHub workflows

## D3R CI

### Add Project File
1. Copy `sample/project-ci.yaml` to your projects `.github/workflows` directory.
2. Push

### Dcoument support versions in composer.json
* `supported` - this version is a required check for merging
* `experimental` - this version should have chcks run but they should not prevent a merge
* `broken` - don't run checks yet
```json
    "extra": {
        "php-versions": {
            "7.3": {
                "status": "supported"
            },
            "7.4": {
                "status": "supported"
            },
            "8.0": {
                "status": "experimental"
            },
            "8.1": {
                "status": "broken",
                "notes": "composer install fails due to a dependency of d3r/core"
            }
        }
    }
 ```
