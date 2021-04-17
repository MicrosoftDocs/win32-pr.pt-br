---
description: Adiciona um Sprite à lista de sprites em lote.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: 'ID3DXSprite: método RAW de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761629"
---
# <a name="id3dxspritedraw-method"></a><span data-ttu-id="a02c0-103">ID3DXSprite: método RAW de:D</span><span class="sxs-lookup"><span data-stu-id="a02c0-103">ID3DXSprite::Draw method</span></span>

<span data-ttu-id="a02c0-104">Adiciona um Sprite à lista de sprites em lote.</span><span class="sxs-lookup"><span data-stu-id="a02c0-104">Adds a sprite to the list of batched sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="a02c0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a02c0-105">Syntax</span></span>


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a><span data-ttu-id="a02c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a02c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a02c0-107">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a02c0-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02c0-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a02c0-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a02c0-109">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura Sprite.</span><span class="sxs-lookup"><span data-stu-id="a02c0-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the sprite texture.</span></span>

</dd> <dt>

<span data-ttu-id="a02c0-110">*pSrcRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a02c0-110">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02c0-111">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="a02c0-111">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="a02c0-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que indica a parte da textura de origem a ser usada para o sprite.</span><span class="sxs-lookup"><span data-stu-id="a02c0-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that indicates the portion of the source texture to use for the sprite.</span></span> <span data-ttu-id="a02c0-113">Se esse parâmetro for **nulo**, a imagem de origem inteira será usada para o sprite.</span><span class="sxs-lookup"><span data-stu-id="a02c0-113">If this parameter is **NULL**, then the entire source image is used for the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="a02c0-114">*pCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a02c0-114">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02c0-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a02c0-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a02c0-116">Ponteiro para um vetor [**D3DXVECTOR3**](d3dxvector3.md) que identifica o centro do Sprite.</span><span class="sxs-lookup"><span data-stu-id="a02c0-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite.</span></span> <span data-ttu-id="a02c0-117">Se esse argumento for **nulo**, o ponto (0, 0, 0) será usado, que é o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="a02c0-117">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="a02c0-118">*pPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a02c0-118">*pPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02c0-119">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a02c0-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a02c0-120">Ponteiro para um vetor [**D3DXVECTOR3**](d3dxvector3.md) que identifica a posição do Sprite.</span><span class="sxs-lookup"><span data-stu-id="a02c0-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite.</span></span> <span data-ttu-id="a02c0-121">Se esse argumento for **nulo**, o ponto (0, 0, 0) será usado, que é o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="a02c0-121">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="a02c0-122">*Cor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a02c0-122">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02c0-123">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a02c0-123">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a02c0-124">Tipo de [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="a02c0-124">[**D3DCOLOR**](d3dcolor.md) type.</span></span> <span data-ttu-id="a02c0-125">Os canais de cor e alfa são modulados por esse valor.</span><span class="sxs-lookup"><span data-stu-id="a02c0-125">The color and alpha channels are modulated by this value.</span></span> <span data-ttu-id="a02c0-126">Um valor de 0xFFFFFFFF mantém a cor da fonte original e os dados alfa.</span><span class="sxs-lookup"><span data-stu-id="a02c0-126">A value of 0xFFFFFFFF maintains the original source color and alpha data.</span></span> <span data-ttu-id="a02c0-127">Use a [**macro \_ RGBA D3DCOLOR**](d3dcolor-rgba.md) para ajudar a gerar essa cor.</span><span class="sxs-lookup"><span data-stu-id="a02c0-127">Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a02c0-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a02c0-128">Return value</span></span>

<span data-ttu-id="a02c0-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a02c0-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a02c0-130">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a02c0-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a02c0-131">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a02c0-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a02c0-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a02c0-132">Remarks</span></span>

<span data-ttu-id="a02c0-133">Para dimensionar, girar ou traduzir um Sprite, chame [**ID3DXSprite:: SetTransform**](id3dxsprite--settransform.md) com uma matriz que contém os valores de SRT (escala, rotação e conversão), antes de chamar ID3DXSprite::D RAW.</span><span class="sxs-lookup"><span data-stu-id="a02c0-133">To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw.</span></span> <span data-ttu-id="a02c0-134">Para obter informações sobre como definir valores de SRT em uma matriz, consulte [transformações de matriz](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="a02c0-134">For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a02c0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a02c0-135">Requirements</span></span>



| <span data-ttu-id="a02c0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a02c0-136">Requirement</span></span> | <span data-ttu-id="a02c0-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a02c0-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a02c0-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a02c0-138">Header</span></span><br/>  | <dl> <span data-ttu-id="a02c0-139"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a02c0-139"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a02c0-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a02c0-140">Library</span></span><br/> | <dl> <span data-ttu-id="a02c0-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a02c0-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a02c0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a02c0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a02c0-143">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="a02c0-143">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="a02c0-144">**ID3DXSprite:: GetTransform**</span><span class="sxs-lookup"><span data-stu-id="a02c0-144">**ID3DXSprite::GetTransform**</span></span>](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
