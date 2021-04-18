---
description: Define informações de posição, textura e cor sobre um Sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Estrutura de D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105794009"
---
# <a name="d3dx10_sprite-structure"></a><span data-ttu-id="32d7c-103">\_Estrutura de Sprite D3DX10</span><span class="sxs-lookup"><span data-stu-id="32d7c-103">D3DX10\_SPRITE structure</span></span>

<span data-ttu-id="32d7c-104">Define informações de posição, textura e cor sobre um Sprite.</span><span class="sxs-lookup"><span data-stu-id="32d7c-104">Defines position, texture, and color information about a sprite.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d7c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32d7c-105">Syntax</span></span>


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a><span data-ttu-id="32d7c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="32d7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="32d7c-107">**matWorld**</span><span class="sxs-lookup"><span data-stu-id="32d7c-107">**matWorld**</span></span>
</dt> <dd>

<span data-ttu-id="32d7c-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="32d7c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32d7c-109">A transformação modelo-mundo do Sprite.</span><span class="sxs-lookup"><span data-stu-id="32d7c-109">The sprite's model-world transformation.</span></span> <span data-ttu-id="32d7c-110">Isso define a posição e a orientação do sprite no espaço do mundo.</span><span class="sxs-lookup"><span data-stu-id="32d7c-110">This defines the position and orientation of the sprite in world space.</span></span>

</dd> <dt>

<span data-ttu-id="32d7c-111">**TexCoord**</span><span class="sxs-lookup"><span data-stu-id="32d7c-111">**TexCoord**</span></span>
</dt> <dd>

<span data-ttu-id="32d7c-112">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="32d7c-112">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32d7c-113">Deslocamento do canto superior esquerdo da textura que indica onde a imagem Sprite deve começar na textura.</span><span class="sxs-lookup"><span data-stu-id="32d7c-113">Offset from the upper-left corner of the texture indicating where the sprite image should start in the texture.</span></span> <span data-ttu-id="32d7c-114">**TexCoord** está em coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="32d7c-114">**TexCoord** is in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="32d7c-115">**TexSize**</span><span class="sxs-lookup"><span data-stu-id="32d7c-115">**TexSize**</span></span>
</dt> <dd>

<span data-ttu-id="32d7c-116">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="32d7c-116">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32d7c-117">Um vetor que contém a largura e a altura do sprite em coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="32d7c-117">A vector containing the width and height of the sprite in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="32d7c-118">**ColorModulate**</span><span class="sxs-lookup"><span data-stu-id="32d7c-118">**ColorModulate**</span></span>
</dt> <dd>

<span data-ttu-id="32d7c-119">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="32d7c-119">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32d7c-120">Uma cor que será multiplicada pela cor do pixel antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="32d7c-120">A color that will be multiplied with the pixel color before rendering.</span></span>

</dd> <dt>

<span data-ttu-id="32d7c-121">**pTexture**</span><span class="sxs-lookup"><span data-stu-id="32d7c-121">**pTexture**</span></span>
</dt> <dd>

<span data-ttu-id="32d7c-122">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="32d7c-122">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span></span>

</dd> <dd>

<span data-ttu-id="32d7c-123">Ponteiro para uma exibição de recurso de sombreador que representa a textura de Sprite.</span><span class="sxs-lookup"><span data-stu-id="32d7c-123">Pointer to a shader-resource view representing the sprite's texture.</span></span> <span data-ttu-id="32d7c-124">Consulte a [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="32d7c-124">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="32d7c-125">**TextureIndex**</span><span class="sxs-lookup"><span data-stu-id="32d7c-125">**TextureIndex**</span></span>
</dt> <dd>

<span data-ttu-id="32d7c-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32d7c-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32d7c-127">O índice da textura.</span><span class="sxs-lookup"><span data-stu-id="32d7c-127">The index of the texture.</span></span> <span data-ttu-id="32d7c-128">Se pTexture não representar uma matriz de textura, isso deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="32d7c-128">If pTexture does not represent a texture array, then this should be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32d7c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32d7c-129">Requirements</span></span>



| <span data-ttu-id="32d7c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="32d7c-130">Requirement</span></span> | <span data-ttu-id="32d7c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="32d7c-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32d7c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32d7c-132">Header</span></span><br/> | <dl> <span data-ttu-id="32d7c-133"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="32d7c-133"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32d7c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="32d7c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d7c-135">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="32d7c-135">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
