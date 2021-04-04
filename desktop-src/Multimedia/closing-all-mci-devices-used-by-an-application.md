---
title: Fechando todos os dispositivos MCI usados por um aplicativo
description: Fechando todos os dispositivos MCI usados por um aplicativo
ms.assetid: 1d7d3800-b38f-4187-ba57-9849fef4d707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84db0bc6a6160098a3714f9cc7dbf455427bc28
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823682"
---
# <a name="closing-all-mci-devices-used-by-an-application"></a><span data-ttu-id="fabea-103">Fechando todos os dispositivos MCI usados por um aplicativo</span><span class="sxs-lookup"><span data-stu-id="fabea-103">Closing All MCI Devices Used by an Application</span></span>

<span data-ttu-id="fabea-104">O exemplo a seguir fecha todos os dispositivos MCI que são abertos por um aplicativo usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fabea-104">The following example closes all of the MCI devices that are opened by an application using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID;
DWORD dwReturn;
 
// Closes all MCI devices opened by this application.
// Waits until devices are closed before returning.

if(dwReturn = mciSendCommand(MCI_ALL_DEVICE_ID, MCI_CLOSE, MCI_WAIT, 
    NULL))
    
    // Error, unable to close all devices.
    
```



 

 