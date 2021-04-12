---
description: Recupera o dispositivo associado ao objeto Sprite.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: 'Método ID3DXSprite:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370987"
---
# <a name="id3dxspritegetdevice-method"></a><span data-ttu-id="93d7a-103">Método ID3DXSprite:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="93d7a-103">ID3DXSprite::GetDevice method</span></span>

<span data-ttu-id="93d7a-104">Recupera o dispositivo associado ao objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="93d7a-104">Retrieves the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d7a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93d7a-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="93d7a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93d7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d7a-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="93d7a-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="93d7a-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="93d7a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="93d7a-109">Endereço de um ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que representa o objeto de dispositivo Direct3D associado ao objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="93d7a-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d7a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93d7a-110">Return value</span></span>

<span data-ttu-id="93d7a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93d7a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93d7a-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93d7a-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="93d7a-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="93d7a-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="93d7a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="93d7a-114">Remarks</span></span>

<span data-ttu-id="93d7a-115">Chamar esse método aumentará a contagem de referência interna na interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="93d7a-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="93d7a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93d7a-116">Requirements</span></span>



| <span data-ttu-id="93d7a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="93d7a-117">Requirement</span></span> | <span data-ttu-id="93d7a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="93d7a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93d7a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93d7a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="93d7a-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d7a-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="93d7a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93d7a-121">Library</span></span><br/> | <dl> <span data-ttu-id="93d7a-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93d7a-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93d7a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="93d7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d7a-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="93d7a-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
