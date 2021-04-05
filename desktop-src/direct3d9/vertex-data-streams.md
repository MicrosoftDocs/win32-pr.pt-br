---
description: As interfaces de renderização para o Direct3D consistem em métodos que processam primitivos de dados de vértice armazenados em um ou mais buffers de dados.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Fluxos de dados de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645800"
---
# <a name="vertex-data-streams-direct3d-9"></a><span data-ttu-id="6a947-103">Fluxos de dados de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6a947-103">Vertex Data Streams (Direct3D 9)</span></span>

<span data-ttu-id="6a947-104">As interfaces de renderização para o Direct3D consistem em métodos que processam primitivos de dados de vértice armazenados em um ou mais buffers de dados.</span><span class="sxs-lookup"><span data-stu-id="6a947-104">The rendering interfaces for Direct3D consist of methods that render primitives from vertex data stored in one or more data buffers.</span></span> <span data-ttu-id="6a947-105">Os dados de vértice consistem em elementos de vértice combinados para formar componentes de vértice.</span><span class="sxs-lookup"><span data-stu-id="6a947-105">Vertex data consists of vertex elements combined to form vertex components.</span></span> <span data-ttu-id="6a947-106">Os elementos Vertex, a menor unidade de um vértice, representam entidades como position, normal ou Color.</span><span class="sxs-lookup"><span data-stu-id="6a947-106">Vertex elements, the smallest unit of a vertex, represent entities such as position, normal, or color.</span></span>

<span data-ttu-id="6a947-107">Os componentes de vértice são um ou mais elementos de vértice armazenados de forma contígua (intercalados por vértice) em um único buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="6a947-107">Vertex components are one or more vertex elements stored contiguously (interleaved per vertex) in a single memory buffer.</span></span> <span data-ttu-id="6a947-108">Um vértice completo consiste em um ou mais componentes, onde cada componente está em um buffer de memória separado.</span><span class="sxs-lookup"><span data-stu-id="6a947-108">A complete vertex consists of one or more components, where each component is in a separate memory buffer.</span></span> <span data-ttu-id="6a947-109">Para renderizar um primitivo, vários componentes de vértice são lidos e montados para que os vértices completos estejam disponíveis para processamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="6a947-109">To render a primitive, multiple vertex components are read and assembled so that complete vertices are available for vertex processing.</span></span> <span data-ttu-id="6a947-110">O diagrama a seguir mostra o processo de renderização de primitivos usando componentes de vértice.</span><span class="sxs-lookup"><span data-stu-id="6a947-110">The following diagram shows the process of rendering primitives using vertex components.</span></span>

![diagrama do processo para renderizar primitivos usando componentes de vértice](images/vertexdata.png)

<span data-ttu-id="6a947-112">Os primitivos de renderização consistem em duas etapas.</span><span class="sxs-lookup"><span data-stu-id="6a947-112">Rendering primitives consists of two steps.</span></span> <span data-ttu-id="6a947-113">Primeiro, configure um ou mais fluxos de componentes de vértice; em segundo lugar, invoque um método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para renderizar desses fluxos.</span><span class="sxs-lookup"><span data-stu-id="6a947-113">First, set up one or more vertex component streams; second, invoke a [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method to render from those streams.</span></span> <span data-ttu-id="6a947-114">A identificação dos elementos de vértice dentro desses fluxos de componente é especificada pelo sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="6a947-114">Identification of vertex elements within these component streams is specified by the vertex shader.</span></span>

<span data-ttu-id="6a947-115">Os métodos [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) especificam um deslocamento nos fluxos de dados de vértice para que um subconjunto contíguo arbitrário dos primitivos dentro de um conjunto de dados de vértice possa ser renderizado com cada invocação de desenho.</span><span class="sxs-lookup"><span data-stu-id="6a947-115">The [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) methods specify an offset in the vertex data streams so that an arbitrary contiguous subset of the primitives within one set of vertex data can be rendered with each draw invocation.</span></span> <span data-ttu-id="6a947-116">Isso permite que você altere o estado de renderização do dispositivo entre grupos de primitivos que são processados dos mesmos buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="6a947-116">This enables you to change the device rendering state between groups of primitives that are rendered from the same vertex buffers.</span></span>

<span data-ttu-id="6a947-117">Há suporte para métodos de desenho indexados e não indexados.</span><span class="sxs-lookup"><span data-stu-id="6a947-117">Both indexed and nonindexed drawing methods are supported.</span></span> <span data-ttu-id="6a947-118">Para obter mais informações, consulte [renderizando de vértices e buffers de índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="6a947-118">For more information, see [Rendering from Vertex and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a947-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a947-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a947-120">Primitivos de renderização</span><span class="sxs-lookup"><span data-stu-id="6a947-120">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
