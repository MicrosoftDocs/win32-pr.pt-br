---
description: Aplica dados de medianiz de textura armazenados a um buffer de textura ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'Método ID3DXPRTBuffer:: EvalGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796221"
---
# <a name="id3dxprtbufferevalgh-method"></a><span data-ttu-id="2948d-103">Método ID3DXPRTBuffer:: EvalGH</span><span class="sxs-lookup"><span data-stu-id="2948d-103">ID3DXPRTBuffer::EvalGH method</span></span>

<span data-ttu-id="2948d-104">Aplica dados de medianiz de textura armazenados a um buffer de textura [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="2948d-104">Applies stored texture gutter data to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2948d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2948d-105">Syntax</span></span>


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a><span data-ttu-id="2948d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2948d-106">Parameters</span></span>

<span data-ttu-id="2948d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2948d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2948d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2948d-108">Return value</span></span>

<span data-ttu-id="2948d-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2948d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2948d-110">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2948d-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2948d-111">Se o método falhar, o valor a seguir será retornado.</span><span class="sxs-lookup"><span data-stu-id="2948d-111">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="2948d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2948d-112">Remarks</span></span>

<span data-ttu-id="2948d-113">Esse método faz uma chamada interna para [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) para recuperar e aplicar dados de medianiz de textura.</span><span class="sxs-lookup"><span data-stu-id="2948d-113">This method makes an internal call to [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) to retrieve and apply texture gutter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2948d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2948d-114">Requirements</span></span>



| <span data-ttu-id="2948d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2948d-115">Requirement</span></span> | <span data-ttu-id="2948d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2948d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2948d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2948d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2948d-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2948d-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2948d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2948d-119">Library</span></span><br/> | <dl> <span data-ttu-id="2948d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2948d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2948d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2948d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2948d-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="2948d-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




