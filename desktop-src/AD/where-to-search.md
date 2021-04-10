---
title: Decidindo onde Pesquisar
description: Este tópico explica as diferentes pesquisas que podem ser executadas no Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidindo onde Pesquisar o AD
- Active Directory AD, pesquisando, decidindo onde Pesquisar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293880"
---
# <a name="deciding-where-to-search"></a><span data-ttu-id="b6734-105">Decidindo onde Pesquisar</span><span class="sxs-lookup"><span data-stu-id="b6734-105">Deciding Where to Search</span></span>

<span data-ttu-id="b6734-106">Este tópico explica as diferentes pesquisas que podem ser executadas no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b6734-106">This topic explains the different searches that can be performed in Active Directory Domain Services.</span></span>

<span data-ttu-id="b6734-107">Todas as pesquisas são executadas em um dos seguintes contextos de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="b6734-107">All searches are performed in one of the following naming contexts:</span></span>

-   <span data-ttu-id="b6734-108">Domínio, incluindo partições de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b6734-108">Domain, including application directory partitions</span></span>
-   <span data-ttu-id="b6734-109">Contêiner de esquema</span><span class="sxs-lookup"><span data-stu-id="b6734-109">Schema container</span></span>
-   <span data-ttu-id="b6734-110">Contêiner de configuração</span><span class="sxs-lookup"><span data-stu-id="b6734-110">Configuration container</span></span>
-   <span data-ttu-id="b6734-111">Catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6734-111">Global catalog</span></span>

## <a name="searching-a-domain"></a><span data-ttu-id="b6734-112">Pesquisando um domínio</span><span class="sxs-lookup"><span data-stu-id="b6734-112">Searching a Domain</span></span>

<span data-ttu-id="b6734-113">Os domínios contêm a maioria dos objetos altamente usados, como usuários, contatos, grupos, unidades organizacionais, computadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b6734-113">Domains contain most of the highly used objects such as users, contacts, groups, organizational units, computers, and so on.</span></span> <span data-ttu-id="b6734-114">A maioria das consultas pesquisará um domínio.</span><span class="sxs-lookup"><span data-stu-id="b6734-114">Most queries will search a domain.</span></span> <span data-ttu-id="b6734-115">Para obter mais informações sobre como pesquisar um domínio, consulte [pesquisando o conteúdo do domínio](searching-domain-contents.md).</span><span class="sxs-lookup"><span data-stu-id="b6734-115">For more information about searching a domain, see [Searching Domain Contents](searching-domain-contents.md).</span></span>

## <a name="searching-the-schema-container"></a><span data-ttu-id="b6734-116">Pesquisando o contêiner de esquema</span><span class="sxs-lookup"><span data-stu-id="b6734-116">Searching the Schema Container</span></span>

<span data-ttu-id="b6734-117">O contêiner de esquema contém os objetos [**classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que fornecem a definição formal de todas as classes e atributos que podem existir em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b6734-117">The schema container contains the [**classSchema**](/windows/desktop/ADSchema/c-classschema) and [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects that provide the formal definition of every class and attribute that can exist in Active Directory Domain Services.</span></span> <span data-ttu-id="b6734-118">Para pesquisar objetos no contêiner de esquema, associe-se ao contêiner de esquema em qualquer controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b6734-118">To search for objects in the schema container, bind to the schema container on any domain controller.</span></span> <span data-ttu-id="b6734-119">O contêiner de esquema está disponível em todos os controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="b6734-119">The schema container is available on all domain controllers.</span></span> <span data-ttu-id="b6734-120">O nome distinto do contêiner de esquema é obtido do atributo **schemaNamingContext** de RootDSE.</span><span class="sxs-lookup"><span data-stu-id="b6734-120">The distinguished name of the schema container is obtained from the **schemaNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="b6734-121">Para obter mais informações sobre o rootDSE e o atributo **schemaNamingContext** , consulte [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="b6734-121">For more information about rootDSE and the **schemaNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="b6734-122">Para obter mais informações sobre a leitura do contêiner esquema ou esquema abstrato, consulte [diretrizes para associação ao esquema](guidelines-for-binding-to-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="b6734-122">For more information about reading from the schema or abstract schema container, see [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).</span></span>

## <a name="searching-the-configuration-container"></a><span data-ttu-id="b6734-123">Pesquisando o contêiner de configuração</span><span class="sxs-lookup"><span data-stu-id="b6734-123">Searching the Configuration Container</span></span>

<span data-ttu-id="b6734-124">O contêiner de configuração contém informações de configuração, como sites, serviços e especificadores de exibição, para toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="b6734-124">The configuration container contains configuration information, such as sites, services and display specifiers, for the entire forest.</span></span> <span data-ttu-id="b6734-125">Para pesquisar objetos no contêiner de configuração, associe-se ao contêiner de configuração em qualquer controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b6734-125">To search for objects in the configuration container, bind to the configuration container on any domain controller.</span></span> <span data-ttu-id="b6734-126">O contêiner de configuração está disponível em todos os controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="b6734-126">The configuration container is available on all domain controllers.</span></span> <span data-ttu-id="b6734-127">O nome distinto do contêiner de configuração é obtido do atributo **configurationNamingContext** de RootDSE.</span><span class="sxs-lookup"><span data-stu-id="b6734-127">The distinguished name of the configuration container is obtained from the **configurationNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="b6734-128">Para obter mais informações sobre o rootDSE e o atributo **configurationNamingContext** , consulte [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="b6734-128">For more information about rootDSE and the **configurationNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

## <a name="searching-the-global-catalog"></a><span data-ttu-id="b6734-129">Pesquisando o catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6734-129">Searching the Global Catalog</span></span>

<span data-ttu-id="b6734-130">O catálogo global mantém uma réplica de cada objeto em Active Directory Domain Services, mas com apenas um pequeno número de seus atributos.</span><span class="sxs-lookup"><span data-stu-id="b6734-130">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="b6734-131">Os atributos no catálogo global são aqueles usados com mais frequência em operações de pesquisa, como nomes e sobrenome de um usuário, nomes de logon e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b6734-131">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="b6734-132">Para obter mais informações sobre como pesquisar o catálogo global, consulte [pesquisando o catálogo global](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="b6734-132">For more information about searching the global catalog, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 