---
title: Usar o Active Directory Domain Services
description: Esta seção fornece diretrizes para a gravação de aplicativos que usam ou publicam dados em um serviço de diretório Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, usando
- Active Directory Domain Services Active Directory, usando
- Exemplos de Active Directory Active Directory
- Exemplos de Active Directory Domain Services Active Directory
- exemplos Active Directory
- Active Directory Active Directory, exemplos consulte Active Directory Domain Services exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642911"
---
# <a name="using-active-directory-domain-services"></a><span data-ttu-id="d2c23-109">Usar o Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d2c23-109">Using Active Directory Domain Services</span></span>

<span data-ttu-id="d2c23-110">Esta seção fornece diretrizes para a gravação de aplicativos que usam ou publicam dados em um serviço de diretório Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d2c23-110">This section provides guidelines for writing applications that use or publish data in an Active Directory directory service.</span></span>

> [!Note]  
> <span data-ttu-id="d2c23-111">A documentação a seguir destina-se a programadores de computadores.</span><span class="sxs-lookup"><span data-stu-id="d2c23-111">The following documentation is for computer programmers.</span></span> <span data-ttu-id="d2c23-112">Se você estiver tentando resolver um erro de impressão Active Directory Home, consulte a [seguinte sugestão](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) nas páginas da Comunidade da Microsoft; Se isso não ajudar, tente essas recomendações no [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span><span class="sxs-lookup"><span data-stu-id="d2c23-112">If you are trying to resolve an Active Directory home printing error, see the [following suggestion](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) from the Microsoft community pages; if that doesn't help, try these recommendations from [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span></span>

 

<span data-ttu-id="d2c23-113">Active Directory Domain Services estão em conformidade com o Lightweight Directory Access Protocol 3,0, que é definido pela RFC 2251 e por outras RFCs.</span><span class="sxs-lookup"><span data-stu-id="d2c23-113">Active Directory Domain Services are compliant with Lightweight Directory Access Protocol 3.0, which is defined by RFC 2251 and other RFCs.</span></span> <span data-ttu-id="d2c23-114">Qualquer um dos seguintes conjuntos de API pode ser usado para acessar Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="d2c23-114">Any of the following API sets can be used to access Active Directory Domain Services.</span></span> <span data-ttu-id="d2c23-115">Cada conjunto de API tem vantagens e desvantagens que dependem da linguagem de programação, do ambiente de programação e do método pretendido de execução.</span><span class="sxs-lookup"><span data-stu-id="d2c23-115">Each API set has advantages and disadvantages that depend on the programming language, programming environment, and intended method of execution.</span></span> <span data-ttu-id="d2c23-116">A maioria dos exemplos neste guia usa ADSI, que é compatível com linguagens como C e C++, bem como linguagens em conformidade com a automação, como Microsoft Visual Basic e Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="d2c23-116">The majority of the examples in this guide use ADSI, which is supported by languages such as C and C++, as well as automation-compliant languages such as Microsoft Visual Basic and Visual Basic Scripting Edition.</span></span>

<span data-ttu-id="d2c23-117">Para obter mais informações sobre tecnologias de Active Directory Domain Services específicas, consulte:</span><span class="sxs-lookup"><span data-stu-id="d2c23-117">For more information about specific Active Directory Domain Services technologies, see:</span></span>

-   [<span data-ttu-id="d2c23-118">Protocolo Lightweight Directory Access</span><span class="sxs-lookup"><span data-stu-id="d2c23-118">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [<span data-ttu-id="d2c23-119">Active Directory Service Interfaces</span><span class="sxs-lookup"><span data-stu-id="d2c23-119">Active Directory Service Interfaces</span></span>](../adsi/active-directory-service-interfaces-adsi.md)
-   [<span data-ttu-id="d2c23-120">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="d2c23-120">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)

<span data-ttu-id="d2c23-121">Esta seção aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d2c23-121">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="d2c23-122">Associando a Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d2c23-122">Binding to Active Directory Domain Services</span></span>](binding-to-active-directory-domain-services.md)
-   [<span data-ttu-id="d2c23-123">Pesquisando no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d2c23-123">Searching in Active Directory Domain Services</span></span>](searching-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d2c23-124">Criando e excluindo objetos no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d2c23-124">Creating and Deleting Objects in Active Directory Domain Services</span></span>](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d2c23-125">Movendo objetos</span><span class="sxs-lookup"><span data-stu-id="d2c23-125">Moving Objects</span></span>](moving-objects.md)
-   [<span data-ttu-id="d2c23-126">Lendo e gravando atributos de objetos no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d2c23-126">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d2c23-127">Controlando o acesso a objetos no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d2c23-127">Controlling Access to Objects in Active Directory Domain Services</span></span>](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="d2c23-128">Estendendo o esquema</span><span class="sxs-lookup"><span data-stu-id="d2c23-128">Extending the Schema</span></span>](extending-the-schema.md)
-   [<span data-ttu-id="d2c23-129">Estendendo a interface do usuário para objetos de diretório</span><span class="sxs-lookup"><span data-stu-id="d2c23-129">Extending the User Interface for Directory Objects</span></span>](extending-the-user-interface-for-directory-objects.md)
-   [<span data-ttu-id="d2c23-130">Gerenciando usuários</span><span class="sxs-lookup"><span data-stu-id="d2c23-130">Managing Users</span></span>](managing-users.md)
-   [<span data-ttu-id="d2c23-131">Gerenciando grupos</span><span class="sxs-lookup"><span data-stu-id="d2c23-131">Managing Groups</span></span>](managing-groups.md)
-   [<span data-ttu-id="d2c23-132">Controlando alterações</span><span class="sxs-lookup"><span data-stu-id="d2c23-132">Tracking Changes</span></span>](tracking-changes.md)
-   [<span data-ttu-id="d2c23-133">Publicação de serviço</span><span class="sxs-lookup"><span data-stu-id="d2c23-133">Service Publication</span></span>](service-publication.md)
-   [<span data-ttu-id="d2c23-134">Contas de logon de serviço</span><span class="sxs-lookup"><span data-stu-id="d2c23-134">Service Logon Accounts</span></span>](service-logon-accounts.md)
-   [<span data-ttu-id="d2c23-135">Autenticação mútua usando Kerberos</span><span class="sxs-lookup"><span data-stu-id="d2c23-135">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
-   [<span data-ttu-id="d2c23-136">Fazendo backup e restaurando Active Directory</span><span class="sxs-lookup"><span data-stu-id="d2c23-136">Backing Up and Restoring Active Directory</span></span>](backing-up-and-restoring-an-active-directory-server.md)
-   [<span data-ttu-id="d2c23-137">Armazenando Dados Dinâmicos</span><span class="sxs-lookup"><span data-stu-id="d2c23-137">Storing Dynamic Data</span></span>](storing-dynamic-data.md)
-   [<span data-ttu-id="d2c23-138">Partições de diretório de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d2c23-138">Application Directory Partitions</span></span>](application-directory-partitions.md)
-   [<span data-ttu-id="d2c23-139">Detectando o modo de operação de um domínio</span><span class="sxs-lookup"><span data-stu-id="d2c23-139">Detecting the Operation Mode of a Domain</span></span>](detecting-the-operation-mode-of-a-domain.md)

 

 