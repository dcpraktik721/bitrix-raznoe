# NEXT_STEP_RECOMMENDATION

## Current Verdict: REPO_MISSING_ON_SERVER

## Required Next Steps

1. CLONE REPO TO SERVER (required before any deploy gate)
2.    git clone <REPO_URL> /home/bitrix/deploy_repo
3.   Expected files:
4.      - tools/import_staging_service_page.php
5.     - tools/rollback_delete_staging_element.php
6.    - docs/mvp3_merge_protezirovanie_2026-05-11_approved_configs/production.page.merged.json
  
      - 2. VERIFY SHA256 after clone
        3.    Expected: importer=3f17135e..., rollback=bd9f5caf..., payload=5172e506...
       
        4.3. ADD SSH KEY to server via Timeweb panel (Access -> SSH keys)
           This enables standard CI/CD without serial console workaround.

        4. RESOLVE HOSTNAME ambiguity
        5.    Server is prod.praktik72.ru. Verify this is intended dev target.
       
        6.5. RE-RUN ssh_readonly_deploy_check after steps 1-3
           If all pass -> SERVER_READY_FOR_DEV_HOST_GATE
           Then: DEV_HOST_STAGING_CREATE_SAFE_EXECUTION_GATE --dry-run --bitrix-aware
