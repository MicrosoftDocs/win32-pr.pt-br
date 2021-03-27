---
title: O que há de novo no SDK de agosto de 2009 do Windows 7/Direct3D 11
description: Esta versão do Windows 7/Direct3D 11 é fornecida como parte do SDK do DirectX e contém novos recursos, ferramentas e documentação.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642164"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a><span data-ttu-id="d8df6-103">O que há de novo no SDK de agosto de 2009 do Windows 7/Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d8df6-103">What's New in the August 2009 Windows 7/Direct3D 11 SDK</span></span>

<span data-ttu-id="d8df6-104">Esta versão do Windows 7/Direct3D 11 é fornecida como parte do SDK do DirectX e contém novos recursos, ferramentas e documentação.</span><span class="sxs-lookup"><span data-stu-id="d8df6-104">This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8df6-105">Item</span><span class="sxs-lookup"><span data-stu-id="d8df6-105">Item</span></span></th>
<th><span data-ttu-id="d8df6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8df6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8df6-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span><span class="sxs-lookup"><span data-stu-id="d8df6-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span></span><br/></td>
<td><span data-ttu-id="d8df6-108">O Direct2D é uma API de gráficos 2D, de modo imediato e com aceleração de hardware que fornece alto desempenho e renderização de alta qualidade para geometria, bitmaps e texto 2D.</span><span class="sxs-lookup"><span data-stu-id="d8df6-108">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="d8df6-109">A API Direct2D foi projetada para interoperar bem com Direct3D e GDI.</span><span class="sxs-lookup"><span data-stu-id="d8df6-109">The Direct2D API is designed to interoperate well with Direct3D and GDI.</span></span> <span data-ttu-id="d8df6-110">Esse SDK permite que os desenvolvedores avaliem a API e gravem aplicativos simples, com algumas das funcionalidades mais avançadas possíveis em computadores configurados corretamente.</span><span class="sxs-lookup"><span data-stu-id="d8df6-110">This SDK allows developers to evaluate the API and write simple applications, with some of the more advanced functionality possible on properly configured machines.</span></span> <br/> <span data-ttu-id="d8df6-111">A <a href="/windows/win32/direct2d/direct2d-portal">documentação</a> e os <a href="/previous-versions//dd372354(v=vs.85)">exemplos</a> do Direct2D estão disponíveis no momento no msdn.</span><span class="sxs-lookup"><span data-stu-id="d8df6-111"><a href="/windows/win32/direct2d/direct2d-portal">Documentation</a> and <a href="/previous-versions//dd372354(v=vs.85)">samples</a> for Direct2D are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8df6-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d8df6-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span></span><br/></td>
<td><span data-ttu-id="d8df6-113">O DirectWrite fornece suporte para renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução, suporte completo a texto e layout Unicode e muito mais:</span><span class="sxs-lookup"><span data-stu-id="d8df6-113">DirectWrite provides support for high-quality text rendering, resolution-independent outline fonts, full Unicode text and layout support, and much, much more:</span></span><br/>
<ul>
<li><span data-ttu-id="d8df6-114">Um sistema de layout de texto independente de dispositivo que melhora a legibilidade do texto em documentos e na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d8df6-114">A device-independent text layout system that improves text readability in documents and in UI.</span></span><br/></li>
<li><span data-ttu-id="d8df6-115">Renderização de texto ClearType de alta qualidade, sub-pixel, que pode usar tecnologia de renderização GDI Direct3D, Direct2D ou específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8df6-115">High-quality, sub-pixel, ClearType text rendering that can use GDI Direct3D, Direct2D, or application-specific rendering technology.</span></span><br/></li>
<li><span data-ttu-id="d8df6-116">Suporte para texto de vários formatos.</span><span class="sxs-lookup"><span data-stu-id="d8df6-116">Support for multi-format text.</span></span> <br/></li>
<li><span data-ttu-id="d8df6-117">Suporte para os recursos de tipografia avançada de fontes OpenType.</span><span class="sxs-lookup"><span data-stu-id="d8df6-117">Support for the advanced typography features of OpenType fonts.</span></span><br/></li>
<li><span data-ttu-id="d8df6-118">Suporte para layout e renderização de texto em todos os idiomas com suporte no Windows.</span><span class="sxs-lookup"><span data-stu-id="d8df6-118">Support for the layout and rendering of text in all languages supported by Windows.</span></span><br/></li>
</ul>
<span data-ttu-id="d8df6-119">Esse SDK permite que os desenvolvedores avaliem a API e gravem aplicativos básicos apenas para fins de demonstração.</span><span class="sxs-lookup"><span data-stu-id="d8df6-119">This SDK allows developers to evaluate the API and write basic applications for demonstration purposes only.</span></span><br/> <span data-ttu-id="d8df6-120">A <a href="/windows/win32/directwrite/direct-write-portal">documentação</a> e os <a href="/windows/win32/directwrite/samples">exemplos</a> do DirectWrite estão disponíveis no momento no msdn.</span><span class="sxs-lookup"><span data-stu-id="d8df6-120"><a href="/windows/win32/directwrite/direct-write-portal">Documentation</a> and <a href="/windows/win32/directwrite/samples">samples</a> for DirectWrite are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8df6-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="d8df6-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1</span></span><br/></td>
<td><span data-ttu-id="d8df6-122">O <a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">dxgi 1,1</a> se baseia em dxgi 1,0 e estará disponível no Windows Vista e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d8df6-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1.1</a> builds on DXGI 1.0 and will be available on both Windows Vista and Windows 7.</span></span> <span data-ttu-id="d8df6-123">DXGI 1,1 adiciona vários recursos novos:</span><span class="sxs-lookup"><span data-stu-id="d8df6-123">DXGI 1.1 adds several new features:</span></span><br/>
<ul>
<li><span data-ttu-id="d8df6-124">Suporte a superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="d8df6-124">Synchronized Shared Surfaces Support.</span></span> <span data-ttu-id="d8df6-125">Isso permite o compartilhamento eficiente de superfície de leitura e gravação entre vários dispositivos D3D (podem estar entre D3D10 e D3D11).</span><span class="sxs-lookup"><span data-stu-id="d8df6-125">This enables efficient read and write surface sharing between multiple D3D (could be between D3D10 and D3D11) devices.</span></span><br/></li>
<li><span data-ttu-id="d8df6-126">Suporte ao formato BGRA.</span><span class="sxs-lookup"><span data-stu-id="d8df6-126">BGRA format support.</span></span> <span data-ttu-id="d8df6-127">Isso permite que o GDI seja renderizado na mesma superfície DXGI direcionada por um dispositivo Direct2D, Direct3D 10,1 ou Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="d8df6-127">This allows GDI to render to the same DXGI surface targeted by a Direct2D, Direct3D 10.1 or Direct3D 11 device.</span></span> <br/></li>
<li><span data-ttu-id="d8df6-128">Latência máxima do quadro.</span><span class="sxs-lookup"><span data-stu-id="d8df6-128">Maximum Frame Latency.</span></span> <span data-ttu-id="d8df6-129">Usando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: SetMaximumFrameLatency</strong></a> e <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: GetMaximumFrameLatency</strong></a>, os títulos podem controlar o número de quadros que têm permissão para serem armazenados em uma fila, antes do envio para renderização.</span><span class="sxs-lookup"><span data-stu-id="d8df6-129">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency</strong></a>, titles can control the number of frames that are allowed to be stored in a queue, before submission for rendering.</span></span> <span data-ttu-id="d8df6-130">A latência é geralmente usada para controlar como a CPU escolhe entre responder a entradas de usuário e quadros que estão na fila de renderização.</span><span class="sxs-lookup"><span data-stu-id="d8df6-130">Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.</span></span><br/></li>
<li><span data-ttu-id="d8df6-131">Enumeração de adaptador.</span><span class="sxs-lookup"><span data-stu-id="d8df6-131">Adapter Enumeration.</span></span> <span data-ttu-id="d8df6-132">Usando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>, os títulos podem enumerar adaptadores locais sem monitores ou saídas anexados, bem como adaptadores com saídas anexadas.</span><span class="sxs-lookup"><span data-stu-id="d8df6-132">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, titles can enumerates local adapters without any monitors or outputs attached, as well as adapters with outputs attached.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8df6-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Amostras atualizadas</span><span class="sxs-lookup"><span data-stu-id="d8df6-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Updated Samples</span></span><br/></td>
<td><span data-ttu-id="d8df6-134">Esta versão tem vários exemplos novos e atualizados.</span><span class="sxs-lookup"><span data-stu-id="d8df6-134">This release has several new and updated samples.</span></span><br/>
<ul>
<li><span data-ttu-id="d8df6-135">O novo <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> é uma ilustração de técnicas de processamento de sombreador de computação mais avançadas que podem ser executadas em uma GPU d3d10 ou D3D11.</span><span class="sxs-lookup"><span data-stu-id="d8df6-135">The new <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> is an illustration of more advanced compute shader processing techniques that can be run on a D3D10 or D3D11 GPU.</span></span></li>
<li><span data-ttu-id="d8df6-136">O <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">exemplo de HDRToneMappingCS11</a> foi expandido para implementar efeitos de desfoque e flor (além de mapeamento de Tom) usando o sombreador de computação, bem como fornecer implementações de sombreador de pixel para comparação.</span><span class="sxs-lookup"><span data-stu-id="d8df6-136">The <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 sample</a> has been expanded to implement blur and bloom effects (in addition to tone mapping) using compute shader, as well as providing pixel shader implementations for comparison.</span></span></li>
<li><span data-ttu-id="d8df6-137">O <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">exemplo de MultithreadedRendering11</a> foi atualizado significativamente, com ativos de arte mais complexos e processamento por thread mais intensivo.</span><span class="sxs-lookup"><span data-stu-id="d8df6-137">The <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11 sample</a> has been significantly updated, with more complex art assets and more intensive per-thread processing.</span></span></li>
<li><span data-ttu-id="d8df6-138">O <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">exemplo SubD11</a> foi atualizado com um novo modelo facial, e o exemplo agora aproveita o recurso de computação de proximidade do exportador de conteúdo de exemplos.</span><span class="sxs-lookup"><span data-stu-id="d8df6-138">The <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11 sample</a> has been updated with a new facial model, and the sample now leverages the adjacency computation feature of the Samples Content Exporter.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d8df6-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8df6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8df6-140">Recursos introduzidos em versões anteriores</span><span class="sxs-lookup"><span data-stu-id="d8df6-140">Features Introduced In Previous Releases</span></span>](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

