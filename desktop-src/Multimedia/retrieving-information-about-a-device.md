---
title: Recuperando informações sobre um dispositivo
description: Recuperando informações sobre um dispositivo
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS comando
- MCI_STATUS comando
- MCI_INFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916594"
---
# <a name="retrieving-information-about-a-device"></a>Recuperando informações sobre um dispositivo

Cada dispositivo responde aos comandos [**de recurso**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**\_ status do MCI**](mci-status.md)) e [**informações**](info.md) ([**MCI \_ info**](mci-info.md)). Esses comandos obtêm informações sobre o dispositivo. Por exemplo, o comando a seguir retornará "true" se um dispositivo **cdaudio** puder ejetar o disco:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Os sinalizadores listados para os comandos obrigatórios e básicos fornecem uma quantidade mínima de informações sobre um dispositivo. Muitos dispositivos complementam os comandos obrigatórios e básicos com sinalizadores estendidos para fornecer informações adicionais sobre o dispositivo.

 

 




