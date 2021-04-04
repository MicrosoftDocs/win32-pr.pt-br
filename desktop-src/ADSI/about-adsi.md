---
title: Sobre as interfaces de serviço do Active Directory
description: A ADSI (Active Directory interfaces de serviço) abstrai os recursos dos serviços de diretório de diferentes provedores de rede em um ambiente de computação distribuído para apresentar um único conjunto de interfaces de serviço de diretório para gerenciar recursos de rede.
ms.assetid: 6d601af5-7470-42c2-b99e-21174ea008b1
ms.tgt_platform: multiple
keywords:
- Sobre o ADSI de interfaces de serviço Active Directory
- ADSI, sobre
- ADSI de interfaces de serviço Active Directory, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc083b33a633335da12915257fcddff1174a6858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084015"
---
# <a name="about-active-directory-service-interfaces"></a><span data-ttu-id="f7e32-106">Sobre as interfaces de serviço do Active Directory</span><span class="sxs-lookup"><span data-stu-id="f7e32-106">About Active Directory Service Interfaces</span></span>

<span data-ttu-id="f7e32-107">A ADSI (Active Directory interfaces de serviço) abstrai os recursos dos serviços de diretório de diferentes provedores de rede em um ambiente de computação distribuído para apresentar um único conjunto de interfaces de serviço de diretório para gerenciar recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="f7e32-107">Active Directory Service Interfaces (ADSI) abstracts the capabilities of directory services from different network providers in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="f7e32-108">Os administradores e desenvolvedores podem usar os serviços ADSI para enumerar e gerenciar os recursos em um serviço de diretório, não importa qual ambiente de rede contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f7e32-108">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="f7e32-109">A ADSI facilita a execução de tarefas administrativas comuns, como a adição de novos usuários, o gerenciamento de impressoras e a localização de recursos em todo o ambiente de computação distribuído.</span><span class="sxs-lookup"><span data-stu-id="f7e32-109">ADSI makes it easier to perform common administrative tasks, such as adding new users, managing printers, and locating resources throughout the distributed computing environment.</span></span>

<span data-ttu-id="f7e32-110">A ADSI torna mais fácil para os desenvolvedores "habilitar o diretório" seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f7e32-110">ADSI makes it easy for developers to "directory enable" their applications.</span></span> <span data-ttu-id="f7e32-111">Os administradores e desenvolvedores lidam com um único conjunto de interfaces de serviço de diretório, independentemente de quais serviços de diretório estão instalados.</span><span class="sxs-lookup"><span data-stu-id="f7e32-111">Administrators and developers handle a single set of directory service interfaces, regardless of which directory services are installed.</span></span>

<span data-ttu-id="f7e32-112">Os tópicos a seguir são discutidos nesta introdução:</span><span class="sxs-lookup"><span data-stu-id="f7e32-112">The following topics are discussed in this introduction:</span></span>

-   [<span data-ttu-id="f7e32-113">Vários serviços de diretório</span><span class="sxs-lookup"><span data-stu-id="f7e32-113">Multiple Directory Services</span></span>](multiple-directory-services.md)
-   [<span data-ttu-id="f7e32-114">Quem usará Active Directory interfaces de serviço?</span><span class="sxs-lookup"><span data-stu-id="f7e32-114">Who Will Use Active Directory Service Interfaces?</span></span>](who-will-use-active-directory-service-interfaces.md)
-   [<span data-ttu-id="f7e32-115">Serviços de diretório hoje</span><span class="sxs-lookup"><span data-stu-id="f7e32-115">Directory Services Today</span></span>](directory-services-today.md)
-   [<span data-ttu-id="f7e32-116">Benefícios do uso de interfaces de serviço do Active Directory</span><span class="sxs-lookup"><span data-stu-id="f7e32-116">Benefits of Using Active Directory Service Interfaces</span></span>](benefits-of-using-active-directory-service-interfaces.md)
-   [<span data-ttu-id="f7e32-117">Arquitetura de interfaces de serviço Active Directory</span><span class="sxs-lookup"><span data-stu-id="f7e32-117">Active Directory Service Interfaces Architecture</span></span>](active-directory-service-interfaces-architecture.md)
-   [<span data-ttu-id="f7e32-118">Suporte à linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="f7e32-118">Programming Language Support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="f7e32-119">Propriedades e atributos ADSI</span><span class="sxs-lookup"><span data-stu-id="f7e32-119">ADSI Properties and Attributes</span></span>](adsi-properties-and-attributes.md)

## <a name="what-you-should-know-before-reading-this-guide"></a><span data-ttu-id="f7e32-120">O que você deve saber antes de ler este guia</span><span class="sxs-lookup"><span data-stu-id="f7e32-120">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="f7e32-121">Este guia pressupõe que você esteja familiarizado com o Component Object Model (COM) e com a automação, e que você sabe como programar em Visual Basic ou C/C++.</span><span class="sxs-lookup"><span data-stu-id="f7e32-121">This guide assumes that you are familiar with the Component Object Model (COM) and Automation, and that you know how to program in either Visual Basic or C/C++.</span></span>

<span data-ttu-id="f7e32-122">Alguns dos termos usados neste guia são exclusivos do ADSI ou do ambiente de serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="f7e32-122">Some of the terms used in this guide are unique to either ADSI or the directory services environment.</span></span> <span data-ttu-id="f7e32-123">Outros termos serão familiares, mas podem ter significados um pouco diferentes nesses ambientes.</span><span class="sxs-lookup"><span data-stu-id="f7e32-123">Other terms will be familiar but may have slightly different meanings in these environments.</span></span>

## <a name="further-reading-about-adsi-and-related-topics"></a><span data-ttu-id="f7e32-124">Leitura adicional sobre ADSI e tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7e32-124">Further Reading about ADSI and Related Topics</span></span>

<span data-ttu-id="f7e32-125">Para obter mais informações sobre as interfaces de serviço Active Directory e as tecnologias nas quais elas se baseiam, você pode encontrar as seguintes fontes úteis.</span><span class="sxs-lookup"><span data-stu-id="f7e32-125">For more information about Active Directory Service Interfaces and the technologies on which they are based, you may find the following sources helpful.</span></span>

<span data-ttu-id="f7e32-126">Brockschmidt, Kraig.</span><span class="sxs-lookup"><span data-stu-id="f7e32-126">Brockschmidt, Kraig.</span></span> <span data-ttu-id="f7e32-127">*Dentro do OLE*, 2ª edição.</span><span class="sxs-lookup"><span data-stu-id="f7e32-127">*Inside OLE*, 2nd edition.</span></span> <span data-ttu-id="f7e32-128">Redmond, WA: Microsoft Press, 1995.</span><span class="sxs-lookup"><span data-stu-id="f7e32-128">Redmond, WA: Microsoft Press, 1995.</span></span>

<span data-ttu-id="f7e32-129">Chappell, David.</span><span class="sxs-lookup"><span data-stu-id="f7e32-129">Chappell, David.</span></span> <span data-ttu-id="f7e32-130">*Noções básicas sobre ActiveX e OLE*.</span><span class="sxs-lookup"><span data-stu-id="f7e32-130">*Understanding ActiveX and OLE*.</span></span> <span data-ttu-id="f7e32-131">Redmond, WA: Microsoft Press, 1996.</span><span class="sxs-lookup"><span data-stu-id="f7e32-131">Redmond, WA: Microsoft Press, 1996.</span></span>

<span data-ttu-id="f7e32-132">Hahn, Steven.</span><span class="sxs-lookup"><span data-stu-id="f7e32-132">Hahn, Steven.</span></span> <span data-ttu-id="f7e32-133">*Referência do programador ASP ADSI*.</span><span class="sxs-lookup"><span data-stu-id="f7e32-133">*ADSI ASP Programmer's Reference*.</span></span> <span data-ttu-id="f7e32-134">Wrox Press Ltd., 1998.</span><span class="sxs-lookup"><span data-stu-id="f7e32-134">Wrox Press Ltd., 1998.</span></span>

<span data-ttu-id="f7e32-135">Harrison, Richard.</span><span class="sxs-lookup"><span data-stu-id="f7e32-135">Harrison, Richard.</span></span> <span data-ttu-id="f7e32-136">*Segurança da Web ASP/MTS/ADSI*.</span><span class="sxs-lookup"><span data-stu-id="f7e32-136">*ASP/MTS/ADSI Web Security*.</span></span> <span data-ttu-id="f7e32-137">Prentice Hall, 1999.</span><span class="sxs-lookup"><span data-stu-id="f7e32-137">Prentice Hall, 1999.</span></span>

<span data-ttu-id="f7e32-138">Referência do programador de OLE DB da Microsoft versão 1,0, 1996.</span><span class="sxs-lookup"><span data-stu-id="f7e32-138">Microsoft's OLE DB Programmer's Reference Version 1.0, 1996.</span></span>

<span data-ttu-id="f7e32-139">*Referência do programador de OLE 2, volume dois*.</span><span class="sxs-lookup"><span data-stu-id="f7e32-139">*OLE 2 Programmer's Reference, Volume Two*.</span></span> <span data-ttu-id="f7e32-140">Redmond, WA: Microsoft Press, 1994.</span><span class="sxs-lookup"><span data-stu-id="f7e32-140">Redmond, WA: Microsoft Press, 1994.</span></span>

<span data-ttu-id="f7e32-141">Rogersize, Dale.</span><span class="sxs-lookup"><span data-stu-id="f7e32-141">Rogerson, Dale.</span></span> <span data-ttu-id="f7e32-142">*Dentro de com*.</span><span class="sxs-lookup"><span data-stu-id="f7e32-142">*Inside COM*.</span></span> <span data-ttu-id="f7e32-143">Redmond, WA: Microsoft Press, 1997.</span><span class="sxs-lookup"><span data-stu-id="f7e32-143">Redmond, WA: Microsoft Press, 1997.</span></span>

<span data-ttu-id="f7e32-144">*A especificação de design de serviço Active Directory versão 2,0*.</span><span class="sxs-lookup"><span data-stu-id="f7e32-144">*The Active Directory Service Design Specification Version 2.0*.</span></span>

<span data-ttu-id="f7e32-145">*A especificação de Component Object Model*.</span><span class="sxs-lookup"><span data-stu-id="f7e32-145">*The Component Object Model Specification*.</span></span>

<span data-ttu-id="f7e32-146">(Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.)</span><span class="sxs-lookup"><span data-stu-id="f7e32-146">(These resources may not be available in some languages and countries/regions.)</span></span>

 

 




