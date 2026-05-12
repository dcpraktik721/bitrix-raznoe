—# REPO_LOCATION_CHECK

## Result: REPO_MISSING_ON_SERVER

All 6 find commands returned empty (no matches):

- find /home -maxdepth 6 -name import_staging_service_page.php -> empty
- - find /home -maxdepth 7 -path mvp3_merge* -> empty
  - - find / -xdev -maxdepth 8 -name import_staging_service_page.php -> empty
    - - find / -xdev -maxdepth 8 -name rollback_delete_staging_element.php -> empty
      - - find / -xdev -maxdepth 8 -type d -name mvp3_merge_protezirovanie_2026-05-11_approved_configs -> empty
        - - find / -xdev -maxdepth 8 -name production.page.merged.json -> empty
         
          - Only .git found: /home/bitrix/dehydrated/.git (Let's Encrypt ACME, unrelated)
         
          - docs/ under docroot = PDF clinic documents only, no mvp3_merge content.
         
          - ## Verdict
         
          - REPO_MISSING_ON_SERVER
