---
title: maxtessfactor
description: Indica o valor máximo que o sombreador envoltória retornaria para qualquer fator de mosaico.
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823457"
---
# <a name="maxtessfactor"></a><span data-ttu-id="f47a6-103">maxtessfactor</span><span class="sxs-lookup"><span data-stu-id="f47a6-103">maxtessfactor</span></span>

<span data-ttu-id="f47a6-104">Indica o valor máximo que o sombreador envoltória retornaria para qualquer fator de mosaico.</span><span class="sxs-lookup"><span data-stu-id="f47a6-104">Indicates the maximum value that the hull shader would return for any tessellation factor.</span></span>


```
maxtessfactor(X)   
```



## <a name="remarks"></a><span data-ttu-id="f47a6-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f47a6-105">Remarks</span></span>

<span data-ttu-id="f47a6-106">Esse atributo coloca um limite superior na quantidade de mosaico solicitado para ajudar um driver a determinar a quantidade máxima de recursos necessários para o mosaico.</span><span class="sxs-lookup"><span data-stu-id="f47a6-106">This attribute puts an upper bound on the amount of tessellation requested to help a driver determine the maximum amount of resources required for tessellation.</span></span>

<span data-ttu-id="f47a6-107">Esse atributo tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f47a6-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f47a6-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="f47a6-108">Vertex</span></span> | <span data-ttu-id="f47a6-109">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f47a6-109">Hull</span></span> | <span data-ttu-id="f47a6-110">Domínio</span><span class="sxs-lookup"><span data-stu-id="f47a6-110">Domain</span></span> | <span data-ttu-id="f47a6-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="f47a6-111">Geometry</span></span> | <span data-ttu-id="f47a6-112">16x16</span><span class="sxs-lookup"><span data-stu-id="f47a6-112">Pixel</span></span> | <span data-ttu-id="f47a6-113">Computação</span><span class="sxs-lookup"><span data-stu-id="f47a6-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="f47a6-114">x</span><span class="sxs-lookup"><span data-stu-id="f47a6-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="f47a6-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f47a6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f47a6-116">Atributos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="f47a6-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="f47a6-117">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f47a6-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




