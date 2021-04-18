---
description: Bloqueia o buffer de malha que contém os dados de atributo de malha e retorna um ponteiro para ele.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'Método ID3DXMesh:: LockAttributeBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760487"
---
# <a name="id3dxmeshlockattributebuffer-method"></a><span data-ttu-id="6af5f-103">Método ID3DXMesh:: LockAttributeBuffer</span><span class="sxs-lookup"><span data-stu-id="6af5f-103">ID3DXMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="6af5f-104">Bloqueia o buffer de malha que contém os dados de atributo de malha e retorna um ponteiro para ele.</span><span class="sxs-lookup"><span data-stu-id="6af5f-104">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af5f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6af5f-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="6af5f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6af5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af5f-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6af5f-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5f-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6af5f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6af5f-109">Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado.</span><span class="sxs-lookup"><span data-stu-id="6af5f-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="6af5f-110">Para esse método, os sinalizadores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6af5f-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="6af5f-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="6af5f-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="6af5f-112">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="6af5f-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="6af5f-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="6af5f-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="6af5f-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6af5f-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="6af5f-115">Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="6af5f-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="6af5f-116">*ppData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6af5f-116">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6af5f-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6af5f-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="6af5f-118">Endereço de um ponteiro para um buffer que contém um DWORD para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="6af5f-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af5f-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6af5f-119">Return value</span></span>

<span data-ttu-id="6af5f-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6af5f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6af5f-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6af5f-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6af5f-122">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6af5f-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af5f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6af5f-123">Remarks</span></span>

<span data-ttu-id="6af5f-124">Se [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) tiver sido chamado, a malha também terá uma tabela de atributos que pode ser acessada usando o método [**ID3DXBaseMesh:: getattributetable**](id3dxbasemesh--getattributetable.md) .</span><span class="sxs-lookup"><span data-stu-id="6af5f-124">If [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) has been called, the mesh will also have an attribute table that can be accessed using the [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af5f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6af5f-125">Requirements</span></span>



| <span data-ttu-id="6af5f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af5f-126">Requirement</span></span> | <span data-ttu-id="6af5f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6af5f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6af5f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6af5f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6af5f-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6af5f-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6af5f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6af5f-130">Library</span></span><br/> | <dl> <span data-ttu-id="6af5f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6af5f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6af5f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6af5f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af5f-133">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="6af5f-133">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="6af5f-134">**ID3DXMesh::UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="6af5f-134">**ID3DXMesh::UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="6af5f-135">**ID3DXBaseMesh:: getattributetable**</span><span class="sxs-lookup"><span data-stu-id="6af5f-135">**ID3DXBaseMesh::GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[<span data-ttu-id="6af5f-136">**ID3DXMesh:: SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="6af5f-136">**ID3DXMesh::SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
