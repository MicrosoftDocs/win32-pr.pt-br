---
description: Adicione uma matriz de sprites ao lote de sprites a serem renderizados.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: 'ID3DX10Sprite: método rawSpritesBuffered de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764258"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a><span data-ttu-id="1bf58-103">ID3DX10Sprite: método rawSpritesBuffered de:D</span><span class="sxs-lookup"><span data-stu-id="1bf58-103">ID3DX10Sprite::DrawSpritesBuffered method</span></span>

<span data-ttu-id="1bf58-104">Adicione uma matriz de sprites ao lote de sprites a serem renderizados.</span><span class="sxs-lookup"><span data-stu-id="1bf58-104">Add an array of sprites to the batch of sprites to be rendered.</span></span> <span data-ttu-id="1bf58-105">Isso deve ser chamado entre chamadas para [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)e [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) deve ser chamado antes de end enviar todos os sprites em lote para o dispositivo para renderização.</span><span class="sxs-lookup"><span data-stu-id="1bf58-105">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md), and [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) must be called before End to send all of the batched sprites to the device for rendering.</span></span> <span data-ttu-id="1bf58-106">Esse método Draw é mais útil ao desenhar um pequeno número de sprites que você deseja armazenar em buffer em um lote grande, como fontes.</span><span class="sxs-lookup"><span data-stu-id="1bf58-106">This draw method is most useful when drawing a small number of sprites that you want buffered into a large batch, such as fonts.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf58-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bf58-107">Syntax</span></span>


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a><span data-ttu-id="1bf58-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bf58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bf58-109">*pSprites* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bf58-109">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bf58-110">Tipo: **[ **D3DX10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bf58-110">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="1bf58-111">A matriz de sprites a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="1bf58-111">The array of sprites to draw.</span></span> <span data-ttu-id="1bf58-112">Confira [**D3DX10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="1bf58-112">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bf58-113">*cSprites* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bf58-113">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bf58-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bf58-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bf58-115">O número de sprites em pSprites.</span><span class="sxs-lookup"><span data-stu-id="1bf58-115">The number of sprites in pSprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bf58-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1bf58-116">Return value</span></span>

<span data-ttu-id="1bf58-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bf58-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bf58-118">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1bf58-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1bf58-119">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="1bf58-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf58-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bf58-120">Requirements</span></span>



| <span data-ttu-id="1bf58-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf58-121">Requirement</span></span> | <span data-ttu-id="1bf58-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1bf58-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf58-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bf58-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1bf58-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf58-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1bf58-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1bf58-125">Library</span></span><br/> | <dl> <span data-ttu-id="1bf58-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bf58-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf58-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bf58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf58-128">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="1bf58-128">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="1bf58-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="1bf58-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
