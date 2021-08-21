---
title: Reflexão de mensagem
description: Reflexão de mensagem
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9191e0e189f8653518aaabb3c31785cde960538b0828d56669096ebf1d63f1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048044"
---
# <a name="message-reflection"></a>Reflexão de mensagem

É altamente recomendável que um contêiner de controle ActiveX suporte à reflexão de mensagem. Isso resultará em uma operação mais eficiente para controles de subclasse. Se a reflexão de mensagem tiver suporte, a propriedade de ambiente MessageReflect deverá ter suporte e ter um valor **true.** Se um contêiner não implementar a reflexão de mensagem, a CDK do OLE criará duas janelas para cada controle de subclasse, a fim de fornecer reflexão de mensagem em nome do contêiner de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 




