---
title: Função UpdateSubresources (D3dx12. h)
description: Atualiza os subrecursos, todas as matrizes de subrecurso devem ser preenchidas, normalmente chamando ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
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
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791547"
---
# <a name="updatesubresources-function"></a><span data-ttu-id="72ab8-104">Função UpdateSubresources</span><span class="sxs-lookup"><span data-stu-id="72ab8-104">UpdateSubresources function</span></span>

<span data-ttu-id="72ab8-105">Atualiza os subrecursos, todas as matrizes de subrecurso devem ser preenchidas, normalmente chamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="72ab8-105">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span>

## <a name="syntax"></a><span data-ttu-id="72ab8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72ab8-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="72ab8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72ab8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72ab8-108">*pCmdList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="72ab8-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="72ab8-110">A lista de comandos, como um ponteiro para um [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="72ab8-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-111">*pDestinationResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="72ab8-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="72ab8-113">O recurso de destino, como um ponteiro para um [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="72ab8-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-114">*pIntermediate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="72ab8-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="72ab8-116">O recurso intermediário, como um ponteiro para um [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="72ab8-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-117">*FirstSubresource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-117">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="72ab8-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="72ab8-119">O índice do primeiro subrecurso no recurso.</span><span class="sxs-lookup"><span data-stu-id="72ab8-119">The index of the first subresource in the resource.</span></span> <span data-ttu-id="72ab8-120">O intervalo de valores válidos é de 0 a D3D12 \_ req \_ subrecursos.</span><span class="sxs-lookup"><span data-stu-id="72ab8-120">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-121">*NumSubresources* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-121">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="72ab8-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="72ab8-123">O número de subrecursos no recurso.</span><span class="sxs-lookup"><span data-stu-id="72ab8-123">The number of subresources in the resource.</span></span> <span data-ttu-id="72ab8-124">O intervalo de valores válidos é de 0 a (D3D12 \_ req \_ subresources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="72ab8-124">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-125">*RequiredSize*</span><span class="sxs-lookup"><span data-stu-id="72ab8-125">*RequiredSize*</span></span> 
</dt> <dd>

<span data-ttu-id="72ab8-126">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="72ab8-126">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="72ab8-127">O tamanho necessário, em bytes, para a atualização.</span><span class="sxs-lookup"><span data-stu-id="72ab8-127">The required size, in bytes, for the update.</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-128">*pLayouts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-128">*pLayouts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-129">Tipo: **\* const [**D3D12 \_ colocou a \_ \_ superfície do subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)**</span><span class="sxs-lookup"><span data-stu-id="72ab8-129">Type: **const [**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)\***</span></span>

<span data-ttu-id="72ab8-130">Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para as estruturas que contêm a descrição e o posicionamento dos subrecursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="72ab8-130">Pointer to an array (of length *NumSubresources*) of pointers to the structures that contains the description and placement of the resource's subresources.</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-131">*pNumRows* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-131">*pNumRows* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-132">Tipo: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="72ab8-132">Type: **const [**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="72ab8-133">Ponteiro para uma matriz (de comprimento *NumSubresources*) de UINTs contendo o número de linhas para cada subrecurso.</span><span class="sxs-lookup"><span data-stu-id="72ab8-133">Pointer to an array (of length *NumSubresources*) of UINTS containing the number of rows for each subresource.</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-134">*pRowSizesInBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-134">*pRowSizesInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-135">Tipo: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="72ab8-135">Type: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="72ab8-136">Ponteiro para uma matriz (de comprimento *NumSubresources*) de UINTs contendo o tamanho, em bytes, de cada linha.</span><span class="sxs-lookup"><span data-stu-id="72ab8-136">Pointer to an array (of length *NumSubresources*) of UINTS containing the size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="72ab8-137">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72ab8-137">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab8-138">Tipo: **const [**D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***</span><span class="sxs-lookup"><span data-stu-id="72ab8-138">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="72ab8-139">Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para D3D12 estruturas de [**\_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contêm descrições dos dados de subrecurso usados para a atualização.</span><span class="sxs-lookup"><span data-stu-id="72ab8-139">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72ab8-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72ab8-140">Return value</span></span>

<span data-ttu-id="72ab8-141">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="72ab8-141">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="72ab8-142">O tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="72ab8-142">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="72ab8-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72ab8-143">Requirements</span></span>



| <span data-ttu-id="72ab8-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="72ab8-144">Requirement</span></span> | <span data-ttu-id="72ab8-145">Valor</span><span class="sxs-lookup"><span data-stu-id="72ab8-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72ab8-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72ab8-146">Header</span></span><br/>  | <dl> <span data-ttu-id="72ab8-147"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="72ab8-147"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="72ab8-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72ab8-148">Library</span></span><br/> | <dl> <span data-ttu-id="72ab8-149"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72ab8-149"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="72ab8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="72ab8-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="72ab8-151"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72ab8-151"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72ab8-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="72ab8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ab8-153">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="72ab8-153">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="72ab8-154">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="72ab8-154">Subresources</span></span>](subresources.md)
</dt> </dl>

 

