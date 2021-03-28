---
title: função Abort (Corecrt \_ encerrar. h)
description: Envia uma mensagem de erro para a fila de informações e encerra a chamada de emissão ou expedição atual que está sendo executada.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- anular função HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968712"
---
# <a name="abort-function"></a><span data-ttu-id="a845b-104">Função abort</span><span class="sxs-lookup"><span data-stu-id="a845b-104">abort function</span></span>

<span data-ttu-id="a845b-105">Envia uma mensagem de erro para a fila de informações e encerra a chamada de emissão ou expedição atual que está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="a845b-105">Submits an error message to the information queue and terminates the current draw or dispatch call being executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a845b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a845b-106">Syntax</span></span>

``` syntax
void abort(
    
);
```

## <a name="parameters"></a><span data-ttu-id="a845b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a845b-107">Parameters</span></span>

<dl> <dt>

 
</dt> <dd>

<span data-ttu-id="a845b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a845b-108">None</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a845b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a845b-109">Return value</span></span>

<span data-ttu-id="a845b-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a845b-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a845b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a845b-111">Remarks</span></span>

<span data-ttu-id="a845b-112">Esta operação não faz nada em rasterizadores que não dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="a845b-112">This operation does nothing on rasterizers that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="a845b-113">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a845b-113">Minimum Shader Model</span></span>

<span data-ttu-id="a845b-114">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a845b-114">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a845b-115">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a845b-115">Shader Model</span></span>                                                        | <span data-ttu-id="a845b-116">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a845b-116">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="a845b-117">Shader Model 4 (DirectX HLSL) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a845b-117">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a845b-118">sim</span><span class="sxs-lookup"><span data-stu-id="a845b-118">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="a845b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a845b-119">Requirements</span></span>



| <span data-ttu-id="a845b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a845b-120">Requirement</span></span> | <span data-ttu-id="a845b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a845b-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a845b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a845b-122">Header</span></span><br/> | <dl> <span data-ttu-id="a845b-123"><dt>Corecrt \_ encerrar. h</dt></span><span class="sxs-lookup"><span data-stu-id="a845b-123"><dt>Corecrt\_terminate.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a845b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a845b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a845b-125">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="a845b-125">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





