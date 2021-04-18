---
description: Cria um objeto de buffer.
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: Função D3DXCreateBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc54813ea9947d263febcbe843702124c68ba747
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785960"
---
# <a name="d3dxcreatebuffer-function"></a><span data-ttu-id="2b4c9-103">Função D3DXCreateBuffer</span><span class="sxs-lookup"><span data-stu-id="2b4c9-103">D3DXCreateBuffer function</span></span>

<span data-ttu-id="2b4c9-104">Cria um objeto de buffer.</span><span class="sxs-lookup"><span data-stu-id="2b4c9-104">Creates a buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b4c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b4c9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="2b4c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b4c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b4c9-107">*NumBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b4c9-107">*NumBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4c9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b4c9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b4c9-109">Tamanho do buffer a ser criado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2b4c9-109">Size of the buffer to create, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2b4c9-110">*ppBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2b4c9-110">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4c9-111">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b4c9-111">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2b4c9-112">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que representa o objeto de buffer criado.</span><span class="sxs-lookup"><span data-stu-id="2b4c9-112">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, representing the created buffer object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b4c9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b4c9-113">Return value</span></span>

<span data-ttu-id="2b4c9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b4c9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b4c9-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b4c9-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b4c9-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2b4c9-116">If the function fails, the return value can be one of the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b4c9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b4c9-117">Requirements</span></span>



| <span data-ttu-id="2b4c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b4c9-118">Requirement</span></span> | <span data-ttu-id="2b4c9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2b4c9-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4c9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b4c9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2b4c9-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b4c9-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2b4c9-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b4c9-122">Library</span></span><br/> | <dl> <span data-ttu-id="2b4c9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b4c9-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b4c9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b4c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b4c9-125">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="2b4c9-125">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
