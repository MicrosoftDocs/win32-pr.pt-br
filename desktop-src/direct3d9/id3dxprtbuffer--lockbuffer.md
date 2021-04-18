---
description: Bloqueia um intervalo de dados de exemplo de vértice ou Texel e Obtém um ponteiro para o local na memória de buffer.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'Método ID3DXPRTBuffer:: LockBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796114"
---
# <a name="id3dxprtbufferlockbuffer-method"></a><span data-ttu-id="70117-103">Método ID3DXPRTBuffer:: LockBuffer</span><span class="sxs-lookup"><span data-stu-id="70117-103">ID3DXPRTBuffer::LockBuffer method</span></span>

<span data-ttu-id="70117-104">Bloqueia um intervalo de dados de exemplo de vértice ou Texel e Obtém um ponteiro para o local na memória de buffer.</span><span class="sxs-lookup"><span data-stu-id="70117-104">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="70117-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70117-105">Syntax</span></span>


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="70117-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70117-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70117-107">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70117-107">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70117-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70117-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70117-109">Índice da amostra de dados de vértice ou Texel.</span><span class="sxs-lookup"><span data-stu-id="70117-109">Index of the sample of vertex or texel data.</span></span>

</dd> <dt>

<span data-ttu-id="70117-110">*NumSamples* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70117-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70117-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70117-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70117-112">Número de vértices (ou texels) amostrados.</span><span class="sxs-lookup"><span data-stu-id="70117-112">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="70117-113">*ppData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70117-113">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70117-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="70117-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="70117-115">Ponteiro para o local na memória em que começa a amostra inicial.</span><span class="sxs-lookup"><span data-stu-id="70117-115">Pointer to the location in memory where the Start sample begins.</span></span> <span data-ttu-id="70117-116">O layout de memória dos dados de buffer é:</span><span class="sxs-lookup"><span data-stu-id="70117-116">The memory layout of the buffer data is:</span></span>


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70117-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70117-117">Return value</span></span>

<span data-ttu-id="70117-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70117-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70117-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="70117-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="70117-120">Se o método falhar, o seguinte valor será retornado:</span><span class="sxs-lookup"><span data-stu-id="70117-120">If the method fails, the following value will be returned:</span></span>

## <a name="remarks"></a><span data-ttu-id="70117-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="70117-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="70117-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70117-122">Requirements</span></span>



| <span data-ttu-id="70117-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="70117-123">Requirement</span></span> | <span data-ttu-id="70117-124">Valor</span><span class="sxs-lookup"><span data-stu-id="70117-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70117-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70117-125">Header</span></span><br/>  | <dl> <span data-ttu-id="70117-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="70117-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="70117-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70117-127">Library</span></span><br/> | <dl> <span data-ttu-id="70117-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70117-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70117-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="70117-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70117-130">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="70117-130">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="70117-131">**ID3DXPRTBuffer::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="70117-131">**ID3DXPRTBuffer::GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[<span data-ttu-id="70117-132">**ID3DXPRTBuffer::GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="70117-132">**ID3DXPRTBuffer::GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[<span data-ttu-id="70117-133">**ID3DXPRTBuffer::GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="70117-133">**ID3DXPRTBuffer::GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
