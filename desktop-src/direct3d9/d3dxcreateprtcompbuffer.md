---
description: Cria um buffer de PRT (transferência de radiante de computação compactada) compactado a partir de um objeto ID3DXPRTBuffer descompactado. Essa função deve ser usada com buffers por vértice ou volume.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Função D3DXCreatePRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298633"
---
# <a name="d3dxcreateprtcompbuffer-function"></a><span data-ttu-id="b2b8a-104">Função D3DXCreatePRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="b2b8a-104">D3DXCreatePRTCompBuffer function</span></span>

<span data-ttu-id="b2b8a-105">Cria um buffer de PRT (transferência de radiante de computação compactada) compactado a partir de um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) descompactado.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-105">Creates a compressed precomputed radiance transfer (PRT) buffer from an uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="b2b8a-106">Essa função deve ser usada com buffers por vértice ou volume.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-106">This function should be used with per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b8a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2b8a-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b2b8a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2b8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b8a-109">*Qualidade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b2b8a-109">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b8a-110">Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-110">Type: **[**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span></span>

<span data-ttu-id="b2b8a-111">Qualidade da compactação de harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="b2b8a-111">Quality of spherical harmonic (SH) compression.</span></span> <span data-ttu-id="b2b8a-112">Consulte [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span><span class="sxs-lookup"><span data-stu-id="b2b8a-112">See [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b8a-113">*NumClusters* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2b8a-113">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b8a-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2b8a-115">Número de clusters a serem usados para compactação.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-115">Number of clusters to use for compression.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8a-116">*NumPCA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2b8a-116">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b8a-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2b8a-118">Número de vetores de base do PCA (análise de componente principal) a serem usados em cada cluster.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-118">Number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8a-119">*pCB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2b8a-119">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b8a-120">Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-120">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="b2b8a-121">Ponteiro opcional para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que é usada para calcular a porcentagem de computações de compactação de PRT concluídas.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-121">Optional pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that is used to compute the percentage of PRT compression computations completed.</span></span> <span data-ttu-id="b2b8a-122">A função de retorno de chamada deve ser implementada para retornar S \_ OK para continuar executando a rotina de compactação.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-122">The callback function must be implemented to return S\_OK to keep running the compression routine.</span></span> <span data-ttu-id="b2b8a-123">Qualquer outro valor irá parar a compactação.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-123">Any other value will halt compression.</span></span> <span data-ttu-id="b2b8a-124">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8a-125">*lpUserContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2b8a-125">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b8a-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2b8a-127">Ponteiro opcional para um valor definido pelo usuário passado para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b8a-127">Optional pointer to a user-defined value passed to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function.</span></span> <span data-ttu-id="b2b8a-128">Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-128">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span> <span data-ttu-id="b2b8a-129">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-129">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8a-130">*pBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2b8a-130">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b8a-131">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-131">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b2b8a-132">Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) não compactado que será compactado.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-132">Address of a pointer to the uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8a-133">*ppBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b2b8a-133">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b8a-134">Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2b8a-134">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="b2b8a-135">Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-135">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2b8a-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2b8a-136">Return value</span></span>

<span data-ttu-id="b2b8a-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2b8a-138">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2b8a-139">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b2b8a-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b8a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b8a-140">Requirements</span></span>



| <span data-ttu-id="b2b8a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b8a-141">Requirement</span></span> | <span data-ttu-id="b2b8a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b2b8a-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b8a-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2b8a-143">Header</span></span><br/>  | <dl> <span data-ttu-id="b2b8a-144"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b8a-144"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b2b8a-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2b8a-145">Library</span></span><br/> | <dl> <span data-ttu-id="b2b8a-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2b8a-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2b8a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2b8a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b8a-148">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="b2b8a-148">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="b2b8a-149">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-149">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="b2b8a-150">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="b2b8a-150">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
