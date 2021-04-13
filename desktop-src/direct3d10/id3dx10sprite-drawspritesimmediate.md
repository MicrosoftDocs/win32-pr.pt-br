---
description: Desenhe uma matriz de sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: 'ID3DX10Sprite: método rawSpritesImmediate de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298873"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a><span data-ttu-id="12ab7-103">ID3DX10Sprite: método rawSpritesImmediate de:D</span><span class="sxs-lookup"><span data-stu-id="12ab7-103">ID3DX10Sprite::DrawSpritesImmediate method</span></span>

<span data-ttu-id="12ab7-104">Desenhe uma matriz de sprites.</span><span class="sxs-lookup"><span data-stu-id="12ab7-104">Draw an array of sprites.</span></span> <span data-ttu-id="12ab7-105">Isso enviará imediatamente os sprites para o dispositivo para renderização, que é diferente de [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , que adiciona apenas uma matriz de sprites a um lote de sprites a serem renderizados quando [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="12ab7-105">This will immediately send the sprites to the device for rendering, which is different from [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) which only adds an array of sprites to a batch of sprites to be rendered when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) is called.</span></span> <span data-ttu-id="12ab7-106">Esse método Draw é mais útil ao desenhar um grande número de sprites que já foram classificados na CPU (ou não precisam ser classificados), como em um sistema de partículas.</span><span class="sxs-lookup"><span data-stu-id="12ab7-106">This draw method is most useful when drawing a large number of sprites that have already been sorted on the CPU (or do not need to be sorted), such as in a particle system.</span></span> <span data-ttu-id="12ab7-107">Isso deve ser chamado entre chamadas para [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: End**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="12ab7-107">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12ab7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12ab7-108">Syntax</span></span>


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a><span data-ttu-id="12ab7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12ab7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ab7-110">*pSprites* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12ab7-110">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ab7-111">Tipo: **[ **D3DX10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="12ab7-111">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="12ab7-112">A matriz de sprites a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="12ab7-112">The array of sprites to draw.</span></span> <span data-ttu-id="12ab7-113">Confira [**D3DX10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="12ab7-113">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="12ab7-114">*cSprites* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12ab7-114">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ab7-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12ab7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12ab7-116">O número de sprites em pSprites.</span><span class="sxs-lookup"><span data-stu-id="12ab7-116">The number of sprites in pSprites.</span></span>

</dd> <dt>

<span data-ttu-id="12ab7-117">*cbSprite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12ab7-117">*cbSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ab7-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12ab7-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12ab7-119">O tamanho da estrutura Sprite que você está passando para pSprites.</span><span class="sxs-lookup"><span data-stu-id="12ab7-119">The size of the sprite structure you are passing into pSprites.</span></span> <span data-ttu-id="12ab7-120">Passar em 0 é o equivalente a passar em sizeof (D3DX10 \_ Sprite).</span><span class="sxs-lookup"><span data-stu-id="12ab7-120">Passing in 0 is the equivalent of passing in sizeof(D3DX10\_SPRITE).</span></span>

</dd> <dt>

<span data-ttu-id="12ab7-121">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="12ab7-121">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ab7-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12ab7-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12ab7-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="12ab7-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ab7-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12ab7-124">Return value</span></span>

<span data-ttu-id="12ab7-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12ab7-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12ab7-126">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12ab7-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="12ab7-127">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="12ab7-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ab7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ab7-128">Requirements</span></span>



| <span data-ttu-id="12ab7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ab7-129">Requirement</span></span> | <span data-ttu-id="12ab7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="12ab7-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12ab7-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12ab7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="12ab7-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="12ab7-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="12ab7-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12ab7-133">Library</span></span><br/> | <dl> <span data-ttu-id="12ab7-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12ab7-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ab7-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="12ab7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ab7-136">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="12ab7-136">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="12ab7-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="12ab7-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
