---
description: Reamostrar um buffer ID3DXPRTBuffer de entrada e salvá-lo em um buffer de saída. Esse método pode ser usado para converter um buffer de vértice em um buffer de textura e vice-versa. Ele também pode ser usado para converter buffers de canal único em buffers de 3 canais e vice-versa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'Método ID3DXPRTEngine:: ResampleBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664086"
---
# <a name="id3dxprtengineresamplebuffer-method"></a><span data-ttu-id="bce64-105">Método ID3DXPRTEngine:: ResampleBuffer</span><span class="sxs-lookup"><span data-stu-id="bce64-105">ID3DXPRTEngine::ResampleBuffer method</span></span>

<span data-ttu-id="bce64-106">Reamostrar um buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada e salvá-lo em um buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="bce64-106">Resamples an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer and saves it to an output buffer.</span></span> <span data-ttu-id="bce64-107">Esse método pode ser usado para converter um buffer de vértice em um buffer de textura e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="bce64-107">This method can be used to convert a vertex buffer to a texture buffer and vice-versa.</span></span> <span data-ttu-id="bce64-108">Ele também pode ser usado para converter buffers de canal único em buffers de 3 canais e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="bce64-108">It can also be used to convert single-channel buffers to 3-channel buffers and vice-versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce64-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bce64-109">Syntax</span></span>


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a><span data-ttu-id="bce64-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bce64-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce64-111">*pBufferIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bce64-111">*pBufferIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce64-112">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bce64-112">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bce64-113">Ponteiro para o buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="bce64-113">Pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bce64-114">*pBufferOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bce64-114">*pBufferOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bce64-115">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bce64-115">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bce64-116">Ponteiro para o buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="bce64-116">Pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce64-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bce64-117">Return value</span></span>

<span data-ttu-id="bce64-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bce64-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bce64-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bce64-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bce64-120">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bce64-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce64-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bce64-121">Requirements</span></span>



| <span data-ttu-id="bce64-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bce64-122">Requirement</span></span> | <span data-ttu-id="bce64-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bce64-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bce64-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bce64-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bce64-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bce64-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bce64-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bce64-126">Library</span></span><br/> | <dl> <span data-ttu-id="bce64-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bce64-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bce64-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bce64-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce64-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="bce64-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 




