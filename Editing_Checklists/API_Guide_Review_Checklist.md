## API Guide Review Checklist
Use this checklist to make sure that an API Guide follows the defined style, structure and writing guidelines in your tech writing portfolio.

### Global API Guide Checklist

- [ ] Verify application disclaimer is at the top of the guide.

- [ ] Verify Table of Contents comes after the disclaimer, and includes all accurate heading 1s in the guide.
      
- [ ] Verify that the Overview includes the sub-sections: **Common Use Cases** and **Technical Details** and that these sub-sections have bulleted lists of the information.

- [ ] Test all JSON code syntax to make sure it's valid using a proper [JSON formatter](https://www.freeformatter.com/json-formatter.html).

- [ ] Adhere to the API Guide template, even if the information for a specific section is limited. For example, for the Pagination section, if the API does not support traditional pagination mechanisms, state that in this section. In addition, provide information about another way the API controls the number of returned results.

- [ ] Make sure to use the proper Note Markdown syntax throughout the guide: > **Note:** {TEXT OF NOTE}
 
- [ ] Make sure all topic titles are initial-capped and not in sentence case.

 - [ ] Make sure parameter names are included in the `backtick` style.

 - [ ] Make sure parameter values are in **bold**.

 - [ ] For top-level parameters, the description should be: "Top-level x key" where "x" is the top-level key for the object. For example, "Top-level weather key."
