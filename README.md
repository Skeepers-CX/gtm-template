# GTM Template for Skeepers SDK

Custom template for client use on Google Tag Management solution

## How to use

The template is defined by the template.tpl file, there you will find the associated info, template parameters, the code used (Templates use a sandboxed javascript, full details on how to use [here](https://developers.google.com/tag-platform/tag-manager/templates/sandboxed-javascript)), web permissions and tests.

If you want to modify the template you must 

- Upload the template.tpl file to google tag manager 
- Make the necessary modifications

It is important to preserve existing functions when editing the template. A sandboxed version of javascript is used for the code, full details [here](https://developers.google.com/tag-platform/tag-manager/templates/sandboxed-javascript)

## Template modifications for clients

Once you have modified and tested the template file you have to publish for client use. To do this update the metadata.yaml as prescribed on [google documentation](https://developers.google.com/tag-platform/tag-manager/templates/gallery) 

The metadata.yaml file is used to determine which version of your template to use in the gallery. To publish new versions, you need to add the change number (SHA number) to the versions section of your metadata.yaml file.

1. Locate the commit that includes the changes that you want to push, and copy the SHA number. An easy way to do this is in GitHub is to go to a commit view and click the clipboard icon (clipboard icon). This will copy the entire SHA number to your clipboard.
2. Add a new sha entry to the top of your versions list in metadata.yaml. (See the example below.)
3. Add changeNotes to briefly describe changes contained in this new version. You can create multiline comments, if desired. (See the example below.)
4. Commit the change to metadata.yaml and your update will appear in the gallery typically within 2 to 3 days.

This example demonstrates how to add new version information including the SHA number and change notes:

```
homepage: "https://www.example.com"
documentation: "https://www.example.com/documentation"
versions:
# Latest version
    - sha: 5f02a788b90ae804f86b04aa24af8937e567874c
      changeNotes: |2
        Fix bug with the whatsamajig.
        Improve menu options.
        Update API calls.
# Older versions
    - sha: 5f02a788b90ae804f86b04aa24af8937e567874b
      changeNotes: Adds eject button.
    - sha: 5f02a788b90ae804f86b04aa24af8937e567874a
      changeNotes: Initial release.
```

  Important: Every published version of the template should be included in the versions section ordered in reverse chronological order, (most recent to oldest).
  Note: Not every incremental commit needs to be included as a version change to the Community Templates Gallery. For example, if you make incremental changes in commits 1, 2, and 3, and the final version is commit 4, you should have just one entry for commit 4 that includes all changes from commits 1, 2, and 3.