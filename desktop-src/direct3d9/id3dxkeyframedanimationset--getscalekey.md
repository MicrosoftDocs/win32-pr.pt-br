---
description: Obter informações de escala para um quadro-chave específico no conjunto de animações.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: 'Método ID3DXKeyframedAnimationSet:: GetScaleKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58cbd432404fcd511140a7368999161f5e44f77f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298794"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a><span data-ttu-id="d9803-103">Método ID3DXKeyframedAnimationSet:: GetScaleKey</span><span class="sxs-lookup"><span data-stu-id="d9803-103">ID3DXKeyframedAnimationSet::GetScaleKey method</span></span>

<span data-ttu-id="d9803-104">Obter informações de escala para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="d9803-104">Get scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9803-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9803-105">Syntax</span></span>


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="d9803-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9803-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9803-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9803-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9803-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9803-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9803-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="d9803-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="d9803-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9803-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9803-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9803-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9803-112">Quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d9803-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="d9803-113">*pScaleKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9803-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9803-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="d9803-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="d9803-115">Ponteiro para os dados de escala.</span><span class="sxs-lookup"><span data-stu-id="d9803-115">Pointer to the scale data.</span></span> <span data-ttu-id="d9803-116">Consulte [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="d9803-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9803-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9803-117">Return value</span></span>

<span data-ttu-id="d9803-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9803-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9803-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9803-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d9803-120">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d9803-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9803-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9803-121">Requirements</span></span>



| <span data-ttu-id="d9803-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9803-122">Requirement</span></span> | <span data-ttu-id="d9803-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d9803-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9803-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9803-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d9803-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9803-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d9803-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9803-126">Library</span></span><br/> | <dl> <span data-ttu-id="d9803-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9803-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9803-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9803-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9803-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d9803-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
