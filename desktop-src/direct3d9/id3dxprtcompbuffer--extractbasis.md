---
description: Extrai os vetores de base de ACP (análise de componente principal) para um determinado cluster de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'Método ID3DXPRTCompBuffer:: ExtractBasis (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765056"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a><span data-ttu-id="97485-103">Método ID3DXPRTCompBuffer:: ExtractBasis</span><span class="sxs-lookup"><span data-stu-id="97485-103">ID3DXPRTCompBuffer::ExtractBasis method</span></span>

<span data-ttu-id="97485-104">Extrai os vetores de base de ACP (análise de componente principal) para um determinado cluster de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="97485-104">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="97485-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97485-105">Syntax</span></span>


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a><span data-ttu-id="97485-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97485-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97485-107">*Cluster* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="97485-107">*Cluster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97485-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97485-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97485-109">Cluster para o qual a base será extraída.</span><span class="sxs-lookup"><span data-stu-id="97485-109">Cluster for which the basis will be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="97485-110">*pClusterBasis* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="97485-110">*pClusterBasis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97485-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="97485-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="97485-112">Ponteiro para uma matriz de dados de vetor de base para cluster.</span><span class="sxs-lookup"><span data-stu-id="97485-112">Pointer to an array of basis vector data for Cluster.</span></span> <span data-ttu-id="97485-113">O tamanho dos dados FLUTUANTEs armazenados será: (1 + número de vetores do PCA por cluster) \* (número de coeficientes) \* (número de canais de cores)</span><span class="sxs-lookup"><span data-stu-id="97485-113">The size of the FLOAT data stored will be: (1 + Number of PCA vectors per cluster) \* (Number of coefficients) \* (Number of color channels)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97485-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97485-114">Return value</span></span>

<span data-ttu-id="97485-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97485-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97485-116">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97485-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="97485-117">Se o método falhar, o valor a seguir será retornado.</span><span class="sxs-lookup"><span data-stu-id="97485-117">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="97485-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97485-118">Requirements</span></span>



| <span data-ttu-id="97485-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="97485-119">Requirement</span></span> | <span data-ttu-id="97485-120">Valor</span><span class="sxs-lookup"><span data-stu-id="97485-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97485-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97485-121">Header</span></span><br/>  | <dl> <span data-ttu-id="97485-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="97485-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="97485-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97485-123">Library</span></span><br/> | <dl> <span data-ttu-id="97485-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97485-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97485-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="97485-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97485-126">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="97485-126">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
