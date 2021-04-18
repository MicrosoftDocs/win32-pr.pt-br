---
description: Cria um buffer de PRT (transferência radiante em computação) que pode ser compactado ou preenchido por um simulador. Essa função deve ser usada para criar buffers por pixel.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: Função D3DXCreatePRTBufferTex (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764275"
---
# <a name="d3dxcreateprtbuffertex-function"></a><span data-ttu-id="98d59-104">Função D3DXCreatePRTBufferTex</span><span class="sxs-lookup"><span data-stu-id="98d59-104">D3DXCreatePRTBufferTex function</span></span>

<span data-ttu-id="98d59-105">Cria um buffer de PRT (transferência radiante em computação) que pode ser compactado ou preenchido por um simulador.</span><span class="sxs-lookup"><span data-stu-id="98d59-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="98d59-106">Essa função deve ser usada para criar buffers por pixel.</span><span class="sxs-lookup"><span data-stu-id="98d59-106">This function should be used to create per-pixel buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d59-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98d59-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="98d59-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98d59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d59-109">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98d59-109">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98d59-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98d59-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98d59-111">Largura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="98d59-111">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="98d59-112">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98d59-112">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98d59-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98d59-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98d59-114">Altura da textura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="98d59-114">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="98d59-115">*NumCoeffs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98d59-115">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98d59-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98d59-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98d59-117">Número de coeficientes por local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="98d59-117">Number of coefficients per sample location.</span></span> <span data-ttu-id="98d59-118">Ao usar o PRT harmônica (SH) de esférico, o número de coeficientes deve ser pedido ², em que Order é a ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="98d59-118">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="98d59-119">A ordem deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="98d59-119">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="98d59-120">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="98d59-120">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="98d59-121">*NumChannels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98d59-121">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98d59-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98d59-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98d59-123">Número de canais de cores a serem definidos na malha.</span><span class="sxs-lookup"><span data-stu-id="98d59-123">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="98d59-124">Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.</span><span class="sxs-lookup"><span data-stu-id="98d59-124">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="98d59-125">*ppBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98d59-125">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98d59-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="98d59-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="98d59-127">Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) criado.</span><span class="sxs-lookup"><span data-stu-id="98d59-127">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98d59-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98d59-128">Return value</span></span>

<span data-ttu-id="98d59-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98d59-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98d59-130">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="98d59-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="98d59-131">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="98d59-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d59-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="98d59-132">Remarks</span></span>

<span data-ttu-id="98d59-133">Quando o buffer é criado, todos os valores são inicializados como zero.</span><span class="sxs-lookup"><span data-stu-id="98d59-133">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d59-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98d59-134">Requirements</span></span>



| <span data-ttu-id="98d59-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d59-135">Requirement</span></span> | <span data-ttu-id="98d59-136">Valor</span><span class="sxs-lookup"><span data-stu-id="98d59-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98d59-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98d59-137">Header</span></span><br/>  | <dl> <span data-ttu-id="98d59-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="98d59-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="98d59-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98d59-139">Library</span></span><br/> | <dl> <span data-ttu-id="98d59-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98d59-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98d59-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="98d59-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d59-142">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="98d59-142">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="98d59-143">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="98d59-143">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
