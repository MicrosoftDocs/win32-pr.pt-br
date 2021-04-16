---
description: 'Saiba mais sobre: limitações do modelo de script'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitações do modelo de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757450"
---
# <a name="limitations-of-the-scripting-model"></a>Limitações do modelo de script

> [!Note]  
> Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows). Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

O modelo de script da aquisição de imagens do Windows (WIA) expõe um subconjunto da funcionalidade WIA. A tabela a seguir fornece descrições das limitações do modelo de script. 

| Funcionalidade WIA               | Limitação de modelo de script                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suprimindo a interface do usuário  | Não é possível suprimir a interface do usuário para definir propriedades de dispositivo/transferência.                                                                                                                                                                                               |
| Definir propriedades              | Não é possível definir (gravar) nenhuma propriedade de dispositivo ou item.                                                                                                                                                                                                                        |
| Registrando para eventos de retorno de chamada | Só pode receber notificação para três eventos especificados: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)e [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md). |
| Tratando erros                 | Não é possível manipular erros WIA.                                                                                                                                                                                                                                                |



 

 

 
