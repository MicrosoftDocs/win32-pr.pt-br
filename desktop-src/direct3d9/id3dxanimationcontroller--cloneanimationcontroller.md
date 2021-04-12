---
description: Clones, ou cópias, um controlador de animação.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'Método ID3DXAnimationController:: CloneAnimationController (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298809"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a><span data-ttu-id="16b4f-103">Método ID3DXAnimationController:: CloneAnimationController</span><span class="sxs-lookup"><span data-stu-id="16b4f-103">ID3DXAnimationController::CloneAnimationController method</span></span>

<span data-ttu-id="16b4f-104">Clones, ou cópias, um controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="16b4f-104">Clones, or copies, an animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16b4f-105">Syntax</span></span>


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="16b4f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16b4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b4f-107">*MaxNumAnimationOutputs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b4f-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b4f-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b4f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b4f-109">Número máximo de saídas de animação às quais o controlador pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="16b4f-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="16b4f-110">*MaxNumAnimationSets* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b4f-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b4f-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b4f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b4f-112">Número máximo de conjuntos de animação aos quais o controlador pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="16b4f-112">Maximum number of animation sets the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="16b4f-113">*MaxNumTracks* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b4f-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b4f-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b4f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b4f-115">Número máximo de faixas às quais o controlador pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="16b4f-115">Maximum number of tracks the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="16b4f-116">*MaxNumEvents* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b4f-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b4f-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b4f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b4f-118">Número máximo de eventos aos quais o controlador pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="16b4f-118">Maximum number of events the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="16b4f-119">*ppAnimController* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16b4f-119">*ppAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b4f-120">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="16b4f-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="16b4f-121">Endereço de um ponteiro para o controlador de animação [**ID3DXAnimationController**](id3dxanimationcontroller.md) clonado.</span><span class="sxs-lookup"><span data-stu-id="16b4f-121">Address of a pointer to the cloned [**ID3DXAnimationController**](id3dxanimationcontroller.md) animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b4f-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16b4f-122">Return value</span></span>

<span data-ttu-id="16b4f-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16b4f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16b4f-124">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16b4f-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="16b4f-125">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="16b4f-125">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b4f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b4f-126">Requirements</span></span>



| <span data-ttu-id="16b4f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b4f-127">Requirement</span></span> | <span data-ttu-id="16b4f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="16b4f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16b4f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16b4f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="16b4f-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b4f-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="16b4f-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16b4f-131">Library</span></span><br/> | <dl> <span data-ttu-id="16b4f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16b4f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16b4f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="16b4f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b4f-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="16b4f-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
