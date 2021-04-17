---
description: Define o peso de mesclagem de prioridade para a faixa de animação especificada.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'Método ID3DXAnimationController:: SetTrackPriority (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798016"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a><span data-ttu-id="11067-103">Método ID3DXAnimationController:: SetTrackPriority</span><span class="sxs-lookup"><span data-stu-id="11067-103">ID3DXAnimationController::SetTrackPriority method</span></span>

<span data-ttu-id="11067-104">Define o peso de mesclagem de prioridade para a faixa de animação especificada.</span><span class="sxs-lookup"><span data-stu-id="11067-104">Sets the priority blending weight for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="11067-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11067-105">Syntax</span></span>


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a><span data-ttu-id="11067-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11067-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11067-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11067-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11067-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11067-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11067-109">Identificador de faixa.</span><span class="sxs-lookup"><span data-stu-id="11067-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="11067-110">*Prioridade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="11067-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11067-111">Tipo: **[ **\_ tipo de D3DXPRIORITY**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="11067-111">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

<span data-ttu-id="11067-112">Controlar prioridade.</span><span class="sxs-lookup"><span data-stu-id="11067-112">Track priority.</span></span> <span data-ttu-id="11067-113">Esse parâmetro deve ser definido como uma das constantes do [**\_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="11067-113">This parameter should be set to one of the constants from [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11067-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11067-114">Return value</span></span>

<span data-ttu-id="11067-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11067-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11067-116">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11067-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="11067-117">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="11067-117">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="11067-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="11067-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="11067-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11067-119">Requirements</span></span>



| <span data-ttu-id="11067-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="11067-120">Requirement</span></span> | <span data-ttu-id="11067-121">Valor</span><span class="sxs-lookup"><span data-stu-id="11067-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11067-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11067-122">Header</span></span><br/>  | <dl> <span data-ttu-id="11067-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="11067-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="11067-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11067-124">Library</span></span><br/> | <dl> <span data-ttu-id="11067-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11067-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11067-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="11067-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11067-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="11067-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
