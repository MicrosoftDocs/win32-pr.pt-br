---
description: Recupera o dispositivo associado à malha.
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: 'Método ID3DXBaseMesh:: GetDevice (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b866c86bf759305a4626f0ff5ecaa8e35bfd75d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012120"
---
# <a name="id3dxbasemeshgetdevice-method"></a><span data-ttu-id="128b2-103">Método ID3DXBaseMesh:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="128b2-103">ID3DXBaseMesh::GetDevice method</span></span>

<span data-ttu-id="128b2-104">Recupera o dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="128b2-104">Retrieves the device associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="128b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="128b2-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="128b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="128b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128b2-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="128b2-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="128b2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="128b2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="128b2-109">Endereço de um ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que representa o objeto de dispositivo Direct3D associado à malha.</span><span class="sxs-lookup"><span data-stu-id="128b2-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128b2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="128b2-110">Return value</span></span>

<span data-ttu-id="128b2-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="128b2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="128b2-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="128b2-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="128b2-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="128b2-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="128b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="128b2-114">Remarks</span></span>

<span data-ttu-id="128b2-115">Chamar esse método aumentará a contagem de referência interna na interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="128b2-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="128b2-116">Não se esqueça de chamar [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) quando terminar de usar essa interface **IDirect3DDevice9** ou você terá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="128b2-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="128b2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="128b2-117">Requirements</span></span>



| <span data-ttu-id="128b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="128b2-118">Requirement</span></span> | <span data-ttu-id="128b2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="128b2-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="128b2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="128b2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="128b2-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="128b2-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="128b2-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="128b2-122">Library</span></span><br/> | <dl> <span data-ttu-id="128b2-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="128b2-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="128b2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="128b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="128b2-125">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="128b2-125">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
