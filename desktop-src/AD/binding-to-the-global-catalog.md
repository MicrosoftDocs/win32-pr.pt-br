---
title: Associação ao catálogo global
description: O catálogo global é um namespace que contém dados de diretório para todos os domínios em uma floresta.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Associação ao AD do catálogo global
- AD de catálogo global, associando a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007359"
---
# <a name="binding-to-the-global-catalog"></a><span data-ttu-id="fe13a-105">Associação ao catálogo global</span><span class="sxs-lookup"><span data-stu-id="fe13a-105">Binding to the Global Catalog</span></span>

<span data-ttu-id="fe13a-106">O catálogo global é um namespace que contém dados de diretório para todos os domínios em uma floresta.</span><span class="sxs-lookup"><span data-stu-id="fe13a-106">The Global Catalog is a namespace that contains directory data for all domains in a forest.</span></span> <span data-ttu-id="fe13a-107">O catálogo global contém uma réplica parcial de cada diretório de domínio.</span><span class="sxs-lookup"><span data-stu-id="fe13a-107">The Global Catalog contains a partial replica of every domain directory.</span></span> <span data-ttu-id="fe13a-108">Ele contém uma entrada para cada objeto na floresta da empresa, mas não contém todas as propriedades de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="fe13a-108">It contains an entry for every object in the enterprise forest, but does not contain all the properties of each object.</span></span> <span data-ttu-id="fe13a-109">Em vez disso, ele contém apenas as propriedades especificadas para inclusão no catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-109">Instead, it contains only the properties specified for inclusion in the Global Catalog.</span></span>

<span data-ttu-id="fe13a-110">O catálogo global é armazenado em servidores específicos em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="fe13a-110">The Global Catalog is stored on specific servers throughout the enterprise.</span></span> <span data-ttu-id="fe13a-111">Somente os controladores de domínio podem servir como servidores de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-111">Only domain controllers can serve as Global Catalog servers.</span></span> <span data-ttu-id="fe13a-112">Os administradores indicam se um determinado controlador de domínio contém um catálogo global usando o Active Directory sites e o Gerenciador de serviços.</span><span class="sxs-lookup"><span data-stu-id="fe13a-112">Administrators indicate whether a given domain controller holds a Global Catalog by using the Active Directory Sites and Services Manager.</span></span>

<span data-ttu-id="fe13a-113">Para associar ao catálogo global com a ADSI, use o moniker "GC:".</span><span class="sxs-lookup"><span data-stu-id="fe13a-113">To bind to the Global Catalog with ADSI, use the "GC:" moniker.</span></span>

<span data-ttu-id="fe13a-114">Há duas maneiras de se associar ao catálogo global para executar uma pesquisa em uma floresta:</span><span class="sxs-lookup"><span data-stu-id="fe13a-114">There are two ways to bind to the Global Catalog to perform a search in a forest:</span></span>

-   <span data-ttu-id="fe13a-115">Associe-se ao objeto raiz da empresa para pesquisar em todos os domínios na floresta.</span><span class="sxs-lookup"><span data-stu-id="fe13a-115">Bind to the enterprise root object to search across all domains in the forest.</span></span>
-   <span data-ttu-id="fe13a-116">Associar a um objeto específico para pesquisar o objeto e seus filhos.</span><span class="sxs-lookup"><span data-stu-id="fe13a-116">Bind to a specific object to search that object and its children.</span></span> <span data-ttu-id="fe13a-117">Por exemplo, se você associar a um domínio que tem dois domínios abaixo dele em uma árvore de domínio na floresta, poderá pesquisar entre esses três domínios.</span><span class="sxs-lookup"><span data-stu-id="fe13a-117">For example, if you bind to a domain that has two domains beneath it in a domain tree in the forest, you can search across those three domains.</span></span> <span data-ttu-id="fe13a-118">Lembre-se de que o nome distinto para o objeto a ser associado é exatamente o mesmo que o nome distinto usado para ligar ao namespace "LDAP:".</span><span class="sxs-lookup"><span data-stu-id="fe13a-118">Be aware that the distinguished name for the object to bind to is exactly the same as the distinguished name used to bind to the "LDAP:" namespace.</span></span> <span data-ttu-id="fe13a-119">Lembre-se de que "LDAP:" é uma réplica completa de um único domínio e que "GC:" é uma réplica parcial de todos os domínios na floresta.</span><span class="sxs-lookup"><span data-stu-id="fe13a-119">Recall that "LDAP:" is a full replica of a single domain and that "GC:" is a partial replica of all domains in the forest.</span></span>

<span data-ttu-id="fe13a-120">Assim como no moniker "LDAP:", você pode usar a associação sem servidor ou associar a um servidor de catálogo global específico.</span><span class="sxs-lookup"><span data-stu-id="fe13a-120">As with the "LDAP:" moniker, you can use serverless binding or bind to a specific Global Catalog server.</span></span> <span data-ttu-id="fe13a-121">Se estiver pesquisando na floresta atual, use a associação sem servidor.</span><span class="sxs-lookup"><span data-stu-id="fe13a-121">If searching in the current forest, use serverless binding.</span></span> <span data-ttu-id="fe13a-122">No entanto, se pesquisar em outra floresta, especifique um nome de domínio ou um servidor de catálogo global para associar, como mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe13a-122">However, if searching in another forest, specify either a domain name or a Global Catalog server to bind to, such as shown in the following examples.</span></span>

<span data-ttu-id="fe13a-123">Associar usando o nome de domínio:</span><span class="sxs-lookup"><span data-stu-id="fe13a-123">Bind using the domain name:</span></span>

``` syntax
GC://fabrikam.com
```

<span data-ttu-id="fe13a-124">Associar usando o nome do servidor:</span><span class="sxs-lookup"><span data-stu-id="fe13a-124">Bind using the server name:</span></span>

``` syntax
GC://servername
```

<span data-ttu-id="fe13a-125">Você também pode associar a um objeto específico dentro do catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-125">You can also bind to a specific object within the Global Catalog.</span></span> <span data-ttu-id="fe13a-126">Para associar ao objeto Sales no domínio fabrikam, use o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe13a-126">To bind to the sales object in the fabrikam domain, use the following format.</span></span>

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="fe13a-127">Ou, para associar ao objeto Sales no servidor, use o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe13a-127">Or, to bind to the sales object on the server, use the following format.</span></span>

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="fe13a-128">**Para Pesquisar toda a floresta**</span><span class="sxs-lookup"><span data-stu-id="fe13a-128">**To search the entire forest**</span></span>

1.  <span data-ttu-id="fe13a-129">Associe-se à raiz do namespace do catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-129">Bind to the root of the Global Catalog namespace.</span></span>
2.  <span data-ttu-id="fe13a-130">Enumere o contêiner do catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-130">Enumerate the Global Catalog container.</span></span> <span data-ttu-id="fe13a-131">O contêiner de catálogo global contém um único objeto que você pode usar para Pesquisar toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="fe13a-131">The Global Catalog container contains a single object that you can use to search the entire forest.</span></span>
3.  <span data-ttu-id="fe13a-132">Use o objeto no contêiner para executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fe13a-132">Use the object in the container to perform the search.</span></span> <span data-ttu-id="fe13a-133">Em C/C++, chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) no objeto para que você possa usar a interface **IDirectorySearch** para executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fe13a-133">In C/C++, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer on the object so that you can use the **IDirectorySearch** interface to perform the search.</span></span> <span data-ttu-id="fe13a-134">Em Visual Basic, use o objeto retornado da enumeração em sua consulta ADO.</span><span class="sxs-lookup"><span data-stu-id="fe13a-134">In Visual Basic, use the object returned from the enumeration in your ADO query.</span></span>

<span data-ttu-id="fe13a-135">Para enumerar os servidores de catálogo global em um site, execute uma pesquisa de subárvore LDAP de "CN = <yoursite> , CN = sites <DN of the configurationNamingContext> ", usando a cadeia de caracteres de filtro a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe13a-135">To enumerate the Global Catalog servers in a site, perform an LDAP subtree search of "cn=<yoursite>,cn=sites,<DN of the configurationNamingContext>", using the following filter string.</span></span>

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

<span data-ttu-id="fe13a-136">Esse filtro usa o **\_ bit de regra de correspondência LDAP \_ \_ \_ e** o operador de regra de correspondência (1.2.840.113556.1.4.803) para localizar objetos **nTDSDSA** que têm o bit de ordem inferior definido no bitmask do atributo **Options** .</span><span class="sxs-lookup"><span data-stu-id="fe13a-136">This filter uses the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator (1.2.840.113556.1.4.803) to find **nTDSDSA** objects that have the low-order bit set in the bitmask of the **options** attribute.</span></span> <span data-ttu-id="fe13a-137">O bit de ordem inferior, que corresponde ao **NTDSDSA \_ opt \_ é \_** constante de GC definido em NTDSAPI. h, identifica o objeto **NTDSDSA** de um servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-137">The low-order bit, which corresponds to the **NTDSDSA\_OPT\_IS\_GC** constant defined in Ntdsapi.h, identifies the **nTDSDSA** object of a Global Catalog server.</span></span> <span data-ttu-id="fe13a-138">Para obter mais informações sobre regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="fe13a-138">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="fe13a-139">O pai do objeto **nTDSDSA** é o objeto Server, e a propriedade **dNSHostName** do objeto Server é o nome DNS do servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-139">The parent of the **nTDSDSA** object is the server object, and the **dNSHostName** property of the server object is the DNS name of the Global Catalog server.</span></span>

<span data-ttu-id="fe13a-140">Você não pode usar \# definir constantes como **NTDSDSA \_ opt \_ é \_** o bit de regra de correspondência de GC e **LDAP \_ \_ \_ \_ e** diretamente em uma cadeia de caracteres de filtro de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fe13a-140">You cannot use \#define constants such as **NTDSDSA\_OPT\_IS\_GC** and **LDAP\_MATCHING\_RULE\_BIT\_AND** directly in a search filter string.</span></span> <span data-ttu-id="fe13a-141">No entanto, você pode usar essas constantes como argumentos para uma função, como [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) , para inserir os valores constantes em uma cadeia de caracteres de filtro.</span><span class="sxs-lookup"><span data-stu-id="fe13a-141">However, you could use these constants as arguments to a function such as [**swprintf\_s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) to insert the constant values into a filter string.</span></span>

<span data-ttu-id="fe13a-142">O catálogo global não representa toda a estrutura de árvore da floresta.</span><span class="sxs-lookup"><span data-stu-id="fe13a-142">The global catalog does not represent the entire forest tree structure.</span></span> <span data-ttu-id="fe13a-143">Por exemplo, você pode esperar que o exemplo de código a seguir Enumere todos os domínios na floresta e todos os objetos filho de cada domínio.</span><span class="sxs-lookup"><span data-stu-id="fe13a-143">For example, you might expect that the following code example would enumerate all of the domains in the forest and all child objects of each domain.</span></span> <span data-ttu-id="fe13a-144">Na realidade, o que ele realmente faz é enumerar todos os domínios na floresta, mas nenhum dos objetos de domínio enumerados contém quaisquer filhos.</span><span class="sxs-lookup"><span data-stu-id="fe13a-144">In reality, what it actually does is enumerate all of the domains in the forest, but none of the enumerated domain objects contain any children.</span></span> <span data-ttu-id="fe13a-145">Essa é uma limitação do catálogo global.</span><span class="sxs-lookup"><span data-stu-id="fe13a-145">This is a limitation of the global catalog.</span></span>


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="fe13a-146">Para corrigir isso, é necessário associar a cada objeto de domínio e, em seguida, enumerar os objetos filho de cada domínio.</span><span class="sxs-lookup"><span data-stu-id="fe13a-146">To correct this, it is necessary to bind to each domain object and then enumerate the child objects of each domain.</span></span> <span data-ttu-id="fe13a-147">A técnica apropriada é mostrada no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe13a-147">The proper technique is shown in the following code example.</span></span>


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="fe13a-148">Para obter mais informações e exemplos de código que mostram como pesquisar uma floresta inteira, consulte [exemplo de código para pesquisar uma floresta](example-code-for-searching-a-forest.md).</span><span class="sxs-lookup"><span data-stu-id="fe13a-148">For more information and code examples that show how to search an entire forest, see [Example Code for Searching a Forest](example-code-for-searching-a-forest.md).</span></span>

 

 