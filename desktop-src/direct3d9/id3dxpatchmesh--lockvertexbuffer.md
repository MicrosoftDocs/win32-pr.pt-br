---
description: Bloquear o buffer de vértice.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'Método ID3DXPatchMesh:: LockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837955"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a><span data-ttu-id="eb2f6-103">Método ID3DXPatchMesh:: LockVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="eb2f6-103">ID3DXPatchMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="eb2f6-104">Bloquear o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-104">Lock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb2f6-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="eb2f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb2f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb2f6-107">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="eb2f6-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb2f6-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb2f6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb2f6-109">Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="eb2f6-110">Para esse método, os sinalizadores válidos são:</span><span class="sxs-lookup"><span data-stu-id="eb2f6-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="eb2f6-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="eb2f6-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="eb2f6-112">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="eb2f6-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="eb2f6-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="eb2f6-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="eb2f6-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="eb2f6-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="eb2f6-115">D3DLOCK \_ NOoverwrite</span><span class="sxs-lookup"><span data-stu-id="eb2f6-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="eb2f6-116">Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="eb2f6-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb2f6-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="eb2f6-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="eb2f6-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb2f6-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eb2f6-119">\*Ponteiro void para um buffer de memória que contém os dados de vértice retornados.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-119">VOID\* pointer to a memory buffer containing the returned vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb2f6-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb2f6-120">Return value</span></span>

<span data-ttu-id="eb2f6-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb2f6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb2f6-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eb2f6-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb2f6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb2f6-124">Remarks</span></span>

<span data-ttu-id="eb2f6-125">O buffer de vértice é geralmente bloqueado, gravado e, em seguida, desbloqueado para leitura.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-125">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

<span data-ttu-id="eb2f6-126">As malhas de patch usam buffers de índice de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-126">Patch meshes use 16-bit index buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb2f6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb2f6-127">Requirements</span></span>



| <span data-ttu-id="eb2f6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb2f6-128">Requirement</span></span> | <span data-ttu-id="eb2f6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="eb2f6-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2f6-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb2f6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="eb2f6-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb2f6-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="eb2f6-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb2f6-132">Library</span></span><br/> | <dl> <span data-ttu-id="eb2f6-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb2f6-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb2f6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb2f6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb2f6-135">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="eb2f6-135">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
