---
description: No Direct3D 10, o estado do dispositivo é agrupado em objetos de estado, o que reduz significativamente o custo das alterações de estado.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objetos de estado (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790610"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="e8a97-103">Objetos de estado (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e8a97-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="e8a97-104">No Direct3D 10, o estado do dispositivo é agrupado em objetos de estado, o que reduz significativamente o custo das alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="e8a97-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="e8a97-105">Há vários objetos de estado, e cada um deles é projetado para inicializar um conjunto de estado para um estágio de pipeline específico.</span><span class="sxs-lookup"><span data-stu-id="e8a97-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="e8a97-106">Você pode criar até 4096 de cada tipo de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="e8a97-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="e8a97-107">Estado de layout de entrada</span><span class="sxs-lookup"><span data-stu-id="e8a97-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="e8a97-108">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="e8a97-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="e8a97-109">Estado do estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="e8a97-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="e8a97-110">Estado do Blend</span><span class="sxs-lookup"><span data-stu-id="e8a97-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="e8a97-111">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="e8a97-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="e8a97-112">Considerações sobre desempenho</span><span class="sxs-lookup"><span data-stu-id="e8a97-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="e8a97-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8a97-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="e8a97-114">Estado de layout de entrada</span><span class="sxs-lookup"><span data-stu-id="e8a97-114">Input-Layout State</span></span>

<span data-ttu-id="e8a97-115">Esse grupo de estado (consulte [**o \_ elemento de entrada d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) determina como o estágio de montagem de [entrada](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) lê dados dos buffers de entrada e os monta para uso pelo sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="e8a97-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="e8a97-116">Isso inclui o estado, como o número de elementos no buffer de entrada e a assinatura dos dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8a97-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="e8a97-117">O estágio de Assembler de entrada é um novo estágio no pipeline cujo trabalho é transmitir primitivos da memória para o pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8a97-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="e8a97-118">Para criar um objeto de estado de layout de entrada, consulte [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="e8a97-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="e8a97-119">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="e8a97-119">Rasterizer State</span></span>

<span data-ttu-id="e8a97-120">Esse grupo de estado (consulte [**d3d10 do \_ rasterizador \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) inicializa o [estágio do rasterizador](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="e8a97-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="e8a97-121">Esse objeto inclui o estado como modos preenchimento ou eliminação, permitindo o recorte de um retângulo de corte e a configuração de parâmetros de várias amostras.</span><span class="sxs-lookup"><span data-stu-id="e8a97-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="e8a97-122">Este estágio rasteriza os primitivos em pixels, realizando operações como recorte e mapeamento de primitivos no visor.</span><span class="sxs-lookup"><span data-stu-id="e8a97-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="e8a97-123">Para criar um objeto de estado do rasterizador, consulte [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span><span class="sxs-lookup"><span data-stu-id="e8a97-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="e8a97-124">Estado do estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="e8a97-124">Depth-Stencil State</span></span>

<span data-ttu-id="e8a97-125">Esse grupo de estado (consulte [**o \_ estêncil de profundidade do d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) inicializa a parte do estêncil de profundidade do [estágio de mesclagem de saída](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="e8a97-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="e8a97-126">Mais especificamente, esse objeto inicializa os testes de estêncil e profundidade.</span><span class="sxs-lookup"><span data-stu-id="e8a97-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="e8a97-127">Para criar um objeto de estado de estêncil de profundidade, consulte [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span><span class="sxs-lookup"><span data-stu-id="e8a97-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="e8a97-128">Estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="e8a97-128">Blend State</span></span>

<span data-ttu-id="e8a97-129">Esse grupo de estado (consulte [**d3d10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) inicializa a parte de mesclagem do [estágio de fusão de saída](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="e8a97-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="e8a97-130">Para criar um objeto de estado de mesclagem, consulte [**Createblendstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span><span class="sxs-lookup"><span data-stu-id="e8a97-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="e8a97-131">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="e8a97-131">Sampler State</span></span>

<span data-ttu-id="e8a97-132">Esse grupo de estado (consulte [**a \_ amostra \_ de d3d10 desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) Inicializa um objeto de amostra.</span><span class="sxs-lookup"><span data-stu-id="e8a97-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="e8a97-133">Um objeto de amostra é usado pelos estágios de sombreador para filtrar texturas na memória.</span><span class="sxs-lookup"><span data-stu-id="e8a97-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a97-134">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="e8a97-134">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="e8a97-135">No Direct3D 10, o objeto de amostra não está mais ligado a uma textura específica – ele apenas descreve como fazer a filtragem de acordo com qualquer recurso anexado.</span><span class="sxs-lookup"><span data-stu-id="e8a97-135">In Direct3D 10, the sampler object is no longer bound to a specific texture - it just describes how to do filtering given any attached resource.</span></span> |



 

<span data-ttu-id="e8a97-136">Para criar um objeto de estado de amostra, consulte [**Createsamplestate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="e8a97-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="e8a97-137">Considerações sobre desempenho</span><span class="sxs-lookup"><span data-stu-id="e8a97-137">Performance Considerations</span></span>

<span data-ttu-id="e8a97-138">Projetar a API para usar objetos de estado cria várias vantagens de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e8a97-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="e8a97-139">Isso inclui validação de estado no momento da criação de objeto, habilitação do cache de objetos de estado no hardware e redução considerável da quantidade de estado que é passada durante uma chamada de API de configuração de estado (passando um manipulador para o objeto de estado em vez do estado).</span><span class="sxs-lookup"><span data-stu-id="e8a97-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="e8a97-140">Para obter essas melhorias de desempenho, é necessário criar os objetos de estado quando seu aplicativo for inicializado, logo antes do seu loop de renderização.</span><span class="sxs-lookup"><span data-stu-id="e8a97-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="e8a97-141">Os objetos de estado são imutáveis, ou seja, depois que são criados, não podem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="e8a97-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="e8a97-142">Em vez disso, você deve destruí-los ou recriá-los.</span><span class="sxs-lookup"><span data-stu-id="e8a97-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="e8a97-143">Para lidar com essa restrição, você pode criar até 4096 de cada tipo de objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="e8a97-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="e8a97-144">Por exemplo, você pode criar vários objetos de amostra com várias combinações de estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="e8a97-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="e8a97-145">A alteração do estado de amostra é então realizada chamando a API Set apropriada que passa um identificador para o objeto (em oposição ao estado de amostra).</span><span class="sxs-lookup"><span data-stu-id="e8a97-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="e8a97-146">Isso reduz significativamente a quantidade de sobrecarga durante cada quadro de renderização para alterar o estado, uma vez que o número de chamadas e a quantidade de dados são consideravelmente reduzidos.</span><span class="sxs-lookup"><span data-stu-id="e8a97-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="e8a97-147">Como alternativa, você pode optar por usar o sistema de efeito que gerenciará automaticamente a criação e destruição eficientes de objetos de estado para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8a97-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8a97-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8a97-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8a97-149">Recursos de API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e8a97-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
