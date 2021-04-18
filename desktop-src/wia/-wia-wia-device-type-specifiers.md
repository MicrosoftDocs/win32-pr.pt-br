---
description: Os especificadores de tipo de dispositivo WIA (aquisição de imagem do Windows) são constantes que indicam o tipo de dispositivo anexado ao computador de um usuário.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Especificadores de tipo de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793866"
---
# <a name="wia-device-type-specifiers"></a>Especificadores de tipo de dispositivo WIA

Os especificadores de tipo de dispositivo WIA (aquisição de imagem do Windows) são constantes que indicam o tipo de dispositivo anexado ao computador de um usuário. Use a \_ macro obter \_ tipo STIDEVICE para obter esses valores da Propriedade do tipo de dispositivo WIA. Estes são especificadores de tipo de dispositivo WIA válidos: 

| Tipo de dispositivo                 | Significado                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| StiDeviceTypeDefault        | Dispositivo WIA genérico. Durante as enumerações de dispositivo, essa constante é usada para enumerar todos os dispositivos WIA.                         |
| StiDeviceTypeDigitalCamera  | O dispositivo é uma câmera. *Não há suporte para este especificador por* Windows Vista *e posterior.*                                     |
| StiDeviceTypeScanner        | O dispositivo é um scanner.                                                                                                    |
| StiDeviceTypeStreamingVideo | O dispositivo contém vídeo de streaming. *Não há suporte para este especificador por* Windows Server 2003 *,* Windows Vista *ou posterior.* |



 

 

 



