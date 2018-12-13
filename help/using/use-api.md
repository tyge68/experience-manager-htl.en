---
title: HTL Use-API
seo-title: HTL Use-API
description: null
seo-description: "Two APIs are available for HTL: Java Use-API and Javascript Use-API"
uuid: ab44aa5c-ce7e-40b9-97fb-e86c6a28405c
contentOwner: User
products: SG_EXPERIENCEMANAGER/HTL
topic-tags: html-template-language
content-type: reference
discoiquuid: 89004426-eb59-4b63-913f-51bf98662773
mwpw-migration-script-version: 2017-10-12T21 46 58.665-0400
index: y
internal: n
snippet: y
---

# HTL Use-API{#htl-use-api}

The following table gives an overview of the pros and cons of each API.

||**Java Use-API**|**JavaScript Use-API**|
|--- |--- |--- |
|**Pros**|<ul><li>faster</li><li>can be inspected with a debugger</li><li>easy to unit-test</li></ul>|<ul><li>can be modified by front-end developers</li><li>is located within the component, keeping the view logic of a component close to it's corresponding template</li></ul>|
|**Cons**|<ul><li>cannot be modified by front-end developers</li></ul>|<ul><li>slower</li><li>no debugger (yet)</li><li>harder to unit-test</li></ul>|


For page components, it is recommended to use a mixed model, where all model logic is located in Java, providing clear APIs that are agnostic to anything that happens in the view (i.e. within the components). AEM comes with great default models like the Page or the Resource API that should be able to cover most cases.

All view logic that is specific to a component should be placed within that component as JavaScript, because it belongs to that component.
