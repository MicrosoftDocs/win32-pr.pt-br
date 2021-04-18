---
description: Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado ID3DXPRTCompBuffer e adiciona os dados a um objeto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'Método ID3DXPRTCompBuffer:: ExtractToMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784683"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a><span data-ttu-id="1bc0b-103">Método ID3DXPRTCompBuffer:: ExtractToMesh</span><span class="sxs-lookup"><span data-stu-id="1bc0b-103">ID3DXPRTCompBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="1bc0b-104">Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) e adiciona os dados a um objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc0b-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc0b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bc0b-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="1bc0b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bc0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc0b-107">*NumPCA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bc0b-107">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc0b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bc0b-109">Número de coeficientes do PCA a serem extraídos do buffer.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-109">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1bc0b-110">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1bc0b-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc0b-111">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="1bc0b-112">Descrições de uso de vértice da malha.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-112">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="1bc0b-113">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="1bc0b-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bc0b-114">*UsageIndexStart* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bc0b-114">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc0b-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bc0b-116">Índice inicial para os coeficientes do PCA a serem armazenados na malha.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-116">Starting index for PCA coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1bc0b-117">*pScene* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1bc0b-117">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc0b-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1bc0b-119">Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) que armazenará os coeficientes do PCA.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-119">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc0b-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1bc0b-120">Return value</span></span>

<span data-ttu-id="1bc0b-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bc0b-122">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1bc0b-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc0b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bc0b-124">Requirements</span></span>



| <span data-ttu-id="1bc0b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bc0b-125">Requirement</span></span> | <span data-ttu-id="1bc0b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1bc0b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc0b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bc0b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1bc0b-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bc0b-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1bc0b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1bc0b-129">Library</span></span><br/> | <dl> <span data-ttu-id="1bc0b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bc0b-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bc0b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bc0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc0b-132">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="1bc0b-132">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
