---
description: Bloqueia o buffer de atributo.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'Método ID3DXPatchMesh:: LockAttributeBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105754088"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a><span data-ttu-id="d9a22-103">Método ID3DXPatchMesh:: LockAttributeBuffer</span><span class="sxs-lookup"><span data-stu-id="d9a22-103">ID3DXPatchMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="d9a22-104">Bloqueia o buffer de atributo.</span><span class="sxs-lookup"><span data-stu-id="d9a22-104">Locks the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9a22-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="d9a22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9a22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a22-107">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="d9a22-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a22-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9a22-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9a22-109">Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado.</span><span class="sxs-lookup"><span data-stu-id="d9a22-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="d9a22-110">Para esse método, os sinalizadores válidos são:</span><span class="sxs-lookup"><span data-stu-id="d9a22-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="d9a22-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="d9a22-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="d9a22-112">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="d9a22-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="d9a22-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="d9a22-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="d9a22-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d9a22-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="d9a22-115">Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="d9a22-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9a22-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d9a22-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a22-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9a22-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="d9a22-118">Endereço de um ponteiro para um buffer que contém um DWORD para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="d9a22-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a22-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9a22-119">Return value</span></span>

<span data-ttu-id="d9a22-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9a22-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9a22-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9a22-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d9a22-122">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d9a22-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a22-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9a22-123">Remarks</span></span>

<span data-ttu-id="d9a22-124">O buffer de atributo é geralmente bloqueado, gravado e, em seguida, desbloqueado para leitura.</span><span class="sxs-lookup"><span data-stu-id="d9a22-124">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a22-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9a22-125">Requirements</span></span>



| <span data-ttu-id="d9a22-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9a22-126">Requirement</span></span> | <span data-ttu-id="d9a22-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d9a22-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a22-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9a22-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d9a22-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9a22-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d9a22-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9a22-130">Library</span></span><br/> | <dl> <span data-ttu-id="d9a22-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9a22-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9a22-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9a22-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a22-133">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d9a22-133">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
