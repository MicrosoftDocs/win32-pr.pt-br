---
description: Recupera o dispositivo Direct3D associado à superfície de renderização.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: 'Método ID3DXRenderToSurface:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298816"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a><span data-ttu-id="66f8f-103">Método ID3DXRenderToSurface:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="66f8f-103">ID3DXRenderToSurface::GetDevice method</span></span>

<span data-ttu-id="66f8f-104">Recupera o dispositivo Direct3D associado à superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="66f8f-104">Retrieves the Direct3D device associated with the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66f8f-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="66f8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f8f-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="66f8f-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="66f8f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="66f8f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="66f8f-109">Endereço de um ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que representa o objeto de dispositivo Direct3D associado à superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="66f8f-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f8f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66f8f-110">Return value</span></span>

<span data-ttu-id="66f8f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66f8f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66f8f-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="66f8f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="66f8f-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="66f8f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="66f8f-114">Chamar esse método aumentará a contagem de referência interna na interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="66f8f-114">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="66f8f-115">Não se esqueça de chamar [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) quando terminar de usar essa interface **IDirect3DDevice9** ou você terá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="66f8f-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f8f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f8f-116">Requirements</span></span>



| <span data-ttu-id="66f8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f8f-117">Requirement</span></span> | <span data-ttu-id="66f8f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="66f8f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66f8f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f8f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="66f8f-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f8f-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="66f8f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66f8f-121">Library</span></span><br/> | <dl> <span data-ttu-id="66f8f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66f8f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66f8f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="66f8f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f8f-124">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="66f8f-124">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
