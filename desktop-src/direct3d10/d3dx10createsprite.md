---
description: Crie um sprite para desenhar uma textura 2D. Observação em vez de usar essa função, recomendamos que você use Direct2D e a biblioteca DirectXTK, SpriteBatch Class.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Função D3DX10CreateSprite (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789342"
---
# <a name="d3dx10createsprite-function"></a><span data-ttu-id="49225-103">Função D3DX10CreateSprite</span><span class="sxs-lookup"><span data-stu-id="49225-103">D3DX10CreateSprite function</span></span>

<span data-ttu-id="49225-104">Crie um sprite para desenhar uma textura 2D.</span><span class="sxs-lookup"><span data-stu-id="49225-104">Create a sprite for drawing a 2D texture.</span></span>

> [!Note]  
> <span data-ttu-id="49225-105">Em vez de usar essa função, recomendamos que você use [Direct2D](../direct2d/direct2d-portal.md) e a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteBatch** Class.</span><span class="sxs-lookup"><span data-stu-id="49225-105">Instead of using this function, we recommend that you use [Direct2D](../direct2d/direct2d-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteBatch** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="49225-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49225-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="49225-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49225-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49225-108">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49225-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49225-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="49225-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="49225-110">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que irá desenhar o sprite.</span><span class="sxs-lookup"><span data-stu-id="49225-110">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will draw the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="49225-111">*cDeviceBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49225-111">*cDeviceBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49225-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49225-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49225-113">O tamanho do buffer de vértice, em número de sprites, que será enviado ao dispositivo quando [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) ou [**ID3DX10Sprite::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="49225-113">The size of the vertex buffer, in number of sprites, that will be sent to the device when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) or [**ID3DX10Sprite::DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) is called.</span></span> <span data-ttu-id="49225-114">Isso deve ser um pequeno número se você souber que estará renderizando um pequeno número de sprites por vez (para economizar memória) e um grande número se você souber que será renderizado um grande número de sprites por vez.</span><span class="sxs-lookup"><span data-stu-id="49225-114">This should be a small number if you know you will be rendering a small number of sprites at a time (to save memory) and a large number if you know you will be rendering a large number of sprites at a time.</span></span> <span data-ttu-id="49225-115">O valor máximo é 4096.</span><span class="sxs-lookup"><span data-stu-id="49225-115">The maximum value is 4096.</span></span> <span data-ttu-id="49225-116">Se 0 for especificado, o tamanho do buffer de vértice será definido automaticamente como 4096.</span><span class="sxs-lookup"><span data-stu-id="49225-116">If 0 is specified, the vertex buffer size will automatically be set to 4096.</span></span>

</dd> <dt>

<span data-ttu-id="49225-117">*ppSprite* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="49225-117">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49225-118">Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="49225-118">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)\***</span></span>

<span data-ttu-id="49225-119">O endereço de um ponteiro para uma interface Sprite (consulte a [**interface ID3DX10Sprite**](id3dx10sprite.md)).</span><span class="sxs-lookup"><span data-stu-id="49225-119">The address of a pointer to a sprite interface (see [**ID3DX10Sprite Interface**](id3dx10sprite.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49225-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49225-120">Return value</span></span>

<span data-ttu-id="49225-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49225-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49225-122">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49225-122">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="49225-123">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="49225-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="49225-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49225-124">Requirements</span></span>



| <span data-ttu-id="49225-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="49225-125">Requirement</span></span> | <span data-ttu-id="49225-126">Valor</span><span class="sxs-lookup"><span data-stu-id="49225-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49225-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49225-127">Header</span></span><br/>  | <dl> <span data-ttu-id="49225-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="49225-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="49225-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49225-129">Library</span></span><br/> | <dl> <span data-ttu-id="49225-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49225-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49225-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="49225-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49225-132">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="49225-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
