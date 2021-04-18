---
title: Função UpdateSubresources (heap-alocação) (D3dx12. h)
description: Atualiza os subrecursos com uma implementação de alocação de heap.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
keywords:
- Função UpdateSubresources
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771609"
---
# <a name="updatesubresources-heap-allocating-function"></a><span data-ttu-id="5481e-104">Função UpdateSubresources (heap-alocando)</span><span class="sxs-lookup"><span data-stu-id="5481e-104">UpdateSubresources (heap-allocating) function</span></span>

<span data-ttu-id="5481e-105">Atualiza os subrecursos com uma implementação de alocação de heap.</span><span class="sxs-lookup"><span data-stu-id="5481e-105">Updates subresources with a heap-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5481e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5481e-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="5481e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5481e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5481e-108">*pCmdList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5481e-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5481e-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="5481e-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="5481e-110">Um ponteiro para a interface [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5481e-110">A pointer to the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface for the command list.</span></span>

</dd> <dt>

<span data-ttu-id="5481e-111">*pDestinationResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5481e-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5481e-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="5481e-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="5481e-113">Um ponteiro para a interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="5481e-113">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="5481e-114">*pIntermediate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5481e-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5481e-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="5481e-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="5481e-116">Um ponteiro para a interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa o recurso intermediário.</span><span class="sxs-lookup"><span data-stu-id="5481e-116">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="5481e-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="5481e-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="5481e-118">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5481e-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5481e-119">O deslocamento, em bytes, para o recurso intermediário.</span><span class="sxs-lookup"><span data-stu-id="5481e-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="5481e-120">*FirstSubresource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5481e-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5481e-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5481e-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5481e-122">O índice do primeiro subrecurso no recurso.</span><span class="sxs-lookup"><span data-stu-id="5481e-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="5481e-123">O intervalo de valores válidos é de 0 a D3D12 \_ req \_ subrecursos.</span><span class="sxs-lookup"><span data-stu-id="5481e-123">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="5481e-124">*NumSubresources* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5481e-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5481e-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5481e-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5481e-126">O número de subrecursos no recurso.</span><span class="sxs-lookup"><span data-stu-id="5481e-126">The number of subresources in the resource.</span></span> <span data-ttu-id="5481e-127">O intervalo de valores válidos é de 0 a (D3D12 \_ req \_ subresources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="5481e-127">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="5481e-128">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5481e-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5481e-129">Tipo: **[ **D3D12 \_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="5481e-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="5481e-130">Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para D3D12 estruturas de [**\_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contêm descrições dos dados de subrecurso usados para a atualização.</span><span class="sxs-lookup"><span data-stu-id="5481e-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5481e-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5481e-131">Return value</span></span>

<span data-ttu-id="5481e-132">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5481e-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5481e-133">O tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5481e-133">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5481e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5481e-134">Requirements</span></span>



| <span data-ttu-id="5481e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5481e-135">Requirement</span></span> | <span data-ttu-id="5481e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5481e-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5481e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5481e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="5481e-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5481e-138"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5481e-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5481e-139">Library</span></span><br/> | <dl> <span data-ttu-id="5481e-140"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5481e-140"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5481e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5481e-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="5481e-142"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5481e-142"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5481e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="5481e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5481e-144">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="5481e-144">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5481e-145">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="5481e-145">Subresources</span></span>](subresources.md)
</dt> </dl>

 

