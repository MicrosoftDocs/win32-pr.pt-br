---
description: 'Sinalizadores de Sprite que dizem ao comportamento da API de desenho de Sprite. Eles são passados em ID3DX10Sprite:: Begin.'
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: Enumeração de D3DX10_SPRITE_FLAG (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790424"
---
# <a name="d3dx10_sprite_flag-enumeration"></a><span data-ttu-id="cc53e-104">\_Enumeração de \_ sinalizador Sprite D3DX10</span><span class="sxs-lookup"><span data-stu-id="cc53e-104">D3DX10\_SPRITE\_FLAG enumeration</span></span>

<span data-ttu-id="cc53e-105">Sinalizadores de Sprite que dizem ao comportamento da API de desenho de Sprite.</span><span class="sxs-lookup"><span data-stu-id="cc53e-105">Sprite flags that tell the sprite drawing API how to behave.</span></span> <span data-ttu-id="cc53e-106">Eles são passados em [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).</span><span class="sxs-lookup"><span data-stu-id="cc53e-106">These are passed into [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc53e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc53e-107">Syntax</span></span>


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a><span data-ttu-id="cc53e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="cc53e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cc53e-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Textura de \_ classificação de Sprite D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="cc53e-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10\_SPRITE\_SORT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="cc53e-110">Classifique os sprites por textura antes da renderização para que, quando houver muitos sprites com a mesma textura que textura de todos os sprites sejam renderizados ao mesmo tempo, melhorando o desempenho.</span><span class="sxs-lookup"><span data-stu-id="cc53e-110">Sort the sprites by texture before rendering so that when there are many sprites with the same texture that texture all of those sprites will be rendered at the same time, thereby improving performance.</span></span>

</dd> <dt>

<span data-ttu-id="cc53e-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 \_ Sprite \_ classificar \_ profundidade \_ \_ de volta para \_ frente**</span><span class="sxs-lookup"><span data-stu-id="cc53e-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_BACK\_TO\_FRONT**</span></span>
</dt> <dd>

<span data-ttu-id="cc53e-112">Classifique os sprites de volta para frente para que os mais distantes da câmera sejam desenhados primeiro.</span><span class="sxs-lookup"><span data-stu-id="cc53e-112">Sort the sprites from back to front to that those farther away from the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="cc53e-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ Sprite \_ classificar \_ profundidade \_ \_ de \_ fundo para trás**</span><span class="sxs-lookup"><span data-stu-id="cc53e-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_FRONT\_TO\_BACK**</span></span>
</dt> <dd>

<span data-ttu-id="cc53e-114">Classifique os sprites de frente para trás para que os mais próximos da câmera sejam desenhados primeiro.</span><span class="sxs-lookup"><span data-stu-id="cc53e-114">Sort the sprites from front to back so that those closer to the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="cc53e-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ Sprite \_ Salvar \_ estado**</span><span class="sxs-lookup"><span data-stu-id="cc53e-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10\_SPRITE\_SAVE\_STATE**</span></span>
</dt> <dd>

<span data-ttu-id="cc53e-116">Salva o estado para que quando [**ID3DX10Sprite:: End**](id3dx10sprite-end.md) for chamado, ele irá restaurar o estado para o caminho anterior a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="cc53e-116">Saves the state so that when [**ID3DX10Sprite::End**](id3dx10sprite-end.md) is called, it will restore the state to the way it was before [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) was called.</span></span>

</dd> <dt>

<span data-ttu-id="cc53e-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**\_Texturas do D3DX10 Sprite \_ ADDREF \_**</span><span class="sxs-lookup"><span data-stu-id="cc53e-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10\_SPRITE\_ADDREF\_TEXTURES**</span></span>
</dt> <dd>

<span data-ttu-id="cc53e-118">Chama AddRef em todas as texturas quando elas são passadas para [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).</span><span class="sxs-lookup"><span data-stu-id="cc53e-118">Calls AddRef on all of the textures when they are passed into [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc53e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc53e-119">Remarks</span></span>

<span data-ttu-id="cc53e-120">Após a conclusão de uma classificação de front-to-back ou de trás para frente, ela fará automaticamente uma classificação secundária por textura.</span><span class="sxs-lookup"><span data-stu-id="cc53e-120">After a front-to-back or back-to-front sort is done, it will automatically do a secondary sort by texture.</span></span> <span data-ttu-id="cc53e-121">Isso é útil quando há muitos sprites com a mesma textura no mesmo plano, como ao desenhar a interface do usuário em um jogo.</span><span class="sxs-lookup"><span data-stu-id="cc53e-121">This is helpful for when there are many sprites with the same texture all on the same plane, such as when drawing the user interface in a game.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc53e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc53e-122">Requirements</span></span>



| <span data-ttu-id="cc53e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc53e-123">Requirement</span></span> | <span data-ttu-id="cc53e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cc53e-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc53e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc53e-125">Header</span></span><br/> | <dl> <span data-ttu-id="cc53e-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc53e-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc53e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc53e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc53e-128">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="cc53e-128">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




