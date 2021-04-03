---
title: Por que Active Directory Domain Services usa esse modelo de replicação
description: Este tópico explica os motivos para o sistema de forma livre usado pelo Active Directory Domain Services para um modelo de replicação.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Modelo de replicação Active Directory, vantagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822246"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Por que Active Directory Domain Services usa esse modelo de replicação

Este tópico explica os motivos para o sistema de forma livre usado pelo Active Directory Domain Services para um modelo de replicação.

Active Directory Domain Services são um sistema de forma livre pelos seguintes motivos:

-   Os clientes exigem uma solução altamente distribuída na qual partes do diretório podem ser distribuídas em suas redes e administradas localmente.
-   Clientes grandes geralmente crescem para milhões de objetos, centenas ou milhares de réplicas ou ambos.
-   Muitas redes de clientes fornecem apenas conectividade intermitente a alguns locais; por exemplo, plataformas de análise de petróleo remotas e são fornecidos em Sea, portanto, o sistema deve ser tolerante a operações parcialmente conectadas ou desconectadas.

Não há como garantir a conscientização total do estado atual ou futuro de um sistema distribuído, pois o conhecimento das alterações de Estado deve ser propagado e a propagação leva tempo, durante o qual podem ocorrer mais alterações de estado.

Sistemas rigidamente acoplados tratam incertezas ao tentar eliminá-lo. Isso é feito por meio de restrições em atualizações, exigindo que todos os nós ou uma maioria dos nós estejam disponíveis antes que as atualizações possam ser executadas, usando esquemas de bloqueio distribuídos ou um mestre único para recursos críticos, restringindo todos os nós a serem bem conectados ou alguma combinação dessas técnicas. Quanto mais rigidamente os nós de computação em um sistema distribuído estiverem, menor será o limite de dimensionamento.

Os sistemas de forma livre manipulam incertezas por tolerar-lo. Um sistema de forma livre permite que os nós tenham exibições diferentes do estado geral do sistema e fornece algoritmos para resolver conflitos.

Soluções rigidamente acopladas foram rejeitadas como inadequadas para Active Directory Domain Services devido aos requisitos de administração local, operação desconectada e escalabilidade para números muito grandes de nós. O modelo levemente acoplado escolhido, a consistência de vários mestres com convergência, atende a todos os requisitos.

 

 




