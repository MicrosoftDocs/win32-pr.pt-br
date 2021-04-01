---
title: Abrindo um dispositivo simples usando a constante Device-Type
description: Abrindo um dispositivo simples usando a constante Device-Type
ms.assetid: 6ed5fd4b-534a-4e03-8130-07f831403a8e
keywords:
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef65cf4546da2d7f7b6fdb5883232d0b1802f7b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084486"
---
# <a name="opening-a-simple-device-by-using-the-device-type-constant"></a>Abrindo um dispositivo simples usando a constante Device-Type

O exemplo a seguir abre um dispositivo de áudio de CD especificando uma constante do tipo de dispositivo usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;

// Opens a CD audio device by specifying a device-type constant.

mciOpenParms.lpstrDeviceType = (LPCSTR) MCI_DEVTYPE_CD_AUDIO;

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_TYPE_ID, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 