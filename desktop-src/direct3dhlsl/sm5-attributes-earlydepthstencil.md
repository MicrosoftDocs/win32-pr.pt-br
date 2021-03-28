---
title: earlydepthstencil
description: Força o teste de estêncil de profundidade antes da execução de um sombreador.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988609"
---
# <a name="earlydepthstencil"></a><span data-ttu-id="bdab6-103">earlydepthstencil</span><span class="sxs-lookup"><span data-stu-id="bdab6-103">earlydepthstencil</span></span>

<span data-ttu-id="bdab6-104">Força o teste de estêncil de profundidade antes da execução de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="bdab6-104">Forces depth-stencil testing before a shader executes.</span></span>


```
earlydepthstencil   
```



## <a name="remarks"></a><span data-ttu-id="bdab6-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdab6-105">Remarks</span></span>

<span data-ttu-id="bdab6-106">O teste de estêncil de profundidade normalmente é feito durante o processamento de pixel por um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="bdab6-106">Depth-stencil testing is normally done during pixel processing by a pixel shader.</span></span> <span data-ttu-id="bdab6-107">Forçar o teste de estêncil de profundidade inicial faz com que os testes sejam feitos antes da execução do sombreador; a finalidade é melhorar o desempenho por pixel, removendo/reduzindo/evitando o processamento de pixel desnecessário.</span><span class="sxs-lookup"><span data-stu-id="bdab6-107">Forcing early depth-stencil testing causes the testing to be done prior to the shader execution; the purpose is to improve per-pixel performance by culling/reducing/avoiding unnecessary pixel processing.</span></span>

<span data-ttu-id="bdab6-108">Um aplicativo pode forçar o teste de estêncil de profundidade inicial fornecendo o atributo ou o hardware pode executar o teste de estêncil de profundidade inicial, desde que nenhum valor de profundidade seja gravado e nenhuma operação de acesso não ordenada seja executada em um sombreador como uma otimização.</span><span class="sxs-lookup"><span data-stu-id="bdab6-108">An application can force early depth-stencil testing by supplying the attribute or the hardware may execute early depth-stencil testing provided no depth values are written and no unordered access operations are performed in a shader as an optimization.</span></span>

<span data-ttu-id="bdab6-109">Esse atributo tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="bdab6-109">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="bdab6-110">Vértice</span><span class="sxs-lookup"><span data-stu-id="bdab6-110">Vertex</span></span> | <span data-ttu-id="bdab6-111">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bdab6-111">Hull</span></span> | <span data-ttu-id="bdab6-112">Domínio</span><span class="sxs-lookup"><span data-stu-id="bdab6-112">Domain</span></span> | <span data-ttu-id="bdab6-113">Geometria</span><span class="sxs-lookup"><span data-stu-id="bdab6-113">Geometry</span></span> | <span data-ttu-id="bdab6-114">16x16</span><span class="sxs-lookup"><span data-stu-id="bdab6-114">Pixel</span></span> | <span data-ttu-id="bdab6-115">Computação</span><span class="sxs-lookup"><span data-stu-id="bdab6-115">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bdab6-116">x</span><span class="sxs-lookup"><span data-stu-id="bdab6-116">x</span></span>     |         |



 

## <a name="related-topics"></a><span data-ttu-id="bdab6-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdab6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdab6-118">Atributos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="bdab6-118">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="bdab6-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bdab6-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




