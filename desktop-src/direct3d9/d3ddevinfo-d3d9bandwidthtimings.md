---
description: Métricas de taxa de transferência para ajudar na compreensão do desempenho de um aplicativo.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Estrutura de D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172961"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a><span data-ttu-id="6f61d-103">\_Estrutura D3DDEVINFO D3D9BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="6f61d-103">D3DDEVINFO\_D3D9BANDWIDTHTIMINGS structure</span></span>

<span data-ttu-id="6f61d-104">Métricas de taxa de transferência para ajudar na compreensão do desempenho de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f61d-104">Throughput metrics for help in understanding the performance of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f61d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f61d-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a><span data-ttu-id="6f61d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6f61d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f61d-107">**MaxBandwidthUtilized**</span><span class="sxs-lookup"><span data-stu-id="6f61d-107">**MaxBandwidthUtilized**</span></span>
</dt> <dd>

<span data-ttu-id="6f61d-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f61d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6f61d-109">A largura de banda ou a taxa máxima de transferência de dados da CPU do host para a GPU.</span><span class="sxs-lookup"><span data-stu-id="6f61d-109">The bandwidth or maximum data transfer rate from the host CPU to the GPU.</span></span> <span data-ttu-id="6f61d-110">Normalmente, essa é a largura de banda do barramento PCI ou AGP que conecta a CPU e a GPU.</span><span class="sxs-lookup"><span data-stu-id="6f61d-110">This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="6f61d-111">**FrontEndUploadMemoryUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="6f61d-111">**FrontEndUploadMemoryUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="6f61d-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f61d-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6f61d-113">Percentual de utilização de memória ao carregar dados da CPU do host para a GPU.</span><span class="sxs-lookup"><span data-stu-id="6f61d-113">Memory utilized percentage when uploading data from the host CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="6f61d-114">**VertexRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="6f61d-114">**VertexRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="6f61d-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f61d-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6f61d-116">Porcentagem de produtividade do vértice.</span><span class="sxs-lookup"><span data-stu-id="6f61d-116">Vertex throughput percentage.</span></span> <span data-ttu-id="6f61d-117">Este é o número de vértices processados em comparação com a taxa de processamento de vértice máximo teórica.</span><span class="sxs-lookup"><span data-stu-id="6f61d-117">This is the number of vertices processed compared to the theoretical maximum vertex processing rate.</span></span>

</dd> <dt>

<span data-ttu-id="6f61d-118">**TriangleSetupRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="6f61d-118">**TriangleSetupRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="6f61d-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f61d-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6f61d-120">Porcentagem de taxa de transferência de configuração de triângulo.</span><span class="sxs-lookup"><span data-stu-id="6f61d-120">Triangle set-up throughput percentage.</span></span> <span data-ttu-id="6f61d-121">Este é o número de triângulos que são configurados para rasterização em comparação com a taxa de configuração de triângulo máximo teórica.</span><span class="sxs-lookup"><span data-stu-id="6f61d-121">This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.</span></span>

</dd> <dt>

<span data-ttu-id="6f61d-122">**FillRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="6f61d-122">**FillRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="6f61d-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f61d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6f61d-124">Porcentagem de produtividade de preenchimento de pixel.</span><span class="sxs-lookup"><span data-stu-id="6f61d-124">Pixel fill throughput percentage.</span></span> <span data-ttu-id="6f61d-125">Este é o número de pixels que são preenchidos em comparação com o preenchimento de pixel teórico.</span><span class="sxs-lookup"><span data-stu-id="6f61d-125">This is the number of pixels that are filled compared to the theoretical pixel fill.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f61d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f61d-126">Requirements</span></span>



| <span data-ttu-id="6f61d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f61d-127">Requirement</span></span> | <span data-ttu-id="6f61d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6f61d-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f61d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f61d-129">Header</span></span><br/> | <dl> <span data-ttu-id="6f61d-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f61d-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f61d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f61d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f61d-132">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="6f61d-132">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="6f61d-133">**GetData**</span><span class="sxs-lookup"><span data-stu-id="6f61d-133">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
