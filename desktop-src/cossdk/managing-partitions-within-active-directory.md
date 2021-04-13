---
description: Como alternativa ao gerenciamento de partições Active Directory por meio da ferramenta administrativa usuários e computadores Active Directory, você pode gerenciar partições COM+ programaticamente por meio do uso de um conjunto de objetos COM+ na ADSI (interface do sistema do Active Directory).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gerenciando partições no Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501081"
---
# <a name="managing-partitions-within-active-directory"></a><span data-ttu-id="eaf26-103">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="eaf26-103">Managing Partitions Within Active Directory</span></span>

<span data-ttu-id="eaf26-104">Como alternativa ao gerenciamento de partições Active Directory por meio da ferramenta administrativa usuários e computadores Active Directory, você pode gerenciar partições COM+ programaticamente por meio do uso de um conjunto de objetos COM+ na ADSI (interface do sistema do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="eaf26-104">As an alternative to managing Active Directory partitions through the Active Directory Users and Computers administrative tool, you can manage COM+ partitions programmatically through the use of a set of COM+ objects within Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="eaf26-105">Independentemente da técnica administrativa que você escolher para gerenciar partições COM+, há uma sequência geral de etapas que os administradores devem seguir:</span><span class="sxs-lookup"><span data-stu-id="eaf26-105">Regardless of the administrative technique you choose for managing COM+ partitions, there is a general sequence of steps that administrators must follow:</span></span>

1.  <span data-ttu-id="eaf26-106">Crie as novas partições COM+ dentro de Active Directory para seu domínio.</span><span class="sxs-lookup"><span data-stu-id="eaf26-106">Create the new COM+ partitions within Active Directory for your domain.</span></span>
2.  <span data-ttu-id="eaf26-107">Crie conjuntos de partições COM+ dentro de Active Directory e mapeie-os para suas partições COM+ recém-criadas.</span><span class="sxs-lookup"><span data-stu-id="eaf26-107">Create COM+ partition sets within Active Directory, and map them to your newly created COM+ partitions.</span></span>
3.  <span data-ttu-id="eaf26-108">Configure suas partições de Active Directory no computador local, usando o objeto COM+ apropriado.</span><span class="sxs-lookup"><span data-stu-id="eaf26-108">Configure your Active Directory partitions on your local machine, using the appropriate COM+ object.</span></span> <span data-ttu-id="eaf26-109">Quando você configura uma partição de Active Directory em um computador local, uma pasta de **aplicativos com+** é criada automaticamente nessa pasta de partição.</span><span class="sxs-lookup"><span data-stu-id="eaf26-109">When you configure an Active Directory partition on a local machine, a **COM+ Applications** folder is automatically created in that partition folder.</span></span>
4.  <span data-ttu-id="eaf26-110">Instale seus aplicativos COM+ nas partições COM+ apropriadas.</span><span class="sxs-lookup"><span data-stu-id="eaf26-110">Install your COM+ applications in the appropriate COM+ partitions.</span></span>

<span data-ttu-id="eaf26-111">Todas as etapas anteriores podem ser feitas programaticamente, usando um conjunto de interfaces Active Directory chamado ADSI.</span><span class="sxs-lookup"><span data-stu-id="eaf26-111">All of the preceding steps can be done programmatically, using a set of Active Directory interfaces called ADSI.</span></span> <span data-ttu-id="eaf26-112">Os objetos disponíveis para o gerenciamento de partições que estão disponíveis no ADSI são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="eaf26-112">The objects available for managing partitions that are available within ADSI are as follows:</span></span>

-   <span data-ttu-id="eaf26-113">\_nome do USERPARTITIONSETLINK DS \_</span><span class="sxs-lookup"><span data-stu-id="eaf26-113">DS\_USERPARTITIONSETLINK\_NAME</span></span>
-   <span data-ttu-id="eaf26-114">\_nome do PARTITIONLINK DS \_</span><span class="sxs-lookup"><span data-stu-id="eaf26-114">DS\_PARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="eaf26-115">\_nome do OBJECTID DS \_</span><span class="sxs-lookup"><span data-stu-id="eaf26-115">DS\_OBJECTID\_NAME</span></span>
-   <span data-ttu-id="eaf26-116">\_nome do DEFAULTPARTITIONLINK DS \_</span><span class="sxs-lookup"><span data-stu-id="eaf26-116">DS\_DEFAULTPARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="eaf26-117">\_nome do USERlink do DS \_</span><span class="sxs-lookup"><span data-stu-id="eaf26-117">DS\_USERLINK\_NAME</span></span>
-   <span data-ttu-id="eaf26-118">\_nome do particionado DS \_</span><span class="sxs-lookup"><span data-stu-id="eaf26-118">DS\_PARTITIONSET\_NAME</span></span>
-   <span data-ttu-id="eaf26-119">\_nome da partição DS \_</span><span class="sxs-lookup"><span data-stu-id="eaf26-119">DS\_PARTITION\_NAME</span></span>

<span data-ttu-id="eaf26-120">Para obter informações sobre como criar e gerenciar partições COM+ por meio do uso do Active Directory usuários e computadores e ferramentas administrativas de serviços de componentes, consulte a ajuda online disponível em cada ferramenta.</span><span class="sxs-lookup"><span data-stu-id="eaf26-120">For information on creating and managing COM+ partitions through the use of the Active Directory Users and Computers and Component Services administrative tools, see the online help available from within each tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaf26-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eaf26-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaf26-122">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="eaf26-122">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="eaf26-123">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="eaf26-123">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="eaf26-124">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="eaf26-124">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="eaf26-125">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="eaf26-125">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="eaf26-126">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="eaf26-126">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



