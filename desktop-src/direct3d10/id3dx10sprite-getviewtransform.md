---
description: Obter a transformação de exibição que se aplica a todos os sprites.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'Método ID3DX10Sprite:: GetViewTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761618"
---
# <a name="id3dx10spritegetviewtransform-method"></a><span data-ttu-id="ddab5-103">Método ID3DX10Sprite:: GetViewTransform</span><span class="sxs-lookup"><span data-stu-id="ddab5-103">ID3DX10Sprite::GetViewTransform method</span></span>

<span data-ttu-id="ddab5-104">Obter a transformação de exibição que se aplica a todos os sprites.</span><span class="sxs-lookup"><span data-stu-id="ddab5-104">Get the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddab5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddab5-105">Syntax</span></span>


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="ddab5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddab5-107">*pViewTransform* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ddab5-107">*pViewTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddab5-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddab5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ddab5-109">Ponteiro para um [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) que será definido como a transformação do sprite do espaço do mundo original.</span><span class="sxs-lookup"><span data-stu-id="ddab5-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddab5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ddab5-110">Return value</span></span>

<span data-ttu-id="ddab5-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddab5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddab5-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ddab5-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ddab5-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ddab5-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddab5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddab5-114">Requirements</span></span>



| <span data-ttu-id="ddab5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddab5-115">Requirement</span></span> | <span data-ttu-id="ddab5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ddab5-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddab5-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ddab5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ddab5-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddab5-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddab5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddab5-119">Library</span></span><br/> | <dl> <span data-ttu-id="ddab5-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddab5-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddab5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddab5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddab5-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="ddab5-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="ddab5-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ddab5-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
