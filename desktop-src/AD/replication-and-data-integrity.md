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
# <a name="replication-and-data-integrity"></a><span data-ttu-id="82f1d-104">Replicação e integridade de dados</span><span class="sxs-lookup"><span data-stu-id="82f1d-104">Replication and Data Integrity</span></span>

<span data-ttu-id="82f1d-105">Active Directory Domain Services fornecer *atualização de vários mestres*.</span><span class="sxs-lookup"><span data-stu-id="82f1d-105">Active Directory Domain Services provide *multi-master update*.</span></span> <span data-ttu-id="82f1d-106">A atualização de vários mestres significa que todas as réplicas completas de uma determinada partição são graváveis (as réplicas parciais em servidores de catálogo global não são graváveis). A atualização de vários mestres significa que as atualizações não são bloqueadas mesmo quando algumas réplicas são inoperáveis.</span><span class="sxs-lookup"><span data-stu-id="82f1d-106">Multi-master update means that all full replicas of a given partition are writable (the partial replicas on global catalog servers are not writable.) Multi-master update means that updates are not blocked even when some replicas are inoperable.</span></span> <span data-ttu-id="82f1d-107">O servidor de Active Directory propaga as alterações da réplica atualizada para todas as outras réplicas.</span><span class="sxs-lookup"><span data-stu-id="82f1d-107">The Active Directory server propagates the changes from the updated replica to all other replicas.</span></span> <span data-ttu-id="82f1d-108">A replicação é automática e transparente.</span><span class="sxs-lookup"><span data-stu-id="82f1d-108">Replication is automatic and transparent.</span></span>

<span data-ttu-id="82f1d-109">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="82f1d-109">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="82f1d-110">O modelo de replicação no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="82f1d-110">The Replication Model in Active Directory Domain Services</span></span>](replication-model-in-active-directory-domain-services.md)
-   [<span data-ttu-id="82f1d-111">Comportamento de replicação no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="82f1d-111">Replication Behavior in Active Directory Domain Services</span></span>](replication-behavior-in-active-directory-domain-services.md)
-   [<span data-ttu-id="82f1d-112">Detectando e evitando a latência de replicação</span><span class="sxs-lookup"><span data-stu-id="82f1d-112">Detecting and Avoiding Replication Latency</span></span>](detecting-and-avoiding-replication-latency.md)

 

 




