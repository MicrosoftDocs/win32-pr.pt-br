---
description: Bloqueia um buffer de vértice e Obtém um ponteiro para a memória de buffer de vértice.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'Método ID3DXBaseMesh:: LockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815467"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a><span data-ttu-id="d1e17-103">Método ID3DXBaseMesh:: LockVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="d1e17-103">ID3DXBaseMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="d1e17-104">Bloqueia um buffer de vértice e Obtém um ponteiro para a memória de buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="d1e17-104">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e17-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1e17-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="d1e17-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1e17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e17-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d1e17-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e17-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1e17-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1e17-109">Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado.</span><span class="sxs-lookup"><span data-stu-id="d1e17-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="d1e17-110">Para esse método, os sinalizadores válidos são:</span><span class="sxs-lookup"><span data-stu-id="d1e17-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="d1e17-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="d1e17-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="d1e17-112">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="d1e17-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="d1e17-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="d1e17-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="d1e17-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d1e17-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="d1e17-115">D3DLOCK \_ NOoverwrite</span><span class="sxs-lookup"><span data-stu-id="d1e17-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="d1e17-116">Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="d1e17-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e17-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d1e17-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e17-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1e17-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1e17-119">\*Ponteiro void para um buffer que contém os dados do vértice.</span><span class="sxs-lookup"><span data-stu-id="d1e17-119">VOID\* pointer to a buffer containing the vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e17-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1e17-120">Return value</span></span>

<span data-ttu-id="d1e17-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1e17-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1e17-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1e17-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1e17-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d1e17-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e17-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1e17-124">Remarks</span></span>

<span data-ttu-id="d1e17-125">Ao trabalhar com buffers de vértice, você tem permissão para fazer várias chamadas de bloqueio; no entanto, você deve garantir que o número de chamadas de bloqueio corresponda ao número de chamadas de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="d1e17-125">When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="d1e17-126">Chamadas de DrawPrimitive não terão sucesso com qualquer contagem de bloqueios pendentes em qualquer buffer de vértice definido no momento.</span><span class="sxs-lookup"><span data-stu-id="d1e17-126">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e17-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1e17-127">Requirements</span></span>



| <span data-ttu-id="d1e17-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e17-128">Requirement</span></span> | <span data-ttu-id="d1e17-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d1e17-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e17-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1e17-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d1e17-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e17-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d1e17-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1e17-132">Library</span></span><br/> | <dl> <span data-ttu-id="d1e17-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1e17-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1e17-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1e17-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e17-135">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d1e17-135">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
