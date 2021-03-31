---
title: Associação a objetos Well-Known usando WKGUID
description: Este tópico mostra como associar objetos usando a cadeia de caracteres de associação WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Associação a objetos de Well-Known usando o AD WKGUID
- Active Directory, usando, associação, usando WKGUID para associar a objetos bem conhecidos
- objetos conhecidos do AD
- objetos conhecidos do AD, ligando-se ao usando WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640436"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a><span data-ttu-id="adb7e-107">Associação a objetos Well-Known usando WKGUID</span><span class="sxs-lookup"><span data-stu-id="adb7e-107">Binding to Well-Known Objects Using WKGUID</span></span>

<span data-ttu-id="adb7e-108">Os contêineres podem ter um ou mais subobjetos importantes que podem ser renomeados ou movidos.</span><span class="sxs-lookup"><span data-stu-id="adb7e-108">Containers can have one, or more, important subobjects that can be renamed or moved.</span></span> <span data-ttu-id="adb7e-109">Pode ser difícil controlar esses subobjetos e criar cadeias de vinculação corretas para eles, especialmente se eles forem renomeados ou movidos.</span><span class="sxs-lookup"><span data-stu-id="adb7e-109">It can be difficult to track these subobjects and build correct binding strings for them, especially if they are renamed or moved.</span></span>

<span data-ttu-id="adb7e-110">Para dar suporte à associação de renomeação segura a esses objetos dentro desses contêineres, Active Directory Domain Services têm dois atributos: **wellKnownObjects** e **otherWellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="adb7e-110">To support rename-safe binding to these objects within these containers, Active Directory Domain Services have two attributes: **wellKnownObjects** and **otherWellKnownObjects**.</span></span> <span data-ttu-id="adb7e-111">Esses atributos têm uma sintaxe de atributo de \_ DN ADSTYPE \_ com \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="adb7e-111">These attributes have an attribute syntax of ADSTYPE\_DN\_WITH\_BINARY.</span></span> <span data-ttu-id="adb7e-112">Eles permitem vários valores e contêm as tuplas GUID/DN de objetos bem conhecidos dentro dos contêineres nos quais eles estão definidos.</span><span class="sxs-lookup"><span data-stu-id="adb7e-112">They allow multiple values and contain the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="adb7e-113">O servidor de Active Directory mantém a parte do nome distinto de cada entrada **wellKnownObjects** e **otherWellKnownObjects** para que ela contenha o nome distinto atual do objeto especificado quando a entrada foi criada.</span><span class="sxs-lookup"><span data-stu-id="adb7e-113">The Active Directory server maintains the distinguished name portion of each **wellKnownObjects** and **otherWellKnownObjects** entry so that it contains the current distinguished name of the object specified when the entry was created.</span></span>

<span data-ttu-id="adb7e-114">A propriedade **otherWellKnownObjects** pode ser definida e usada em qualquer objeto.</span><span class="sxs-lookup"><span data-stu-id="adb7e-114">The **otherWellKnownObjects** property can be set and used on any object.</span></span>

<span data-ttu-id="adb7e-115">A propriedade **wellKnownObjects** é usada nos contêineres de configuração e DomainDNS.</span><span class="sxs-lookup"><span data-stu-id="adb7e-115">The **wellKnownObjects** property is used on the domainDNS and configuration containers.</span></span> <span data-ttu-id="adb7e-116">A propriedade **wellKnownObjects** é uma propriedade somente do sistema e só pode ser modificada pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="adb7e-116">The **wellKnownObjects** property is a system-only property and can only be modified by the operating system.</span></span>

<span data-ttu-id="adb7e-117">O contêiner **domainDns** tem os seguintes objetos bem conhecidos:</span><span class="sxs-lookup"><span data-stu-id="adb7e-117">The **domainDNS** container has the following well-known objects:</span></span>

-   <span data-ttu-id="adb7e-118">Usuários</span><span class="sxs-lookup"><span data-stu-id="adb7e-118">Users</span></span>
-   <span data-ttu-id="adb7e-119">Computadores</span><span class="sxs-lookup"><span data-stu-id="adb7e-119">Computers</span></span>
-   <span data-ttu-id="adb7e-120">Sistema</span><span class="sxs-lookup"><span data-stu-id="adb7e-120">System</span></span>
-   <span data-ttu-id="adb7e-121">Controladores de Domínio</span><span class="sxs-lookup"><span data-stu-id="adb7e-121">Domain Controllers</span></span>
-   <span data-ttu-id="adb7e-122">Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="adb7e-122">Infrastructure</span></span>
-   <span data-ttu-id="adb7e-123">Objetos excluídos</span><span class="sxs-lookup"><span data-stu-id="adb7e-123">Deleted Objects</span></span>
-   <span data-ttu-id="adb7e-124">Perdidos e encontrados</span><span class="sxs-lookup"><span data-stu-id="adb7e-124">Lost and Found</span></span>

<span data-ttu-id="adb7e-125">O contêiner de configuração tem o objeto bem conhecido: objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="adb7e-125">The configuration container has the well-known object: Deleted Objects.</span></span>

<span data-ttu-id="adb7e-126">Esses objetos estão em cada **domainDns** e contêiner de configuração em um serviço domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="adb7e-126">These objects are in every **domainDNS** and configuration container in an Active Directory Domain Service.</span></span>

<span data-ttu-id="adb7e-127">Você pode associar a um objeto conhecido usando o formato de associação WKGUID.</span><span class="sxs-lookup"><span data-stu-id="adb7e-127">You can bind to a well-known object using the WKGUID binding format.</span></span> <span data-ttu-id="adb7e-128">Só há suporte para associação com WKGUID em Active Directory Domain Services, ou seja, o provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="adb7e-128">Binding with WKGUID is only supported in Active Directory Domain Services, that is, the LDAP provider.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="adb7e-129">Sempre use o formato de associação WKGUID para se associar aos objetos conhecidos, conforme listado acima, nos contêineres de domínio e configuração.</span><span class="sxs-lookup"><span data-stu-id="adb7e-129">Always use the WKGUID binding format to bind to the well-known objects, as listed above, in the domain and configuration containers.</span></span> <span data-ttu-id="adb7e-130">Isso garante que esses contêineres possam ser associados mesmo se forem movidos ou renomeados.</span><span class="sxs-lookup"><span data-stu-id="adb7e-130">This ensures that these containers can be bound to even if they are moved or renamed.</span></span>

 

<span data-ttu-id="adb7e-131">O formato da cadeia de vinculação WKGUID é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="adb7e-131">The WKGUID binding string format is as follows:</span></span>


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



<span data-ttu-id="adb7e-132">" &lt; nome do servidor &gt; " é o nome do servidor de diretório.</span><span class="sxs-lookup"><span data-stu-id="adb7e-132">"&lt;server name&gt;" is the directory server name.</span></span> <span data-ttu-id="adb7e-133">O " &lt; nome do servidor &gt; " é opcional.</span><span class="sxs-lookup"><span data-stu-id="adb7e-133">The "&lt;server name&gt;" is optional.</span></span>

<span data-ttu-id="adb7e-134">" &lt; Xxxxx &gt; " é a representação de cadeia de caracteres do valor HEXADECIMAL do GUID que representa o objeto bem conhecido.</span><span class="sxs-lookup"><span data-stu-id="adb7e-134">"&lt;XXXXX&gt;" is the string representation of the hexadecimal value of the GUID that represents the well-known object.</span></span> <span data-ttu-id="adb7e-135">A cadeia de caracteres GUID é especificada no formulário "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" e não é a mesma forma que a cadeia de caracteres GUID produzida pela função [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , que usa o formato "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="adb7e-135">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form and is not the same form as the GUID string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, which takes the form "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span></span> <span data-ttu-id="adb7e-136">Para obter mais informações e um exemplo de código que mostra como criar uma cadeia de caracteres vinculável de um GUID, consulte [exemplo de código para criar uma representação de cadeia de caracteres vinculável de um GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="adb7e-136">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span>

<span data-ttu-id="adb7e-137">Para associar a um objeto especificado em **otherWellKnownObjects** em um objeto, especifique " &lt; xxxxx &gt; " como a forma de cadeia de caracteres de associação do GUID de objeto conhecido do objeto.</span><span class="sxs-lookup"><span data-stu-id="adb7e-137">To bind to an object specified in **otherWellKnownObjects** in an object, specify "&lt;XXXXX&gt;" as the bind string form of the well-known object GUID of the object.</span></span> <span data-ttu-id="adb7e-138">Para obter mais informações, consulte [lendo o OBJECTguid de um objeto e criando uma representação de cadeia de caracteres do GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span><span class="sxs-lookup"><span data-stu-id="adb7e-138">For more information, see [Reading an Object's objectGUID and Creating a String Representation of the GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span></span> <span data-ttu-id="adb7e-139">Para obter mais informações sobre como definir a propriedade **otherWellKnownObjects** em objetos, consulte [habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span><span class="sxs-lookup"><span data-stu-id="adb7e-139">For more information about setting the **otherWellKnownObjects** property on objects, see [Enabling Rename-Safe Binding with the otherWellKnownObjects Property](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span></span>

<span data-ttu-id="adb7e-140">Para associar a um objeto especificado em **wellKnownObjects** em domainDns ou contêineres de configuração, especifique " &lt; xxxxx &gt; " como uma das constantes a seguir, listadas na tabela a seguir, conforme definido em NTDSAPI. h.</span><span class="sxs-lookup"><span data-stu-id="adb7e-140">To bind to an object specified in **wellKnownObjects** in domainDNS or configuration containers, specify "&lt;XXXXX&gt;" as one of the following constants, listed in the following table, as defined in Ntdsapi.h.</span></span>



| <span data-ttu-id="adb7e-141">Contêiner</span><span class="sxs-lookup"><span data-stu-id="adb7e-141">Container</span></span>          | <span data-ttu-id="adb7e-142">Identificador GUID</span><span class="sxs-lookup"><span data-stu-id="adb7e-142">GUID Identifier</span></span>                         |
|--------------------|-----------------------------------------|
| <span data-ttu-id="adb7e-143">Usuários</span><span class="sxs-lookup"><span data-stu-id="adb7e-143">Users</span></span>              | <span data-ttu-id="adb7e-144">\_contêiner de usuários GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="adb7e-144">GUID\_USERS\_CONTAINER\_W</span></span>               |
| <span data-ttu-id="adb7e-145">Computadores</span><span class="sxs-lookup"><span data-stu-id="adb7e-145">Computers</span></span>          | <span data-ttu-id="adb7e-146">\_contêiner COMPUTRS \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="adb7e-146">GUID\_COMPUTRS\_CONTAINER\_W</span></span>            |
| <span data-ttu-id="adb7e-147">Sistema</span><span class="sxs-lookup"><span data-stu-id="adb7e-147">System</span></span>             | <span data-ttu-id="adb7e-148">contêiner de sistemas de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="adb7e-148">GUID\_SYSTEMS\_CONTAINER\_W</span></span>             |
| <span data-ttu-id="adb7e-149">Controladores de Domínio</span><span class="sxs-lookup"><span data-stu-id="adb7e-149">Domain Controllers</span></span> | <span data-ttu-id="adb7e-150">contêiner de controladores de domínio do GUID \_ \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="adb7e-150">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span> |
| <span data-ttu-id="adb7e-151">Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="adb7e-151">Infrastructure</span></span>     | <span data-ttu-id="adb7e-152">contêiner de infraestrutura de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="adb7e-152">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>      |
| <span data-ttu-id="adb7e-153">Objetos excluídos</span><span class="sxs-lookup"><span data-stu-id="adb7e-153">Deleted Objects</span></span>    | <span data-ttu-id="adb7e-154">\_contêiner de objetos excluídos de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="adb7e-154">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>    |
| <span data-ttu-id="adb7e-155">Perdidos e encontrados</span><span class="sxs-lookup"><span data-stu-id="adb7e-155">Lost and Found</span></span>     | <span data-ttu-id="adb7e-156">contêiner de LOSTANDFOUND de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="adb7e-156">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>        |



 

<span data-ttu-id="adb7e-157">Por exemplo, para associar ao contêiner de usuário em um domínio, especifique **o \_ contêiner de usuários GUID \_ \_ W** como " &lt; xxxxx &gt; ".</span><span class="sxs-lookup"><span data-stu-id="adb7e-157">For example, to bind to the user container in a domain, specify **GUID\_USERS\_CONTAINER\_W** as "&lt;XXXXX&gt;".</span></span>

<span data-ttu-id="adb7e-158">" &lt; container DN &gt; " é o nome distinto do objeto de contêiner que tem esse objeto representado como um valor em sua propriedade **wellKnownObjects** .</span><span class="sxs-lookup"><span data-stu-id="adb7e-158">"&lt;container DN&gt;" is the distinguished name of the container object that has this object represented as a value in its **wellKnownObjects** property.</span></span> <span data-ttu-id="adb7e-159">Por exemplo, para associar ao contêiner usuários em um domínio, especifique o nome distinto do domínio como o " &lt; DN do contêiner &gt; ".</span><span class="sxs-lookup"><span data-stu-id="adb7e-159">For example, to bind to the users container in a domain, specify the domain distinguished name as the "&lt;container DN&gt;".</span></span>

<span data-ttu-id="adb7e-160">Por exemplo, para associar ao contêiner usuários do domínio Fabrikam.com, use a cadeia de vinculação a seguir.</span><span class="sxs-lookup"><span data-stu-id="adb7e-160">For example, to bind to the users container of the domain Fabrikam.com, use the following binding string.</span></span>

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

<span data-ttu-id="adb7e-161">Para obter mais informações e um exemplo de código que mostra como associar a um GUID bem conhecido, consulte [código de exemplo para associação a objetos bem conhecidos](example-code-for-binding-to-well-known-objects.md).</span><span class="sxs-lookup"><span data-stu-id="adb7e-161">For more information and a code example that shows how to bind to a well-known GUID, see [Example Code for Binding to Well Known Objects](example-code-for-binding-to-well-known-objects.md).</span></span>

 

 