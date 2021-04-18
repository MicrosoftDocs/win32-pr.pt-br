---
title: Windows Deployment Services
description: Implantar sistemas operacionais Windows. Configure novos clientes com uma instalação baseada em rede sem exigir que os administradores visitem cada computador ou instalem diretamente da mídia de CD ou DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Serviço de implantação do Windows serviços de implantação do Windows
- Serviços de implantação do Windows serviços de implantação do Windows, home page
- serviços de implantação serviços de implantação do Windows
- Serviços de implantação do Windows WDS consulte serviços de implantação do Windows
- Serviços de instalação remota serviços de implantação do Windows consulte serviços de implantação do Windows
- Serviços de implantação do Windows RIS consulte serviços de implantação do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105772993"
---
# <a name="windows-deployment-services"></a><span data-ttu-id="96d5d-110">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="96d5d-110">Windows Deployment Services</span></span>

## <a name="purpose"></a><span data-ttu-id="96d5d-111">Finalidade</span><span class="sxs-lookup"><span data-stu-id="96d5d-111">Purpose</span></span>

<span data-ttu-id="96d5d-112">O WDS (serviços de implantação do Windows) é a versão revisada do RIS (serviços de instalação remota).</span><span class="sxs-lookup"><span data-stu-id="96d5d-112">Windows Deployment Services (WDS) is the revised version of Remote Installation Services (RIS).</span></span> <span data-ttu-id="96d5d-113">O WDS permite a implantação de sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="96d5d-113">WDS enables the deployment of Windows operating systems.</span></span> <span data-ttu-id="96d5d-114">Você pode usar o WDS para configurar novos clientes com uma instalação baseada em rede sem exigir que os administradores visitem cada computador ou instalem diretamente da mídia de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="96d5d-114">You can use WDS to set up new clients with a network-based installation without requiring that administrators visit each computer or install directly from CD or DVD media.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="96d5d-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="96d5d-115">Developer audience</span></span>

<span data-ttu-id="96d5d-116">O público-alvo principal da API do WDS é para grupos que desenvolvem ferramentas e processos personalizados para ti e outros grupos de administração do computador.</span><span class="sxs-lookup"><span data-stu-id="96d5d-116">The primary developer audience of the WDS API is for groups that develop custom tools and processes for IT and other computer administration groups.</span></span> <span data-ttu-id="96d5d-117">Em ambientes em que a solução padrão WDS (serviços de implantação do Windows) não pode ser usada, a API do WDS permite o acesso programático a alguns componentes do WDS.</span><span class="sxs-lookup"><span data-stu-id="96d5d-117">In environments where the standard Windows Deployment Services (WDS) solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

<span data-ttu-id="96d5d-118">Os OEMs (fabricantes originais do equipamento), os integradores de sistemas e os profissionais de ti corporativos que procuram informações sobre como implantar o Windows em novos computadores, devem ver as informações sobre a solução padrão do WDS (serviços de implantação do Windows) no [guia passo a passo da atualização dos serviços de implantação do Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e o [WAIK (Kit de instalação automatizada do Windows)](https://www.microsoft.com/download/details.aspx?id=10333).</span><span class="sxs-lookup"><span data-stu-id="96d5d-118">Original Equipment Manufacturers (OEMs), system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard Windows Deployment Services (WDS) solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="96d5d-119">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="96d5d-119">Run-time requirements</span></span>

<span data-ttu-id="96d5d-120">O WDS está disponível como um complemento para o Windows Server 2003 com Service Pack 1 (SP1) e está incluído no sistema operacional a partir do Windows Server 2003 com Service Pack 2 (SP2) e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="96d5d-120">WDS is available as an add-on for Windows Server 2003 with Service Pack 1 (SP1) and is included in the operating system starting with Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2008.</span></span> <span data-ttu-id="96d5d-121">A API do servidor PXE do WDS requer a função de servidor WDS no servidor para implementar provedores PXE personalizados.</span><span class="sxs-lookup"><span data-stu-id="96d5d-121">The WDS PXE Server API requires the WDS server role on the server to implement custom PXE providers.</span></span> <span data-ttu-id="96d5d-122">A API do cliente do WDS requer a fase Microsoft Ambiente de Pré-Instalação do Windows (Windows PE 2,0) do processamento da instalação.</span><span class="sxs-lookup"><span data-stu-id="96d5d-122">The WDS Client API requires the Microsoft Windows Preinstallation Environment (Windows PE 2.0) phase of setup processing.</span></span> <span data-ttu-id="96d5d-123">Uma imagem inicializável de RAMDISK do Windows PE 2,0 no. O formato WIM deve ser baixado como parte do processo de inicialização de rede para implementar clientes WDS personalizados.</span><span class="sxs-lookup"><span data-stu-id="96d5d-123">A RAMDISK bootable image of Windows PE 2.0 in the .WIM format must be downloaded as part of the network boot process to implement custom WDS clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="96d5d-124">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="96d5d-124">In this section</span></span>



| <span data-ttu-id="96d5d-125">Tópico</span><span class="sxs-lookup"><span data-stu-id="96d5d-125">Topic</span></span>                                                                                                 | <span data-ttu-id="96d5d-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="96d5d-126">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="96d5d-127">Sobre a API dos serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="96d5d-127">About the Windows Deployment Services API</span></span>](about-the-windows-deployment-services-api.md)<br/> | <span data-ttu-id="96d5d-128">Informações gerais sobre a API do servidor WDS e a API do cliente WDS.</span><span class="sxs-lookup"><span data-stu-id="96d5d-128">General information about the WDS Server API and WDS Client API.</span></span><br/>    |
| [<span data-ttu-id="96d5d-129">Referência dos serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="96d5d-129">Windows Deployment Services Reference</span></span>](windows-deployment-services-reference.md)<br/>         | <span data-ttu-id="96d5d-130">Descreve as funções e estruturas dos serviços de implantação do Windows.</span><span class="sxs-lookup"><span data-stu-id="96d5d-130">Describes the Windows Deployment Services functions and structures.</span></span><br/> |



 

 

