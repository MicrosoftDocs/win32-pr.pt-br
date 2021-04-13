---
description: Valida uma malha.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: Função D3DXValidMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298571"
---
# <a name="d3dxvalidmesh-function"></a><span data-ttu-id="57bf1-103">Função D3DXValidMesh</span><span class="sxs-lookup"><span data-stu-id="57bf1-103">D3DXValidMesh function</span></span>

<span data-ttu-id="57bf1-104">Valida uma malha.</span><span class="sxs-lookup"><span data-stu-id="57bf1-104">Validates a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="57bf1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57bf1-105">Syntax</span></span>


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="57bf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57bf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57bf1-107">*pMeshIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57bf1-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57bf1-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="57bf1-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="57bf1-109">Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , representando a malha a ser testada.</span><span class="sxs-lookup"><span data-stu-id="57bf1-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="57bf1-110">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57bf1-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57bf1-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="57bf1-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="57bf1-112">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha a ser testada.</span><span class="sxs-lookup"><span data-stu-id="57bf1-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="57bf1-113">*ppErrorsAndWarnings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="57bf1-113">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57bf1-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="57bf1-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="57bf1-115">Retorna um buffer que contém uma cadeia de caracteres de erros e avisos, que explicam os problemas encontrados na malha.</span><span class="sxs-lookup"><span data-stu-id="57bf1-115">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57bf1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57bf1-116">Return value</span></span>

<span data-ttu-id="57bf1-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="57bf1-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="57bf1-118">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="57bf1-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="57bf1-119">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DXERR \_ INVALIDMESH, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="57bf1-119">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="57bf1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="57bf1-120">Remarks</span></span>

<span data-ttu-id="57bf1-121">Esse método valida a malha verificando índices inválidos.</span><span class="sxs-lookup"><span data-stu-id="57bf1-121">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="57bf1-122">As informações de erro estão disponíveis na saída do depurador.</span><span class="sxs-lookup"><span data-stu-id="57bf1-122">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="57bf1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57bf1-123">Requirements</span></span>



| <span data-ttu-id="57bf1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57bf1-124">Requirement</span></span> | <span data-ttu-id="57bf1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="57bf1-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57bf1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57bf1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="57bf1-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="57bf1-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="57bf1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57bf1-128">Library</span></span><br/> | <dl> <span data-ttu-id="57bf1-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57bf1-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57bf1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="57bf1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bf1-131">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="57bf1-131">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
