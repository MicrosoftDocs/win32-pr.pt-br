---
description: Obtém os valores de escala, rotação e translação do conjunto de animações.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'Método ID3DXAnimationSet:: GetSRT (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793388"
---
# <a name="id3dxanimationsetgetsrt-method"></a><span data-ttu-id="693e9-103">Método ID3DXAnimationSet:: GetSRT</span><span class="sxs-lookup"><span data-stu-id="693e9-103">ID3DXAnimationSet::GetSRT method</span></span>

<span data-ttu-id="693e9-104">Obtém os valores de escala, rotação e translação do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="693e9-104">Gets the scale, rotation, and translation values of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="693e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="693e9-105">Syntax</span></span>


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="693e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="693e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="693e9-107">*PeriodicPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="693e9-107">*PeriodicPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="693e9-108">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="693e9-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="693e9-109">Posição do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="693e9-109">Position of the animation set.</span></span> <span data-ttu-id="693e9-110">A posição pode ser obtida chamando [**ID3DXAnimationSet:: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span><span class="sxs-lookup"><span data-stu-id="693e9-110">The position can be obtained by calling [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span></span>

</dd> <dt>

<span data-ttu-id="693e9-111">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="693e9-111">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="693e9-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="693e9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="693e9-113">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="693e9-113">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="693e9-114">*pScale* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="693e9-114">*pScale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693e9-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="693e9-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="693e9-116">Ponteiro para o vetor [**D3DXVECTOR3**](d3dxvector3.md) que descreve a escala do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="693e9-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="693e9-117">*protação* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="693e9-117">*pRotation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693e9-118">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="693e9-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="693e9-119">Ponteiro para o quaternion [**D3DXQUATERNION**](d3dxquaternion.md) que descreve a rotação do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="693e9-119">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="693e9-120">*pTranslation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="693e9-120">*pTranslation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693e9-121">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="693e9-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="693e9-122">Ponteiro para o vetor [**D3DXVECTOR3**](d3dxvector3.md) que descreve a tradução do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="693e9-122">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="693e9-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="693e9-123">Return value</span></span>

<span data-ttu-id="693e9-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="693e9-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="693e9-125">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="693e9-125">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="693e9-126">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="693e9-126">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="693e9-127">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="693e9-127">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="693e9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="693e9-128">Requirements</span></span>



| <span data-ttu-id="693e9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="693e9-129">Requirement</span></span> | <span data-ttu-id="693e9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="693e9-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="693e9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="693e9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="693e9-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="693e9-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="693e9-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="693e9-133">Library</span></span><br/> | <dl> <span data-ttu-id="693e9-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="693e9-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="693e9-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="693e9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="693e9-136">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="693e9-136">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
