---
description: Processing rules simplify data collection and manage content as it is sent to reporting.
subtopic: Processing rules
title: Processing rules overview
topic: Admin tools
uuid: 6b4ee7c9-2b86-47a6-b64c-c8d644fff67d
---

# Processing rules overview

Processing rules simplify data collection and manage content as it is sent to reporting. Processing rules help simplify interaction with IT groups and Web developers by providing an interface to:

* Set an event on the product overview page 
* Populate campaign with a query string parameter 
* Concatenate category and page name in a prop for easier reporting 
* Copy an eVar into a prop to see paths
* Clean up misspelled site sections
* Pull internal search terms or a campaign ID from the query string into an eVar

>[!VIDEO](https://video.tv.adobe.com/v/26124/?quality=12&learn=on)

## Processing Rules Permissions {#section_8A4846688050453784DAE4D89355169A}

Administrators have rights to use processing rules **by default**. Administrators can also grant these rights to non-administrators through the Admin Tools interface. For instructions, see []

![](assets/processing-rules.png)

>[!IMPORTANT]
>
>Because processing rules permanently affect Analytics data, Adobe strongly recommends that processing rules administrators receive certification training in Adobe Analytics, and be familiar with all sources of data for your report suites (standard web sites, mobile sites, mobile apps, Data Insertion API, and so on). Knowledge of the context data variables and standard variables populated in various platforms will help prevent accidental deletion or alteration of data.

## Use Context Data to Simplify Data Collection {#section_09EEA03612D24C15839631AA9E9668D8}

Context data variables are a type of variable that are available only to processing rules. To use context data variables, key/value data pairs are sent in by your implementation, and processing rules are used to capture these values in standard Analytics variables. This frees programmers from understanding exactly which prop and/or eVar should contain which value.


<code>s.contextData['author'] = "Robert Munsch"</code>

<code>s.contextData['section'] = "books"</code>

<code>s.contextData['genre'] = "Youth"</code>

1. Map author to eVar2
2. Map section to Prop1, eVar3
3. If section and author exist set event5

See [Context Data Variables](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) in Implementation Help.

## Use Processing Rules to Transform Hit Data and Trigger Events {#section_8284E72E999244E091CD7FB1A22342B6}

Processing rules can monitor incoming values to transform common typos and set events based on reported data. Props can be copied to eVars. Values can be concatenated for reports, and events can be set.

## Using Context Data Variables in Reporting {#section_BD098BC503024A0B8703596628071134}

Once context data variables are defined within your implementation, they must be copied to variables such as eVars to be used in reporting.

For more information, go [here](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) and [here](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md).
