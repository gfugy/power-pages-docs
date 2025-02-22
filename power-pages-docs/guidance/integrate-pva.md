---
title: "How to: Embed a chatbot on a webpage"
description: Learn how to embed a Power Virtual Agent chatbot on a webpage in Power Pages.
author: neerajnandwana-msft
ms.topic: guidance
ms.custom: 
ms.date: 02/21/2023
ms.subservice:
ms.author: nenandw 
ms.reviewer: ndoelman
contributors:
    - nickdoelman
    - neerajnandwana-msft
---

# How to: Embed a chatbot on a webpage

The Power Pages design studio doesn't have the ability to add a chatbot component to a webpage using the components panel. 

> [!NOTE]
> You can [add a chatbot](/power-apps/maker/portals/add-chatbot) using the legacy portal Studio for websites created in Power Apps.

The following steps provide an alternative method to embed a Power Virtual Agent chatbot on a Power Pages webpage.

## Prerequisites

- A Power Pages subscription or trial. [Get a Power Pages trial here](../getting-started/trial-signup.md).
- A Power Pages site created. [Create a Power Pages site](../getting-started/create-manage.md).
- A Power Virtual Agents subscription or trial. [Sign up for a Power Virtual Agents trial](/power-virtual-agents/sign-up-individual).
- A Power Virtual Agents chatbot. [Create and delete Power Virtual Agents bots](/power-virtual-agents/authoring-first-bot).

## Locate chatbot ID

In the following steps, we'll get the chatbot ID that we'll use to embed into Power Pages.

1. The Power Virtual Agents home page, select **Publish** from the side menu.

1. In the **Optimize your bot** section, choose **Go to Channels**.

    :::image type="content" source="media/pva/pva-channels.png" alt-text="Select Power Virtual Agents channels.":::

1. In the **Channels** section, select **Custom website**.

1. In the slide-out panel in the **Default embed code** section, select and copy the code following the `/bots/` path (this code is the **chatbot id**).

    :::image type="content" source="media/pva/embedcode.png" alt-text="Copying the embed code.":::

## Add chatbot to the site

In the following step, we'll update the **Bot Consumer** table with our chatbot information.

1. Go to [Power Pages](https://aka.ms/mpp).

1. Select **Edit** on the site you want to add the chatbot.

1. Select **Data** workspace.

1. Locate the **Bot Consumer** table.

1. Select the blank row.

1. Select **Edit row using form**

1. Enter in the following values into the table:

    | Field | Data |
    | - | - |
    | Name | Any name you choose, for example *TestBot* |
    | Bot Schema Name | The chatbot ID you copied from the Power Virtual Agent page. For example: `new_bot_df0a07025507434b9ebb085434ac755f`. |
    | Website | Select the lookup to the website where you want to host the chatbot. |
    | Config Json | Key-in parentheses characters. `{}` |
    
    :::image type="content" source="media/pva/chatbot-record.png" alt-text="Updating chatbot record.":::

## Add chatbot to website or to specific webpages

The following steps will specify if the chatbot will be visible on all pages of the site or only on specific pages. 
- If a chatbot is only linked to one or more webpages, and no chatbot linked to a website, then the chatbot will only appear on those pages.
- If a chatbot is linked to a website, it will appear on all webpages.
- If both a website and webpages are linked to chatbots, the chatbot linked to the specific webpage will take precedence, and the chatbot linked to the site will appear on all other pages.

> [!NOTE]
> Once you specify relationships to either the website or the webpage records, you will be unable to remove the association and will need delete and recreate the **bot consumer** record and re-establish the relationships.

### Add chatbot to website

1. Select the **Related** tab, select **Websites**.

1. Select **Add Existing Website**

1. Choose the website where you want to host the chatbot. 

    :::image type="content" source="media/pva/select-website.png" alt-text="Select website.":::

1. Select **Add**.

1. Select **Save & Close**

1. Select **Done** on the **Currently editing a row** pop-up window.

### Add chatbot to specific webpages

1. Select the **Related** tab, select **Websites**.

1. Select **Add Existing Website**

1. Choose the website where you want to host the chatbot. 

    :::image type="content" source="media/pva/select-webpage.png" alt-text="Select webpage.":::

1. Select **Add**.

1. Select **Save & Close**

1. Select **Done** on the **Currently editing a row** pop-up window.

## Testing your chatbot on Power Pages

1. Select **Preview**, followed by **Desktop** to preview the site

1. You should be able to view and interact with your chatbot.

    :::image type="content" source="media/pva/chatbot.png" alt-text="Use chatbot on webpage.":::

## See Also

- [Power Virtual Agents](/power-virtual-agents/)

