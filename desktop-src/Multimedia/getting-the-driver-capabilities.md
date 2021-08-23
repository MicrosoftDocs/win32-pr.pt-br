---
title: Obter as funcionalidades do driver
description: Obter as funcionalidades do driver
ms.assetid: 761886db-b2e5-449c-b526-6e992cc1b42f
keywords:
- drivers,drivers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5bd178b1658ccecd9af26e6729fc00beab95b55fb4c8189feeada92c029d5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691306"
---
# <a name="getting-the-driver-capabilities"></a>Obter as funcionalidades do driver

O exemplo a seguir [**usa ogetGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) e [**ogetGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) para determinar se os serviços do Joystick estão disponíveis e se um conector está anexado a uma das portas.


```C++
JOYINFO joyinfo; 
UINT wNumDevs, wDeviceID; 
BOOL bDev1Attached, bDev2Attached; 
 
    if((wNumDevs = joyGetNumDevs()) == 0) 
        return ERR_NODRIVER; 
    bDev1Attached = joyGetPos(JOYSTICKID1,&joyinfo) != JOYERR_UNPLUGGED; 
    bDev2Attached = wNumDevs == 2 && joyGetPos(JOYSTICKID2,&joyinfo) != 
        JOYERR_UNPLUGGED; 
    if(bDev1Attached || bDev2Attached)   // decide which joystick to use 
        wDeviceID = bDev1Attached ? JOYSTICKID1 : JOYSTICKID2; 
    else 
        return ERR_NODEVICE; 

```



 

 