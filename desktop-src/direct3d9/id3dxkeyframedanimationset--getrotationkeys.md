---
description: Preenche uma matriz com dados de chave de rotação usados para animação de quadro chave.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'Método ID3DXKeyframedAnimationSet:: GetRotationKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664092"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a><span data-ttu-id="cd6d5-103">Método ID3DXKeyframedAnimationSet:: GetRotationKeys</span><span class="sxs-lookup"><span data-stu-id="cd6d5-103">ID3DXKeyframedAnimationSet::GetRotationKeys method</span></span>

<span data-ttu-id="cd6d5-104">Preenche uma matriz com dados de chave de rotação usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="cd6d5-104">Fills an array with rotational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd6d5-105">Syntax</span></span>


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="cd6d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd6d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6d5-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6d5-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6d5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd6d5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd6d5-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="cd6d5-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d5-110">*pRotationKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd6d5-110">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6d5-111">Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="cd6d5-111">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="cd6d5-112">Ponteiro para uma matriz alocada pelo usuário de quaternions [**D3DXKEY do \_ Quaternion**](d3dxkey-quaternion.md) que o método deve preencher com dados de rotação de animação.</span><span class="sxs-lookup"><span data-stu-id="cd6d5-112">Pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method is to fill with animation rotation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd6d5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd6d5-113">Return value</span></span>

<span data-ttu-id="cd6d5-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd6d5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd6d5-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd6d5-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cd6d5-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cd6d5-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd6d5-117">Requirements</span></span>



| <span data-ttu-id="cd6d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd6d5-118">Requirement</span></span> | <span data-ttu-id="cd6d5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cd6d5-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6d5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd6d5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cd6d5-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd6d5-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cd6d5-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd6d5-122">Library</span></span><br/> | <dl> <span data-ttu-id="cd6d5-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd6d5-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd6d5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd6d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6d5-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="cd6d5-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="cd6d5-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="cd6d5-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
