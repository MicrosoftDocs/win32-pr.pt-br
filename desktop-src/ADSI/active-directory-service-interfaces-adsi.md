---
title: Active Directory Service Interfaces
description: Introdução às interfaces de serviços Active Directory, com links para guias diferentes.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfaces de serviço Active Directory (consulte ADSI)
- ADSI ADSI, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008363"
---
# <a name="active-directory-service-interfaces"></a><span data-ttu-id="ff455-106">Active Directory Service Interfaces</span><span class="sxs-lookup"><span data-stu-id="ff455-106">Active Directory Service Interfaces</span></span>

## <a name="purpose"></a><span data-ttu-id="ff455-107">Finalidade</span><span class="sxs-lookup"><span data-stu-id="ff455-107">Purpose</span></span>

<span data-ttu-id="ff455-108">A ADSI (Active Directory Service Interfaces) é um conjunto de interfaces COM usadas para acessar os recursos dos serviços de diretório de diferentes provedores de rede.</span><span class="sxs-lookup"><span data-stu-id="ff455-108">Active Directory Service Interfaces (ADSI) is a set of COM interfaces used to access the features of directory services from different network providers.</span></span> <span data-ttu-id="ff455-109">A ADSI é usada em um ambiente de computação distribuído para apresentar um único conjunto de interfaces de serviço de diretório para gerenciar recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="ff455-109">ADSI is used in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="ff455-110">Os administradores e desenvolvedores podem usar os serviços ADSI para enumerar e gerenciar os recursos em um serviço de diretório, não importa qual ambiente de rede contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="ff455-110">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="ff455-111">A ADSI permite tarefas administrativas comuns, como a adição de novos usuários, o gerenciamento de impressoras e a localização de recursos em um ambiente de computação distribuído.</span><span class="sxs-lookup"><span data-stu-id="ff455-111">ADSI enables common administrative tasks, such as adding new users, managing printers, and locating resources in a distributed computing environment.</span></span>

> [!Note]  
> <span data-ttu-id="ff455-112">A documentação a seguir destina-se a programadores de computadores.</span><span class="sxs-lookup"><span data-stu-id="ff455-112">The following documentation is for computer programmers.</span></span> <span data-ttu-id="ff455-113">Se você for um usuário final tentando depurar um erro de impressão ou um problema de rede doméstica, consulte os [fóruns da Comunidade da Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ff455-113">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="ff455-114">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="ff455-114">Where applicable</span></span>

<span data-ttu-id="ff455-115">Os administradores de rede podem usar o ADSI para automatizar tarefas comuns, como adicionar usuários e grupos, gerenciar impressoras e definir permissões em recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="ff455-115">Network Administrators can use ADSI to automate common tasks, such as adding users and groups, managing printers, and setting permissions on network resources.</span></span>

<span data-ttu-id="ff455-116">Fornecedores independentes de software e desenvolvedores de usuários finais podem usar o ADSI para "diretório habilitado" para seus produtos e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ff455-116">Independent Software Vendors and end-user developers can use ADSI to "directory enable" their products and applications.</span></span> <span data-ttu-id="ff455-117">Os serviços podem se publicar em um diretório, os clientes podem usar o diretório para localizar os serviços, e ambos podem usar o diretório para localizar e manipular outros objetos de interesse.</span><span class="sxs-lookup"><span data-stu-id="ff455-117">Services can publish themselves in a directory, clients can use the directory to find the services, and both can use the directory to find and manipulate other objects of interest.</span></span> <span data-ttu-id="ff455-118">Como as interfaces de serviço do Active Directory são independentes dos serviços de diretório subjacentes, os produtos e aplicativos habilitados para diretório podem operar com êxito em vários ambientes de rede e de diretório.</span><span class="sxs-lookup"><span data-stu-id="ff455-118">Because Active Directory Service Interfaces are independent of the underlying directory service(s), directory-enabled products and applications can operate successfully in multiple network and directory environments.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ff455-119">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="ff455-119">Developer audience</span></span>

<span data-ttu-id="ff455-120">Você pode escrever aplicativos cliente ADSI em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="ff455-120">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="ff455-121">Para a maioria das tarefas administrativas, a ADSI define interfaces e objetos acessíveis a partir de linguagens em conformidade com a automação, como o Microsoft Visual Basic, o Microsoft Visual Basic Scripting Edition (VBScript) e o Java, para obter mais linguagens de desempenho e eficiência, como C e C++.</span><span class="sxs-lookup"><span data-stu-id="ff455-121">For most administrative tasks, ADSI defines interfaces and objects accessible from Automation-compliant languages like Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and Java to the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="ff455-122">Uma boa base na programação COM é útil para o programador ADSI.</span><span class="sxs-lookup"><span data-stu-id="ff455-122">A good foundation in COM programming is useful to the ADSI programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ff455-123">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="ff455-123">Run-time requirements</span></span>

<span data-ttu-id="ff455-124">O Active Directory é executado em controladores de domínio do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ff455-124">Active Directory runs on Windows Server domain controllers.</span></span> <span data-ttu-id="ff455-125">No entanto, os aplicativos cliente que usam ADSI podem ser escritos e executados no Windows.</span><span class="sxs-lookup"><span data-stu-id="ff455-125">However, client applications using ADSI may be written and run on Windows.</span></span> <span data-ttu-id="ff455-126">Além disso, os desenvolvedores deverão ter o SDK (Software Development Kit) da plataforma, também disponível no site do MSDN.</span><span class="sxs-lookup"><span data-stu-id="ff455-126">In addition, developers will want the Platform Software Development Kit (SDK), also available on the MSDN website.</span></span> <span data-ttu-id="ff455-127">Para investigar o conteúdo de Active Directory, use o snap-in do MMC usuários e computadores Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ff455-127">To investigate the contents of Active Directory, use the Active Directory Users and Computers MMC snap-in.</span></span> <span data-ttu-id="ff455-128">Esse snap-in substitui a ferramenta ADSVW que estava disponível para versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="ff455-128">This snap-in replaces the Adsvw tool that was available for previous versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ff455-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ff455-129">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ff455-130">Sobre o ADSI</span><span class="sxs-lookup"><span data-stu-id="ff455-130">About ADSI</span></span>](about-adsi.md)
</dt> <dd>

<span data-ttu-id="ff455-131">Informações gerais sobre ADSI.</span><span class="sxs-lookup"><span data-stu-id="ff455-131">General information about ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="ff455-132">Usando ADSI</span><span class="sxs-lookup"><span data-stu-id="ff455-132">Using ADSI</span></span>](using-adsi.md)
</dt> <dd>

<span data-ttu-id="ff455-133">Guia do programador para usar o ADSI.</span><span class="sxs-lookup"><span data-stu-id="ff455-133">Programmer's Guide to using ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="ff455-134">Tutoriais de início rápido do ADSI</span><span class="sxs-lookup"><span data-stu-id="ff455-134">ADSI Quick-start Tutorials</span></span>](adsi-quick-start-tutorials.md)
</dt> <dd>

<span data-ttu-id="ff455-135">Usando o ADSI com a automação para gerenciar diretórios.</span><span class="sxs-lookup"><span data-stu-id="ff455-135">Using ADSI with Automation to manage directories.</span></span>

</dd> <dt>

[<span data-ttu-id="ff455-136">Referência ADSI</span><span class="sxs-lookup"><span data-stu-id="ff455-136">ADSI Reference</span></span>](adsi-reference.md)
</dt> <dd>

<span data-ttu-id="ff455-137">Documentação de interfaces e métodos ADSI.</span><span class="sxs-lookup"><span data-stu-id="ff455-137">Documentation of ADSI interfaces and methods.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ff455-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff455-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff455-139">O Component Object Model</span><span class="sxs-lookup"><span data-stu-id="ff455-139">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> <dt>

[<span data-ttu-id="ff455-140">Clientes e servidores COM</span><span class="sxs-lookup"><span data-stu-id="ff455-140">COM Clients and Servers</span></span>](../com/com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="ff455-141">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ff455-141">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 