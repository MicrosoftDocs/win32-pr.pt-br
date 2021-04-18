---
description: Recupera as opções de malha habilitadas para esta malha no momento da criação.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'Método ID3DXBaseMesh:: getoptions (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785280"
---
# <a name="id3dxbasemeshgetoptions-method"></a><span data-ttu-id="1ffe2-103">Método ID3DXBaseMesh:: getoptions</span><span class="sxs-lookup"><span data-stu-id="1ffe2-103">ID3DXBaseMesh::GetOptions method</span></span>

<span data-ttu-id="1ffe2-104">Recupera as opções de malha habilitadas para esta malha no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-104">Retrieves the mesh options enabled for this mesh at creation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ffe2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ffe2-105">Syntax</span></span>


```C++
DWORD GetOptions();
```



## <a name="parameters"></a><span data-ttu-id="1ffe2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ffe2-106">Parameters</span></span>

<span data-ttu-id="1ffe2-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ffe2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ffe2-108">Return value</span></span>

<span data-ttu-id="1ffe2-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffe2-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ffe2-110">Retorna uma combinação de um ou mais dos sinalizadores a seguir, indicando as opções habilitadas para esta malha no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-110">Returns a combination of one or more of the following flags, indicating the options enabled for this mesh at creation time.</span></span>



| <span data-ttu-id="1ffe2-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1ffe2-111">Value</span></span>                   | <span data-ttu-id="1ffe2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ffe2-112">Description</span></span>                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ffe2-113">D3DXMESH \_ 32 bits</span><span class="sxs-lookup"><span data-stu-id="1ffe2-113">D3DXMESH\_32BIT</span></span>         | <span data-ttu-id="1ffe2-114">Use índices de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-114">Use 32-bit indices.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="1ffe2-115">D3DXMESH \_ DONOTCLIP</span><span class="sxs-lookup"><span data-stu-id="1ffe2-115">D3DXMESH\_DONOTCLIP</span></span>     | <span data-ttu-id="1ffe2-116">Use o \_ sinalizador de uso D3DUSAGE DONOTCLIP para os buffers de vértice e de índice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-116">Use the D3DUSAGE\_DONOTCLIP usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="1ffe2-117">D3DXMESH \_ dinâmico</span><span class="sxs-lookup"><span data-stu-id="1ffe2-117">D3DXMESH\_DYNAMIC</span></span>       | <span data-ttu-id="1ffe2-118">Equivalente a especificar o D3DXMESH \_ VB \_ Dynamic e D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-118">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>                                                                                                                   |
| <span data-ttu-id="1ffe2-119">D3DXMESH \_ RTPATCHES</span><span class="sxs-lookup"><span data-stu-id="1ffe2-119">D3DXMESH\_RTPATCHES</span></span>     | <span data-ttu-id="1ffe2-120">Use o \_ sinalizador de uso D3DUSAGE RTPATCHES para os buffers de vértice e de índice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-120">Use the D3DUSAGE\_RTPATCHES usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="1ffe2-121">D3DXMESH \_ NPATCHES</span><span class="sxs-lookup"><span data-stu-id="1ffe2-121">D3DXMESH\_NPATCHES</span></span>      | <span data-ttu-id="1ffe2-122">A especificação desse sinalizador faz com que o vértice e o buffer do índice da malha sejam criados com o \_ sinalizador D3DUSAGE NPATCHES.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-122">Specifying this flag causes the vertex and index buffer of the mesh to be created with D3DUSAGE\_NPATCHES flag.</span></span> <span data-ttu-id="1ffe2-123">Isso será necessário se o objeto de malha for renderizado usando o aprimoramento de N-patch.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-123">This is required if the mesh object is to be rendered using N-Patch enhancement.</span></span> |
| <span data-ttu-id="1ffe2-124">\_Gerenciado D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="1ffe2-124">D3DXMESH\_MANAGED</span></span>       | <span data-ttu-id="1ffe2-125">Equivalente a especificar o D3DXMESH \_ VB \_ gerenciado e o D3DXMESH \_ IB \_ gerenciados.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-125">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>                                                                                                                   |
| <span data-ttu-id="1ffe2-126">Pontos de D3DXMESH \_</span><span class="sxs-lookup"><span data-stu-id="1ffe2-126">D3DXMESH\_POINTS</span></span>        | <span data-ttu-id="1ffe2-127">Use o \_ sinalizador de uso de pontos D3DUSAGE para os buffers de vértice e de índice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-127">Use the D3DUSAGE\_POINTS usage flag for vertex and index buffers.</span></span>                                                                                                                                |
| <span data-ttu-id="1ffe2-128">D3DXMESH \_ IB \_ Dynamic</span><span class="sxs-lookup"><span data-stu-id="1ffe2-128">D3DXMESH\_IB\_DYNAMIC</span></span>   | <span data-ttu-id="1ffe2-129">Use o \_ sinalizador de uso dinâmico D3DUSAGE para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-129">Use the D3DUSAGE\_DYNAMIC usage flag for index buffers.</span></span>                                                                                                                                          |
| <span data-ttu-id="1ffe2-130">D3DXMESH \_ IB \_ gerenciado</span><span class="sxs-lookup"><span data-stu-id="1ffe2-130">D3DXMESH\_IB\_MANAGED</span></span>   | <span data-ttu-id="1ffe2-131">Use a \_ classe de memória gerenciada D3DPOOL para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-131">Use the D3DPOOL\_MANAGED memory class for index buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="1ffe2-132">D3DXMESH \_ IB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="1ffe2-132">D3DXMESH\_IB\_SYSTEMMEM</span></span> | <span data-ttu-id="1ffe2-133">Use a \_ classe de memória D3DPOOL SYSTEMMEM para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-133">Use the D3DPOOL\_SYSTEMMEM memory class for index buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="1ffe2-134">D3DXMESH \_ IB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="1ffe2-134">D3DXMESH\_IB\_WRITEONLY</span></span> | <span data-ttu-id="1ffe2-135">Use o \_ sinalizador de uso de WRITEONLY D3DUSAGE para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-135">Use the D3DUSAGE\_WRITEONLY usage flag for index buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="1ffe2-136">D3DXMESH \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="1ffe2-136">D3DXMESH\_SYSTEMMEM</span></span>     | <span data-ttu-id="1ffe2-137">Equivalente a especificar D3DXMESH \_ VB \_ SYSTEMMEM e D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-137">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>                                                                                                               |
| <span data-ttu-id="1ffe2-138">D3DXMESH \_ VB \_ Dynamic</span><span class="sxs-lookup"><span data-stu-id="1ffe2-138">D3DXMESH\_VB\_DYNAMIC</span></span>   | <span data-ttu-id="1ffe2-139">Use o \_ sinalizador de uso dinâmico D3DUSAGE para buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-139">Use the D3DUSAGE\_DYNAMIC usage flag for vertex buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="1ffe2-140">Gerenciado por D3DXMESH \_ VB \_</span><span class="sxs-lookup"><span data-stu-id="1ffe2-140">D3DXMESH\_VB\_MANAGED</span></span>   | <span data-ttu-id="1ffe2-141">Use a \_ classe de memória gerenciada D3DPOOL para buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-141">Use the D3DPOOL\_MANAGED memory class for vertex buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="1ffe2-142">D3DXMESH \_ VB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="1ffe2-142">D3DXMESH\_VB\_SYSTEMMEM</span></span> | <span data-ttu-id="1ffe2-143">Use a \_ classe de memória D3DPOOL SYSTEMMEM para os buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-143">Use the D3DPOOL\_SYSTEMMEM memory class for vertex buffers.</span></span>                                                                                                                                      |
| <span data-ttu-id="1ffe2-144">D3DXMESH \_ VB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="1ffe2-144">D3DXMESH\_VB\_WRITEONLY</span></span> | <span data-ttu-id="1ffe2-145">Use o \_ sinalizador de uso de WRITEONLY D3DUSAGE para buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-145">Use the D3DUSAGE\_WRITEONLY usage flag for vertex buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="1ffe2-146">\_WRITEONLY D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="1ffe2-146">D3DXMESH\_WRITEONLY</span></span>     | <span data-ttu-id="1ffe2-147">Equivalente a especificar ambos D3DXMESH \_ VB \_ WRITEONLY e D3DXMESH \_ IB \_ WriteOnly.</span><span class="sxs-lookup"><span data-stu-id="1ffe2-147">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>                                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="1ffe2-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ffe2-148">Requirements</span></span>



| <span data-ttu-id="1ffe2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ffe2-149">Requirement</span></span> | <span data-ttu-id="1ffe2-150">Valor</span><span class="sxs-lookup"><span data-stu-id="1ffe2-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ffe2-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ffe2-151">Header</span></span><br/>  | <dl> <span data-ttu-id="1ffe2-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ffe2-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1ffe2-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ffe2-153">Library</span></span><br/> | <dl> <span data-ttu-id="1ffe2-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ffe2-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ffe2-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ffe2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ffe2-156">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="1ffe2-156">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
