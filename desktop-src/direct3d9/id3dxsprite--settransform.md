---
description: Define a transformação Sprite.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'Método ID3DXSprite:: SetTransform (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173065"
---
# <a name="id3dxspritesettransform-method"></a><span data-ttu-id="a503f-103">Método ID3DXSprite:: SetTransform</span><span class="sxs-lookup"><span data-stu-id="a503f-103">ID3DXSprite::SetTransform method</span></span>

<span data-ttu-id="a503f-104">Define a transformação Sprite.</span><span class="sxs-lookup"><span data-stu-id="a503f-104">Sets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="a503f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a503f-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="a503f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a503f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a503f-107">*pTransform* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a503f-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a503f-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a503f-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a503f-109">Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação do sprite do espaço do mundo original.</span><span class="sxs-lookup"><span data-stu-id="a503f-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="a503f-110">Use essa transformação para dimensionar, girar ou transformar o sprite.</span><span class="sxs-lookup"><span data-stu-id="a503f-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a503f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a503f-111">Return value</span></span>

<span data-ttu-id="a503f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a503f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a503f-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a503f-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a503f-114">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="a503f-114">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="a503f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a503f-115">Requirements</span></span>



| <span data-ttu-id="a503f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a503f-116">Requirement</span></span> | <span data-ttu-id="a503f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a503f-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a503f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a503f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a503f-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a503f-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a503f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a503f-120">Library</span></span><br/> | <dl> <span data-ttu-id="a503f-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a503f-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a503f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a503f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a503f-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="a503f-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="a503f-124">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a503f-124">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




