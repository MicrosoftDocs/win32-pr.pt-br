---
description: 'Esta seção contém informações sobre as seguintes interfaces de sombreador:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfaces de sombreador (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457044"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a><span data-ttu-id="54f2a-103">Interfaces de sombreador (gráficos do Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="54f2a-103">Shader Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="54f2a-104">Esta seção contém informações sobre as seguintes interfaces de sombreador:</span><span class="sxs-lookup"><span data-stu-id="54f2a-104">This section contains information about the following shader interfaces:</span></span>

<span data-ttu-id="54f2a-105">Cada uma dessas interfaces de sombreador gerencia um sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="54f2a-105">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="54f2a-106">A interface é criada quando um sombreador é compilado e, em seguida, é passada para várias APIs que precisam de acesso a um sombreador compilado; como ao associar um sombreador a um estágio de pipeline ou obter uma assinatura de sombreador.</span><span class="sxs-lookup"><span data-stu-id="54f2a-106">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>



| <span data-ttu-id="54f2a-107">Interfaces Pipeline-Stage</span><span class="sxs-lookup"><span data-stu-id="54f2a-107">Pipeline-Stage Interfaces</span></span>                                      | <span data-ttu-id="54f2a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="54f2a-108">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54f2a-109">**Interface ID3D10GeometryShader**</span><span class="sxs-lookup"><span data-stu-id="54f2a-109">**ID3D10GeometryShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | <span data-ttu-id="54f2a-110">Um sombreador Geometry implementa processamento por primitivo no [estágio Geometry-Shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="54f2a-110">A geometry-shader implements per-primitive processing in the [geometry-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> |
| [<span data-ttu-id="54f2a-111">**Interface ID3D10PixelShader**</span><span class="sxs-lookup"><span data-stu-id="54f2a-111">**ID3D10PixelShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | <span data-ttu-id="54f2a-112">Um sombreador de pixel implementa processamento por pixel no [estágio pixel-shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="54f2a-112">A pixel-shader implements per-pixel processing in the [pixel-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>           |
| [<span data-ttu-id="54f2a-113">**Interface ID3D10VertexShader**</span><span class="sxs-lookup"><span data-stu-id="54f2a-113">**ID3D10VertexShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | <span data-ttu-id="54f2a-114">Um sombreador de vértice implementa processamento por vértice no [estágio Vertex-Shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="54f2a-114">A vertex-shader implements per-vertex processing in the [vertex-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>        |



 

<span data-ttu-id="54f2a-115">As interfaces Shader-Reflection permitem que um aplicativo Inspecione o conteúdo de um sombreador no tempo de design/autor.</span><span class="sxs-lookup"><span data-stu-id="54f2a-115">Shader-reflection interfaces allow an application to inspect the contents of a shader at design/author time.</span></span> <span data-ttu-id="54f2a-116">A reflexão de sombreador não é útil para definir variáveis em tempo de execução, pois é um espelho dos dados do sombreador e, portanto, não dá suporte a métodos para definir dados.</span><span class="sxs-lookup"><span data-stu-id="54f2a-116">Shader reflection is not useful for setting variables at runtime as it is a mirror of the shader data, and therefore supports no methods for setting data.</span></span>



| <span data-ttu-id="54f2a-117">Interfaces Shader-Reflection</span><span class="sxs-lookup"><span data-stu-id="54f2a-117">Shader-Reflection Interfaces</span></span>                                                                   | <span data-ttu-id="54f2a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="54f2a-118">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="54f2a-119">**Interface ID3D10ShaderReflection**</span><span class="sxs-lookup"><span data-stu-id="54f2a-119">**ID3D10ShaderReflection Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | <span data-ttu-id="54f2a-120">Uma interface COM para ler informações de um sombreador compilado no momento do autor.</span><span class="sxs-lookup"><span data-stu-id="54f2a-120">A COM interface for reading information from a compiled shader at author time.</span></span>     |
| [<span data-ttu-id="54f2a-121">**Interface ID3D10ShaderReflectionConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="54f2a-121">**ID3D10ShaderReflectionConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | <span data-ttu-id="54f2a-122">Uma interface auxiliar para obter uma interface de buffer constante de reflexo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="54f2a-122">A helper interface for getting a shader-reflection constant-buffer interface.</span></span>      |
| [<span data-ttu-id="54f2a-123">**Interface ID3D10ShaderReflectionType**</span><span class="sxs-lookup"><span data-stu-id="54f2a-123">**ID3D10ShaderReflectionType Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | <span data-ttu-id="54f2a-124">Uma interface auxiliar para obter uma interface do tipo Shader-Reflection.</span><span class="sxs-lookup"><span data-stu-id="54f2a-124">A helper interface for getting a shader-reflection-type interface.</span></span>                 |
| [<span data-ttu-id="54f2a-125">**Interface ID3D10ShaderReflectionVariable**</span><span class="sxs-lookup"><span data-stu-id="54f2a-125">**ID3D10ShaderReflectionVariable Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | <span data-ttu-id="54f2a-126">Uma interface auxiliar para obter uma interface Shader-Reflection-Variable.</span><span class="sxs-lookup"><span data-stu-id="54f2a-126">A helper interface for getting a shader-reflection-variable interface.</span></span>             |
| [<span data-ttu-id="54f2a-127">**Interface ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="54f2a-127">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | <span data-ttu-id="54f2a-128">Uma interface Shader-Reflection para ler informações de uma exibição de recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="54f2a-128">A shader-reflection interface for reading information from a shader-resource view.</span></span> |



 

<span data-ttu-id="54f2a-129">As APIs de reflexão de sombreador implementam uma interface de reflexão de sombreador COM ([**interface ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) e várias interfaces auxiliares não com (o restante das interfaces).</span><span class="sxs-lookup"><span data-stu-id="54f2a-129">Shader reflection APIs implement one COM shader reflection interface ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) and several non-COM helper interfaces (the rest of the interfaces).</span></span> <span data-ttu-id="54f2a-130">A **interface ID3D10ShaderReflection** é criada quando um objeto de reflexo de sombreador é criado.</span><span class="sxs-lookup"><span data-stu-id="54f2a-130">**ID3D10ShaderReflection Interface** is created when a shader reflection object is created.</span></span> <span data-ttu-id="54f2a-131">Ele segue as regras COM padrão; a criação da interface aumenta a contagem de referência e a interface deve ser liberada quando não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="54f2a-131">It follows standard COM rules; creating the interface increases a reference count and the interface must be released when it is no longer needed.</span></span> <span data-ttu-id="54f2a-132">As interfaces do sombreador-Reflection restantes são interfaces auxiliares que não herdam de IUnknown.</span><span class="sxs-lookup"><span data-stu-id="54f2a-132">The remaining shader-reflection interfaces are helper interfaces that do not inherit from IUnknown.</span></span> <span data-ttu-id="54f2a-133">Isso significa que eles não alteram nenhuma contagem de referência quando são criados e não precisam ser destruídos quando você termina com eles.</span><span class="sxs-lookup"><span data-stu-id="54f2a-133">This means that they do not change any reference count when they are created, and they do not need to be destroyed when you are finished with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54f2a-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54f2a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54f2a-135">Referência do sombreador</span><span class="sxs-lookup"><span data-stu-id="54f2a-135">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
