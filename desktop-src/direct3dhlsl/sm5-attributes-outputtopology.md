---
title: outputtopology
description: Define o tipo primitivo de saída para o Tessellator.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916877"
---
# <a name="outputtopology"></a><span data-ttu-id="b95bb-103">outputtopology</span><span class="sxs-lookup"><span data-stu-id="b95bb-103">outputtopology</span></span>

<span data-ttu-id="b95bb-104">Define o tipo primitivo de saída para o Tessellator.</span><span class="sxs-lookup"><span data-stu-id="b95bb-104">Defines the output primitive type for the tessellator.</span></span>


```
outputtopology(X)      
```



## <a name="remarks"></a><span data-ttu-id="b95bb-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b95bb-105">Remarks</span></span>

<span data-ttu-id="b95bb-106">X deve ser [**ponto**](dx-graphics-hlsl-geometry-shader.md), **linha**, **triângulo ou \_** **semiangular e deve \_ estar** entre aspas.</span><span class="sxs-lookup"><span data-stu-id="b95bb-106">X must be either [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle\_cw**, or **triangle\_ccw** and must be inside quotes.</span></span> <span data-ttu-id="b95bb-107">Aqui estão as opções válidas para este atributo:</span><span class="sxs-lookup"><span data-stu-id="b95bb-107">Here are the valid options for this attribute:</span></span>


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



<span data-ttu-id="b95bb-108">Esse atributo tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b95bb-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b95bb-109">Vértice</span><span class="sxs-lookup"><span data-stu-id="b95bb-109">Vertex</span></span> | <span data-ttu-id="b95bb-110">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b95bb-110">Hull</span></span> | <span data-ttu-id="b95bb-111">Domínio</span><span class="sxs-lookup"><span data-stu-id="b95bb-111">Domain</span></span> | <span data-ttu-id="b95bb-112">Geometria</span><span class="sxs-lookup"><span data-stu-id="b95bb-112">Geometry</span></span> | <span data-ttu-id="b95bb-113">16x16</span><span class="sxs-lookup"><span data-stu-id="b95bb-113">Pixel</span></span> | <span data-ttu-id="b95bb-114">Computação</span><span class="sxs-lookup"><span data-stu-id="b95bb-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="b95bb-115">x</span><span class="sxs-lookup"><span data-stu-id="b95bb-115">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="b95bb-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b95bb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b95bb-117">Atributos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="b95bb-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="b95bb-118">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b95bb-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




