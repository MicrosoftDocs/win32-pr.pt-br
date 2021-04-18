---
description: Extrai dados de coeficiente de um buffer de canal único e adiciona os dados a um objeto ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'Método ID3DXPRTBuffer:: ExtractToMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760608"
---
# <a name="id3dxprtbufferextracttomesh-method"></a><span data-ttu-id="73588-103">Método ID3DXPRTBuffer:: ExtractToMesh</span><span class="sxs-lookup"><span data-stu-id="73588-103">ID3DXPRTBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="73588-104">Extrai dados de coeficiente de um buffer de canal único e adiciona os dados a um objeto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="73588-104">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="73588-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73588-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="73588-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73588-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73588-107">*NumCoefficients* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73588-107">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73588-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73588-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73588-109">Número de coeficientes a serem extraídos do buffer.</span><span class="sxs-lookup"><span data-stu-id="73588-109">Number of coefficients to extract from the buffer.</span></span> <span data-ttu-id="73588-110">Ao usar o PRT (transferência de radiante) de harmônica esférica (SH), o número de coeficientes deve ser o pedido ².</span><span class="sxs-lookup"><span data-stu-id="73588-110">When using spherical harmonic (SH) precomputed radiance transfer (PRT), the number of coefficients should be Order ².</span></span> <span data-ttu-id="73588-111">A ordem deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="73588-111">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="73588-112">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="73588-112">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73588-113">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="73588-113">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="73588-114">Descrições de uso de vértice da malha.</span><span class="sxs-lookup"><span data-stu-id="73588-114">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="73588-115">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="73588-115">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="73588-116">*UsageIndexStart* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73588-116">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73588-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73588-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73588-118">Índice inicial para coeficientes a serem armazenados na malha.</span><span class="sxs-lookup"><span data-stu-id="73588-118">Starting index for coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="73588-119">*pScene* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73588-119">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73588-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="73588-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="73588-121">Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) que armazenará coeficientes.</span><span class="sxs-lookup"><span data-stu-id="73588-121">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73588-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73588-122">Return value</span></span>

<span data-ttu-id="73588-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73588-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73588-124">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73588-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="73588-125">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="73588-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="73588-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73588-126">Requirements</span></span>



| <span data-ttu-id="73588-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="73588-127">Requirement</span></span> | <span data-ttu-id="73588-128">Valor</span><span class="sxs-lookup"><span data-stu-id="73588-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73588-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73588-129">Header</span></span><br/>  | <dl> <span data-ttu-id="73588-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="73588-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="73588-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73588-131">Library</span></span><br/> | <dl> <span data-ttu-id="73588-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73588-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73588-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="73588-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73588-134">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="73588-134">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
