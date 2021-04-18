---
title: Sombreadores HLSL de raytracing do Direct3D 12
description: Os seguintes sombreadores HLSL dão suporte ao pipeline do Direct3D 12 raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105749500"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="097c6-103">Sombreadores HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="097c6-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="097c6-104">Os seguintes sombreadores HLSL dão suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="097c6-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="097c6-105">Esses sombreadores são funções compiladas em uma biblioteca, com o modelo de destino lib_6_3 e identificados por um atributo *[Shader ("shadertype")]* na função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="097c6-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="097c6-106">Consulte **intrínsecos** e **valores do sistema** para ver o que é permitido para cada tipo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="097c6-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="097c6-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="097c6-107">In this section</span></span>



| <span data-ttu-id="097c6-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="097c6-108">Topic</span></span>                                                                                                       | <span data-ttu-id="097c6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="097c6-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="097c6-110">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="097c6-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="097c6-111">Um sombreador que é invocado quando Ray interseções não são opacas.</span><span class="sxs-lookup"><span data-stu-id="097c6-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="097c6-112">**Sombreador resgatável**</span><span class="sxs-lookup"><span data-stu-id="097c6-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="097c6-113">Um sombreador que é invocado de outro sombreador com o intrínseco **CallShader** .</span><span class="sxs-lookup"><span data-stu-id="097c6-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="097c6-114">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="097c6-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="097c6-115">Um sombreador que é invocado quando está habilitado e a visita mais próxima foi determinada ou Ray a pesquisa de interseção terminou.</span><span class="sxs-lookup"><span data-stu-id="097c6-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="097c6-116">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="097c6-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="097c6-117">Um sombreador que é usado para implementar primitivos de interseção personalizados para raios interseccionando um volume limitado associado (caixa delimitadora).</span><span class="sxs-lookup"><span data-stu-id="097c6-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="097c6-118">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="097c6-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="097c6-119">Um sombreador que é invocado quando nenhuma interseção de Ray é encontrada ou aceita.</span><span class="sxs-lookup"><span data-stu-id="097c6-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="097c6-120">**Sombreador da geração de raio**</span><span class="sxs-lookup"><span data-stu-id="097c6-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="097c6-121">Um sombreador que chama [**TraceRay**](traceray-function.md) para gerar raios.</span><span class="sxs-lookup"><span data-stu-id="097c6-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="097c6-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="097c6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="097c6-123">Referência principal</span><span class="sxs-lookup"><span data-stu-id="097c6-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="097c6-124">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="097c6-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





