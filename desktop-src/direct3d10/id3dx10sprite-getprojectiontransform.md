---
description: Obtenha a matriz de projeção Sprite que é aplicada a todos os sprites.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'Método ID3DX10Sprite:: GetProjectionTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664116"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a><span data-ttu-id="235b6-103">Método ID3DX10Sprite:: GetProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="235b6-103">ID3DX10Sprite::GetProjectionTransform method</span></span>

<span data-ttu-id="235b6-104">Obtenha a matriz de projeção Sprite que é aplicada a todos os sprites.</span><span class="sxs-lookup"><span data-stu-id="235b6-104">Get the sprite projection matrix that is applied to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="235b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="235b6-105">Syntax</span></span>


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="235b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="235b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235b6-107">*pProjectionTransform* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="235b6-107">*pProjectionTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="235b6-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="235b6-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="235b6-109">Ponteiro para um [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) que será definido como a matriz de projeção do Sprite.</span><span class="sxs-lookup"><span data-stu-id="235b6-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the sprite's projection matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235b6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="235b6-110">Return value</span></span>

<span data-ttu-id="235b6-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="235b6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="235b6-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="235b6-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="235b6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="235b6-113">Requirements</span></span>



| <span data-ttu-id="235b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="235b6-114">Requirement</span></span> | <span data-ttu-id="235b6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="235b6-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="235b6-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="235b6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="235b6-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="235b6-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="235b6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="235b6-118">Library</span></span><br/> | <dl> <span data-ttu-id="235b6-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="235b6-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235b6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="235b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235b6-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="235b6-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="235b6-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="235b6-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
