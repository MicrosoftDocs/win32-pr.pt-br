---
description: 'Saiba mais sobre: Limitações do modelo de script'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitações do modelo de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4a1b2dc25c1ea73fd9d793e4d3de1bff7c8193b04aadbe00796ca4a021791886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208058"
---
# <a name="limitations-of-the-scripting-model"></a>Limitações do modelo de script

> [!Note]  
> Esse sistema de scripts foi substituído pela camada de automação wia (aquisição de imagem) Windows imagem. Consulte [Windows de Automação de Aquisição de Imagem.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

O Windows de script WIA (Aquisição de Imagem) expõe um subconjunto da funcionalidade wia. A tabela a seguir fornece descrições das limitações do modelo de script. 

| Funcionalidade do WIA               | Limitação do modelo de script                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suprimindo a interface do usuário  | Não é possível suprimir a interface do usuário para definir propriedades de dispositivo/transferência.                                                                                                                                                                                               |
| Definir propriedades              | Não é possível definir (gravar) nenhuma propriedade de dispositivo ou item.                                                                                                                                                                                                                        |
| Registrando para eventos de retorno de chamada | Só pode receber notificação para três eventos especificados: [**OnTransferComplete,**](-wia--iwiaevents-ontransfercomplete.md) [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)e [**OnDeviceDisconnected.**](-wia--iwiaevents-ondevicedisconnected.md) |
| Tratando erros                 | Não é possível lidar com erros de WIA.                                                                                                                                                                                                                                                |



 

 

 
