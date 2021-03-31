---
title: Arquitetura de Gerenciamento Remoto do Windows
description: A arquitetura de Gerenciamento Remoto do Windows consiste em componentes nos computadores cliente e servidor.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641571"
---
# <a name="windows-remote-management-architecture"></a><span data-ttu-id="c788d-103">Arquitetura de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="c788d-103">Windows Remote Management Architecture</span></span>

<span data-ttu-id="c788d-104">A arquitetura de Gerenciamento Remoto do Windows consiste em componentes nos computadores cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="c788d-104">The Windows Remote Management architecture consists of components on the client and server computers.</span></span> <span data-ttu-id="c788d-105">A ilustração a seguir mostra os componentes em ambos os computadores, como os componentes interagem com outros componentes e o protocolo que é usado para se comunicar entre os computadores.</span><span class="sxs-lookup"><span data-stu-id="c788d-105">The following illustration shows the components on both computers, how the components interact with other components, and the protocol that is used to communicate between the computers.</span></span>

![arquitetura do WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a><span data-ttu-id="c788d-107">Solicitando cliente</span><span class="sxs-lookup"><span data-stu-id="c788d-107">Requesting Client</span></span>

<span data-ttu-id="c788d-108">Os seguintes componentes do WinRM residem no computador que está executando o script que solicita dados.</span><span class="sxs-lookup"><span data-stu-id="c788d-108">The following WinRM components reside on the computer that is running the script that requests data.</span></span>

-   <span data-ttu-id="c788d-109">Aplicativo WinRM</span><span class="sxs-lookup"><span data-stu-id="c788d-109">WinRM application</span></span>

    <span data-ttu-id="c788d-110">Essa é a ferramenta de linha de comando do script ou do **WinRM** que usa a API de script do WinRM para fazer chamadas para dados de solicitação ou para executar métodos.</span><span class="sxs-lookup"><span data-stu-id="c788d-110">This is the script or **Winrm** command-line tool that uses the WinRM scripting API to make calls to request data or to execute methods.</span></span> <span data-ttu-id="c788d-111">Para obter mais informações, consulte a [API de script do WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c788d-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

-   <span data-ttu-id="c788d-112">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-112">WSMAuto.dll</span></span>

    <span data-ttu-id="c788d-113">A camada de automação que fornece suporte a scripts.</span><span class="sxs-lookup"><span data-stu-id="c788d-113">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="c788d-114">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-114">WsmCL.dll</span></span>

    <span data-ttu-id="c788d-115">Camada C API no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c788d-115">C API layer within the operating system.</span></span>

-   <span data-ttu-id="c788d-116">API HTTP</span><span class="sxs-lookup"><span data-stu-id="c788d-116">HTTP API</span></span>

    <span data-ttu-id="c788d-117">O WinRM requer suporte para transporte HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c788d-117">WinRM requires support for HTTP and HTTPS transport.</span></span>

## <a name="responding-server"></a><span data-ttu-id="c788d-118">Respondendo ao servidor</span><span class="sxs-lookup"><span data-stu-id="c788d-118">Responding Server</span></span>

<span data-ttu-id="c788d-119">Os seguintes componentes do WinRM residem no computador que está respondendo.</span><span class="sxs-lookup"><span data-stu-id="c788d-119">The following WinRM components reside on the responding computer.</span></span>

-   <span data-ttu-id="c788d-120">API HTTP</span><span class="sxs-lookup"><span data-stu-id="c788d-120">HTTP API</span></span>

    <span data-ttu-id="c788d-121">O WinRM requer suporte para transporte HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c788d-121">WinRM requires support for HTTP and HTTPS transport.</span></span>

-   <span data-ttu-id="c788d-122">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-122">WSMAuto.dll</span></span>

    <span data-ttu-id="c788d-123">A camada de automação que fornece suporte a scripts.</span><span class="sxs-lookup"><span data-stu-id="c788d-123">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="c788d-124">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-124">WsmCL.dll</span></span>

    <span data-ttu-id="c788d-125">Camada C API no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c788d-125">C API layer within the operating system.</span></span>

-   <span data-ttu-id="c788d-126">WsmSvc.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-126">WsmSvc.dll</span></span>

    <span data-ttu-id="c788d-127">Serviço de [*escuta*](windows-remote-management-glossary.md) do WinRM.</span><span class="sxs-lookup"><span data-stu-id="c788d-127">WinRM [*listener*](windows-remote-management-glossary.md) service.</span></span>

-   <span data-ttu-id="c788d-128">WsmProv.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-128">WsmProv.dll</span></span>

    <span data-ttu-id="c788d-129">Subsistema do provedor.</span><span class="sxs-lookup"><span data-stu-id="c788d-129">Provider subsystem.</span></span>

-   <span data-ttu-id="c788d-130">WsmRes.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-130">WsmRes.dll</span></span>

    <span data-ttu-id="c788d-131">Arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c788d-131">Resource file.</span></span>

-   <span data-ttu-id="c788d-132">WsmWmiPl.dll</span><span class="sxs-lookup"><span data-stu-id="c788d-132">WsmWmiPl.dll</span></span>

    <span data-ttu-id="c788d-133">[*Plug-in WMI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c788d-133">[*WMI plug-in*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="c788d-134">Isso permite que você obtenha dados WMI por meio do WinRM.</span><span class="sxs-lookup"><span data-stu-id="c788d-134">This allows you to obtain WMI data through WinRM.</span></span>

-   <span data-ttu-id="c788d-135">Driver de IPMI (interface de gerenciamento de plataforma inteligente) e provedor IPMI WMI</span><span class="sxs-lookup"><span data-stu-id="c788d-135">Intelligent Platform Management Interface (IPMI) driver and WMI IPMI provider</span></span>

    <span data-ttu-id="c788d-136">Esses componentes fornecem dados de hardware que são solicitados usando as classes IPMI.</span><span class="sxs-lookup"><span data-stu-id="c788d-136">These components supply any hardware data that is requested using the IPMI classes.</span></span> <span data-ttu-id="c788d-137">Para obter mais informações, consulte [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="c788d-137">For more information, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="c788d-138">O hardware do BMC deve ter sido detectado pelo SMBIOS ou pelo dispositivo criado manualmente pelo carregamento do driver.</span><span class="sxs-lookup"><span data-stu-id="c788d-138">BMC hardware must have been detected by the SMBIOS or the device created manually by loading the driver.</span></span> <span data-ttu-id="c788d-139">Para obter mais informações, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="c788d-139">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c788d-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c788d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c788d-141">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="c788d-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 