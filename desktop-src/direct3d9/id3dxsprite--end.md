---
description: 'Chama ID3DXSprite:: flush e restaura o estado do dispositivo para como ele estava antes de ID3DXSprite:: Begin foi chamado.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'Método ID3DXSprite:: End (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370983"
---
# <a name="id3dxspriteend-method"></a><span data-ttu-id="952fc-103">Método ID3DXSprite:: End</span><span class="sxs-lookup"><span data-stu-id="952fc-103">ID3DXSprite::End method</span></span>

<span data-ttu-id="952fc-104">Chama [**ID3DXSprite:: flush**](id3dxsprite--flush.md) e restaura o estado do dispositivo para como ele estava antes de [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="952fc-104">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="952fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="952fc-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="952fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="952fc-106">Parameters</span></span>

<span data-ttu-id="952fc-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="952fc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="952fc-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="952fc-108">Return value</span></span>

<span data-ttu-id="952fc-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="952fc-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="952fc-110">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="952fc-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="952fc-111">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="952fc-111">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="952fc-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="952fc-112">Remarks</span></span>

<span data-ttu-id="952fc-113">**ID3DXSprite:: End** não pode ser usado como um substituto para [**IDirect3DDevice9:: endcena**](/windows/desktop/api) ou [**ID3DXRenderToSurface:: endcena**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="952fc-113">**ID3DXSprite::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="952fc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="952fc-114">Requirements</span></span>



| <span data-ttu-id="952fc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="952fc-115">Requirement</span></span> | <span data-ttu-id="952fc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="952fc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="952fc-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="952fc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="952fc-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="952fc-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="952fc-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="952fc-119">Library</span></span><br/> | <dl> <span data-ttu-id="952fc-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="952fc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="952fc-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="952fc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952fc-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="952fc-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="952fc-123">**ID3DXSprite:: Begin**</span><span class="sxs-lookup"><span data-stu-id="952fc-123">**ID3DXSprite::Begin**</span></span>](id3dxsprite--begin.md)
</dt> </dl>

 

 




