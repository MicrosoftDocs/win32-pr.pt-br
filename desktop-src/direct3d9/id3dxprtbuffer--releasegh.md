---
description: Desassocia um objeto ID3DXTextureGutterHelper anexado ao objeto ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'Método ID3DXPRTBuffer:: ReleaseGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371020"
---
# <a name="id3dxprtbufferreleasegh-method"></a><span data-ttu-id="9ffdf-103">Método ID3DXPRTBuffer:: ReleaseGH</span><span class="sxs-lookup"><span data-stu-id="9ffdf-103">ID3DXPRTBuffer::ReleaseGH method</span></span>

<span data-ttu-id="9ffdf-104">Desassocia um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) anexado ao objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9ffdf-104">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffdf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ffdf-105">Syntax</span></span>


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a><span data-ttu-id="9ffdf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ffdf-106">Parameters</span></span>

<span data-ttu-id="9ffdf-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ffdf-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ffdf-108">Return value</span></span>

<span data-ttu-id="9ffdf-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ffdf-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ffdf-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ffdf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ffdf-111">Remarks</span></span>

<span data-ttu-id="9ffdf-112">Esse método libera o ponteiro para a interface [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="9ffdf-112">This method releases the pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface.</span></span>

<span data-ttu-id="9ffdf-113">Você deve garantir que o número de chamadas [**ID3DXPRTBuffer:: AttachGH**](id3dxprtbuffer--attachgh.md) corresponda ao número de chamadas **ID3DXPRTBuffer:: ReleaseGH** .</span><span class="sxs-lookup"><span data-stu-id="9ffdf-113">You must ensure that the number of [**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) calls matches the number of **ID3DXPRTBuffer::ReleaseGH** calls.</span></span> <span data-ttu-id="9ffdf-114">Depois de chamar **ID3DXPRTBuffer:: ReleaseGH**, o ponteiro PGH retornado por **ID3DXPRTBuffer:: AttachGH** não deve mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-114">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ffdf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ffdf-115">Requirements</span></span>



| <span data-ttu-id="9ffdf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ffdf-116">Requirement</span></span> | <span data-ttu-id="9ffdf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9ffdf-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffdf-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ffdf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9ffdf-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ffdf-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9ffdf-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ffdf-120">Library</span></span><br/> | <dl> <span data-ttu-id="9ffdf-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ffdf-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ffdf-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ffdf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffdf-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="9ffdf-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="9ffdf-124">**ID3DXPRTBuffer::AttachGH**</span><span class="sxs-lookup"><span data-stu-id="9ffdf-124">**ID3DXPRTBuffer::AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




