---
title: Função DeviceMemoryBarrier
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória do dispositivo tenham sido concluídos.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- HLSL da função DeviceMemoryBarrier
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364551"
---
# <a name="devicememorybarrier-function"></a><span data-ttu-id="f4103-104">Função DeviceMemoryBarrier</span><span class="sxs-lookup"><span data-stu-id="f4103-104">DeviceMemoryBarrier function</span></span>

<span data-ttu-id="f4103-105">Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória do dispositivo tenham sido concluídos.</span><span class="sxs-lookup"><span data-stu-id="f4103-105">Blocks execution of all threads in a group until all device memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4103-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4103-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="f4103-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4103-107">Parameters</span></span>

<span data-ttu-id="f4103-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f4103-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4103-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4103-109">Return value</span></span>

<span data-ttu-id="f4103-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f4103-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4103-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4103-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="f4103-112">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f4103-112">Minimum Shader Model</span></span>

<span data-ttu-id="f4103-113">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f4103-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f4103-114">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f4103-114">Shader Model</span></span>                                                                | <span data-ttu-id="f4103-115">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f4103-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f4103-116">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="f4103-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f4103-117">sim</span><span class="sxs-lookup"><span data-stu-id="f4103-117">yes</span></span>       |



 

<span data-ttu-id="f4103-118">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f4103-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f4103-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="f4103-119">Vertex</span></span> | <span data-ttu-id="f4103-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f4103-120">Hull</span></span> | <span data-ttu-id="f4103-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="f4103-121">Domain</span></span> | <span data-ttu-id="f4103-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="f4103-122">Geometry</span></span> | <span data-ttu-id="f4103-123">16x16</span><span class="sxs-lookup"><span data-stu-id="f4103-123">Pixel</span></span> | <span data-ttu-id="f4103-124">Computação</span><span class="sxs-lookup"><span data-stu-id="f4103-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f4103-125">x</span><span class="sxs-lookup"><span data-stu-id="f4103-125">x</span></span>     | <span data-ttu-id="f4103-126">x</span><span class="sxs-lookup"><span data-stu-id="f4103-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f4103-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4103-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4103-128">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="f4103-128">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f4103-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f4103-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




