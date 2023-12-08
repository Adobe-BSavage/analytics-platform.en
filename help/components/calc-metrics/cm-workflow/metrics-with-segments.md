---
description: Filtering on individual metrics allows you to make metric comparisons within the same report.
title: Filtered metrics
feature: Calculated Metrics
exl-id: 37cc93df-9f51-42b3-918f-ed5864991621
---
# Filtered metrics

In the Calculated metric builder, you can apply filters within your metric definition. This is helpful if you want to derive new metrics to use in your analysis. Keep in mind, filter definitions can be updated through the Filter builder. If changes are made, the filter will automatically update anywhere it is applied, including if it is part of a calculated metric definition.

![Summary and Definition of filters for Countries = Germany and Unique Visitors](assets/german-visitors.png)

## Create a filtered metric {#create}

Let's say you want to compare different aspects of a "German Visitors" filter to those of an "International Visitors" filter. You can create metrics that will give you insights such as:

* How does content browsing behavior compare between the two groups? (Another example would be: How does the conversion rate compare between the two filters?) 
* As a percentage of total persons, how many German persons browse certain pages, versus International persons? 
* Where are the biggest differences in terms of which content is accessed by these different filters?

Build and save a metric called "German Visitors" and a metric called "International Visitors":

1. Create an adhoc filter in the Calculated metric builder called "German Visitors", where "Countries" equals "Germany". Drag the Countries dimension into the Definition canvas and select [!UICONTROL **Germany**] as the value:

   ![Adhoc filter showing Countries equals Germany](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >You can also do this in the [Filter Builder](/help/components/filters/create-filters.md), but we have simplified the workflow by making dimensions available in the Calculated metric builder. "Adhoc" means that the filter is not visible in the **[!UICONTROL Filters]** list in the left rail. You can however, make it public by hovering over the "i" icon next to it and clicking **[!UICONTROL Make public]**.

1. Drag the Germany filter into the Definition canvas and drag the Unique Visitors metric within it:

   ![Summary and Definition of Countries equal Germany and Unique Visitors](assets/german-visitors.png)

1. Select [!UICONTROL **Save**] to save the calculated metric.

1. Create an adhoc filter in the Calculated metric builder called "international Visitors", where "Countries" does not equal "Germany".

   Drag the Countries dimension into the Definition canvas, select [!UICONTROL **Germany**] as the value, then select [!UICONTROL **does not equal**] as the operator. 

1. Drag the Unique Visitors metric within it.

1. Select [!UICONTROL **Save**] to save the calculated metric.

1. In Analysis Workspace, drag the **[!UICONTROL Page]** Dimension into a Freeform Table and drag the 2 new calculated metrics next to each other to the top:

   ![Freeform Table showing Page dimension for German Visitors and International visitors](assets/workspace-pages.png)

Here is a video overview:

>[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12)

## Percent of total metrics {#percent-total}

You can take the example above a step further by comparing your filter to a total population. To do so, create two new metrics, "% of Total German Visitors" and "% of Total International Visitors":

1. Drop the German (or International) Visitors filter into the canvas.
1. Drop another German (or International) Visitors filter below. However, this time, click its configuration (gear) icon to select the Metric Type "Total". The Format should be "Percent". The operator should be "divided by". You end up with this metric definition:

   ![Countries equals Germany and Total Unique Visitors](assets/cm_metric_total.png)

1. Apply this metric to your project:

   ![Freeform Table with Page and % of Total German visitors](assets/cm_percent_total.png)
