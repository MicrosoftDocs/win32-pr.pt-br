---
description: Define a transformação de exibição Mundial da mão direita para um Sprite. Uma chamada para esse método é necessária antes de obter ou classificar sprites.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'Método ID3DXSprite:: SetWorldViewRH (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765315"
---
# <a name="id3dxspritesetworldviewrh-method"></a><span data-ttu-id="c0da1-104">Método ID3DXSprite:: SetWorldViewRH</span><span class="sxs-lookup"><span data-stu-id="c0da1-104">ID3DXSprite::SetWorldViewRH method</span></span>

<span data-ttu-id="c0da1-105">Define a transformação de exibição Mundial da mão direita para um Sprite.</span><span class="sxs-lookup"><span data-stu-id="c0da1-105">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="c0da1-106">Uma chamada para esse método é necessária antes de obter ou classificar sprites.</span><span class="sxs-lookup"><span data-stu-id="c0da1-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0da1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0da1-107">Syntax</span></span>


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="c0da1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0da1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0da1-109">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0da1-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0da1-110">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0da1-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c0da1-111">Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação do mundo.</span><span class="sxs-lookup"><span data-stu-id="c0da1-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="c0da1-112">Se for **NULL**, a matriz de identidade será usada para a transformação mundial.</span><span class="sxs-lookup"><span data-stu-id="c0da1-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="c0da1-113">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0da1-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0da1-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0da1-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c0da1-115">Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="c0da1-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="c0da1-116">Se for **NULL**, a matriz de identidade será usada para a transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="c0da1-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0da1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0da1-117">Return value</span></span>

<span data-ttu-id="c0da1-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0da1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0da1-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0da1-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c0da1-120">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="c0da1-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c0da1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0da1-121">Remarks</span></span>

<span data-ttu-id="c0da1-122">Uma chamada para esse método (ou para [**ID3DXSprite:: SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) será necessária se o sprite for renderizado com o [D3DXSprite \_ \_ mural](d3dxsprite.md), D3DXSprite \_ \_ classificar \_ profundidade \_ FRONTTOBACK ou D3DXSprite \_ \_ \_ \_ valor do sinalizador BACKTOFRONT de profundidade de classificação em [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="c0da1-122">A call to this method (or to [**ID3DXSprite::SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0da1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0da1-123">Requirements</span></span>



| <span data-ttu-id="c0da1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0da1-124">Requirement</span></span> | <span data-ttu-id="c0da1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c0da1-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0da1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0da1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c0da1-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0da1-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c0da1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0da1-128">Library</span></span><br/> | <dl> <span data-ttu-id="c0da1-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0da1-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c0da1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0da1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0da1-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="c0da1-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




