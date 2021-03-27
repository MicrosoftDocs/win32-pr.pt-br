---
title: Função GroupMemoryBarrierWithGroupSync
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos compartilhados do grupo tenham sido concluídos e todos os threads do grupo tenham chegado a essa chamada.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- HLSL da função GroupMemoryBarrierWithGroupSync
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104967059"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a><span data-ttu-id="5b8c1-104">Função GroupMemoryBarrierWithGroupSync</span><span class="sxs-lookup"><span data-stu-id="5b8c1-104">GroupMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="5b8c1-105">Bloqueia a execução de todos os threads em um grupo até que todos os acessos compartilhados do grupo tenham sido concluídos e todos os threads do grupo tenham chegado a essa chamada.</span><span class="sxs-lookup"><span data-stu-id="5b8c1-105">Blocks execution of all threads in a group until all group shared accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8c1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b8c1-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="5b8c1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b8c1-107">Parameters</span></span>

<span data-ttu-id="5b8c1-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5b8c1-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b8c1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b8c1-109">Return value</span></span>

<span data-ttu-id="5b8c1-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5b8c1-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b8c1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b8c1-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="5b8c1-112">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="5b8c1-112">Minimum Shader Model</span></span>

<span data-ttu-id="5b8c1-113">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5b8c1-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5b8c1-114">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="5b8c1-114">Shader Model</span></span>                                                                | <span data-ttu-id="5b8c1-115">Com suporte</span><span class="sxs-lookup"><span data-stu-id="5b8c1-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5b8c1-116">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="5b8c1-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5b8c1-117">sim</span><span class="sxs-lookup"><span data-stu-id="5b8c1-117">yes</span></span>       |



 

<span data-ttu-id="5b8c1-118">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="5b8c1-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5b8c1-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="5b8c1-119">Vertex</span></span> | <span data-ttu-id="5b8c1-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="5b8c1-120">Hull</span></span> | <span data-ttu-id="5b8c1-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="5b8c1-121">Domain</span></span> | <span data-ttu-id="5b8c1-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="5b8c1-122">Geometry</span></span> | <span data-ttu-id="5b8c1-123">16x16</span><span class="sxs-lookup"><span data-stu-id="5b8c1-123">Pixel</span></span> | <span data-ttu-id="5b8c1-124">Computação</span><span class="sxs-lookup"><span data-stu-id="5b8c1-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="5b8c1-125">x</span><span class="sxs-lookup"><span data-stu-id="5b8c1-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5b8c1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b8c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8c1-127">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="5b8c1-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="5b8c1-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5b8c1-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




