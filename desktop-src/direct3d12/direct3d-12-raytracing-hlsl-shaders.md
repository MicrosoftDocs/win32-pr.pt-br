---
title: Sombreadores HLSL de raytracing do Direct3D 12
description: Veja links para artigos que descrevem sombreadores de HLSL (linguagem de sombreador de alto nível) que suportam o pipeline de raytracing do Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394831"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="6157b-103">Sombreadores HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6157b-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="6157b-104">Os sombreadores HLSL a seguir são suportados pelo pipeline de raytracing do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="6157b-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="6157b-105">Esses sombreadores são funções compiladas em uma biblioteca, com o modelo de destino lib_6_3 e identificadas por um atributo *[shader("shadertype")]* na função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6157b-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="6157b-106">Consulte **Intrínsecos** **e Valores do Sistema** para ver o que é permitido para cada tipo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6157b-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6157b-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6157b-107">In this section</span></span>



| <span data-ttu-id="6157b-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="6157b-108">Topic</span></span>                                                                                                       | <span data-ttu-id="6157b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6157b-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6157b-110">**Sombreador de todos os cliques**</span><span class="sxs-lookup"><span data-stu-id="6157b-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="6157b-111">Um sombreador que é invocado quando interseções de raio não são opacas.</span><span class="sxs-lookup"><span data-stu-id="6157b-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6157b-112">**Sombreador resgatável**</span><span class="sxs-lookup"><span data-stu-id="6157b-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="6157b-113">Um sombreador que é invocado de outro sombreador com o **intrínseco CallShader.**</span><span class="sxs-lookup"><span data-stu-id="6157b-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6157b-114">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="6157b-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="6157b-115">Um sombreador que é invocado quando está habilitado e o acerto mais próximo foi determinado ou a pesquisa de interseção de raio terminou.</span><span class="sxs-lookup"><span data-stu-id="6157b-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6157b-116">**Sombreador de interseção**</span><span class="sxs-lookup"><span data-stu-id="6157b-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="6157b-117">Um sombreador usado para implementar primitivos de interseção personalizados para raios intersecção de um volume delimitador associado (caixa delimitador).</span><span class="sxs-lookup"><span data-stu-id="6157b-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6157b-118">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="6157b-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="6157b-119">Um sombreador que é invocado quando nenhuma interseção de raio é encontrada ou aceita.</span><span class="sxs-lookup"><span data-stu-id="6157b-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6157b-120">**Sombreador da geração de raio**</span><span class="sxs-lookup"><span data-stu-id="6157b-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="6157b-121">Um sombreador que chama [**TraceRay para**](traceray-function.md) gerar raios.</span><span class="sxs-lookup"><span data-stu-id="6157b-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="6157b-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6157b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6157b-123">Referência principal</span><span class="sxs-lookup"><span data-stu-id="6157b-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="6157b-124">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6157b-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





