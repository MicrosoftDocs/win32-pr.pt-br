---
title: instance
description: Use este atributo para fazer uma instância de um sombreador de geometria.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006909"
---
# <a name="instance"></a><span data-ttu-id="33da5-103">instance</span><span class="sxs-lookup"><span data-stu-id="33da5-103">instance</span></span>

<span data-ttu-id="33da5-104">Use este atributo para fazer uma instância de um sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="33da5-104">Use this attribute to instance a geometry shader.</span></span>


```
instance(X)   
```



## <a name="remarks"></a><span data-ttu-id="33da5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="33da5-105">Remarks</span></span>

<span data-ttu-id="33da5-106">X é um índice inteiro que indica o número de instâncias a serem executadas para cada item desenhado (por exemplo, para cada triângulo).</span><span class="sxs-lookup"><span data-stu-id="33da5-106">X is an integer index that indicates the number of instances to be executed for each drawn item (for example, for each triangle).</span></span> <span data-ttu-id="33da5-107">Ao usar esse atributo, use [VA \_ GSInstanceID](sv-gsinstanceid.md) para identificar qual instância de um sombreador de geometria está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="33da5-107">When using this attribute, use [SV\_GSInstanceID](sv-gsinstanceid.md) to identify which instance of a geometry shader is being executed.</span></span>

<span data-ttu-id="33da5-108">Esse atributo tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="33da5-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="33da5-109">Vértice</span><span class="sxs-lookup"><span data-stu-id="33da5-109">Vertex</span></span> | <span data-ttu-id="33da5-110">Envoltória</span><span class="sxs-lookup"><span data-stu-id="33da5-110">Hull</span></span> | <span data-ttu-id="33da5-111">Domínio</span><span class="sxs-lookup"><span data-stu-id="33da5-111">Domain</span></span> | <span data-ttu-id="33da5-112">Geometria</span><span class="sxs-lookup"><span data-stu-id="33da5-112">Geometry</span></span> | <span data-ttu-id="33da5-113">16x16</span><span class="sxs-lookup"><span data-stu-id="33da5-113">Pixel</span></span> | <span data-ttu-id="33da5-114">Computação</span><span class="sxs-lookup"><span data-stu-id="33da5-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="33da5-115">x</span><span class="sxs-lookup"><span data-stu-id="33da5-115">x</span></span>        |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="33da5-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33da5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33da5-117">Atributos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="33da5-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="33da5-118">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="33da5-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




