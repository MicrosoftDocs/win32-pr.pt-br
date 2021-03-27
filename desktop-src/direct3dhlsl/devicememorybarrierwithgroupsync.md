---
title: Função DeviceMemoryBarrierWithGroupSync
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória do dispositivo tenham sido concluídos e que todos os threads do grupo tenham atingido essa chamada.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- HLSL da função DeviceMemoryBarrierWithGroupSync
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293290"
---
# <a name="devicememorybarrierwithgroupsync-function"></a><span data-ttu-id="80d3a-104">Função DeviceMemoryBarrierWithGroupSync</span><span class="sxs-lookup"><span data-stu-id="80d3a-104">DeviceMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="80d3a-105">Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória do dispositivo tenham sido concluídos e que todos os threads do grupo tenham atingido essa chamada.</span><span class="sxs-lookup"><span data-stu-id="80d3a-105">Blocks execution of all threads in a group until all device memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d3a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80d3a-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="80d3a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80d3a-107">Parameters</span></span>

<span data-ttu-id="80d3a-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="80d3a-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80d3a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80d3a-109">Return value</span></span>

<span data-ttu-id="80d3a-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="80d3a-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80d3a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="80d3a-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="80d3a-112">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="80d3a-112">Minimum Shader Model</span></span>

<span data-ttu-id="80d3a-113">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="80d3a-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="80d3a-114">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="80d3a-114">Shader Model</span></span>                                                                | <span data-ttu-id="80d3a-115">Com suporte</span><span class="sxs-lookup"><span data-stu-id="80d3a-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="80d3a-116">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="80d3a-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="80d3a-117">sim</span><span class="sxs-lookup"><span data-stu-id="80d3a-117">yes</span></span>       |



 

<span data-ttu-id="80d3a-118">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="80d3a-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="80d3a-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="80d3a-119">Vertex</span></span> | <span data-ttu-id="80d3a-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="80d3a-120">Hull</span></span> | <span data-ttu-id="80d3a-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="80d3a-121">Domain</span></span> | <span data-ttu-id="80d3a-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="80d3a-122">Geometry</span></span> | <span data-ttu-id="80d3a-123">16x16</span><span class="sxs-lookup"><span data-stu-id="80d3a-123">Pixel</span></span> | <span data-ttu-id="80d3a-124">Computação</span><span class="sxs-lookup"><span data-stu-id="80d3a-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="80d3a-125">x</span><span class="sxs-lookup"><span data-stu-id="80d3a-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="80d3a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="80d3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d3a-127">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="80d3a-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="80d3a-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="80d3a-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




