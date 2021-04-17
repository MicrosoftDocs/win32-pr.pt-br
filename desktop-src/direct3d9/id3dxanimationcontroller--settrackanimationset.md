---
description: Aplica a animação definida à faixa especificada.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'Método ID3DXAnimationController:: SetTrackAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762479"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a><span data-ttu-id="43060-103">Método ID3DXAnimationController:: SetTrackAnimationSet</span><span class="sxs-lookup"><span data-stu-id="43060-103">ID3DXAnimationController::SetTrackAnimationSet method</span></span>

<span data-ttu-id="43060-104">Aplica a animação definida à faixa especificada.</span><span class="sxs-lookup"><span data-stu-id="43060-104">Applies the animation set to the specified track.</span></span>

## <a name="syntax"></a><span data-ttu-id="43060-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43060-105">Syntax</span></span>


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="43060-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43060-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43060-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43060-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43060-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43060-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43060-109">Identificador da faixa à qual o conjunto de animações é aplicado.</span><span class="sxs-lookup"><span data-stu-id="43060-109">Identifier of the track to which the animation set is applied.</span></span>

</dd> <dt>

<span data-ttu-id="43060-110">*pAnimSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43060-110">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43060-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="43060-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="43060-112">Ponteiro para o conjunto de animação [**ID3DXAnimationSet**](id3dxanimationset.md) a ser adicionado à faixa.</span><span class="sxs-lookup"><span data-stu-id="43060-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to be added to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43060-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43060-113">Return value</span></span>

<span data-ttu-id="43060-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43060-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43060-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43060-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="43060-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="43060-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="43060-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="43060-117">Remarks</span></span>

<span data-ttu-id="43060-118">Esse método define a animação definida como a faixa especificada para a combinação.</span><span class="sxs-lookup"><span data-stu-id="43060-118">This method sets the animation set to the specified track for mixing.</span></span> <span data-ttu-id="43060-119">O conjunto de animações para cada faixa é mesclado de acordo com o peso e a velocidade da faixa quando o [**adiantamento**](id3dxanimationcontroller--advancetime.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="43060-119">The animation set for each track is blended according to the track weight and speed when [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="43060-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43060-120">Requirements</span></span>



| <span data-ttu-id="43060-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43060-121">Requirement</span></span> | <span data-ttu-id="43060-122">Valor</span><span class="sxs-lookup"><span data-stu-id="43060-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43060-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43060-123">Header</span></span><br/>  | <dl> <span data-ttu-id="43060-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="43060-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="43060-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43060-125">Library</span></span><br/> | <dl> <span data-ttu-id="43060-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43060-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43060-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="43060-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43060-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="43060-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
