---
description: Associa um objeto ID3DXTextureGutterHelper ao objeto ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'Método ID3DXPRTBuffer:: AttachGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764426"
---
# <a name="id3dxprtbufferattachgh-method"></a><span data-ttu-id="56aff-103">Método ID3DXPRTBuffer:: AttachGH</span><span class="sxs-lookup"><span data-stu-id="56aff-103">ID3DXPRTBuffer::AttachGH method</span></span>

<span data-ttu-id="56aff-104">Associa um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) ao objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="56aff-104">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="56aff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56aff-105">Syntax</span></span>


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="56aff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56aff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56aff-107">*PGH* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56aff-107">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56aff-108">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="56aff-108">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="56aff-109">Ponteiro para a interface [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) de um objeto que contém dados de medianiz de textura.</span><span class="sxs-lookup"><span data-stu-id="56aff-109">Pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface of an object that contains texture gutter data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56aff-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56aff-110">Return value</span></span>

<span data-ttu-id="56aff-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56aff-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56aff-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="56aff-112">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="56aff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="56aff-113">Remarks</span></span>

<span data-ttu-id="56aff-114">A contagem de referência do objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) será incrementada automaticamente em um.</span><span class="sxs-lookup"><span data-stu-id="56aff-114">The reference count of the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object will automatically be incremented by one.</span></span> <span data-ttu-id="56aff-115">Todos os ponteiros **ID3DXTextureGutterHelper** existentes serão liberados.</span><span class="sxs-lookup"><span data-stu-id="56aff-115">Any existing **ID3DXTextureGutterHelper** pointers will be released.</span></span>

<span data-ttu-id="56aff-116">Você deve garantir que o número de chamadas **ID3DXPRTBuffer:: AttachGH** corresponda ao número de chamadas [**ID3DXPRTBuffer:: ReleaseGH**](id3dxprtbuffer--releasegh.md) .</span><span class="sxs-lookup"><span data-stu-id="56aff-116">You must ensure that the number of **ID3DXPRTBuffer::AttachGH** calls matches the number of [**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md) calls.</span></span> <span data-ttu-id="56aff-117">Depois de chamar **ID3DXPRTBuffer:: ReleaseGH**, o ponteiro PGH retornado por **ID3DXPRTBuffer:: AttachGH** não deve mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="56aff-117">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="56aff-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56aff-118">Requirements</span></span>



| <span data-ttu-id="56aff-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="56aff-119">Requirement</span></span> | <span data-ttu-id="56aff-120">Valor</span><span class="sxs-lookup"><span data-stu-id="56aff-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56aff-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56aff-121">Header</span></span><br/>  | <dl> <span data-ttu-id="56aff-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="56aff-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="56aff-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56aff-123">Library</span></span><br/> | <dl> <span data-ttu-id="56aff-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56aff-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56aff-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="56aff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56aff-126">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="56aff-126">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="56aff-127">**ID3DXPRTBuffer::ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="56aff-127">**ID3DXPRTBuffer::ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




