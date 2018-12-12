---
title: HTL Use-API
seo-title: HTL Use-API
description: null
seo-description: "Two APIs are available for HTL: Java Use-API and Javascript Use-API"
uuid: 2384cb80-3f93-4799-9387-f073a0aa2734
contentOwner: User
cq-lastmodifiedby: alvawb
products: SG_EXPERIENCEMANAGER/HTL
topic-tags: html-template-language
content-type: reference
discoiquuid: ed208528-e5aa-4e4d-a0fb-7bbcedea26d5
moreHelpPaths: /content/help/en/experience-manager/htl/morehelp/html-template-language;/content/help/en/experience-manager/htl/morehelp/html-template-language
mwpw-migration-script-version: 2017-10-12T21 46 58.665-0400
index: y
internal: n
snippet: y
---

# HTL Use-API{#htl-use-api}

The following table gives an overview of the pros and cons of each API.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <td> </td> 
   <td><strong>Java Use-API</strong></td> 
   <td><strong>JavaScript Use-API</strong></td> 
  </tr>
  <tr>
   <td><strong>Pros</strong></td> 
   <td>
    <ul> 
     <li>faster</li> 
     <li>can be inspected with a debugger</li> 
     <li>easy to unit-test</li> 
    </ul> </td> 
   <td>
    <ul> 
     <li>can be modified by front-end developers</li> 
     <li>is located within the component, keeping the view logic of a component close to it's corresponding template</li> 
    </ul> </td> 
  </tr>
  <tr>
   <td><strong>Cons</strong></td> 
   <td>
    <ul> 
     <li>cannot be modified by front-end developers</li> 
    </ul> </td> 
   <td>
    <ul> 
     <li>slower</li> 
     <li>no debugger (yet)</li> 
     <li>harder to unit-test</li> 
    </ul> </td> 
  </tr>
 </tbody>
</table>

For page components, it is recommended to use a mixed model, where all model logic is located in Java, providing clear APIs that are agnostic to anything that happens in the view (i.e. within the components). AEM comes with great default models like the Page or the Resource API that should be able to cover most cases.

All view logic that is specific to a component should be placed within that component as JavaScript, because it belongs to that component.
