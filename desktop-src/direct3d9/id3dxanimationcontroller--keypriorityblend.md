---
description: Define as chaves de evento de mesclagem para a faixa de animação especificada.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'Método ID3DXAnimationController:: KeyPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298501"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a><span data-ttu-id="47555-103">Método ID3DXAnimationController:: KeyPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="47555-103">ID3DXAnimationController::KeyPriorityBlend method</span></span>

<span data-ttu-id="47555-104">Define as chaves de evento de mesclagem para a faixa de animação especificada.</span><span class="sxs-lookup"><span data-stu-id="47555-104">Sets blending event keys for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="47555-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47555-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="47555-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47555-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47555-107">*NewBlendWeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47555-107">*NewBlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47555-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47555-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47555-109">Número entre 0 e 1 que é usado para mesclar faixas.</span><span class="sxs-lookup"><span data-stu-id="47555-109">Number between 0 and 1 that is used to blend tracks together.</span></span>

</dd> <dt>

<span data-ttu-id="47555-110">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47555-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47555-111">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47555-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47555-112">Tempo global para iniciar o Blend.</span><span class="sxs-lookup"><span data-stu-id="47555-112">Global time to start the blend.</span></span>

</dd> <dt>

<span data-ttu-id="47555-113">*Duração* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47555-113">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47555-114">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47555-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47555-115">Duração de tempo global do Blend.</span><span class="sxs-lookup"><span data-stu-id="47555-115">Global time duration of the blend.</span></span>

</dd> <dt>

<span data-ttu-id="47555-116">*Transição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47555-116">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47555-117">Tipo: **[ **\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="47555-117">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="47555-118">Especifica o tipo de transição usado para a duração do Blend.</span><span class="sxs-lookup"><span data-stu-id="47555-118">Specifies the transition type used for the duration of the blend.</span></span> <span data-ttu-id="47555-119">Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="47555-119">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47555-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47555-120">Return value</span></span>

<span data-ttu-id="47555-121">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="47555-121">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="47555-122">Identificador de evento para o evento de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="47555-122">Event handle to the priority blend event.</span></span> <span data-ttu-id="47555-123">**NULL** será retornado se um ou mais dos parâmetros de entrada forem inválidos ou se nenhum evento gratuito estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="47555-123">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="47555-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="47555-124">Remarks</span></span>

<span data-ttu-id="47555-125">O controlador de animação combina em três fases: as faixas de baixa prioridade são mescladas primeiro, as faixas de alta prioridade são mescladas segundo e, em seguida, os resultados de ambos são misturados.</span><span class="sxs-lookup"><span data-stu-id="47555-125">The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.</span></span>

## <a name="requirements"></a><span data-ttu-id="47555-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47555-126">Requirements</span></span>



| <span data-ttu-id="47555-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="47555-127">Requirement</span></span> | <span data-ttu-id="47555-128">Valor</span><span class="sxs-lookup"><span data-stu-id="47555-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47555-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47555-129">Header</span></span><br/>  | <dl> <span data-ttu-id="47555-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="47555-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="47555-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47555-131">Library</span></span><br/> | <dl> <span data-ttu-id="47555-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47555-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47555-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="47555-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47555-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="47555-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="47555-135">**SetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="47555-135">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
