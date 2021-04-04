---
title: Direct2D
description: .
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2eae62ba2d6ff44920d6b6d4890a8c48bc3c0f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007833"
---
# <a name="direct2d"></a><span data-ttu-id="6bf8c-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="6bf8c-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="6bf8c-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="6bf8c-104">Purpose</span></span>

<span data-ttu-id="6bf8c-105">Direct2D é uma API de elementos gráficos 2D com aceleração de hardware e modo imediato que fornece alto desempenho e renderização de alta qualidade para geometria 2D, bitmaps e texto.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="6bf8c-106">A API Direct2D foi projetada para interoperar bem com GDI, GDI+ e Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6bf8c-107">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="6bf8c-107">Developer audience</span></span>

<span data-ttu-id="6bf8c-108">O Direct2D é projetado principalmente para uso pelas seguintes classes de desenvolvedores:</span><span class="sxs-lookup"><span data-stu-id="6bf8c-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="6bf8c-109">Desenvolvedores de aplicativos nativos de grande escala empresarial.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="6bf8c-110">Desenvolvedores que criam kits de controle e bibliotecas para consumo por desenvolvedores de downstream.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="6bf8c-111">Desenvolvedores que exigem renderização do lado do servidor de gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="6bf8c-112">Os desenvolvedores que usam gráficos do Direct3D e precisam de renderização simples, de alto desempenho em 2 e de texto para menus, elementos de interface do usuário (IU) e HUDs (exibições de cabeçotes).</span><span class="sxs-lookup"><span data-stu-id="6bf8c-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6bf8c-113">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="6bf8c-113">Run-time requirements</span></span>

-   <span data-ttu-id="6bf8c-114">Windows 7 ou Windows Vista com Service Pack 2 (SP2) e atualização de plataforma para Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="6bf8c-115">Windows Server 2008 R2 ou Windows Server 2008 com Service Pack 2 (SP2) e atualização de plataforma para Windows Server 2008 e posterior.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="6bf8c-116">A atualização de plataforma para o Windows Vista e a atualização de plataforma para Windows Server 2008 são um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para o Windows 7, Windows Vista, Windows Server 2008 R2 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="6bf8c-117">Essas atualizações estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="6bf8c-118">Aplicativos de terceiros que exigem atualização de plataforma para Windows Vista ou atualização de plataforma para Windows Server 2008 podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="6bf8c-119">Para obter mais informações sobre as duas atualizações, consulte [atualização de plataforma para Windows Vista](https://support.microsoft.com/kb/971644).</span><span class="sxs-lookup"><span data-stu-id="6bf8c-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="6bf8c-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6bf8c-120">In this section</span></span>



| <span data-ttu-id="6bf8c-121">Tópico</span><span class="sxs-lookup"><span data-stu-id="6bf8c-121">Topic</span></span>                                                                                          | <span data-ttu-id="6bf8c-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bf8c-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bf8c-123">O que há de novo no Direct2D</span><span class="sxs-lookup"><span data-stu-id="6bf8c-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="6bf8c-124">Aqui estão algumas das novas adições ao Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="6bf8c-125">Sobre o Direct2D</span><span class="sxs-lookup"><span data-stu-id="6bf8c-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="6bf8c-126">Apresenta o Direct2D, uma API que fornece aos desenvolvedores do Win32 a capacidade de executar tarefas de renderização de gráficos 2D com desempenho e qualidade visual superiores.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="6bf8c-127">Guia de início rápido do Direct2D para Windows 8</span><span class="sxs-lookup"><span data-stu-id="6bf8c-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="6bf8c-128">Resume as etapas necessárias para desenhar com Direct2D e fornece código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="6bf8c-129">Introdução com Direct2D</span><span class="sxs-lookup"><span data-stu-id="6bf8c-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="6bf8c-130">Descreve como começar a criar aplicativos Direct2D e fornece código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="6bf8c-131">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="6bf8c-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="6bf8c-132">Esta seção contém tópicos de programação conceitual que descrevem como usar a API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="6bf8c-133">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="6bf8c-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="6bf8c-134">Descreve a API Direct2D em detalhes.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="6bf8c-135">Ferramentas e utilitários</span><span class="sxs-lookup"><span data-stu-id="6bf8c-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="6bf8c-136">Ferramentas e utilitários fornecidos para Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="6bf8c-137">Amostras</span><span class="sxs-lookup"><span data-stu-id="6bf8c-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="6bf8c-138">Aplicativos de exemplo que demonstram a API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="6bf8c-139">Glossário do Direct2D</span><span class="sxs-lookup"><span data-stu-id="6bf8c-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="6bf8c-140">Descreve os termos comumente usados pela documentação do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6bf8c-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="6bf8c-141">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="6bf8c-141">Additional resources</span></span>

-   [<span data-ttu-id="6bf8c-142">**Elementos gráficos e jogos do DirectX**</span><span class="sxs-lookup"><span data-stu-id="6bf8c-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="6bf8c-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="6bf8c-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

