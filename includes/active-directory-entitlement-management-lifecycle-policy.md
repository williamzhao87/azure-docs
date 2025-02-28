---
title: include file
description: include file
services: active-directory
author: owinfreyATL
manager: amycolannino
ms.service: active-directory
ms.topic: include
ms.date: 02/27/2023
ms.author: owinfrey
ms.custom: include file
---

## Lifecycle

On the **Lifecycle** tab, you specify when a user's assignment to the access package expires. You can also specify whether users can extend their assignments.

1. In the **Expiration** section, set **Access package assignments expires** to **On date**, **Number of days**, **Number of hours**, or **Never**.

    - For **On date**, select an expiration date in the future.
    - For **Number of days**, specify a number between 0 and 3660 days.
    - For **Number of hours**, specify how many hours.

    Based on your selection, a user's assignment to the access package expires on a certain date, some days after they're approved, or never.

1. If you want the user to request a specific start and end date for their access, select **yes** next to the **Users can request specific timeline** toggle.

1. Select **Show advanced expiration settings** to show more settings.

    ![Access package - Lifecycle Expiration settings](./media/entitlement-management-lifecycle-policy/expiration.png)

1. To allow user to extend their assignments, set **Allow users to extend access** to **Yes**.

    If extensions are allowed in the policy, the user receives an email 14 days and also one day before their access package assignment is set to expire, prompting them to extend the assignment. The user must still be in the scope of the policy at the time they request an extension. Also, if the policy has an explicit end date for assignments, and a user submits a request to extend access, the extension date in the request must be at or before when assignments expire, as defined in the policy that was used to grant the user access to the access package. For example, if the policy indicates that assignments are set to expire on June 30, the maximum extension a user can request is June 30.

    If a user's access is extended, they won't be able to request the access package after the specified extension date (date set in the time zone of the user who created the policy).

1. To require approval to grant an extension, set **Require approval to grant extension** to **Yes**.

    The same approval settings that were specified on the **Requests** tab will be used.

1. Select **Next** or **Update**.
