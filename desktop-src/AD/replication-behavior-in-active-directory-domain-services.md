---
title: Comportamento de replicação no Active Directory Domain Services
description: O comportamento de replicação é consistente e previsível; dado um conjunto de alterações em uma determinada réplica, o resultado pode ser previsto \ 8212; as alterações serão propagadas para todas as outras réplicas.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822253"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a><span data-ttu-id="7e1a0-104">Comportamento de replicação no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7e1a0-104">Replication Behavior in Active Directory Domain Services</span></span>

<span data-ttu-id="7e1a0-105">O comportamento de replicação é consistente e previsível; dado um conjunto de alterações em uma determinada réplica, o resultado pode ser previsto — as alterações serão propagadas para todas as outras réplicas.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-105">Replication behavior is consistent and predictable; given a set of changes to a given replica, the outcome can be predicted—the changes will be propagated to all other replicas.</span></span> <span data-ttu-id="7e1a0-106">É impossível planejar um modelo geral confiável para prever quando as alterações serão aplicadas em todas as outras réplicas ou em uma réplica específica, pois o estado futuro do sistema distribuído como um todo não pode ser conhecido.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-106">Devising a reliable general model for predicting when the changes will be applied at all other replicas, or at a particular replica, is impossible, because the future state of the distributed system as a whole cannot be known.</span></span> <span data-ttu-id="7e1a0-107">Isso é chamado de "latência não determinística" e os aplicativos que usam o diretório devem entender e permitir.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-107">This is called "nondeterministic latency," and applications that use the directory must understand and allow for it.</span></span>

<span data-ttu-id="7e1a0-108">A situação não é tão complexa quanto pode ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-108">The situation is not as complex at it might appear.</span></span> <span data-ttu-id="7e1a0-109">Há apenas três Estados que um aplicativo deve acomodar:</span><span class="sxs-lookup"><span data-stu-id="7e1a0-109">There are only three states that an application must accommodate:</span></span>

-   <span data-ttu-id="7e1a0-110">Distorção de versão: nenhuma das alterações aplicadas a uma determinada réplica de origem foi propagada para uma determinada réplica de destino.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-110">Version Skew: None of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="7e1a0-111">Um aplicativo que lê a réplica de origem vê a nova versão das informações, enquanto um aplicativo que lê o destino vê a versão antiga (ou nada, se as novas informações foram adicionadas pela primeira vez).</span><span class="sxs-lookup"><span data-stu-id="7e1a0-111">An application reading the source replica sees the new version of the information, while an application reading the destination sees the old version (or nothing, if the new information was added for the first time).</span></span> <span data-ttu-id="7e1a0-112">A distorção de versão se aplica a todos os consumidores do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-112">Version skew applies to all directory service consumers.</span></span>
-   <span data-ttu-id="7e1a0-113">Atualização parcial: algumas das alterações aplicadas a uma determinada réplica de origem foram propagadas para uma determinada réplica de destino.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-113">Partial Update: Some of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="7e1a0-114">Um aplicativo que lê a réplica de origem vê as novas informações, enquanto um aplicativo que lê o destino vê uma mistura de informações novas e antigas (ou apenas algumas das novas informações, se as novas informações foram adicionadas pela primeira vez).</span><span class="sxs-lookup"><span data-stu-id="7e1a0-114">An application reading the source replica sees the new information, while an application reading the destination sees a mix of old and new information (or only some of the new information, if the new information was added for the first time).</span></span> <span data-ttu-id="7e1a0-115">A atualização parcial se aplica aos consumidores do serviço de diretório que usam dois ou mais objetos relacionados para armazenar suas informações.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-115">Partial update applies to directory service consumers that use two or more related objects to store their information.</span></span>
-   <span data-ttu-id="7e1a0-116">Estado totalmente replicado: todas as alterações aplicadas a uma determinada réplica de origem foram propagadas para uma determinada réplica de destino.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-116">Fully Replicated State: All of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="7e1a0-117">Os aplicativos nas réplicas de origem e de destino veem as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-117">Applications at the source and destination replicas see the same information.</span></span>

 

 




