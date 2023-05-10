# Summary

This repo contains sample visiualizations that can be installed into a customer's Sumo Logic instance.

# Installation

## Lookups

Whenever a customer uses this app, they will need to create a lookup in their Sumo instance so the dashboards work properly.

Complete the following steps to setup the Lookup used by the Cyral dashboards:

1. Login to your Sumo Logic instance as an Admin
2. Switch to the `Library View`
3. Within the `Library View`, set the View As to `Content Administrator`
4. Within the `Admin Recommended` Folder, click on the `Add New` button
5. From the `Add New` button, select `New Lookup`
6. In the resulting Lookup Configuration screen, use the following settings
  - Name: CategoryLookup
  - Set a TTL: No
  - Choose a size limit handling option: Delete Old Data
  - Create Lookup Table: Upload File
7. Under the `Upload File` heading, click the Upload button.
8. Locate the [CategoryLookupTable.csv](lookups/CategoryLookupTable.csv) file and upload it
9. Set the following fields as Primary Keys:
   - StatementType
   - RepoType
10. Click the Create button
11. Once the lookup is created, edit the sharing settings so that it is shared with all users that will need access
12. Now you can install the Cyral Dashboards

The [CategoryLookup.json](lookups/CategoryLookup.json) file is a reference of how the lookup should be configured once created.

## Dashboards

Once the lookup has been created, you can then install the dashboards.

1. Login to your Sumo Logic instance as an Admin
2. Switch to the `Library View`
3. Within the `Library View`, set the View As to `Content Administrator`
4. Beside the `Admin Recommended` Folder, click on the menu to the right (3 vertical dots) and select `New Folder`
5. Call the new folder `Cyral Dashboards` or some other name of your choice
6. Click the `Add` button
7. Navigate to the `Cyral Dashboards` folder, click on the menu to the right (3 vertical dots) and select `Import`
8. Give the dashboard a name of your choice and then paste the contents of one of the JSON files located in the [dashboards](dashboards/) directory of this repo
9. Click the `Import` button to create the dashboard

Repeat steps 7 - 9 for each of the [dashboards](dashboards/) directory of this repo
