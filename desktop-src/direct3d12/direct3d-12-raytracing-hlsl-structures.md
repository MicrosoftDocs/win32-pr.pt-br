---
title: Estruturas raytracing HLSL (Direct3D 12)
description: As estruturas HLSL a seguir dão suporte ao pipeline do Direct3D 12 raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c48ad6bac76e200587ec76d42dfa9c86b23cd23
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "105762218"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a><span data-ttu-id="b61ad-103">Estruturas raytracing HLSL (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="b61ad-103">Raytracing HLSL structures (Direct3D 12)</span></span>

<span data-ttu-id="b61ad-104">As estruturas HLSL a seguir dão suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="b61ad-104">The following HLSL structures support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b61ad-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b61ad-105">In this section</span></span>



| <span data-ttu-id="b61ad-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="b61ad-106">Topic</span></span>                                                                                                       | <span data-ttu-id="b61ad-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b61ad-107">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b61ad-108">**Estrutura do parâmetro de chamada**</span><span class="sxs-lookup"><span data-stu-id="b61ad-108">**Call Parameter Structure**</span></span>](call-parameter-structure.md)<br/>                              | <span data-ttu-id="b61ad-109">Uma estrutura definida pelo usuário fornecida como um argumento Inout para uma chamada CallShader e como um parâmetro Inout para o sombreador callable.</span><span class="sxs-lookup"><span data-stu-id="b61ad-109">A user-defined structure provided as an inout argument to a CallShader call, and as an inout parameter for the callable shader.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="b61ad-110">**Estrutura de atributos de interseção**</span><span class="sxs-lookup"><span data-stu-id="b61ad-110">**Intersection Attributes Structure**</span></span>](intersection-attributes.md)<br/>                              | <span data-ttu-id="b61ad-111">Uma estrutura definida pelo usuário que é fornecida como um argumento Inout em uma chamada [**TraceRay**](traceray-function.md) e como um parâmetro Inout nos tipos de sombreador que podem acessar a carga Ray.</span><span class="sxs-lookup"><span data-stu-id="b61ad-111">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="b61ad-112">**Estrutura do conteúdo do raio**</span><span class="sxs-lookup"><span data-stu-id="b61ad-112">**Ray Payload Structure**</span></span>](ray-payload.md)<br/>                              | <span data-ttu-id="b61ad-113">Uma estrutura definida pelo usuário que é fornecida como um argumento Inout em uma chamada [**TraceRay**](traceray-function.md) e como um parâmetro Inout nos tipos de sombreador que podem acessar a carga Ray.</span><span class="sxs-lookup"><span data-stu-id="b61ad-113">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="b61ad-114">**Estrutura RayDesc**</span><span class="sxs-lookup"><span data-stu-id="b61ad-114">**RayDesc Structure**</span></span>](raydesc.md)<br/>                              | <span data-ttu-id="b61ad-115">Sinalizadores passados para a função [**TraceRay**](traceray-function.md) para substituir transparência, remoção e comportamento de início.</span><span class="sxs-lookup"><span data-stu-id="b61ad-115">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span><br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a><span data-ttu-id="b61ad-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b61ad-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b61ad-117">Referência principal</span><span class="sxs-lookup"><span data-stu-id="b61ad-117">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="b61ad-118">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b61ad-118">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





