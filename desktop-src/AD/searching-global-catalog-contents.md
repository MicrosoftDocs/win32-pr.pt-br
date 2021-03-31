---
title: Pesquisando o catálogo global
description: Active Directory Domain Services também tem um GC (catálogo global), que contém uma réplica parcial de todos os objetos no diretório.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- pesquisando o catálogo global Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634921"
---
# <a name="searching-the-global-catalog"></a><span data-ttu-id="3816e-104">Pesquisando o catálogo global</span><span class="sxs-lookup"><span data-stu-id="3816e-104">Searching the Global Catalog</span></span>

<span data-ttu-id="3816e-105">Active Directory Domain Services também tem um GC (catálogo global), que contém uma réplica parcial de todos os objetos no diretório.</span><span class="sxs-lookup"><span data-stu-id="3816e-105">Active Directory Domain Services also have a global catalog (GC), which contains a partial replica of all objects in the directory.</span></span> <span data-ttu-id="3816e-106">Ele também contém réplicas parciais dos contêineres de esquema e configuração.</span><span class="sxs-lookup"><span data-stu-id="3816e-106">It also contains partial replicas of the schema and configuration containers.</span></span> <span data-ttu-id="3816e-107">Um ou mais controladores de domínio em um domínio podem armazenar uma cópia do catálogo global.</span><span class="sxs-lookup"><span data-stu-id="3816e-107">One or more domain controllers in a domain can hold a copy of the global catalog.</span></span> <span data-ttu-id="3816e-108">Para obter mais informações sobre como associar a um catálogo global, consulte [associação ao catálogo global](binding-to-the-global-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="3816e-108">For more information about binding to a global catalog, see [Binding to the Global Catalog](binding-to-the-global-catalog.md).</span></span>

<span data-ttu-id="3816e-109">O catálogo global mantém uma réplica de cada objeto em Active Directory Domain Services, mas com apenas um pequeno número de seus atributos.</span><span class="sxs-lookup"><span data-stu-id="3816e-109">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="3816e-110">Os atributos no catálogo global são aqueles usados com mais frequência em operações de pesquisa, como nomes e sobrenome de um usuário, nomes de logon e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3816e-110">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="3816e-111">Os atributos do catálogo global também incluem aqueles necessários para localizar uma réplica completa do objeto.</span><span class="sxs-lookup"><span data-stu-id="3816e-111">The global catalog attributes also include those required to locate a full replica of the object.</span></span> <span data-ttu-id="3816e-112">O catálogo global permite que os usuários localizem objetos de interesse rapidamente sem saber qual domínio os contém e sem exigir um namespace estendido contíguo na empresa; ou seja, você pode pesquisar toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="3816e-112">The global catalog allows users to quickly find objects of interest without knowing what domain holds them and without requiring a contiguous extended namespace in the enterprise; that is, you can search the entire forest.</span></span>

<span data-ttu-id="3816e-113">Portanto, se você associar a um objeto no catálogo global, pesquisará esse objeto e toda a hierarquia abaixo dele — sem precisar ir para nenhum outro servidor.</span><span class="sxs-lookup"><span data-stu-id="3816e-113">So, if you bind to an object in the global catalog, you will search that object and the entire hierarchy below it — without having to go to any other server.</span></span> <span data-ttu-id="3816e-114">No entanto, a pesquisa só pode usar um filtro de consulta que contém propriedades no catálogo global e pode recuperar somente propriedades no catálogo global.</span><span class="sxs-lookup"><span data-stu-id="3816e-114">However, the search can only use a query filter containing properties in the global catalog and can retrieve only properties in the global catalog.</span></span>

<span data-ttu-id="3816e-115">Pesquisar o catálogo global tem os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="3816e-115">Searching the global catalog has the following benefits:</span></span>

-   <span data-ttu-id="3816e-116">O catálogo global permite Pesquisar toda a floresta ou qualquer parte da floresta, bem como os contêineres de esquema e configuração.</span><span class="sxs-lookup"><span data-stu-id="3816e-116">Global catalog enables you to search the entire forest or any part of the forest as well as the schema and configuration containers.</span></span>
-   <span data-ttu-id="3816e-117">O catálogo global permite que você execute uma pesquisa completa em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="3816e-117">Global catalog enables you to perform a complete search on a single server.</span></span> <span data-ttu-id="3816e-118">Nenhuma referência ou caça de referência é necessária.</span><span class="sxs-lookup"><span data-stu-id="3816e-118">No referrals or referral chasing is required.</span></span>

<span data-ttu-id="3816e-119">Pesquisar o catálogo global tem as seguintes desvantagens:</span><span class="sxs-lookup"><span data-stu-id="3816e-119">Searching the global catalog has the following disadvantages:</span></span>

-   <span data-ttu-id="3816e-120">O catálogo global contém um pequeno subconjunto das propriedades em cada objeto.</span><span class="sxs-lookup"><span data-stu-id="3816e-120">Global catalog contains a small subset of the properties on each object.</span></span> <span data-ttu-id="3816e-121">Se o filtro de consulta incluir propriedades que não estão no catálogo global, a consulta avaliará as expressões que contêm essas propriedades como false.</span><span class="sxs-lookup"><span data-stu-id="3816e-121">If your query filter includes properties that are not in the global catalog, the query will evaluate the expressions containing those properties as false.</span></span> <span data-ttu-id="3816e-122">Se você especificar propriedades de catálogo não globais na lista de propriedades a serem retornadas, essas propriedades não serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="3816e-122">If you specify non-global catalog properties in the list of properties to return, those properties are not retrieved.</span></span>
-   <span data-ttu-id="3816e-123">Para pesquisar o catálogo global, um controlador de domínio que contém um catálogo global deve estar disponível.</span><span class="sxs-lookup"><span data-stu-id="3816e-123">To search the global catalog, a domain controller that contains a global catalog must be available.</span></span> <span data-ttu-id="3816e-124">Se um não estiver disponível, você não poderá executar uma pesquisa de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="3816e-124">If one is not available, you cannot perform a global catalog search.</span></span>
-   <span data-ttu-id="3816e-125">O catálogo global é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3816e-125">The global catalog is read-only.</span></span> <span data-ttu-id="3816e-126">Isso significa que você não pode associar a um objeto no catálogo global para criar, modificar ou excluir objetos.</span><span class="sxs-lookup"><span data-stu-id="3816e-126">This means you cannot bind to an object in the global catalog to create, modify, or delete objects.</span></span>

 

 




