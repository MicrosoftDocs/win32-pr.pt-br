---
title: Abrindo um dispositivo simples usando o nome do dispositivo
description: Abrindo um dispositivo simples usando o nome do dispositivo
ms.assetid: 9e116499-2094-40e1-b2bc-3e3b8281a472
keywords:
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f84a852a18da3edb4431308259bacf38623bce3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917188"
---
# <a name="opening-a-simple-device-by-using-the-device-name"></a><span data-ttu-id="76ff4-104">Abrindo um dispositivo simples usando o nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="76ff4-104">Opening a Simple Device by Using the Device Name</span></span>

<span data-ttu-id="76ff4-105">O exemplo a seguir abre um dispositivo de áudio de CD especificando o nome do dispositivo usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="76ff4-105">The following example opens a CD audio device by specifying the device name using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a CD audio device by specifying the device name.

mciOpenParms.lpstrDeviceType = "cdaudio";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN, MCI_OPEN_TYPE,
    (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 