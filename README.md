# SAMF demo
This application can be used to generate various demo data for Software Asset Management tests and demos.

## Contents
### Foundation data records  
These records are used as the basis for generating software installation and subscription data.  
1. core_company - ACME Training
2. samp_custom_sw_publisher – ACME Training
3. samp_custom_sw_product - Cloud Storage (subscription software) and Studio
4. cmdb_software_product_model - Cloud Storage (any version), Studio 1 and Studio 2
5. alm_license - One entitlement for each of the above software models  
### Catalog items  
These catalog items are available in the default Service Catalog, in the Software category. They also appear as modules in the **SAMF demo** application menu.
1. Update computer names  
   Submitting this item will update all computer names to use the format {DEPARTMENT - FIRST NAME}. For subsequent computers assigned to a user, the format {FIRST NAME2}, {FIRST NAME3}, etc. is used. For example:
   - FINANCE - JANE
   - FINANCE - JANE2
   - FINANCE - JANE3  
Note: Only computer records saved directly in the cmdb_ci_computer table are updated. Records in child classes (e.g., cmdb_ci_server) are not updated.
The purpose of this renaming is to assist when creating consumption rules based on department, to allow easy identification of computers belonging to each department in the reconciliation report.
2. Create demo data  
   Creates an installation record and/or a subscription record for the selected software model, user and computer.
3. Normalize discovery model  
   A quick way to manually normalize ACME Training discovery models only, using the above products.
4. Delete demo data  
   Deletes demo data generated for ACME Training. You can delete installation records, discovery models and/or subscription records.
