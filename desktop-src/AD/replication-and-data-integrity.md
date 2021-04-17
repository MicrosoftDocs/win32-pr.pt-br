---
title: Replicação e integridade de dados
description: Active Directory Domain Services fornecer atualização de vários mestres.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, replicação e integridade de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755453"
---
# <a name="replication-and-data-integrity"></a>Replicação e integridade de dados

Active Directory Domain Services fornecer *atualização de vários mestres*. A atualização de vários mestres significa que todas as réplicas completas de uma determinada partição são graváveis (as réplicas parciais em servidores de catálogo global não são graváveis). A atualização de vários mestres significa que as atualizações não são bloqueadas mesmo quando algumas réplicas são inoperáveis. O servidor de Active Directory propaga as alterações da réplica atualizada para todas as outras réplicas. A replicação é automática e transparente.

Para obter mais informações, consulte os tópicos a seguir.

-   [O modelo de replicação no Active Directory Domain Services](replication-model-in-active-directory-domain-services.md)
-   [Comportamento de replicação no Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)
-   [Detectando e evitando a latência de replicação](detecting-and-avoiding-replication-latency.md)

 

 




