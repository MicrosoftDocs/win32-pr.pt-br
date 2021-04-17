---
description: Cria um buffer de PRT (transferência radiante em computação) que pode ser compactado ou preenchido por um simulador. Essa função deve ser usada para criar buffers por vértice ou volume.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Função D3DXCreatePRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790387"
---
# <a name="d3dxcreateprtbuffer-function"></a><span data-ttu-id="e3a9b-104">Função D3DXCreatePRTBuffer</span><span class="sxs-lookup"><span data-stu-id="e3a9b-104">D3DXCreatePRTBuffer function</span></span>

<span data-ttu-id="e3a9b-105">Cria um buffer de PRT (transferência radiante em computação) que pode ser compactado ou preenchido por um simulador.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="e3a9b-106">Essa função deve ser usada para criar buffers por vértice ou volume.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-106">This function should be used to create per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a9b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3a9b-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e3a9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a9b-109">*NumSamples* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3a9b-109">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a9b-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3a9b-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3a9b-111">Número de vértices (ou texels) amostrados.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-111">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="e3a9b-112">*NumCoeffs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3a9b-112">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a9b-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3a9b-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3a9b-114">Número de coeficientes por local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-114">Number of coefficients per sample location.</span></span> <span data-ttu-id="e3a9b-115">Ao usar o PRT harmônica (SH) de esférico, o número de coeficientes deve ser pedido ², em que Order é a ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-115">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="e3a9b-116">A ordem deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-116">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e3a9b-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e3a9b-118">*NumChannels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3a9b-118">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a9b-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3a9b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3a9b-120">Número de canais de cores a serem definidos na malha.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-120">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="e3a9b-121">Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-121">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="e3a9b-122">*ppBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e3a9b-122">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a9b-123">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3a9b-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="e3a9b-124">Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) criado.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-124">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a9b-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3a9b-125">Return value</span></span>

<span data-ttu-id="e3a9b-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3a9b-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3a9b-127">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-127">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e3a9b-128">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-128">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a9b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a9b-129">Remarks</span></span>

<span data-ttu-id="e3a9b-130">Quando o buffer é criado, todos os valores são inicializados como zero.</span><span class="sxs-lookup"><span data-stu-id="e3a9b-130">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a9b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a9b-131">Requirements</span></span>



| <span data-ttu-id="e3a9b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a9b-132">Requirement</span></span> | <span data-ttu-id="e3a9b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e3a9b-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a9b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3a9b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a9b-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a9b-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e3a9b-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3a9b-136">Library</span></span><br/> | <dl> <span data-ttu-id="e3a9b-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3a9b-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3a9b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3a9b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a9b-139">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="e3a9b-139">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="e3a9b-140">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="e3a9b-140">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
