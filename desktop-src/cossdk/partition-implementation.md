---
description: Quando instalado em um servidor de aplicativos, o COM+ cria automaticamente uma partição, conhecida como a partição global.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementação de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793823"
---
# <a name="partition-implementation"></a><span data-ttu-id="b9d97-103">Implementação de partição</span><span class="sxs-lookup"><span data-stu-id="b9d97-103">Partition Implementation</span></span>

<span data-ttu-id="b9d97-104">Quando instalado em um servidor de aplicativos, o COM+ cria automaticamente uma partição, conhecida como a *partição global*.</span><span class="sxs-lookup"><span data-stu-id="b9d97-104">When installed on an application server, COM+ automatically creates a partition, known as the *global partition*.</span></span> <span data-ttu-id="b9d97-105">A partição global inclui um conjunto padrão de aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="b9d97-105">The global partition includes a standard set of COM+ applications.</span></span> <span data-ttu-id="b9d97-106">Os aplicativos COM+ que estão instalados na partição global ficam automaticamente disponíveis para todos os usuários no servidor.</span><span class="sxs-lookup"><span data-stu-id="b9d97-106">COM+ applications that are installed in the global partition are automatically available to all users on the server.</span></span> <span data-ttu-id="b9d97-107">Se você tiver outros aplicativos COM+ que deseja disponibilizar para todos os usuários no servidor, poderá adicioná-los à partição global.</span><span class="sxs-lookup"><span data-stu-id="b9d97-107">If you have other COM+ applications that you would like to make available to all users on the server, you can add them into the global partition.</span></span>

<span data-ttu-id="b9d97-108">Além da partição global, você pode criar outras partições para os usuários somente nesse servidor ou para usuários em todo o domínio.</span><span class="sxs-lookup"><span data-stu-id="b9d97-108">In addition to the global partition, you can create other partitions for users on that server only, or for users throughout the domain.</span></span> <span data-ttu-id="b9d97-109">A criação de partições adicionais e a instalação de várias configurações de um aplicativo COM+ neles permite que os usuários executem essas configurações de aplicativo simultaneamente no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="b9d97-109">Creating additional partitions and installing multiple configurations of a COM+ application into them allows your users to execute those application configurations simultaneously on the same computer.</span></span> <span data-ttu-id="b9d97-110">Além disso, ao instalar aplicativos COM+ em uma partição diferente da partição global, você pode controlar o acesso do usuário a esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b9d97-110">Also, by installing COM+ applications into a partition other than the global partition, you can control user access to those applications.</span></span>

<span data-ttu-id="b9d97-111">**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b9d97-111">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="b9d97-112">A partição global é a única partição COM+ disponível.</span><span class="sxs-lookup"><span data-stu-id="b9d97-112">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="b9d97-113">Para obter mais informações sobre partições locais e partições definidas em Active Directory, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b9d97-113">For more information on local partitions and partitions defined within Active Directory, see the following topics:</span></span>

-   [<span data-ttu-id="b9d97-114">Partições locais</span><span class="sxs-lookup"><span data-stu-id="b9d97-114">Local Partitions</span></span>](local-partitions.md)
-   [<span data-ttu-id="b9d97-115">Partições e Active Directory</span><span class="sxs-lookup"><span data-stu-id="b9d97-115">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
-   [<span data-ttu-id="b9d97-116">Partições padrão</span><span class="sxs-lookup"><span data-stu-id="b9d97-116">Default Partitions</span></span>](default-partitions.md)
-   [<span data-ttu-id="b9d97-117">A partição global</span><span class="sxs-lookup"><span data-stu-id="b9d97-117">The Global Partition</span></span>](the-global-partition.md)
-   [<span data-ttu-id="b9d97-118">Propriedades da partição</span><span class="sxs-lookup"><span data-stu-id="b9d97-118">Partition Properties</span></span>](partition-properties.md)

## <a name="related-topics"></a><span data-ttu-id="b9d97-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9d97-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9d97-120">Restrições de design de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b9d97-120">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="b9d97-121">Componentes e partições em fila COM+</span><span class="sxs-lookup"><span data-stu-id="b9d97-121">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="b9d97-122">Registrando e ativando componentes em partições</span><span class="sxs-lookup"><span data-stu-id="b9d97-122">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="b9d97-123">O que são partições COM+?</span><span class="sxs-lookup"><span data-stu-id="b9d97-123">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



