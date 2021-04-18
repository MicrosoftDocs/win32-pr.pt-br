---
title: Função MemcpySubresource (D3dx12. h)
description: Copia uma linha de subrecurso por linha.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- Função MemcpySubresource
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781143"
---
# <a name="memcpysubresource-function"></a><span data-ttu-id="51905-104">Função MemcpySubresource</span><span class="sxs-lookup"><span data-stu-id="51905-104">MemcpySubresource function</span></span>

<span data-ttu-id="51905-105">Copia uma linha de subrecurso por linha.</span><span class="sxs-lookup"><span data-stu-id="51905-105">Copies a subresource row by row.</span></span>

## <a name="syntax"></a><span data-ttu-id="51905-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51905-106">Syntax</span></span>


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a><span data-ttu-id="51905-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51905-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51905-108">*pDest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51905-108">*pDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51905-109">Tipo: **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***</span><span class="sxs-lookup"><span data-stu-id="51905-109">Type: **const [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)\***</span></span>

<span data-ttu-id="51905-110">Um ponteiro para uma estrutura de [**\_ \_ dest D3D12 MEMCPY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) que descreve o destino da operação de cópia de memória.</span><span class="sxs-lookup"><span data-stu-id="51905-110">A pointer to a [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) structure that describes the destination of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="51905-111">*pSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51905-111">*pSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51905-112">Tipo: **const [**D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***</span><span class="sxs-lookup"><span data-stu-id="51905-112">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="51905-113">Um ponteiro para uma estrutura de [**\_ \_ dados de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que descreve a origem da operação de cópia de memória.</span><span class="sxs-lookup"><span data-stu-id="51905-113">A pointer to a [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structure that describes the source of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="51905-114">*RowSizeInBytes*</span><span class="sxs-lookup"><span data-stu-id="51905-114">*RowSizeInBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="51905-115">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="51905-115">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="51905-116">O tamanho, em bytes, de cada linha.</span><span class="sxs-lookup"><span data-stu-id="51905-116">The size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="51905-117">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="51905-117">*NumRows*</span></span> 
</dt> <dd>

<span data-ttu-id="51905-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="51905-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="51905-119">O número de linhas.</span><span class="sxs-lookup"><span data-stu-id="51905-119">The number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="51905-120">*NumSlices*</span><span class="sxs-lookup"><span data-stu-id="51905-120">*NumSlices*</span></span> 
</dt> <dd>

<span data-ttu-id="51905-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="51905-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="51905-122">O número de fatias.</span><span class="sxs-lookup"><span data-stu-id="51905-122">The number of slices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51905-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51905-123">Return value</span></span>

<span data-ttu-id="51905-124">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="51905-124">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51905-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="51905-125">Remarks</span></span>

<span data-ttu-id="51905-126">Considere também os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="51905-126">Also consider the following methods:</span></span>

-   [<span data-ttu-id="51905-127">**ID3D12Resource::WriteToSubresource**</span><span class="sxs-lookup"><span data-stu-id="51905-127">**ID3D12Resource::WriteToSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [<span data-ttu-id="51905-128">**ID3D12Resource::ReadFromSubresource**</span><span class="sxs-lookup"><span data-stu-id="51905-128">**ID3D12Resource::ReadFromSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [<span data-ttu-id="51905-129">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="51905-129">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a><span data-ttu-id="51905-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51905-130">Requirements</span></span>



| <span data-ttu-id="51905-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="51905-131">Requirement</span></span> | <span data-ttu-id="51905-132">Valor</span><span class="sxs-lookup"><span data-stu-id="51905-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51905-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51905-133">Header</span></span><br/>  | <dl> <span data-ttu-id="51905-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="51905-134"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="51905-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51905-135">Library</span></span><br/> | <dl> <span data-ttu-id="51905-136"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51905-136"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="51905-137">DLL</span><span class="sxs-lookup"><span data-stu-id="51905-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="51905-138"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51905-138"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51905-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="51905-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51905-140">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="51905-140">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="51905-141">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="51905-141">Subresources</span></span>](subresources.md)
</dt> </dl>

 

