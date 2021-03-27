---
title: 'Função RWByteAddressBuffer:: Load2 (uint, uint)'
description: Obtém dois valores e retorna o status da operação.
ms.assetid: E6BBA8A7-D53F-4718-B007-EBDE50FADB06
keywords:
- HLSL da função Load2
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92fc492fddb6ad024a4507829e81dab4886af590
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084551"
---
# <a name="load2uintuint-function"></a><span data-ttu-id="b545b-104">Função Load2 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="b545b-104">Load2(uint,uint) function</span></span>

<span data-ttu-id="b545b-105">Obtém dois valores e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="b545b-105">Gets two values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b545b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b545b-106">Syntax</span></span>


``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="b545b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b545b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b545b-108">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b545b-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b545b-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b545b-109">Type: **uint**</span></span>

<span data-ttu-id="b545b-110">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="b545b-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b545b-111">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b545b-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b545b-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b545b-112">Type: **uint**</span></span>

<span data-ttu-id="b545b-113">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="b545b-113">The status of the operation.</span></span> <span data-ttu-id="b545b-114">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b545b-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b545b-115">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b545b-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b545b-116">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="b545b-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b545b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b545b-117">Return value</span></span>

<span data-ttu-id="b545b-118">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="b545b-118">Type: **uint2**</span></span>

<span data-ttu-id="b545b-119">Dois valores.</span><span class="sxs-lookup"><span data-stu-id="b545b-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b545b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b545b-120">Remarks</span></span>

<span data-ttu-id="b545b-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b545b-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b545b-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="b545b-122">Vertex</span></span> | <span data-ttu-id="b545b-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b545b-123">Hull</span></span> | <span data-ttu-id="b545b-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="b545b-124">Domain</span></span> | <span data-ttu-id="b545b-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="b545b-125">Geometry</span></span> | <span data-ttu-id="b545b-126">16x16</span><span class="sxs-lookup"><span data-stu-id="b545b-126">Pixel</span></span> | <span data-ttu-id="b545b-127">Computação</span><span class="sxs-lookup"><span data-stu-id="b545b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b545b-128">x</span><span class="sxs-lookup"><span data-stu-id="b545b-128">x</span></span>     | <span data-ttu-id="b545b-129">x</span><span class="sxs-lookup"><span data-stu-id="b545b-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b545b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b545b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b545b-131">Métodos Load2</span><span class="sxs-lookup"><span data-stu-id="b545b-131">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> </dl>

 

 