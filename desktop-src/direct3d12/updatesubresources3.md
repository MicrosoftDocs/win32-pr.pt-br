---
title: Função UpdateSubresources (Stack-Alocation) (D3dx12. h)
description: Atualiza os subrecursos com uma implementação de alocação de pilha.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782749"
---
# <a name="updatesubresources-stack-allocating-function"></a><span data-ttu-id="964e8-104">Função UpdateSubresources (pilha-alocação)</span><span class="sxs-lookup"><span data-stu-id="964e8-104">UpdateSubresources (stack-allocating) function</span></span>

<span data-ttu-id="964e8-105">Atualiza os subrecursos com uma implementação de alocação de pilha.</span><span class="sxs-lookup"><span data-stu-id="964e8-105">Updates subresources with a stack-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="964e8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="964e8-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="964e8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="964e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="964e8-108">*pCmdList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="964e8-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964e8-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="964e8-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="964e8-110">A lista de comandos, como um ponteiro para um [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="964e8-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="964e8-111">*pDestinationResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="964e8-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964e8-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="964e8-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="964e8-113">O recurso de destino, como um ponteiro para um [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="964e8-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="964e8-114">*pIntermediate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="964e8-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964e8-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="964e8-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="964e8-116">O recurso intermediário, como um ponteiro para um [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="964e8-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="964e8-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="964e8-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="964e8-118">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="964e8-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="964e8-119">O deslocamento, em bytes, para o recurso intermediário.</span><span class="sxs-lookup"><span data-stu-id="964e8-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="964e8-120">*FirstSubresource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="964e8-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964e8-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="964e8-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="964e8-122">O índice do primeiro subrecurso no recurso.</span><span class="sxs-lookup"><span data-stu-id="964e8-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="964e8-123">Os valores válidos variam de 0 a *MaxSubresources*.</span><span class="sxs-lookup"><span data-stu-id="964e8-123">Valid values range from 0 to *MaxSubresources*.</span></span>

</dd> <dt>

<span data-ttu-id="964e8-124">*NumSubresources* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="964e8-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964e8-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="964e8-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="964e8-126">O número de subrecursos no recurso.</span><span class="sxs-lookup"><span data-stu-id="964e8-126">The number of subresources in the resource.</span></span> <span data-ttu-id="964e8-127">Os valores válidos variam de 1 a (*MaxSubresources*  -  *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="964e8-127">Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="964e8-128">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="964e8-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964e8-129">Tipo: **[ **D3D12 \_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="964e8-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="964e8-130">Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para D3D12 estruturas de [**\_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contêm descrições dos dados de subrecurso usados para a atualização.</span><span class="sxs-lookup"><span data-stu-id="964e8-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="964e8-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="964e8-131">Return value</span></span>

<span data-ttu-id="964e8-132">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="964e8-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="964e8-133">O tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="964e8-133">The size, in bytes, of the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="964e8-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="964e8-134">Remarks</span></span>

<span data-ttu-id="964e8-135">A declaração dessa função começa com: `template <UINT MaxSubresources>`</span><span class="sxs-lookup"><span data-stu-id="964e8-135">The declaration of this function begins with: `template <UINT MaxSubresources>`</span></span>

## <a name="requirements"></a><span data-ttu-id="964e8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="964e8-136">Requirements</span></span>



| <span data-ttu-id="964e8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="964e8-137">Requirement</span></span> | <span data-ttu-id="964e8-138">Valor</span><span class="sxs-lookup"><span data-stu-id="964e8-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="964e8-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="964e8-139">Header</span></span><br/>  | <dl> <span data-ttu-id="964e8-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="964e8-140"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="964e8-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="964e8-141">Library</span></span><br/> | <dl> <span data-ttu-id="964e8-142"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="964e8-142"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="964e8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="964e8-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="964e8-144"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="964e8-144"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="964e8-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="964e8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="964e8-146">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="964e8-146">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="964e8-147">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="964e8-147">Subresources</span></span>](subresources.md)
</dt> </dl>

 

