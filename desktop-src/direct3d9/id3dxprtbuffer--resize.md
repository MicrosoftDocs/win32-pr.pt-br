---
description: Altera o número de amostras contidas no buffer.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'Método ID3DXPRTBuffer:: resize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c54044ffc9e166131faa16c9b438b497c658ef25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807254"
---
# <a name="id3dxprtbufferresize-method"></a><span data-ttu-id="d2af1-103">Método ID3DXPRTBuffer:: Resize</span><span class="sxs-lookup"><span data-stu-id="d2af1-103">ID3DXPRTBuffer::Resize method</span></span>

<span data-ttu-id="d2af1-104">Altera o número de amostras contidas no buffer.</span><span class="sxs-lookup"><span data-stu-id="d2af1-104">Changes the number of samples contained in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2af1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2af1-105">Syntax</span></span>


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a><span data-ttu-id="d2af1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2af1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2af1-107">*NewSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2af1-107">*NewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2af1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2af1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2af1-109">Número de amostras a serem contidas no buffer.</span><span class="sxs-lookup"><span data-stu-id="d2af1-109">Number of samples to be contained in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2af1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2af1-110">Return value</span></span>

<span data-ttu-id="d2af1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2af1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2af1-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2af1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2af1-113">Se o método falhar, o seguinte valor será retornado, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d2af1-113">If the method fails, the following value will be returned, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2af1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2af1-114">Requirements</span></span>



| <span data-ttu-id="d2af1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2af1-115">Requirement</span></span> | <span data-ttu-id="d2af1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d2af1-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2af1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2af1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d2af1-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2af1-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d2af1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2af1-119">Library</span></span><br/> | <dl> <span data-ttu-id="d2af1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2af1-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2af1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2af1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2af1-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="d2af1-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
