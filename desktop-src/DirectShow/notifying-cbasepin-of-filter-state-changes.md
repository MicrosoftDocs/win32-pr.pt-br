---
description: Notificando CBasePin de alterações de estado de filtro
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notificando CBasePin de alterações de estado de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295999"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a><span data-ttu-id="8afd6-103">Notificando CBasePin de alterações de estado de filtro</span><span class="sxs-lookup"><span data-stu-id="8afd6-103">Notifying CBasePin of Filter State Changes</span></span>

<span data-ttu-id="8afd6-104">A classe **CBasePin** é notificada sempre que o estado do filtro proprietário é alterado.</span><span class="sxs-lookup"><span data-stu-id="8afd6-104">The **CBasePin** class is notified whenever the state of the owning filter changes.</span></span> <span data-ttu-id="8afd6-105">Para cada transição de estado, o filtro chama um método correspondente no PIN, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8afd6-105">For each state transition, the filter calls a corresponding method on the pin, as shown in the following table.</span></span>



| <span data-ttu-id="8afd6-106">Novo estado de filtro</span><span class="sxs-lookup"><span data-stu-id="8afd6-106">New Filter State</span></span> | <span data-ttu-id="8afd6-107">Método CBasePin</span><span class="sxs-lookup"><span data-stu-id="8afd6-107">CBasePin Method</span></span>                                 |
|------------------|-------------------------------------------------|
| <span data-ttu-id="8afd6-108">Parado</span><span class="sxs-lookup"><span data-stu-id="8afd6-108">Stopped</span></span>          | [<span data-ttu-id="8afd6-109">**CBasePin:: inativo**</span><span class="sxs-lookup"><span data-stu-id="8afd6-109">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md) |
| <span data-ttu-id="8afd6-110">Em Pausa</span><span class="sxs-lookup"><span data-stu-id="8afd6-110">Paused</span></span>           | [<span data-ttu-id="8afd6-111">**CBasePin:: ativo**</span><span class="sxs-lookup"><span data-stu-id="8afd6-111">**CBasePin::Active**</span></span>](cbasepin-active.md)     |
| <span data-ttu-id="8afd6-112">Executando</span><span class="sxs-lookup"><span data-stu-id="8afd6-112">Running</span></span>          | [<span data-ttu-id="8afd6-113">**CBasePin:: Run**</span><span class="sxs-lookup"><span data-stu-id="8afd6-113">**CBasePin::Run**</span></span>](cbasepin-run.md)           |



 

<span data-ttu-id="8afd6-114">A classe derivada deve substituir esses métodos para responder à alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="8afd6-114">The derived class should override these methods to respond to the state change.</span></span> <span data-ttu-id="8afd6-115">Dependendo do filtro, o PIN pode iniciar um thread de trabalho que fornece amostras, confirmar ou desconfirmar seu alocador de memória e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8afd6-115">Depending on the filter, the pin might start a worker thread that delivers samples, commit or decommit its memory allocator, and so forth.</span></span>

 

 



