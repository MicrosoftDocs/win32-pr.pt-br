---
description: Use este método para readquirir recursos e salvar o estado inicial.
ms.assetid: a326a465-ee90-466d-8e46-22e082e9533c
title: 'Método ID3DXRenderToSurface:: OnResetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09d8e3d2c7b628d36fee12525e9423059a7bd63a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298587"
---
# <a name="id3dxrendertosurfaceonresetdevice-method"></a><span data-ttu-id="0cc42-103">Método ID3DXRenderToSurface:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="0cc42-103">ID3DXRenderToSurface::OnResetDevice method</span></span>

<span data-ttu-id="0cc42-104">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="0cc42-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cc42-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="0cc42-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cc42-106">Parameters</span></span>

<span data-ttu-id="0cc42-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0cc42-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cc42-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0cc42-108">Return value</span></span>

<span data-ttu-id="0cc42-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cc42-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cc42-110">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cc42-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0cc42-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0cc42-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cc42-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cc42-112">Remarks</span></span>

<span data-ttu-id="0cc42-113">ID3DXRenderToSurface:: OnResetDevice deve ser chamado cada vez que o dispositivo for redefinido (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes que quaisquer outros métodos sejam chamados.</span><span class="sxs-lookup"><span data-stu-id="0cc42-113">ID3DXRenderToSurface::OnResetDevice should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="0cc42-114">Este é um bom lugar para readquirir recursos de memória de vídeo e capturar blocos de estado.</span><span class="sxs-lookup"><span data-stu-id="0cc42-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc42-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cc42-115">Requirements</span></span>



| <span data-ttu-id="0cc42-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cc42-116">Requirement</span></span> | <span data-ttu-id="0cc42-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0cc42-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc42-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cc42-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0cc42-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc42-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0cc42-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cc42-120">Library</span></span><br/> | <dl> <span data-ttu-id="0cc42-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cc42-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cc42-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cc42-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc42-123">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="0cc42-123">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
