---
title: Função AllMemoryBarrier
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória tenham sido concluídos.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- HLSL da função AllMemoryBarrier
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365015"
---
# <a name="allmemorybarrier-function"></a><span data-ttu-id="08047-104">Função AllMemoryBarrier</span><span class="sxs-lookup"><span data-stu-id="08047-104">AllMemoryBarrier function</span></span>

<span data-ttu-id="08047-105">Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória tenham sido concluídos.</span><span class="sxs-lookup"><span data-stu-id="08047-105">Blocks execution of all threads in a group until all memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="08047-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08047-106">Syntax</span></span>

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="08047-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08047-107">Parameters</span></span>

<span data-ttu-id="08047-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="08047-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08047-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08047-109">Return value</span></span>

<span data-ttu-id="08047-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="08047-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08047-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="08047-111">Remarks</span></span>

<span data-ttu-id="08047-112">Uma barreira de memória garante que as operações de memória pendentes tenham sido concluídas.</span><span class="sxs-lookup"><span data-stu-id="08047-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="08047-113">Os threads são sincronizados em barreiras de GroupSync.</span><span class="sxs-lookup"><span data-stu-id="08047-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="08047-114">Isso pode paralisar um thread ou threads se as operações de memória estiverem em andamento.</span><span class="sxs-lookup"><span data-stu-id="08047-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="08047-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="08047-115">Minimum Shader Model</span></span>

<span data-ttu-id="08047-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="08047-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="08047-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="08047-117">Shader Model</span></span>                                                                | <span data-ttu-id="08047-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="08047-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="08047-119">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="08047-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="08047-120">sim</span><span class="sxs-lookup"><span data-stu-id="08047-120">yes</span></span>       |



 

<span data-ttu-id="08047-121">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="08047-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="08047-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="08047-122">Vertex</span></span> | <span data-ttu-id="08047-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="08047-123">Hull</span></span> | <span data-ttu-id="08047-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="08047-124">Domain</span></span> | <span data-ttu-id="08047-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="08047-125">Geometry</span></span> | <span data-ttu-id="08047-126">16x16</span><span class="sxs-lookup"><span data-stu-id="08047-126">Pixel</span></span> | <span data-ttu-id="08047-127">Computação</span><span class="sxs-lookup"><span data-stu-id="08047-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="08047-128">x</span><span class="sxs-lookup"><span data-stu-id="08047-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="08047-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="08047-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08047-130">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="08047-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="08047-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="08047-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




