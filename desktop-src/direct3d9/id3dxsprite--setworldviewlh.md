---
description: Define a transformação de exibição Mundial da mão esquerda para um Sprite. Uma chamada para esse método é necessária antes de obter ou classificar sprites.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'Método ID3DXSprite:: SetWorldViewLH (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173064"
---
# <a name="id3dxspritesetworldviewlh-method"></a><span data-ttu-id="29048-104">Método ID3DXSprite:: SetWorldViewLH</span><span class="sxs-lookup"><span data-stu-id="29048-104">ID3DXSprite::SetWorldViewLH method</span></span>

<span data-ttu-id="29048-105">Define a transformação de exibição Mundial da mão esquerda para um Sprite.</span><span class="sxs-lookup"><span data-stu-id="29048-105">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="29048-106">Uma chamada para esse método é necessária antes de obter ou classificar sprites.</span><span class="sxs-lookup"><span data-stu-id="29048-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="29048-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29048-107">Syntax</span></span>


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="29048-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29048-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29048-109">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29048-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29048-110">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="29048-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="29048-111">Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação do mundo.</span><span class="sxs-lookup"><span data-stu-id="29048-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="29048-112">Se for **NULL**, a matriz de identidade será usada para a transformação mundial.</span><span class="sxs-lookup"><span data-stu-id="29048-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="29048-113">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29048-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29048-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="29048-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="29048-115">Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="29048-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="29048-116">Se for **NULL**, a matriz de identidade será usada para a transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="29048-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29048-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29048-117">Return value</span></span>

<span data-ttu-id="29048-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29048-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29048-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29048-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="29048-120">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="29048-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="29048-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="29048-121">Remarks</span></span>

<span data-ttu-id="29048-122">Uma chamada para esse método (ou para [**ID3DXSprite:: SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) será necessária se o sprite for renderizado com o [D3DXSprite \_ \_ mural](d3dxsprite.md), D3DXSprite \_ \_ classificar \_ profundidade \_ FRONTTOBACK ou D3DXSprite \_ \_ \_ \_ valor do sinalizador BACKTOFRONT de profundidade de classificação em [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="29048-122">A call to this method (or to [**ID3DXSprite::SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29048-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29048-123">Requirements</span></span>



| <span data-ttu-id="29048-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="29048-124">Requirement</span></span> | <span data-ttu-id="29048-125">Valor</span><span class="sxs-lookup"><span data-stu-id="29048-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29048-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29048-126">Header</span></span><br/>  | <dl> <span data-ttu-id="29048-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="29048-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="29048-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29048-128">Library</span></span><br/> | <dl> <span data-ttu-id="29048-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29048-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29048-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="29048-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29048-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="29048-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




