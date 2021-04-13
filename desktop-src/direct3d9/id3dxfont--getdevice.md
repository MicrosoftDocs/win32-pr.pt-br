---
description: Recupera o dispositivo Direct3D associado ao objeto Font.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: 'Método ID3DXFont:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2de1b6e2c3b2c2b61576c739d96abc8b8fc8851a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298820"
---
# <a name="id3dxfontgetdevice-method"></a><span data-ttu-id="b842e-103">Método ID3DXFont:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="b842e-103">ID3DXFont::GetDevice method</span></span>

<span data-ttu-id="b842e-104">Recupera o dispositivo Direct3D associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="b842e-104">Retrieves the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b842e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b842e-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="b842e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b842e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b842e-107">*ppDevice* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b842e-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b842e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="b842e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="b842e-109">Endereço de um ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que representa o objeto de dispositivo Direct3D associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="b842e-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b842e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b842e-110">Return value</span></span>

<span data-ttu-id="b842e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b842e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b842e-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b842e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b842e-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="b842e-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="b842e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b842e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b842e-115">Chamar esse método aumentará a contagem de referência interna na interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="b842e-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="b842e-116">Não se esqueça de chamar [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) quando terminar de usar essa interface **IDirect3DDevice9** ou você terá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="b842e-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b842e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b842e-117">Requirements</span></span>



| <span data-ttu-id="b842e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b842e-118">Requirement</span></span> | <span data-ttu-id="b842e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b842e-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b842e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b842e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b842e-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b842e-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b842e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b842e-122">Library</span></span><br/> | <dl> <span data-ttu-id="b842e-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b842e-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b842e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b842e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b842e-125">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="b842e-125">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
