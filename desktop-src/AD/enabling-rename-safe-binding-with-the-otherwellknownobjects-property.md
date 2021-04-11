---
title: Habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects
description: Objetos da classe de contêiner têm um atributo otherWellKnownObjects que você pode usar para associar um GUID com o DN (nome distinto) de um objeto filho no contêiner.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- Propriedade otherWellKnownObjects
- Propriedade otherWellKnownObjects, usando para associação de renomeação segura
- Active Directory, usando, associação, associação de renomeação segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159328"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a><span data-ttu-id="b2bdc-106">Habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="b2bdc-106">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>

<span data-ttu-id="b2bdc-107">Objetos da classe de contêiner têm um atributo **otherWellKnownObjects** que você pode usar para associar um GUID com o DN (nome distinto) de um objeto filho no contêiner.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-107">Objects of the Container class have an **otherWellKnownObjects** attribute that you can use to associate a GUID with the distinguished name (DN) of a child object in the container.</span></span> <span data-ttu-id="b2bdc-108">Se o objeto filho for movido ou renomeado, o servidor de Active Directory atualizará o DN no valor **otherWellKnownObjects** para esse objeto filho.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-108">If the child object is moved or renamed, the Active Directory server updates the DN in the **otherWellKnownObjects** value for that child object.</span></span> <span data-ttu-id="b2bdc-109">Isso permite o uso do recurso de associação WKGUID para associar ao objeto filho usando o GUID e o DN do contêiner em vez do DN do objeto filho.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-109">This enables use of the WKGUID binding feature to bind to the child object using the GUID and the DN of the container rather than the child object's DN.</span></span>

<span data-ttu-id="b2bdc-110">O atributo **otherWellKnownObjects** é equivalente ao atributo **wellKnownObjects** , exceto que aplicativos e serviços podem gravar um valor **otherWellKnownObjects** , mas apenas o sistema pode gravar **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-110">The **otherWellKnownObjects** attribute is equivalent to the **wellKnownObjects** attribute except that applications and services can write an **otherWellKnownObjects** value, but only the system can write **wellKnownObjects**.</span></span>

<span data-ttu-id="b2bdc-111">Usar o atributo **otherWellKnownObjects** e a associação WKGUID é benéfico nas seguintes situações em que a associação renomear-seguro é necessária em relação a um objeto de contêiner específico.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-111">Using **otherWellKnownObjects** attribute and WKGUID binding is beneficial in the following situations where rename-safe binding is required in relation to a specific container object.</span></span>

<span data-ttu-id="b2bdc-112">Se um objeto de contêiner contiver outros objetos importantes ou se objetos importantes puderem ser renomeados ou movidos.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-112">If a container object contains other important objects, or if important objects can be renamed or moved.</span></span>

<span data-ttu-id="b2bdc-113">Se os objetos importantes existirem para cada instância do objeto de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-113">If the important objects exist for each instance of the container object.</span></span> <span data-ttu-id="b2bdc-114">Por exemplo, o sistema usa o atributo **wellKnownObjects** de cada objeto **domainDns** para armazenar um valor para o contêiner Users, que existe em cada instância de um objeto **domainDns** .</span><span class="sxs-lookup"><span data-stu-id="b2bdc-114">For example, the system uses the **wellKnownObjects** attribute of each **domainDNS** object to store a value for the Users container, which exists in every instance of a **domainDNS** object.</span></span> <span data-ttu-id="b2bdc-115">Isso permite que os aplicativos se associem ao contêiner de usuários em uma forma de renomeação segura, especificando o GUID bem conhecido e o DN do contêiner **domainDns** .</span><span class="sxs-lookup"><span data-stu-id="b2bdc-115">This enables applications to bind to the Users container in a rename-safe way by specifying the well-known GUID and the DN of the **domainDNS** container.</span></span> <span data-ttu-id="b2bdc-116">Os aplicativos podem usar o atributo **otherWellKnownObjects** de um contêiner da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-116">Applications can use a container's **otherWellKnownObjects** attribute similarly.</span></span>

<span data-ttu-id="b2bdc-117">Se você precisar de uma associação de renomeação segura e/ou recurso de pesquisa nos objetos importantes.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-117">If you require rename-safe binding and/or search capability on the important objects.</span></span>

<span data-ttu-id="b2bdc-118">**Para adicionar recursos de pesquisa e Associação de renomeação segura**</span><span class="sxs-lookup"><span data-stu-id="b2bdc-118">**To add rename-safe binding and search capabilities**</span></span>

1.  <span data-ttu-id="b2bdc-119">Adicione um valor à propriedade **otherWellKnownObjects** do objeto de contêiner quando o objeto importante for criado dentro desse contêiner.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-119">Add a value to the **otherWellKnownObjects** property of the container object when the important object is created within that container.</span></span> <span data-ttu-id="b2bdc-120">O valor contém o GUID que representa o objeto bem conhecido.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-120">The value contains the GUID that represents the well-known object.</span></span> <span data-ttu-id="b2bdc-121">Lembre-se de que isso não é o **objectGUID** e o **distinguishedName** para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-121">Be aware that this is not the **objectGUID** and the **distinguishedName** for that object.</span></span>
2.  <span data-ttu-id="b2bdc-122">Use o recurso de associação WKGUID para associar ou pesquisar o objeto importante.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-122">Use the WKGUID binding feature to bind to or search the important object.</span></span>

<span data-ttu-id="b2bdc-123">O atributo **otherWellKnownObjects** pode ter vários valores e contém as tuplas GUID/DN de objetos bem conhecidos dentro dos contêineres nos quais eles estão definidos.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-123">The **otherWellKnownObjects** attribute can have multiple values and contains the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="b2bdc-124">O atributo **otherWellKnownObjects** tem a sintaxe DNWithBinary na qual os valores têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="b2bdc-124">The **otherWellKnownObjects** attribute has the DNWithBinary syntax in which values have the following form:</span></span>


```C++
B:<char count>:<well known GUID>:<object DN>
```



<span data-ttu-id="b2bdc-125">Neste exemplo, " &lt; contagem de caracteres &gt; " é a contagem de dígitos hexadecimais em " &lt; GUID bem conhecido &gt; ", que é 32 (número de dígitos hexadecimais em um GUID) para **otherWellKnownObjects** e **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-125">In this example, "&lt;char count&gt;" is the count of hexadecimal digits in "&lt;well known GUID&gt;", which is 32 (number of hex digits in a GUID) for both **otherWellKnownObjects** and **wellKnownObjects**.</span></span> <span data-ttu-id="b2bdc-126">" &lt; GUID bem conhecido &gt; " é a representação de dígito HEXADECIMAL do GUID conhecido.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-126">"&lt;well known GUID&gt;" is the hexadecimal digit representation of the well-known GUID.</span></span> <span data-ttu-id="b2bdc-127">" &lt; Object DN &gt; " é o nome distinto do objeto representado por esse valor de WKO.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-127">"&lt;object DN&gt;" is the distinguished name of the object represented by this WKO value.</span></span> <span data-ttu-id="b2bdc-128">O servidor mantém a parte ObjectDN de cada valor de **wellKnownObjects** e **otherWellKnownObjects** para que ele contenha o nome distinto atual do objeto especificado originalmente quando o valor foi criado.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-128">The server maintains the ObjectDN portion of each **wellKnownObjects** and **otherWellKnownObjects** value so that it contains the current distinguished name of the object originally specified when the value was created.</span></span>

<span data-ttu-id="b2bdc-129">Por exemplo, se {df447b5e-aa5b-11D2-8D53-00c04f79ab81} for o GUID bem conhecido do objeto MyObject no contêiner MyContainer no domínio Fabrikam.com, o valor **otherWellKnownObjects** especificará o GUID bem conhecido e o DN de MyObject:</span><span class="sxs-lookup"><span data-stu-id="b2bdc-129">For example, if {df447b5e-aa5b-11d2-8d53-00c04f79ab81} is the well-known GUID of the MyObject object in the MyContainer container in the Fabrikam.com domain, the **otherWellKnownObjects** value would specify the well-known GUID and the DN of MyObject:</span></span>


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



<span data-ttu-id="b2bdc-130">Para associar a esse objeto, use a seguinte cadeia de vinculação WKGUID que especifica o GUID bem conhecido do objeto e o DN do contêiner:</span><span class="sxs-lookup"><span data-stu-id="b2bdc-130">To bind to this object, use the following WKGUID binding string that specifies the well-known GUID of the object and the DN of the container:</span></span>


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



<span data-ttu-id="b2bdc-131">Após a associação a esse objeto, você pode usar as interfaces COM do ADSI para pesquisar, ler, modificar ou excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="b2bdc-131">After binding to this object, you can use the ADSI COM interfaces to search, read, modify, or delete the object.</span></span>

<span data-ttu-id="b2bdc-132">Para obter mais informações e um exemplo de código que mostra como adicionar um objeto ao atributo **otherWellKnownObjects** , consulte [exemplo de código para criar um objeto de contêiner](example-code-for-creating-a-container-object.md).</span><span class="sxs-lookup"><span data-stu-id="b2bdc-132">For more information and a code example that shows how to add an object to the **otherWellKnownObjects** attribute, see [Example Code for Creating a Container Object](example-code-for-creating-a-container-object.md).</span></span>

 

 




