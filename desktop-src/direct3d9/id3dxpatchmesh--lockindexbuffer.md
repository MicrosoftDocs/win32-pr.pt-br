---
description: Bloquear o buffer de índice.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'Método ID3DXPatchMesh:: LockIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506537"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a><span data-ttu-id="af644-103">Método ID3DXPatchMesh:: LockIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="af644-103">ID3DXPatchMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="af644-104">Bloquear o buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="af644-104">Lock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="af644-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af644-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="af644-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af644-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af644-107">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="af644-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af644-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af644-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af644-109">Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado.</span><span class="sxs-lookup"><span data-stu-id="af644-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="af644-110">Para esse método, os sinalizadores válidos são:</span><span class="sxs-lookup"><span data-stu-id="af644-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="af644-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="af644-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="af644-112">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="af644-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="af644-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="af644-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="af644-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="af644-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="af644-115">Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="af644-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="af644-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="af644-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="af644-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="af644-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="af644-118">\*Ponteiro void para um buffer de memória que contém os dados de índice retornados.</span><span class="sxs-lookup"><span data-stu-id="af644-118">VOID\* pointer to a memory buffer containing the returned index data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af644-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af644-119">Return value</span></span>

<span data-ttu-id="af644-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af644-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af644-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af644-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af644-122">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="af644-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="af644-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="af644-123">Remarks</span></span>

<span data-ttu-id="af644-124">O buffer de índice é geralmente bloqueado, gravado e, em seguida, desbloqueado para leitura.</span><span class="sxs-lookup"><span data-stu-id="af644-124">The index buffer is usually locked, written to, and then unlocked for reading.</span></span> <span data-ttu-id="af644-125">Buffers de índice de malha de patch são buffers de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="af644-125">Patch mesh index buffers are 16-bit buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="af644-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af644-126">Requirements</span></span>



| <span data-ttu-id="af644-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="af644-127">Requirement</span></span> | <span data-ttu-id="af644-128">Valor</span><span class="sxs-lookup"><span data-stu-id="af644-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af644-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af644-129">Header</span></span><br/>  | <dl> <span data-ttu-id="af644-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="af644-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="af644-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af644-131">Library</span></span><br/> | <dl> <span data-ttu-id="af644-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af644-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af644-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="af644-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af644-134">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="af644-134">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="af644-135">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="af644-135">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
