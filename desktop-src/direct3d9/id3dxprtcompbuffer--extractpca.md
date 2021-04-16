---
description: Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'Método ID3DXPRTCompBuffer:: ExtractPCA (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772572"
---
# <a name="id3dxprtcompbufferextractpca-method"></a><span data-ttu-id="80fff-103">Método ID3DXPRTCompBuffer:: ExtractPCA</span><span class="sxs-lookup"><span data-stu-id="80fff-103">ID3DXPRTCompBuffer::ExtractPCA method</span></span>

<span data-ttu-id="80fff-104">Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="80fff-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80fff-105">Syntax</span></span>


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a><span data-ttu-id="80fff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80fff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80fff-107">*StartPCA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80fff-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fff-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80fff-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80fff-109">Índice inicial para coeficientes de projeção do PCA para extrair do buffer.</span><span class="sxs-lookup"><span data-stu-id="80fff-109">Starting index for PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="80fff-110">*NumExtract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80fff-110">*NumExtract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fff-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80fff-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80fff-112">Número de coeficientes de projeção do PCA a serem extraídos do buffer.</span><span class="sxs-lookup"><span data-stu-id="80fff-112">Number of PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="80fff-113">*pPCACoefficients* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80fff-113">*pPCACoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fff-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="80fff-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80fff-115">Ponteiro para o local em que os coeficientes de análise do componente principal clusterizado (CPCA) são gravados.</span><span class="sxs-lookup"><span data-stu-id="80fff-115">Pointer to the location where clustered principal component analysis (CPCA) coefficients are written.</span></span> <span data-ttu-id="80fff-116">O tamanho dos dados gravados é (número de amostras) \* (número de coeficientes do PCA).</span><span class="sxs-lookup"><span data-stu-id="80fff-116">The size of the data written is (Number of Samples) \* (Number of PCA Coefficients).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80fff-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80fff-117">Return value</span></span>

<span data-ttu-id="80fff-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80fff-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80fff-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80fff-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="80fff-120">Se o método falhar, o valor a seguir será retornado.</span><span class="sxs-lookup"><span data-stu-id="80fff-120">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="80fff-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80fff-121">Requirements</span></span>



| <span data-ttu-id="80fff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="80fff-122">Requirement</span></span> | <span data-ttu-id="80fff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="80fff-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80fff-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80fff-124">Header</span></span><br/>  | <dl> <span data-ttu-id="80fff-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="80fff-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="80fff-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80fff-126">Library</span></span><br/> | <dl> <span data-ttu-id="80fff-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80fff-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80fff-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="80fff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fff-129">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="80fff-129">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
