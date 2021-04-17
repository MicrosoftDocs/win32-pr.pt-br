---
title: Função D3D12CalcSubresource (D3dx12. h)
description: Calcula um índice de subrecurso para uma textura.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- Função D3D12CalcSubresource
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762431"
---
# <a name="d3d12calcsubresource-function"></a><span data-ttu-id="a6072-104">Função D3D12CalcSubresource</span><span class="sxs-lookup"><span data-stu-id="a6072-104">D3D12CalcSubresource function</span></span>

<span data-ttu-id="a6072-105">Calcula um índice de subrecurso para uma textura.</span><span class="sxs-lookup"><span data-stu-id="a6072-105">Calculates a subresource index for a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6072-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6072-106">Syntax</span></span>


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="a6072-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6072-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6072-108">*MipSlice*</span><span class="sxs-lookup"><span data-stu-id="a6072-108">*MipSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="a6072-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6072-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6072-110">O índice de base zero para o nível de mipmap a ser abordado; 0 indica o primeiro e mais detalhado nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="a6072-110">The zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.</span></span>

</dd> <dt>

<span data-ttu-id="a6072-111">*ArraySlice*</span><span class="sxs-lookup"><span data-stu-id="a6072-111">*ArraySlice*</span></span> 
</dt> <dd>

<span data-ttu-id="a6072-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6072-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6072-113">O índice de base zero para o nível de matriz a ser abordado; Sempre use 0 para texturas de volume (3D).</span><span class="sxs-lookup"><span data-stu-id="a6072-113">The zero-based index for the array level to address; always use 0 for volume (3D) textures.</span></span>

</dd> <dt>

<span data-ttu-id="a6072-114">*PlaneSlice*</span><span class="sxs-lookup"><span data-stu-id="a6072-114">*PlaneSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="a6072-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6072-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6072-116">O índice de base zero para o nível de plano a ser abordado.</span><span class="sxs-lookup"><span data-stu-id="a6072-116">The zero-based index for the plane level to address.</span></span>

</dd> <dt>

<span data-ttu-id="a6072-117">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="a6072-117">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="a6072-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6072-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6072-119">O número de níveis de mipmap no recurso.</span><span class="sxs-lookup"><span data-stu-id="a6072-119">The number of mipmap levels in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a6072-120">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="a6072-120">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="a6072-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6072-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6072-122">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="a6072-122">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6072-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6072-123">Return value</span></span>

<span data-ttu-id="a6072-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6072-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6072-125">O índice que é igual a MipSlice + (ArraySlice \* MipLevels).</span><span class="sxs-lookup"><span data-stu-id="a6072-125">The index which equals MipSlice + (ArraySlice \* MipLevels).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6072-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6072-126">Remarks</span></span>

<span data-ttu-id="a6072-127">Um buffer é um recurso não estruturado e, portanto, é definido como contendo um único subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a6072-127">A buffer is an unstructured resource and is therefore defined as containing a single subresource.</span></span> <span data-ttu-id="a6072-128">As APIs que usam buffers não precisam de um índice de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a6072-128">APIs that take buffers do not need a subresource index.</span></span> <span data-ttu-id="a6072-129">Uma textura por outro lado é altamente estruturada.</span><span class="sxs-lookup"><span data-stu-id="a6072-129">A texture on the other hand is highly structured.</span></span> <span data-ttu-id="a6072-130">Cada objeto de textura pode conter um ou mais subrecursos, dependendo do tamanho da matriz e do número de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="a6072-130">Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.</span></span>

<span data-ttu-id="a6072-131">Para texturas de volume (3D), todas as fatias de um determinado nível de mipmap são um índice de subrecurso único.</span><span class="sxs-lookup"><span data-stu-id="a6072-131">For volume (3D) textures, all slices for a given mipmap level are a single subresource index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6072-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6072-132">Requirements</span></span>



| <span data-ttu-id="a6072-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6072-133">Requirement</span></span> | <span data-ttu-id="a6072-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a6072-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6072-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6072-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a6072-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6072-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="a6072-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6072-137">Library</span></span><br/> | <dl> <span data-ttu-id="a6072-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6072-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="a6072-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a6072-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="a6072-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6072-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6072-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6072-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6072-142">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="a6072-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a6072-143">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="a6072-143">Subresources</span></span>](subresources.md)
</dt> </dl>

 

