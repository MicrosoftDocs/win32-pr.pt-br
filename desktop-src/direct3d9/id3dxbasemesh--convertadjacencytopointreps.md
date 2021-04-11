---
description: Converte informações de adjacência de malha em uma matriz de representantes de ponto.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'Método ID3DXBaseMesh:: ConvertAdjacencyToPointReps (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172977"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a><span data-ttu-id="4466f-103">Método ID3DXBaseMesh:: ConvertAdjacencyToPointReps</span><span class="sxs-lookup"><span data-stu-id="4466f-103">ID3DXBaseMesh::ConvertAdjacencyToPointReps method</span></span>

<span data-ttu-id="4466f-104">Converte informações de adjacência de malha em uma matriz de representantes de ponto.</span><span class="sxs-lookup"><span data-stu-id="4466f-104">Converts mesh adjacency information to an array of point representatives.</span></span>

## <a name="syntax"></a><span data-ttu-id="4466f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4466f-105">Syntax</span></span>


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a><span data-ttu-id="4466f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4466f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4466f-107">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4466f-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4466f-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4466f-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4466f-109">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="4466f-109">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="4466f-110">O número de bytes nessa matriz deve ser pelo menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="4466f-110">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="4466f-111">*pPRep* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4466f-111">*pPRep* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4466f-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4466f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4466f-113">Ponteiro para uma matriz de um DWORD por vértice da malha que será preenchida com dados representativos de ponto.</span><span class="sxs-lookup"><span data-stu-id="4466f-113">Pointer to an array of one DWORD per vertex of the mesh that will be filled with point representative data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4466f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4466f-114">Return value</span></span>

<span data-ttu-id="4466f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4466f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4466f-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4466f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4466f-117">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4466f-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4466f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4466f-118">Requirements</span></span>



| <span data-ttu-id="4466f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4466f-119">Requirement</span></span> | <span data-ttu-id="4466f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4466f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4466f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4466f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4466f-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4466f-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4466f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4466f-123">Library</span></span><br/> | <dl> <span data-ttu-id="4466f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4466f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4466f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4466f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4466f-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="4466f-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
