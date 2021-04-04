---
description: Remove os dados de escala no quadro de chave especificado.
ms.assetid: b0bf5665-ccfb-4b87-8e88-9a717ef57955
title: 'Método ID3DXKeyframedAnimationSet:: UnregisterScaleKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d1ac3f500b80d8922646fddff9f05d8c91d9c48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930734"
---
# <a name="id3dxkeyframedanimationsetunregisterscalekey-method"></a><span data-ttu-id="d2a33-103">Método ID3DXKeyframedAnimationSet:: UnregisterScaleKey</span><span class="sxs-lookup"><span data-stu-id="d2a33-103">ID3DXKeyframedAnimationSet::UnregisterScaleKey method</span></span>

<span data-ttu-id="d2a33-104">Remove os dados de escala no quadro de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="d2a33-104">Removes the scale data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a33-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2a33-105">Syntax</span></span>


```C++
HRESULT UnregisterScaleKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="d2a33-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2a33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a33-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2a33-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a33-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2a33-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2a33-109">Identificador de animação.</span><span class="sxs-lookup"><span data-stu-id="d2a33-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2a33-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2a33-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a33-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2a33-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2a33-112">Quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="d2a33-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a33-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2a33-113">Return value</span></span>

<span data-ttu-id="d2a33-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2a33-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2a33-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2a33-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d2a33-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d2a33-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a33-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2a33-117">Remarks</span></span>

<span data-ttu-id="d2a33-118">Esse método é lento e não deve ser usado depois que uma animação começou a ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="d2a33-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a33-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2a33-119">Requirements</span></span>



| <span data-ttu-id="d2a33-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a33-120">Requirement</span></span> | <span data-ttu-id="d2a33-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d2a33-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a33-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2a33-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d2a33-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a33-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d2a33-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2a33-124">Library</span></span><br/> | <dl> <span data-ttu-id="d2a33-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2a33-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2a33-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2a33-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a33-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d2a33-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
