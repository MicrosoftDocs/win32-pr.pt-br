---
description: Conceitos de partições COM+
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Conceitos de partições COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456964"
---
# <a name="com-partitions-concepts"></a><span data-ttu-id="55485-103">Conceitos de partições COM+</span><span class="sxs-lookup"><span data-stu-id="55485-103">COM+ Partitions Concepts</span></span>

<span data-ttu-id="55485-104">Em ambientes de computação em que é necessário usar diferentes versões ou configurações de um aplicativo no mesmo computador, os conflitos podem surgir quando uma versão do aplicativo requer componentes diferentes do outro ou quando uma versão requer um componente no computador que é incompatível com a outra versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55485-104">In computing environments where it's necessary to use different versions or configurations of an application on the same computer, conflicts can arise when one version of the application requires different components than the other or when one version requires a component on the computer that is incompatible with the other version of the application.</span></span> <span data-ttu-id="55485-105">No passado, a única maneira de resolver esse problema era manter vários computadores e executar uma versão diferente do aplicativo em cada computador.</span><span class="sxs-lookup"><span data-stu-id="55485-105">In the past, the only way to solve this problem was to maintain multiple computers and run a different version of the application on each computer.</span></span> <span data-ttu-id="55485-106">Essa abordagem é dispendiosa e ineficiente porque aumenta os custos de hardware e a sobrecarga administrativa.</span><span class="sxs-lookup"><span data-stu-id="55485-106">Such an approach is costly and inefficient because it increases hardware costs and administrative overhead.</span></span>

<span data-ttu-id="55485-107">O COM+ resolve esse problema fornecendo o recurso de partições COM+.</span><span class="sxs-lookup"><span data-stu-id="55485-107">COM+ solves this problem by providing the COM+ partitions feature.</span></span> <span data-ttu-id="55485-108">Você pode usar partições COM+ para instalar versões diferentes de um aplicativo COM+ em um computador e executá-las simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="55485-108">You can use COM+ partitions to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="55485-109">Para entender e usar esse recurso, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="55485-109">To understand and use this feature, see the following topics:</span></span>

-   [<span data-ttu-id="55485-110">O que são partições COM+?</span><span class="sxs-lookup"><span data-stu-id="55485-110">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
-   [<span data-ttu-id="55485-111">Implementação de partição</span><span class="sxs-lookup"><span data-stu-id="55485-111">Partition Implementation</span></span>](partition-implementation.md)
-   [<span data-ttu-id="55485-112">Registrando e ativando componentes em partições</span><span class="sxs-lookup"><span data-stu-id="55485-112">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
-   [<span data-ttu-id="55485-113">Componentes e partições em fila COM+</span><span class="sxs-lookup"><span data-stu-id="55485-113">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
-   [<span data-ttu-id="55485-114">Restrições de design de aplicativo</span><span class="sxs-lookup"><span data-stu-id="55485-114">Application Design Restrictions</span></span>](application-design-restrictions.md)

## <a name="related-topics"></a><span data-ttu-id="55485-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55485-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55485-116">Tarefas de partições COM+</span><span class="sxs-lookup"><span data-stu-id="55485-116">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)
</dt> </dl>

 

 



