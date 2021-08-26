---
description: Windows Especificadores de tipo de dispositivo WIA (Aquisição de Imagem) são constantes que indicam o tipo de dispositivo anexado ao computador de um usuário.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Especificadores de tipo de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdefac4672b46fea7a7dad021fa9ebec710b3b77eabb7a1f7cac405b8e7e519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056966"
---
# <a name="wia-device-type-specifiers"></a>Especificadores de tipo de dispositivo WIA

Windows Especificadores de tipo de dispositivo WIA (Aquisição de Imagem) são constantes que indicam o tipo de dispositivo anexado ao computador de um usuário. Use a macro GET \_ STIDEVICE TYPE para obter esses valores da propriedade de tipo \_ de dispositivo WIA. Veja a seguir especificadores de tipo de dispositivo WIA válidos: 

| Tipo de dispositivo                 | Significado                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| AultDeviceTypeDefault        | Dispositivo WIA genérico. Durante enumerações de dispositivo, essa constante é usada para enumerar todos os dispositivos WIA.                         |
| PomDeviceTypeDigitalCamera  | O dispositivo é uma câmera. *Esse especificador não é suportado pelo Windows* Vista e *posterior.*                                     |
| Operação DeviceTypeScanner        | O dispositivo é um scanner.                                                                                                    |
| TipDeviceTypeStreamingVideo | O dispositivo contém vídeo de streaming. *Esse especificador não é suportado pelo* Windows Server 2003, Windows Vista ou *posterior.* |



 

 

 



