---
title: Recuperando informações sobre um filme
description: Recuperando informações sobre um filme
ms.assetid: 678272e0-67fe-4ec1-88a8-924a773445a7
keywords:
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebc7d30d8eaef21bfe869e6cebbae7708758c9c26100562981be5b587aa2834
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805486"
---
# <a name="retrieving-information-about-a-movie"></a>Recuperando informações sobre um filme

O exemplo a seguir define o formato de hora como quadros e obtém a posição atual se o dispositivo estiver sendo executado usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
MCI_DGV_SET_PARMS mciSet; 
MCI_DGV_STATUS_PARMS mciStatus; 
 
// Put in frame mode. 
mciSet.dwTimeFormat = MCI_FORMAT_FRAMES; 
mciSendCommand(wDeviceID, MCI_SET, 
    MCI_SET_TIME_FORMAT, 
    (DWORD)(LPSTR)&mciSet); 
 
mciStatus.dwItem = MCI_STATUS_MODE; 
mciSendCommand(wDeviceID, MCI_STATUS, 
    MCI_STATUS_ITEM, 
    (DWORD)(LPSTR)&mciStatus); 
 
// If device is playing, get the position. 
if (mciStatus.dwReturn == MCI_MODE_PLAY)
{ 
    mciStatus.dwItem = MCI_STATUS_POSITION; 
    mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM, 
        (DWORD)(LPSTR)&mciStatus); 
 
    // Update the position from mciStatus.dwReturn. 
} 
```



 

 