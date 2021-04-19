---
description: Recupera o dispositivo associado ao efeito.
ms.assetid: acef5d0a-b185-4054-8982-0580440ab76b
title: 'Método ID3DXEffect:: GetDevice (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fde2d9f3d9db362bf48fda66e9da10b91a864bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771440"
---
# <a name="id3dxeffectgetdevice-method"></a><span data-ttu-id="59cd7-103">Método ID3DXEffect:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="59cd7-103">ID3DXEffect::GetDevice method</span></span>

<span data-ttu-id="59cd7-104">Recupera o dispositivo associado ao efeito.</span><span class="sxs-lookup"><span data-stu-id="59cd7-104">Retrieves the device associated with the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="59cd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59cd7-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="59cd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59cd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59cd7-107">*ppDevice* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59cd7-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59cd7-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="59cd7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="59cd7-109">Endereço de um ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado ao efeito.</span><span class="sxs-lookup"><span data-stu-id="59cd7-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59cd7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59cd7-110">Return value</span></span>

<span data-ttu-id="59cd7-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59cd7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59cd7-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59cd7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59cd7-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="59cd7-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="59cd7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="59cd7-114">Remarks</span></span>

<span data-ttu-id="59cd7-115">Chamar esse método aumentará a contagem de referência interna para a interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="59cd7-115">Calling this method will increase the internal reference count for the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="59cd7-116">Não se esqueça de chamar IUnknown:: Release quando terminar de usar a interface **IDirect3DDevice9** ou você terá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="59cd7-116">Be sure to call IUnknown::Release when you are done using the **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="59cd7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59cd7-117">Requirements</span></span>



| <span data-ttu-id="59cd7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="59cd7-118">Requirement</span></span> | <span data-ttu-id="59cd7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="59cd7-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59cd7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59cd7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="59cd7-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="59cd7-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="59cd7-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59cd7-122">Library</span></span><br/> | <dl> <span data-ttu-id="59cd7-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59cd7-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="59cd7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="59cd7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59cd7-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="59cd7-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
