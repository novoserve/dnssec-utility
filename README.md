# DNSSEC Utility
NovoServe's DNSSEC Utility used for bulk enabling DNSSEC using PowerDNS and Openprovider.

### Usage
- Rename config.dist.php to config.php and fill in the API credentials.
- Add your domains into $domains, one per line.
- Run the script with: `php dnssec.php`.

### Features
The script currently executes a few tasks before it enabled DNSSEC for a domain:
1. Checks if the domain exists at Openprovider., if not > skip.
2. Checks if the domain is using our nameservers, if not > skip.
3. Checks if the domain is already using DNSSEC, if not > skip.
4. Checks if there is already DNSSEC data in the nameservers, if not > create new DNSSEC data.
5. Finally it sets the DNSSEC data at Openprovider.

### License
MIT License