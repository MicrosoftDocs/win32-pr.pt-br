---
title: Associando a Active Directory Domain Services
description: Em Active Directory Domain Services, o ato de associar um objeto programático a um objeto de Active Directory Domain Services específico é conhecido como associação.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- Associação a Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, associação a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920192"
---
# <a name="binding-to-active-directory-domain-services"></a><span data-ttu-id="136f0-105">Associando a Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="136f0-105">Binding to Active Directory Domain Services</span></span>

<span data-ttu-id="136f0-106">Em Active Directory Domain Services, o ato de associar um objeto programático a um objeto de Active Directory Domain Services específico é conhecido como *Associação*.</span><span class="sxs-lookup"><span data-stu-id="136f0-106">In Active Directory Domain Services, the act of associating a programmatic object with a specific Active Directory Domain Services object is known as *binding*.</span></span> <span data-ttu-id="136f0-107">Quando um objeto programático, como um objeto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , é associado a um objeto de diretório específico, o objeto programático é considerado *associado ao* objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="136f0-107">When a programmatic object, such as an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) object, is associated with a specific directory object, the programmatic object is considered to be *bound to* the directory object.</span></span>

## <a name="binding-functions-and-methods"></a><span data-ttu-id="136f0-108">Funções e métodos de associação</span><span class="sxs-lookup"><span data-stu-id="136f0-108">Binding Functions and Methods</span></span>

<span data-ttu-id="136f0-109">O método de ligação programaticamente a um objeto Active Directory dependerá da tecnologia de programação usada.</span><span class="sxs-lookup"><span data-stu-id="136f0-109">The method for programmatically binding to an Active Directory object will depend on the programming technology that is used.</span></span> <span data-ttu-id="136f0-110">Para obter mais informações sobre a associação a objetos no Active Directory Domain Services com uma tecnologia de programação específica, consulte os tópicos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="136f0-110">For more information about binding to objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="136f0-111">Tecnologia de programação</span><span class="sxs-lookup"><span data-stu-id="136f0-111">Programming technology</span></span>                                                                       | <span data-ttu-id="136f0-112">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="136f0-112">For more information</span></span>                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="136f0-113">Active Directory Service Interfaces</span><span class="sxs-lookup"><span data-stu-id="136f0-113">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="136f0-114">Associação a um objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="136f0-114">Binding to an ADSI Object</span></span>](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [<span data-ttu-id="136f0-115">Protocolo Lightweight Directory Access</span><span class="sxs-lookup"><span data-stu-id="136f0-115">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="136f0-116">Estabelecendo uma sessão LDAP</span><span class="sxs-lookup"><span data-stu-id="136f0-116">Establishing an LDAP Session</span></span>](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [<span data-ttu-id="136f0-117">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="136f0-117">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)                 | <span data-ttu-id="136f0-118">[Associação a objetos de diretório](/previous-versions/ms180840(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="136f0-118">[Binding to Directory Objects](/previous-versions/ms180840(v=vs.90))</span></span> |



 

## <a name="binding-strings"></a><span data-ttu-id="136f0-119">Cadeias de vinculação</span><span class="sxs-lookup"><span data-stu-id="136f0-119">Binding Strings</span></span>

<span data-ttu-id="136f0-120">Todos os métodos e funções de associação exigem uma cadeia de caracteres de associação.</span><span class="sxs-lookup"><span data-stu-id="136f0-120">All bind functions and methods require a binding string.</span></span> <span data-ttu-id="136f0-121">A forma da cadeia de vinculação depende do provedor.</span><span class="sxs-lookup"><span data-stu-id="136f0-121">The form of the binding string depends on the provider.</span></span> <span data-ttu-id="136f0-122">Os Active Directory Domain Services têm suporte de dois provedores, LDAP e WinNT.</span><span class="sxs-lookup"><span data-stu-id="136f0-122">Active Directory Domain Services are supported by two providers, LDAP and WinNT.</span></span>

<span data-ttu-id="136f0-123">A partir do Windows 2000, o provedor LDAP é usado para acessar Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="136f0-123">Beginning with Windows 2000, the LDAP provider is used to access Active Directory Domain Services.</span></span> <span data-ttu-id="136f0-124">A cadeia de caracteres de associação LDAP pode ter um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="136f0-124">The LDAP binding string can take one of the following forms:</span></span>

-   <span data-ttu-id="136f0-125">"LDAP:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="136f0-125">"LDAP://<host name>/<object name>"</span></span>
-   <span data-ttu-id="136f0-126">"GC:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="136f0-126">"GC://<host name>/<object name>"</span></span>

<span data-ttu-id="136f0-127">Nos exemplos acima, "LDAP:" especifica o provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="136f0-127">In the examples above, "LDAP:" specifies the LDAP provider.</span></span> <span data-ttu-id="136f0-128">"GC:" usa o provedor LDAP para associar ao serviço de catálogo global para executar consultas rápidas.</span><span class="sxs-lookup"><span data-stu-id="136f0-128">"GC:" uses the LDAP provider to bind to the Global Catalog service to execute fast queries.</span></span>

<span data-ttu-id="136f0-129">" &lt; nome &gt; do host" especifica o servidor a ser associado e é opcional.</span><span class="sxs-lookup"><span data-stu-id="136f0-129">"&lt;host name&gt;" specifies the server to bind to and is optional.</span></span> <span data-ttu-id="136f0-130">Se possível, não especifique um servidor.</span><span class="sxs-lookup"><span data-stu-id="136f0-130">If possible, do not specify a server.</span></span> <span data-ttu-id="136f0-131">Também é possível associar a um objeto em um domínio diferente.</span><span class="sxs-lookup"><span data-stu-id="136f0-131">It is also possible to bind to an object in a different domain.</span></span> <span data-ttu-id="136f0-132">Para fazer isso, passe o nome DNS (sistema de nomeação de domínio) do domínio de destino para " &lt; nome do host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="136f0-132">To do this pass the domain naming system (DNS) name of the target domain for "&lt;host name&gt;".</span></span> <span data-ttu-id="136f0-133">Por exemplo, para associar ao contêiner usuários no domínio domain2 de fabrikam.com, a cadeia de caracteres de associação seria "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span><span class="sxs-lookup"><span data-stu-id="136f0-133">For example, to bind to the Users container in the domain2 domain of fabrikam.com, the binding string would be "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span></span>

<span data-ttu-id="136f0-134">" &lt; nome &gt; do objeto" representa um objeto específico em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="136f0-134">"&lt;object name&gt;" represents a specific object in Active Directory Domain Services.</span></span> <span data-ttu-id="136f0-135">O nome do objeto pode ser um nome diferenciado ou um GUID de objeto.</span><span class="sxs-lookup"><span data-stu-id="136f0-135">The object name can be a distinguished name or an object GUID.</span></span>

<span data-ttu-id="136f0-136">Para obter mais informações sobre cadeias de vinculação LDAP, consulte [ADsPath do LDAP](/windows/desktop/ADSI/ldap-adspath).</span><span class="sxs-lookup"><span data-stu-id="136f0-136">For more information about LDAP binding strings, see [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span></span>

<span data-ttu-id="136f0-137">Para o Windows NT 4,0, o provedor WinNT é usado para acessar dados de diretório, como usuários, grupos de usuários, computadores, serviços e outros objetos de rede no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="136f0-137">For Windows NT 4.0, the WinNT provider is used for access to directory data such as users, user groups, computers, services, and other network objects in the Windows 2000.</span></span> <span data-ttu-id="136f0-138">O provedor WinNT no Windows 2000 e sistemas posteriores tem funcionalidade limitada em comparação com o provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="136f0-138">The WinNT provider on Windows 2000 and later systems has limited functionality compared to the LDAP provider.</span></span> <span data-ttu-id="136f0-139">Para obter mais informações sobre cadeias de vinculação de WinNT, consulte o [ADsPath do Winnt](/windows/desktop/ADSI/winnt-adspath).</span><span class="sxs-lookup"><span data-stu-id="136f0-139">For more information about WinNT binding strings, see [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span></span>

<span data-ttu-id="136f0-140">Um ADsPath de "LDAP://" ou "GC://" pode ser usado para associar à raiz do namespace.</span><span class="sxs-lookup"><span data-stu-id="136f0-140">An ADsPath of "LDAP://" or "GC://" can be used to bind to the root of the namespace.</span></span> <span data-ttu-id="136f0-141">Quando associado à raiz do namespace, o objeto namespace fornecido não contém propriedades e contém o objeto de domínio para LDAP e um objeto de contêiner que contém uma réplica parcial de todos os domínios na floresta para GC.</span><span class="sxs-lookup"><span data-stu-id="136f0-141">When bound to the root of the namespace, the supplied namespace object contains no properties and contains the domain object for LDAP and a container object containing a partial replica of all domains in the forest for GC.</span></span>

<span data-ttu-id="136f0-142">Para obter mais informações sobre associação em Active Directory Domain Services, consulte:</span><span class="sxs-lookup"><span data-stu-id="136f0-142">For more information about binding in Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="136f0-143">Associação sem servidor e RootDSE</span><span class="sxs-lookup"><span data-stu-id="136f0-143">Serverless Binding and RootDSE</span></span>](serverless-binding-and-rootdse.md)
-   [<span data-ttu-id="136f0-144">Associação ao catálogo global</span><span class="sxs-lookup"><span data-stu-id="136f0-144">Binding to the Global Catalog</span></span>](binding-to-the-global-catalog.md)
-   [<span data-ttu-id="136f0-145">Usando objectGUID para associar a um objeto</span><span class="sxs-lookup"><span data-stu-id="136f0-145">Using objectGUID to Bind to an Object</span></span>](using-objectguid-to-bind-to-an-object.md)
-   [<span data-ttu-id="136f0-146">Associação a objetos Well-Known usando WKGUID</span><span class="sxs-lookup"><span data-stu-id="136f0-146">Binding to Well-Known Objects Using WKGUID</span></span>](binding-to-well-known-objects-using-wkguid.md)
-   [<span data-ttu-id="136f0-147">Associação a um objeto usando um SID</span><span class="sxs-lookup"><span data-stu-id="136f0-147">Binding to an Object Using a SID</span></span>](binding-to-an-object-using-a-sid.md)
-   [<span data-ttu-id="136f0-148">Habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="136f0-148">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [<span data-ttu-id="136f0-149">Autenticação</span><span class="sxs-lookup"><span data-stu-id="136f0-149">Authentication</span></span>](authentication.md)

 

 
