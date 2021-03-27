---
title: Função GroupMemoryBarrier
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos compartilhados de grupo tenham sido concluídos.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- HLSL da função GroupMemoryBarrier
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54a140a892b0e9144ef23fc0290ca3bb3747e90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006266"
---
# <a name="groupmemorybarrier-function"></a><span data-ttu-id="01bc0-104">Função GroupMemoryBarrier</span><span class="sxs-lookup"><span data-stu-id="01bc0-104">GroupMemoryBarrier function</span></span>

<span data-ttu-id="01bc0-105">Bloqueia a execução de todos os threads em um grupo até que todos os acessos compartilhados de grupo tenham sido concluídos.</span><span class="sxs-lookup"><span data-stu-id="01bc0-105">Blocks execution of all threads in a group until all group shared accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="01bc0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01bc0-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="01bc0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01bc0-107">Parameters</span></span>

<span data-ttu-id="01bc0-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="01bc0-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01bc0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01bc0-109">Return value</span></span>

<span data-ttu-id="01bc0-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="01bc0-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01bc0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="01bc0-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="01bc0-112">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="01bc0-112">Minimum Shader Model</span></span>

<span data-ttu-id="01bc0-113">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="01bc0-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="01bc0-114">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="01bc0-114">Shader Model</span></span>                                                                | <span data-ttu-id="01bc0-115">Com suporte</span><span class="sxs-lookup"><span data-stu-id="01bc0-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="01bc0-116">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="01bc0-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="01bc0-117">sim</span><span class="sxs-lookup"><span data-stu-id="01bc0-117">yes</span></span>       |



 

<span data-ttu-id="01bc0-118">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="01bc0-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="01bc0-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="01bc0-119">Vertex</span></span> | <span data-ttu-id="01bc0-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="01bc0-120">Hull</span></span> | <span data-ttu-id="01bc0-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="01bc0-121">Domain</span></span> | <span data-ttu-id="01bc0-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="01bc0-122">Geometry</span></span> | <span data-ttu-id="01bc0-123">16x16</span><span class="sxs-lookup"><span data-stu-id="01bc0-123">Pixel</span></span> | <span data-ttu-id="01bc0-124">Computação</span><span class="sxs-lookup"><span data-stu-id="01bc0-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="01bc0-125">x</span><span class="sxs-lookup"><span data-stu-id="01bc0-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="01bc0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="01bc0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01bc0-127">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="01bc0-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="01bc0-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="01bc0-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




