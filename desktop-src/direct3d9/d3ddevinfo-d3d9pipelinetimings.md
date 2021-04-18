---
description: Porcentagem de tempo de processamento de dados no pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: Estrutura de D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781012"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a><span data-ttu-id="094d4-103">\_Estrutura D3DDEVINFO D3D9PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="094d4-103">D3DDEVINFO\_D3D9PIPELINETIMINGS structure</span></span>

<span data-ttu-id="094d4-104">Porcentagem de tempo de processamento de dados no pipeline.</span><span class="sxs-lookup"><span data-stu-id="094d4-104">Percent of time processing data in the pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="094d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="094d4-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a><span data-ttu-id="094d4-106">Membros</span><span class="sxs-lookup"><span data-stu-id="094d4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="094d4-107">**VertexProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="094d4-107">**VertexProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="094d4-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="094d4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="094d4-109">Porcentagem de tempo gasto na execução de sombreadores de vértice.</span><span class="sxs-lookup"><span data-stu-id="094d4-109">Percent of time spent running vertex shaders.</span></span>

</dd> <dt>

<span data-ttu-id="094d4-110">**PixelProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="094d4-110">**PixelProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="094d4-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="094d4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="094d4-112">Porcentagem de tempo gasto na execução de sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="094d4-112">Percent of time spent running pixel shaders.</span></span>

</dd> <dt>

<span data-ttu-id="094d4-113">**OtherGPUProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="094d4-113">**OtherGPUProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="094d4-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="094d4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="094d4-115">Porcentagem de tempo gasto fazendo outro processamento.</span><span class="sxs-lookup"><span data-stu-id="094d4-115">Percent of time spent doing other processing.</span></span>

</dd> <dt>

<span data-ttu-id="094d4-116">**GPUIdleTimePercent**</span><span class="sxs-lookup"><span data-stu-id="094d4-116">**GPUIdleTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="094d4-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="094d4-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="094d4-118">Porcentagem de tempo não processando nada.</span><span class="sxs-lookup"><span data-stu-id="094d4-118">Percent of time not processing anything.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="094d4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="094d4-119">Remarks</span></span>

<span data-ttu-id="094d4-120">Para obter um melhor desempenho, é recomendável uma carga equilibrada.</span><span class="sxs-lookup"><span data-stu-id="094d4-120">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="094d4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="094d4-121">Requirements</span></span>



| <span data-ttu-id="094d4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="094d4-122">Requirement</span></span> | <span data-ttu-id="094d4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="094d4-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="094d4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="094d4-124">Header</span></span><br/> | <dl> <span data-ttu-id="094d4-125"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="094d4-125"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="094d4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="094d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094d4-127">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="094d4-127">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="094d4-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="094d4-128">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
