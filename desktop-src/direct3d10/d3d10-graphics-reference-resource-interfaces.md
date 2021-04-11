---
description: 'O Direct3D 10 define um número de interfaces para os dois tipos básicos de recursos: buffers e texturas.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de recurso (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089123"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a><span data-ttu-id="592b2-103">Interfaces de recurso (gráficos do Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="592b2-103">Resource Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="592b2-104">O Direct3D 10 define um número de interfaces para os dois tipos básicos de recursos: [buffers](d3d10-graphics-programming-guide-resources-types.md) e texturas.</span><span class="sxs-lookup"><span data-stu-id="592b2-104">Direct3D 10 defines a number of interfaces for the two basic types of resources: [buffers](d3d10-graphics-programming-guide-resources-types.md) and textures.</span></span>



| <span data-ttu-id="592b2-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="592b2-105">Interfaces</span></span>                                           | <span data-ttu-id="592b2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="592b2-106">Description</span></span>                                          |
|------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="592b2-107">**Interface ID3D10Buffer**</span><span class="sxs-lookup"><span data-stu-id="592b2-107">**ID3D10Buffer Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | <span data-ttu-id="592b2-108">Acessa dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="592b2-108">Accesses buffer data.</span></span>                                |
| [<span data-ttu-id="592b2-109">**Interface ID3D10Resource**</span><span class="sxs-lookup"><span data-stu-id="592b2-109">**ID3D10Resource Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | <span data-ttu-id="592b2-110">Classe base para um recurso.</span><span class="sxs-lookup"><span data-stu-id="592b2-110">Base class for a resource.</span></span>                           |
| [<span data-ttu-id="592b2-111">**Interface ID3D10Texture1D**</span><span class="sxs-lookup"><span data-stu-id="592b2-111">**ID3D10Texture1D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | <span data-ttu-id="592b2-112">Acessa dados em uma textura 1D ou uma matriz de textura 1D.</span><span class="sxs-lookup"><span data-stu-id="592b2-112">Accesses data in a 1D texture or a 1D texture array.</span></span> |
| [<span data-ttu-id="592b2-113">**Interface ID3D10Texture2D**</span><span class="sxs-lookup"><span data-stu-id="592b2-113">**ID3D10Texture2D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | <span data-ttu-id="592b2-114">Acessa dados em uma textura 2D ou em uma matriz de textura 2D</span><span class="sxs-lookup"><span data-stu-id="592b2-114">Accesses data in a 2D texture or a 2D texture array</span></span>  |
| [<span data-ttu-id="592b2-115">**Interface ID3D10Texture3D**</span><span class="sxs-lookup"><span data-stu-id="592b2-115">**ID3D10Texture3D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | <span data-ttu-id="592b2-116">Acessa dados em uma textura 3D ou em uma matriz de textura 3D.</span><span class="sxs-lookup"><span data-stu-id="592b2-116">Accesses data in a 3D texture or a 3D texture array.</span></span> |



 

<span data-ttu-id="592b2-117">Um aplicativo usa uma exibição para associar um recurso a um [estágio de pipeline](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="592b2-117">An application uses a view to bind a resource to a [pipeline stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> <span data-ttu-id="592b2-118">A [exibição](d3d10-graphics-programming-guide-resources-access-views.md) define como o recurso pode ser acessado durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="592b2-118">The [view](d3d10-graphics-programming-guide-resources-access-views.md) defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="592b2-119">A API contém essas interfaces de exibição.</span><span class="sxs-lookup"><span data-stu-id="592b2-119">The API contains these view interfaces.</span></span>



| <span data-ttu-id="592b2-120">Interfaces</span><span class="sxs-lookup"><span data-stu-id="592b2-120">Interfaces</span></span>                                                               | <span data-ttu-id="592b2-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="592b2-121">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="592b2-122">**Interface ID3D10DepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="592b2-122">**ID3D10DepthStencilView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | <span data-ttu-id="592b2-123">Acessa dados em uma textura de [estêncil de profundidade](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) .</span><span class="sxs-lookup"><span data-stu-id="592b2-123">Accesses data in a [depth-stencil](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) texture.</span></span> |
| [<span data-ttu-id="592b2-124">**Interface ID3D10RenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="592b2-124">**ID3D10RenderTargetView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | <span data-ttu-id="592b2-125">Acessa dados em um [destino de renderização](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="592b2-125">Accesses data in a [render target](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>        |
| [<span data-ttu-id="592b2-126">**Interface ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="592b2-126">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | <span data-ttu-id="592b2-127">Acessa dados em um sombreador – recurso no Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="592b2-127">Accesses data in a shader-resource in Direct3D 10.0.</span></span>                                                         |
| [<span data-ttu-id="592b2-128">**Interface ID3D10ShaderResourceView1**</span><span class="sxs-lookup"><span data-stu-id="592b2-128">**ID3D10ShaderResourceView1 Interface**</span></span>](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | <span data-ttu-id="592b2-129">Acessa dados em um sombreador – recurso no Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="592b2-129">Accesses data in a shader-resource in Direct3D 10.1.</span></span>                                                         |
| [<span data-ttu-id="592b2-130">**Interface ID3D10View**</span><span class="sxs-lookup"><span data-stu-id="592b2-130">**ID3D10View Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | <span data-ttu-id="592b2-131">Classe base para uma exibição.</span><span class="sxs-lookup"><span data-stu-id="592b2-131">Base class for a view.</span></span>                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="592b2-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="592b2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="592b2-133">Referência de recurso</span><span class="sxs-lookup"><span data-stu-id="592b2-133">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
