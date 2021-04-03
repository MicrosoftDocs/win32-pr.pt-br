---
title: Sobre Active Directory Domain Services
description: Este guia fornece informações essenciais para integrar o Microsoft Active Directory em aplicativos distribuídos projetados para sistemas operacionais que dão suporte a Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, sobre
- Active Directory Domain Services Active Directory, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007592"
---
# <a name="about-active-directory-domain-services"></a><span data-ttu-id="8c6d4-105">Sobre Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="8c6d4-105">About Active Directory Domain Services</span></span>

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a><span data-ttu-id="8c6d4-106">Escrevendo aplicativos poderosos que usam Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="8c6d4-106">Writing Powerful Applications that Use Active Directory Domain Services</span></span>

<span data-ttu-id="8c6d4-107">Este guia fornece informações essenciais para a integração de Active Directory Domain Services em aplicativos distribuídos projetados para sistemas operacionais que dão suporte a Active Directory Domain Services, incluindo:</span><span class="sxs-lookup"><span data-stu-id="8c6d4-107">This guide provides essential information for integrating Active Directory Domain Services in distributed applications designed for operating systems that support Active Directory Domain Services, including:</span></span>

-   <span data-ttu-id="8c6d4-108">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c6d4-108">Windows Server 2008</span></span>
-   <span data-ttu-id="8c6d4-109">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8c6d4-109">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="8c6d4-110">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c6d4-110">Windows Server 2012</span></span>
-   <span data-ttu-id="8c6d4-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8c6d4-111">Windows Server 2012 R2</span></span>
-   <span data-ttu-id="8c6d4-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8c6d4-112">Windows Server 2016</span></span>

> [!Note]  
> <span data-ttu-id="8c6d4-113">Esses tópicos são para desenvolvedores de software.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-113">These topics are for software developers.</span></span> <span data-ttu-id="8c6d4-114">Para problemas de suporte, consulte [suporte da Microsoft](https://windows.microsoft.com/windows/support#1tc).</span><span class="sxs-lookup"><span data-stu-id="8c6d4-114">For support issues, see [Microsoft Support](https://windows.microsoft.com/windows/support#1tc).</span></span> <span data-ttu-id="8c6d4-115">Para obter informações sobre como administrar Active Directory, consulte [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) no TechNet.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-115">For information about administering Active Directory, see [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) at TechNet.</span></span>

 

## <a name="fundamental-directory-features"></a><span data-ttu-id="8c6d4-116">Recursos de diretório fundamental</span><span class="sxs-lookup"><span data-stu-id="8c6d4-116">Fundamental Directory Features</span></span>

<span data-ttu-id="8c6d4-117">Um serviço de diretório é um serviço fundamental para aplicativos distribuídos.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-117">A directory service is a fundamental service for distributed applications.</span></span> <span data-ttu-id="8c6d4-118">Um serviço de diretório deve fornecer os recursos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-118">A directory service must provide the features listed in the following table.</span></span>



| <span data-ttu-id="8c6d4-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="8c6d4-119">Feature</span></span>               | <span data-ttu-id="8c6d4-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c6d4-120">Description</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6d4-121">Transparência da localização</span><span class="sxs-lookup"><span data-stu-id="8c6d4-121">Location transparency</span></span> | <span data-ttu-id="8c6d4-122">Capaz de encontrar dados de usuário, grupo, serviço de rede ou recurso, sem o endereço do objeto</span><span class="sxs-lookup"><span data-stu-id="8c6d4-122">Able to find user, group, networked service, or resource, data without the object address</span></span>           |
| <span data-ttu-id="8c6d4-123">Dados de objetos</span><span class="sxs-lookup"><span data-stu-id="8c6d4-123">Object data</span></span>           | <span data-ttu-id="8c6d4-124">Capaz de armazenar dados de usuário, grupo, organização e serviço em uma árvore hierárquica</span><span class="sxs-lookup"><span data-stu-id="8c6d4-124">Able to store user, group, organization, and service data in a hierarchical tree</span></span>                    |
| <span data-ttu-id="8c6d4-125">Consulta avançada</span><span class="sxs-lookup"><span data-stu-id="8c6d4-125">Rich query</span></span>            | <span data-ttu-id="8c6d4-126">Capaz de localizar um objeto consultando as propriedades do objeto</span><span class="sxs-lookup"><span data-stu-id="8c6d4-126">Able to locate an object by querying for object properties</span></span>                                          |
| <span data-ttu-id="8c6d4-127">Alta disponibilidade</span><span class="sxs-lookup"><span data-stu-id="8c6d4-127">High availability</span></span>     | <span data-ttu-id="8c6d4-128">Capaz de localizar uma réplica do diretório em um local que seja eficiente para operações de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8c6d4-128">Able to locate a replica of the directory at a location that is efficient for read/write operations</span></span> |



 

## <a name="advanced-features-of-active-directory-domain-services"></a><span data-ttu-id="8c6d4-129">Recursos avançados do Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="8c6d4-129">Advanced Features of Active Directory Domain Services</span></span>

<span data-ttu-id="8c6d4-130">Active Directory Domain Services fornece os recursos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-130">Active Directory Domain Services provides the features listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c6d4-131">Recurso</span><span class="sxs-lookup"><span data-stu-id="8c6d4-131">Feature</span></span></th>
<th><span data-ttu-id="8c6d4-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c6d4-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c6d4-133">Suporte para padrões da Internet</span><span class="sxs-lookup"><span data-stu-id="8c6d4-133">Support for Internet standards</span></span></td>
<td><span data-ttu-id="8c6d4-134">Active Directory Domain Services implementa seus recursos de acordo com os padrões de Internet publicados, como LDAP e DNS.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-134">Active Directory Domain Services implements its features in accordance with published Internet standards such as LDAP and DNS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6d4-135">Segurança totalmente integrada e flexível</span><span class="sxs-lookup"><span data-stu-id="8c6d4-135">Tightly integrated and flexible security</span></span></td>
<td><span data-ttu-id="8c6d4-136">As vantagens incluem:</span><span class="sxs-lookup"><span data-stu-id="8c6d4-136">Advantages include:</span></span><br/>
<ul>
<li><span data-ttu-id="8c6d4-137">Opção de pacotes de autenticação.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-137">Choice of authentication packages.</span></span> <span data-ttu-id="8c6d4-138">Kerberos, protocolo SSL (SSL) ou uma combinação; por exemplo, estabeleça um canal SSL para criptografia e, em seguida, use o Kerberos para autenticação.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-138">Kerberos, Secure Sockets Layer (SSL), or a combination; for example, establish an SSL channel for encryption and then use Kerberos for authentication.</span></span></li>
<li><span data-ttu-id="8c6d4-139">Gerenciamento central de acesso de serviço e de recursos usando os usuários e grupos no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-139">Central management of service and resource access by using the users and groups in Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="8c6d4-140">Delegação de administração para que os administradores centrais possam delegar tarefas administrativas, como alteração de senha ou criação e exclusão de objetos específicos.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-140">Delegation of administration so that central administrators can delegate administrative tasks such as password changing or specific object creation and deletion.</span></span></li>
<li><span data-ttu-id="8c6d4-141">O servidor de Active Directory usa os mesmos mecanismos de controle de acesso usados em sistemas de arquivos nos sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-141">The Active Directory server uses the same access control mechanisms used on file systems in the Windows operating systems.</span></span> <span data-ttu-id="8c6d4-142">Portanto, as mesmas ferramentas que gerenciam o controle de acesso em um sistema de arquivos funcionam para Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-142">Thus, the same tools that manage access control on a file system work for Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="8c6d4-143">Infraestrutura de chave pública abrangente.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-143">Comprehensive Public Key infrastructure.</span></span> <span data-ttu-id="8c6d4-144">O suporte ao servidor de certificado da Microsoft e ao cartão inteligente são integrados com o Active Directory Domain Services para fornecer logon de cartão inteligente e gerenciamento de certificados.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-144">The Microsoft Certificate Server and Smart Card support are integrated with Active Directory Domain Services to provide Smart Card logon and Certificate management.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6d4-145">Programável facilmente</span><span class="sxs-lookup"><span data-stu-id="8c6d4-145">Easily programmable</span></span></td>
<td><span data-ttu-id="8c6d4-146">O servidor de Active Directory pode ser acessado e administrado por meio de programação usando a API de <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfaces de serviço do Active Directory</a> , a API do protocolo de acesso ao <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">diretório leve</a> ou o namespace <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</span><span class="sxs-lookup"><span data-stu-id="8c6d4-146">The Active Directory server can be programmatically accessed and administered using the <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces</a> API, <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API, or the <a href="/dotnet/api/system.directoryservices">System.DirectoryServices</a> namespace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6d4-147">Serviços do sistema habilitados para diretório</span><span class="sxs-lookup"><span data-stu-id="8c6d4-147">Directory enabled system services</span></span></td>
<td><span data-ttu-id="8c6d4-148">Seu aplicativo cliente pode ser facilmente implantado em áreas de trabalho distribuídas criando um pacote de Windows Installer e usando o recurso de implantação de aplicativo disponível nos sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-148">Your client application can be easily deployed to distributed desktops by creating a Windows Installer package and using the application deployment feature available in the Windows operating systems.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6d4-149">Integração de aplicativos-chave</span><span class="sxs-lookup"><span data-stu-id="8c6d4-149">Key application integration</span></span></td>
<td><span data-ttu-id="8c6d4-150">Os principais aplicativos distribuídos, como o Exchange, são integrados com o Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-150">Key distributed applications, such as Exchange, are integrated with Active Directory Domain Services.</span></span> <span data-ttu-id="8c6d4-151">Portanto, as empresas podem reduzir o número de serviços de diretório a serem gerenciados.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-151">Thus, companies can reduce the number of directory services to be managed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6d4-152">Esquema rico e extensível</span><span class="sxs-lookup"><span data-stu-id="8c6d4-152">Rich and extensible schema</span></span></td>
<td><span data-ttu-id="8c6d4-153">O esquema define quais objetos e propriedades podem ser gravados e lidos a partir de um serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-153">The schema defines what objects and properties can be written and read from a directory service.</span></span> <span data-ttu-id="8c6d4-154">O esquema de Active Directory é avançado.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-154">The Active Directory Schema is rich.</span></span> <span data-ttu-id="8c6d4-155">A maioria dos objetos e propriedades que um serviço requer estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-155">Most of the objects and properties a service requires are available.</span></span> <span data-ttu-id="8c6d4-156">Caso contrário, um aplicativo distribuído pode estender o esquema para dar suporte aos requisitos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-156">If not, a distributed application can extend the schema to support the application requirements.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8c6d4-157">Para obter mais informações sobre Active Directory Domain Services, consulte:</span><span class="sxs-lookup"><span data-stu-id="8c6d4-157">For more information about Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="8c6d4-158">Conceitos principais do Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="8c6d4-158">Core Concepts of Active Directory Domain Services</span></span>](core-concepts-of-active-directory-domain-services.md)
-   [<span data-ttu-id="8c6d4-159">Arquitetura de Active Directory</span><span class="sxs-lookup"><span data-stu-id="8c6d4-159">Active Directory Architecture</span></span>](active-directory-domain-services-architecture.md)
-   [<span data-ttu-id="8c6d4-160">Esquema do Active Directory</span><span class="sxs-lookup"><span data-stu-id="8c6d4-160">Active Directory Schema</span></span>](active-directory-schema.md)

