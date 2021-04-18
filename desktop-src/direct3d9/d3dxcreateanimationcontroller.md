---
description: Cria um objeto de controlador de animação.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Função D3DXCreateAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763006"
---
# <a name="d3dxcreateanimationcontroller-function"></a><span data-ttu-id="6bac3-103">Função D3DXCreateAnimationController</span><span class="sxs-lookup"><span data-stu-id="6bac3-103">D3DXCreateAnimationController function</span></span>

<span data-ttu-id="6bac3-104">Cria um objeto de controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="6bac3-104">Creates an animation controller object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bac3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bac3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="6bac3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bac3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bac3-107">*MaxNumAnimationOutputs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bac3-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bac3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bac3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bac3-109">Número máximo de saídas de animação às quais o controlador pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="6bac3-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="6bac3-110">*MaxNumAnimationSets* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bac3-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bac3-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bac3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bac3-112">Número máximo de conjuntos de animação que podem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="6bac3-112">Maximum number of animation sets that can be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="6bac3-113">*MaxNumTracks* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bac3-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bac3-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bac3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bac3-115">Número máximo de conjuntos de animação que podem ser misturados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="6bac3-115">Maximum number of animation sets that can be mixed simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="6bac3-116">*MaxNumEvents* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bac3-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bac3-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bac3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bac3-118">Número máximo de eventos pendentes aos quais o controlador dará suporte.</span><span class="sxs-lookup"><span data-stu-id="6bac3-118">Maximum number of outstanding events that the controller will support.</span></span>

</dd> <dt>

<span data-ttu-id="6bac3-119">*ppAnimController* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6bac3-119">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bac3-120">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="6bac3-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="6bac3-121">Ponteiro para o objeto do controlador de animação criado.</span><span class="sxs-lookup"><span data-stu-id="6bac3-121">Pointer to the animation controller object created.</span></span> <span data-ttu-id="6bac3-122">Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="6bac3-122">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bac3-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6bac3-123">Return value</span></span>

<span data-ttu-id="6bac3-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6bac3-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6bac3-125">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6bac3-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6bac3-126">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6bac3-126">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bac3-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bac3-127">Remarks</span></span>

<span data-ttu-id="6bac3-128">Um controlador de animação controla um mixer de animação.</span><span class="sxs-lookup"><span data-stu-id="6bac3-128">An animation controller controls an animation mixer.</span></span> <span data-ttu-id="6bac3-129">O controlador adiciona métodos para modificar parâmetros de mesclagem ao longo do tempo para habilitar transições suaves.</span><span class="sxs-lookup"><span data-stu-id="6bac3-129">The controller adds methods to modify blending parameters over time to enable smooth transitions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bac3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bac3-130">Requirements</span></span>



| <span data-ttu-id="6bac3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bac3-131">Requirement</span></span> | <span data-ttu-id="6bac3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="6bac3-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bac3-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bac3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6bac3-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bac3-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6bac3-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bac3-135">Library</span></span><br/> | <dl> <span data-ttu-id="6bac3-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bac3-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6bac3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bac3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bac3-138">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="6bac3-138">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
