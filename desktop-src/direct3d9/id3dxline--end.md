---
description: 'Restaura o estado do dispositivo para como ele era quando ID3DXLine:: Begin foi chamado.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'Método ID3DXLine:: End (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760930"
---
# <a name="id3dxlineend-method"></a><span data-ttu-id="0bd8f-103">Método ID3DXLine:: End</span><span class="sxs-lookup"><span data-stu-id="0bd8f-103">ID3DXLine::End method</span></span>

<span data-ttu-id="0bd8f-104">Restaura o estado do dispositivo para como ele era quando [**ID3DXLine:: Begin**](id3dxline--begin.md) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="0bd8f-104">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bd8f-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="0bd8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bd8f-106">Parameters</span></span>

<span data-ttu-id="0bd8f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0bd8f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bd8f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bd8f-108">Return value</span></span>

<span data-ttu-id="0bd8f-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bd8f-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bd8f-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bd8f-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0bd8f-111">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="0bd8f-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd8f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bd8f-112">Remarks</span></span>

<span data-ttu-id="0bd8f-113">**ID3DXLine:: End** não pode ser usado como um substituto para [**IDirect3DDevice9:: endcena**](/windows/desktop/api) ou [**ID3DXRenderToSurface:: endcena**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="0bd8f-113">**ID3DXLine::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd8f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bd8f-114">Requirements</span></span>



| <span data-ttu-id="0bd8f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bd8f-115">Requirement</span></span> | <span data-ttu-id="0bd8f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0bd8f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd8f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bd8f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0bd8f-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bd8f-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0bd8f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bd8f-119">Library</span></span><br/> | <dl> <span data-ttu-id="0bd8f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bd8f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bd8f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bd8f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd8f-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="0bd8f-122">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="0bd8f-123">**ID3DXLine:: Begin**</span><span class="sxs-lookup"><span data-stu-id="0bd8f-123">**ID3DXLine::Begin**</span></span>](id3dxline--begin.md)
</dt> </dl>

 

 




