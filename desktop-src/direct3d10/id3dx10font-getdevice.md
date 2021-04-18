---
description: Recupere o dispositivo Direct3D associado ao objeto Font.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'Método ID3DX10Font:: GetDevice (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793307"
---
# <a name="id3dx10fontgetdevice-method"></a><span data-ttu-id="6be5c-103">Método ID3DX10Font:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="6be5c-103">ID3DX10Font::GetDevice method</span></span>

<span data-ttu-id="6be5c-104">Recupere o dispositivo Direct3D associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="6be5c-104">Retrieve the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be5c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6be5c-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="6be5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6be5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be5c-107">*ppDevice* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6be5c-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6be5c-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="6be5c-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="6be5c-109">Endereço de um ponteiro para uma interface ID3D10Device, que representa o objeto de dispositivo Direct3D associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="6be5c-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be5c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6be5c-110">Return value</span></span>

<span data-ttu-id="6be5c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6be5c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6be5c-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6be5c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6be5c-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="6be5c-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be5c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6be5c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6be5c-115">Chamar esse método aumentará a contagem de referência interna na interface ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="6be5c-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span> <span data-ttu-id="6be5c-116">Não se esqueça de chamar IUnknown quando terminar de usar essa interface ID3D10Device ou você terá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="6be5c-116">Be sure to call IUnknown when you are done using this ID3D10Device interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6be5c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6be5c-117">Requirements</span></span>



| <span data-ttu-id="6be5c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be5c-118">Requirement</span></span> | <span data-ttu-id="6be5c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6be5c-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6be5c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6be5c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6be5c-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6be5c-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6be5c-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6be5c-122">Library</span></span><br/> | <dl> <span data-ttu-id="6be5c-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6be5c-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6be5c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6be5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be5c-125">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="6be5c-125">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="6be5c-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6be5c-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




