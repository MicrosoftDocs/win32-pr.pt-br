---
title: DirectWrite (DWrite)
description: Os aplicativos atuais devem dar suporte à renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto e layout Unicode. O DirectWrite, uma API do [DirectX](../directx.md) , fornece esses recursos e muito mais.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2020
ms.locfileid: "104454579"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="577f2-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="577f2-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="577f2-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="577f2-105">Purpose</span></span>

<span data-ttu-id="577f2-106">Os aplicativos atuais devem dar suporte à renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto e layout Unicode.</span><span class="sxs-lookup"><span data-stu-id="577f2-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="577f2-107">O DirectWrite, uma API do [DirectX](../directx.md) , fornece esses recursos e muito mais.</span><span class="sxs-lookup"><span data-stu-id="577f2-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="577f2-108">Um sistema de layout de texto independente de dispositivo que melhora a legibilidade do texto em documentos e na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="577f2-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="577f2-109">Renderização de texto de alta qualidade e subpixel [do Microsoft ClearType](/typography/cleartype/) que pode usar a tecnologia de renderização [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)ou específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="577f2-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="577f2-110">Texto acelerado por hardware, quando usado com [Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="577f2-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="577f2-111">Suporte para texto de vários formatos.</span><span class="sxs-lookup"><span data-stu-id="577f2-111">Support for multi-format text.</span></span>
- <span data-ttu-id="577f2-112">Suporte para os recursos de tipografia avançada de fontes OpenType.</span><span class="sxs-lookup"><span data-stu-id="577f2-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="577f2-113">Suporte para layout e renderização de texto em todos os idiomas com suporte.</span><span class="sxs-lookup"><span data-stu-id="577f2-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="577f2-114">Layout e renderização compatíveis com [GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="577f2-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="577f2-115">A API dá suporte à medição, ao desenho e ao teste de impacto de texto de vários formatos.</span><span class="sxs-lookup"><span data-stu-id="577f2-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="577f2-116">O DirectWrite lida com o texto em todos os idiomas com suporte para aplicativos globais e localizados, criando a infraestrutura de linguagem principal encontrada no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="577f2-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="577f2-117">O DirectWrite também oferece uma API de renderização de glifos de nível inferior para desenvolvedores que queiram executar seu próprio processamento Unicode em glifo.</span><span class="sxs-lookup"><span data-stu-id="577f2-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="577f2-118">A [reunião do projeto](/windows/apps/project-reunion/) apresenta uma nova versão do DirectWrite &mdash; chamada DWriteCore &mdash; , que é executada em versões do Windows até o Windows 8, e abre a porta para você usá-la entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="577f2-118">[Project Reunion](/windows/apps/project-reunion/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="577f2-119">Para obter mais detalhes, consulte [visão geral do DWriteCore](dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="577f2-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="577f2-120">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="577f2-120">Run-time requirements</span></span>

- <span data-ttu-id="577f2-121">Windows 7 ou Windows Vista com Service Pack 2 (SP2) e atualização de plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="577f2-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="577f2-122">Windows Server 2008 R2 ou Windows Server 2008 com Service Pack 2 (SP2) e atualização de plataforma para Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="577f2-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="577f2-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="577f2-123">In this section</span></span>

| <span data-ttu-id="577f2-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="577f2-124">Topic</span></span> | <span data-ttu-id="577f2-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="577f2-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="577f2-126">O que há de novo no DirectWrite</span><span class="sxs-lookup"><span data-stu-id="577f2-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="577f2-127">Aqui estão algumas das novas adições ao DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="577f2-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="577f2-128">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="577f2-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="577f2-129">Os tópicos a seguir fornecem uma visão geral da API do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="577f2-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="577f2-130">Referência da API</span><span class="sxs-lookup"><span data-stu-id="577f2-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="577f2-131">Descreve a API do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="577f2-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="577f2-132">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="577f2-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="577f2-133">Esta seção contém informações sobre programas de exemplo para DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="577f2-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
