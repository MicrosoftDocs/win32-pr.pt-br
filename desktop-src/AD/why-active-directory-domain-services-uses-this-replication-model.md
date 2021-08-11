---
title: Por Active Directory Domain Services usa esse modelo de replicação
description: Este tópico explica os motivos para o sistema de forma livre usado pelo Active Directory Domain Services para um modelo de replicação.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Modelo de replicação do Active Directory , vantagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c137fadf768c97b6d8be962b22c74b45e30bc41c7dfb7e9ea67e1f145cd92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181987"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Por Active Directory Domain Services usa esse modelo de replicação

Este tópico explica os motivos para o sistema de forma livre usado pelo Active Directory Domain Services para um modelo de replicação.

Active Directory Domain Services são um sistema de forma livre pelos seguintes motivos:

-   Os clientes exigem uma solução altamente distribuída na qual partes do diretório podem ser distribuídas entre suas redes e administradas localmente.
-   Os clientes grandes geralmente crescem para milhões de objetos, centenas ou milhares de réplicas ou ambos.
-   Muitas redes de clientes fornecem apenas conectividade intermitente para alguns locais; por exemplo, plataformas de detalhamento de petróleo remoto e navios no mar, portanto, o sistema deve ser tolerante a operações parcialmente conectadas ou desconectadas.

Não há como garantir o reconhecimento completo do estado atual ou futuro de um sistema distribuído porque o conhecimento das alterações de estado deve ser propagado e a propagação leva tempo, durante o qual mais alterações de estado podem ocorrer.

Sistemas firmemente ativos lidam com a incerteza ao tentar eliminá-la. Isso é feito por meio de restrições em atualizações, exigindo que todos os nós ou alguma maioria dos nós esteja disponível antes que as atualizações possam ser executadas, usando esquemas de bloqueio distribuído ou domínio único para recursos críticos, restringindo todos os nós a serem bem conectados ou alguma combinação dessas técnicas. Quanto mais rígidos os nós de computação em um sistema distribuído são, menor é o limite de dimensionamento.

Os sistemas de forma livre lidam com a incerteza tolerando-a. Um sistema de forma livre permite que os nós tenham exibições diferentes do estado geral do sistema e fornece algoritmos para resolver conflitos.

Soluções firmemente anexadas foram rejeitadas como inadequadas para Active Directory Domain Services devido aos requisitos de administração local, operação desconectada e escalabilidade para um número muito grande de nós. O modelo livremente acoplado escolhido, consistência de vários mestres com convergência, atende a todos os requisitos.

 

 




