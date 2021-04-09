---
description: Bloqueia um buffer de índice e Obtém um ponteiro para a memória do buffer de índice.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'Método ID3DXBaseMesh:: LockIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012072"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a><span data-ttu-id="3d39f-103">Método ID3DXBaseMesh:: LockIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="3d39f-103">ID3DXBaseMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="3d39f-104">Bloqueia um buffer de índice e Obtém um ponteiro para a memória do buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="3d39f-104">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d39f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d39f-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="3d39f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d39f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d39f-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3d39f-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d39f-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d39f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d39f-109">Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado.</span><span class="sxs-lookup"><span data-stu-id="3d39f-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="3d39f-110">Para esse método, os sinalizadores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3d39f-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="3d39f-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="3d39f-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="3d39f-112">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="3d39f-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="3d39f-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="3d39f-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="3d39f-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3d39f-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="3d39f-115">Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="3d39f-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d39f-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3d39f-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3d39f-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d39f-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3d39f-118">\*Ponteiro void para um buffer que contém os dados do índice.</span><span class="sxs-lookup"><span data-stu-id="3d39f-118">VOID\* pointer to a buffer containing the index data.</span></span> <span data-ttu-id="3d39f-119">A contagem de índices nesse buffer será igual a [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span><span class="sxs-lookup"><span data-stu-id="3d39f-119">The count of indices in this buffer will be equal to [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d39f-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d39f-120">Return value</span></span>

<span data-ttu-id="3d39f-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d39f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d39f-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d39f-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3d39f-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3d39f-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d39f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d39f-124">Remarks</span></span>

<span data-ttu-id="3d39f-125">Ao trabalhar com buffers de índice, você tem permissão para fazer várias chamadas de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="3d39f-125">When working with index buffers, you are allowed to make multiple lock calls.</span></span> <span data-ttu-id="3d39f-126">No entanto, você deve garantir que o número de chamadas de bloqueio corresponda ao número de chamadas de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="3d39f-126">However, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="3d39f-127">Chamadas de DrawPrimitive não terão sucesso com qualquer contagem de bloqueios pendentes em qualquer buffer de índice definido no momento.</span><span class="sxs-lookup"><span data-stu-id="3d39f-127">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set index buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d39f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d39f-128">Requirements</span></span>



| <span data-ttu-id="3d39f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d39f-129">Requirement</span></span> | <span data-ttu-id="3d39f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3d39f-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d39f-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d39f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3d39f-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d39f-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3d39f-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d39f-133">Library</span></span><br/> | <dl> <span data-ttu-id="3d39f-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d39f-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d39f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d39f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d39f-136">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="3d39f-136">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
