---
title: Reflexão de mensagem
description: Reflexão de mensagem
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004839"
---
# <a name="message-reflection"></a>Reflexão de mensagem

É altamente recomendável que um contêiner de controle ActiveX dê suporte à reflexão de mensagem. Isso resultará em uma operação mais eficiente para controles de subclasse. Se a reflexão da mensagem tiver suporte, a propriedade de ambiente MessageReflect deverá ter suporte e ter um valor de **true**. Se um contêiner não implementar a reflexão de mensagem, o CDK OLE criará duas janelas para cada controle de subclasse, a fim de fornecer a reflexão de mensagem em nome do contêiner de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 




