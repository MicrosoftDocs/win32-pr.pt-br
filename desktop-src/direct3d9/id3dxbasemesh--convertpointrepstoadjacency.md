---
description: Converte dados representativos de ponto em informações de adjacência de malha.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'Método ID3DXBaseMesh:: ConvertPointRepsToAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807933"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a><span data-ttu-id="dd4de-103">Método ID3DXBaseMesh:: ConvertPointRepsToAdjacency</span><span class="sxs-lookup"><span data-stu-id="dd4de-103">ID3DXBaseMesh::ConvertPointRepsToAdjacency method</span></span>

<span data-ttu-id="dd4de-104">Converte dados representativos de ponto em informações de adjacência de malha.</span><span class="sxs-lookup"><span data-stu-id="dd4de-104">Converts point representative data to mesh adjacency information.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd4de-105">Syntax</span></span>


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="dd4de-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd4de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd4de-107">*pPRep* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd4de-107">*pPRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd4de-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dd4de-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dd4de-109">Ponteiro para uma matriz de um DWORD por vértice da malha que contém dados representativos de ponto.</span><span class="sxs-lookup"><span data-stu-id="dd4de-109">Pointer to an array of one DWORD per vertex of the mesh that contains point representative data.</span></span> <span data-ttu-id="dd4de-110">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="dd4de-110">This parameter is optional.</span></span> <span data-ttu-id="dd4de-111">O fornecimento de um valor **nulo** fará com que esse parâmetro seja interpretado como uma matriz de "identidade".</span><span class="sxs-lookup"><span data-stu-id="dd4de-111">Supplying a **NULL** value will cause this parameter to be interpreted as an "identity" array.</span></span>

</dd> <dt>

<span data-ttu-id="dd4de-112">*pAdjacency* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="dd4de-112">*pAdjacency* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd4de-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dd4de-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dd4de-114">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="dd4de-114">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="dd4de-115">O número de bytes nessa matriz deve ser pelo menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="dd4de-115">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd4de-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd4de-116">Return value</span></span>

<span data-ttu-id="dd4de-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd4de-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd4de-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dd4de-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dd4de-119">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dd4de-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd4de-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd4de-120">Requirements</span></span>



| <span data-ttu-id="dd4de-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd4de-121">Requirement</span></span> | <span data-ttu-id="dd4de-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dd4de-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4de-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd4de-123">Header</span></span><br/>  | <dl> <span data-ttu-id="dd4de-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd4de-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dd4de-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd4de-125">Library</span></span><br/> | <dl> <span data-ttu-id="dd4de-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd4de-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd4de-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd4de-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4de-128">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="dd4de-128">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
