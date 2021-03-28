---
title: 'Função ByteAddressBuffer:: Load2 (uint, uint)'
description: Obtém dois valores e o status da operação.
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
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
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007934"
---
# <a name="load2uint-uint-function"></a><span data-ttu-id="cf183-104">Função Load2 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="cf183-104">Load2(uint, uint) function</span></span>

<span data-ttu-id="cf183-105">Obtém dois valores e o status da operação.</span><span class="sxs-lookup"><span data-stu-id="cf183-105">Gets two values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf183-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf183-106">Syntax</span></span>

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="cf183-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf183-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf183-108">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cf183-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf183-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cf183-109">Type: **uint**</span></span>

<span data-ttu-id="cf183-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="cf183-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="cf183-111">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="cf183-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf183-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cf183-112">Type: **uint**</span></span>

<span data-ttu-id="cf183-113">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="cf183-113">The status of the operation.</span></span> <span data-ttu-id="cf183-114">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="cf183-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cf183-115">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="cf183-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cf183-116">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="cf183-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf183-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf183-117">Return value</span></span>

<span data-ttu-id="cf183-118">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="cf183-118">Type: **uint2**</span></span>

<span data-ttu-id="cf183-119">Dois valores.</span><span class="sxs-lookup"><span data-stu-id="cf183-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf183-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf183-120">Remarks</span></span>

<span data-ttu-id="cf183-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="cf183-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cf183-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="cf183-122">Vertex</span></span> | <span data-ttu-id="cf183-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="cf183-123">Hull</span></span> | <span data-ttu-id="cf183-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="cf183-124">Domain</span></span> | <span data-ttu-id="cf183-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="cf183-125">Geometry</span></span> | <span data-ttu-id="cf183-126">16x16</span><span class="sxs-lookup"><span data-stu-id="cf183-126">Pixel</span></span> | <span data-ttu-id="cf183-127">Computação</span><span class="sxs-lookup"><span data-stu-id="cf183-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cf183-128">x</span><span class="sxs-lookup"><span data-stu-id="cf183-128">x</span></span>      | <span data-ttu-id="cf183-129">x</span><span class="sxs-lookup"><span data-stu-id="cf183-129">x</span></span>    | <span data-ttu-id="cf183-130">x</span><span class="sxs-lookup"><span data-stu-id="cf183-130">x</span></span>      | <span data-ttu-id="cf183-131">x</span><span class="sxs-lookup"><span data-stu-id="cf183-131">x</span></span>        | <span data-ttu-id="cf183-132">x</span><span class="sxs-lookup"><span data-stu-id="cf183-132">x</span></span>     | <span data-ttu-id="cf183-133">x</span><span class="sxs-lookup"><span data-stu-id="cf183-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cf183-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf183-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf183-135">Métodos Load2</span><span class="sxs-lookup"><span data-stu-id="cf183-135">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="cf183-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="cf183-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 