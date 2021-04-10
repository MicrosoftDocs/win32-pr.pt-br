---
title: Visão geral da arquitetura dos serviços de enfileiramento de mensagens
description: O MSMQ (serviços de enfileiramento de mensagens) usa um modelo de site/empresa. Normalmente, um site é um local físico, como um edifício. Uma empresa consiste em um ou mais sites e representa uma organização.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292531"
---
# <a name="overview-of-message-queuing-services-architecture"></a>Visão geral da arquitetura dos serviços de enfileiramento de mensagens

O MSMQ (serviços de enfileiramento de mensagens) usa um modelo de site/empresa. Normalmente, um site é um local físico, como um edifício. Uma empresa consiste em um ou mais sites e representa uma organização.

O diagrama a seguir ilustra a arquitetura do serviço MSMQ.

![arquitetura do MSMQ](images/msmq.png)

No coração do MSMQ está o banco de dados do serviço de informações de fila de mensagens (MQIS), que é executado sobre SQL Server. Uma empresa tem um único MQIS mestre, chamado de controlador corporativo primário. Cada site tem seu próprio MQIS, chamado de *controlador de site primário* e zero ou mais *controladores de site de backup*. Por fim, há os computadores cliente individuais, cada um com seu próprio Gerenciador de filas, implementado como um serviço. O controlador corporativo primário também pode ser um controlador de site primário e qualquer controlador também pode ser um cliente.

As filas de mensagens podem ser públicas ou privadas. As filas públicas são registradas em Active Directory e podem ser acessadas pela rede. As mensagens em uma fila pública são roteadas em toda a empresa, sob o controle do MSMQ. As mensagens do aplicativo cliente são movidas do Gerenciador de filas do cliente para a fila de destino viajando entre os gerenciadores de filas dos controladores de site.

As filas particulares são mantidas pelo Gerenciador de filas local e não são registradas no Active Directory. O escopo de mensagens de fila particular é limitado ao computador no qual residem.

 

 




