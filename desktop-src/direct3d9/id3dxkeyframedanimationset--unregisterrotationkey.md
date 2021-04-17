---
description: Remove os dados de rotação no quadro de chave especificado.
ms.assetid: 8e95d684-fa22-4eba-a721-e7551e8f393b
title: 'Método ID3DXKeyframedAnimationSet:: UnregisterRotationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 420a15d0086f94def7db8c7d558640d03b69562f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798280"
---
# <a name="id3dxkeyframedanimationsetunregisterrotationkey-method"></a><span data-ttu-id="a0dac-103">Método ID3DXKeyframedAnimationSet:: UnregisterRotationKey</span><span class="sxs-lookup"><span data-stu-id="a0dac-103">ID3DXKeyframedAnimationSet::UnregisterRotationKey method</span></span>

<span data-ttu-id="a0dac-104">Remove os dados de rotação no quadro de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="a0dac-104">Removes the rotation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0dac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0dac-105">Syntax</span></span>


```C++
HRESULT UnregisterRotationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="a0dac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0dac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0dac-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0dac-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0dac-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0dac-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0dac-109">Identificador de animação.</span><span class="sxs-lookup"><span data-stu-id="a0dac-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a0dac-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0dac-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0dac-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0dac-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0dac-112">Quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="a0dac-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0dac-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0dac-113">Return value</span></span>

<span data-ttu-id="a0dac-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0dac-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0dac-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0dac-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a0dac-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a0dac-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0dac-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0dac-117">Remarks</span></span>

<span data-ttu-id="a0dac-118">Esse método é lento e não deve ser usado depois que uma animação começou a ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="a0dac-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0dac-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0dac-119">Requirements</span></span>



| <span data-ttu-id="a0dac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0dac-120">Requirement</span></span> | <span data-ttu-id="a0dac-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a0dac-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dac-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0dac-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a0dac-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0dac-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a0dac-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0dac-124">Library</span></span><br/> | <dl> <span data-ttu-id="a0dac-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0dac-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0dac-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0dac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0dac-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a0dac-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
