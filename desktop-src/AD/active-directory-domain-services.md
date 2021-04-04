---
title: Active Directory Domain Services
description: A Microsoft Active Directory Domain Services é a base para redes distribuídas criadas nos sistemas operacionais Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 que usam controladores de domínio.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, página inicial
- Active Directory Domain Services Active Directory, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008568"
---
# <a name="active-directory-domain-services"></a><span data-ttu-id="949eb-106">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="949eb-106">Active Directory Domain Services</span></span>

## <a name="purpose"></a><span data-ttu-id="949eb-107">Finalidade</span><span class="sxs-lookup"><span data-stu-id="949eb-107">Purpose</span></span>

<span data-ttu-id="949eb-108">A Microsoft Active Directory Domain Services é a base para redes distribuídas criadas nos sistemas operacionais Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 que usam controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="949eb-108">Microsoft Active Directory Domain Services are the foundation for distributed networks built on Windows 2000 Server, Windows Server 2003 and Microsoft Windows Server 2008 operating systems that use domain controllers.</span></span> <span data-ttu-id="949eb-109">Active Directory Domain Services fornecem armazenamento de dados hierárquicos seguro e estruturado para objetos em uma rede, como usuários, computadores, impressoras e serviços.</span><span class="sxs-lookup"><span data-stu-id="949eb-109">Active Directory Domain Services provide secure, structured, hierarchical data storage for objects in a network such as users, computers, printers, and services.</span></span> <span data-ttu-id="949eb-110">Active Directory Domain Services fornecer suporte para localizar e trabalhar com esses objetos.</span><span class="sxs-lookup"><span data-stu-id="949eb-110">Active Directory Domain Services provide support for locating and working with these objects.</span></span>

<span data-ttu-id="949eb-111">Este guia fornece uma visão geral do Active Directory Domain Services e do código de exemplo para tarefas básicas, como Pesquisar objetos e ler propriedades para tarefas mais avançadas, como publicação de serviço.</span><span class="sxs-lookup"><span data-stu-id="949eb-111">This guide provides an overview of Active Directory Domain Services and sample code for basic tasks, such as searching for objects and reading properties, to more advanced tasks such as service publication.</span></span>

<span data-ttu-id="949eb-112">O Windows 2000 Server e os sistemas operacionais posteriores fornecem uma interface do usuário para que os usuários e administradores trabalhem com os objetos e dados no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="949eb-112">Windows 2000 Server and later operating systems provide a user interface for users and administrators to work with the objects and data in Active Directory Domain Services.</span></span> <span data-ttu-id="949eb-113">Este guia descreve como estender e personalizar essa interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="949eb-113">This guide describes how to extend and customize that user interface.</span></span> <span data-ttu-id="949eb-114">Ele também descreve como estender Active Directory Domain Services definindo novas classes de objeto e atributos.</span><span class="sxs-lookup"><span data-stu-id="949eb-114">It also describes how to extend Active Directory Domain Services by defining new object classes and attributes.</span></span>

> [!Note]  
> <span data-ttu-id="949eb-115">A documentação a seguir destina-se a programadores de computadores.</span><span class="sxs-lookup"><span data-stu-id="949eb-115">The following documentation is for computer programmers.</span></span> <span data-ttu-id="949eb-116">Se você for um usuário final tentando depurar um erro de impressão ou um problema de rede doméstica, consulte os [fóruns da Comunidade da Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="949eb-116">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="949eb-117">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="949eb-117">Where applicable</span></span>

<span data-ttu-id="949eb-118">Os administradores de rede gravam scripts e aplicativos que acessam Active Directory Domain Services para automatizar tarefas administrativas comuns, como adicionar usuários e grupos, gerenciar impressoras e definir permissões para recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="949eb-118">Network administrators write scripts and applications that access Active Directory Domain Services to automate common administrative tasks, such as adding users and groups, managing printers, and setting permissions for network resources.</span></span>

<span data-ttu-id="949eb-119">Fornecedores independentes de software e desenvolvedores de usuário final podem usar Active Directory Domain Services programação para habilitar o diretório de seus produtos e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="949eb-119">Independent software vendors and end-user developers can use Active Directory Domain Services programming to directory-enable their products and applications.</span></span> <span data-ttu-id="949eb-120">Os serviços podem se publicar em Active Directory Domain Services; Os clientes podem usar Active Directory Domain Services para localizar serviços, e ambos podem usar Active Directory Domain Services para localizar e trabalhar com outros objetos em uma rede.</span><span class="sxs-lookup"><span data-stu-id="949eb-120">Services can publish themselves in Active Directory Domain Services; clients can use Active Directory Domain Services to find services, and both can use Active Directory Domain Services to locate and work with other objects on a network.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="949eb-121">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="949eb-121">Developer audience</span></span>

<span data-ttu-id="949eb-122">Os aplicativos que acessam dados no Active Directory Domain Services podem ser gravados usando a API de [interfaces de serviço do Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , a API do protocolo de acesso ao [diretório leve](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) ou o namespace [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="949eb-122">Applications that access data in Active Directory Domain Services can be written using the [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md) API, [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API, or the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="949eb-123">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="949eb-123">Run-time requirements</span></span>

<span data-ttu-id="949eb-124">Active Directory Domain Services executado no Windows 2000 e em controladores de domínio posteriores.</span><span class="sxs-lookup"><span data-stu-id="949eb-124">Active Directory Domain Services run on Windows 2000 and later domain controllers.</span></span> <span data-ttu-id="949eb-125">No entanto, os aplicativos cliente podem ser escritos e executados no Windows Vista, no Windows Server 2003, no Windows XP, no Windows 2000, no Windows NT 4,0, no Windows 98 e no Windows 95.</span><span class="sxs-lookup"><span data-stu-id="949eb-125">However, client applications can be written for and run on Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="949eb-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="949eb-126">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="949eb-127">Sobre Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="949eb-127">About Active Directory Domain Services</span></span>](about-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="949eb-128">Informações gerais sobre Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="949eb-128">General information about Active Directory Domain Services.</span></span>

</dd> <dt>

[<span data-ttu-id="949eb-129">Usar o Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="949eb-129">Using Active Directory Domain Services</span></span>](using-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="949eb-130">Guia de programação do Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="949eb-130">Active Directory Domain Services programming guide.</span></span>

</dd> <dt>

[<span data-ttu-id="949eb-131">Referência de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="949eb-131">Active Directory Domain Services Reference</span></span>](active-directory-domain-services-reference.md)
</dt> <dd>

<span data-ttu-id="949eb-132">Active Directory Domain Services referência de programação.</span><span class="sxs-lookup"><span data-stu-id="949eb-132">Active Directory Domain Services programming reference.</span></span>

</dd> </dl>

 

 