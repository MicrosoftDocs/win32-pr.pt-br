---
description: Como o pipeline interpreta os dados de vértice associados ao estágio de Assembler de entrada. Esses valores primitivos de topologia determinam como os dados de vértice são renderizados na tela.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: '\_Enumeração de topologia primitiva de D3D11 \_'
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104989130"
---
# <a name="d3d11_primitive_topology-enumeration"></a><span data-ttu-id="2b14f-104">\_Enumeração de topologia primitiva de D3D11 \_</span><span class="sxs-lookup"><span data-stu-id="2b14f-104">D3D11\_PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="2b14f-105">Como o pipeline interpreta os dados de vértice associados ao estágio de Assembler de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b14f-105">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="2b14f-106">Esses valores primitivos de topologia determinam como os dados de vértice são renderizados na tela.</span><span class="sxs-lookup"><span data-stu-id="2b14f-106">These primitive topology values determine how the vertex data is rendered on screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b14f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b14f-107">Syntax</span></span>


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a><span data-ttu-id="2b14f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="2b14f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2b14f-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topologia primitiva de D3D11 \_ \_ indefinida**</span><span class="sxs-lookup"><span data-stu-id="2b14f-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-110">O estágio IA não foi inicializado com uma topologia primitiva.</span><span class="sxs-lookup"><span data-stu-id="2b14f-110">The IA stage has not been initialized with a primitive topology.</span></span> <span data-ttu-id="2b14f-111">O estágio IA não funcionará corretamente, a menos que uma topologia primitiva seja definida.</span><span class="sxs-lookup"><span data-stu-id="2b14f-111">The IA stage will not function properly unless a primitive topology is defined.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ do \_ ponto de topologia primitivo \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-113">Interprete os dados de vértice como uma lista de pontos.</span><span class="sxs-lookup"><span data-stu-id="2b14f-113">Interpret the vertex data as a list of points.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ da \_ linha de topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-115">Interprete os dados de vértice como uma lista de linhas.</span><span class="sxs-lookup"><span data-stu-id="2b14f-115">Interpret the vertex data as a list of lines.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**\_LINESTRIP de \_ topologia D3D11 primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-117">Interprete os dados de vértice como uma faixa de linha.</span><span class="sxs-lookup"><span data-stu-id="2b14f-117">Interpret the vertex data as a line strip.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**\_TRIângulolist de topologia primitiva de D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-119">Interprete os dados de vértice como uma lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="2b14f-119">Interpret the vertex data as a list of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**\_TRIANGLESTRIP de \_ topologia D3D11 primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-121">Interprete os dados de vértice como uma faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="2b14f-121">Interpret the vertex data as a triangle strip.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ da \_ linha da topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-123">Interprete os dados de vértice como uma lista de linhas com dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="2b14f-123">Interpret the vertex data as list of lines with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ \_ LINESTRIP de topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-125">Interprete os dados de vértice como uma faixa de linha com dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="2b14f-125">Interpret the vertex data as line strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ da \_ topologia primitiva de \_ triângulolist \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-127">Interprete os dados de vértice como uma lista de triângulos com dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="2b14f-127">Interpret the vertex data as list of triangles with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ \_ TRIANGLESTRIP de topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-129">Interprete os dados de vértice como uma faixa de triângulo com dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="2b14f-129">Interpret the vertex data as triangle strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**\_Patch de \_ ponto de controle da topologia D3D11 primitiva \_ 1 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-131">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-131">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia primitiva de D3D11 2**</span><span class="sxs-lookup"><span data-stu-id="2b14f-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-133">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-133">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST de ponto de controle \_ da topologia D3D11 primitiva 3**</span><span class="sxs-lookup"><span data-stu-id="2b14f-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-135">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-135">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia primitiva de D3D11 \_ 4 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-137">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-137">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 5 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-139">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-139">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 6**</span><span class="sxs-lookup"><span data-stu-id="2b14f-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-141">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-141">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 7**</span><span class="sxs-lookup"><span data-stu-id="2b14f-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-143">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-143">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 8**</span><span class="sxs-lookup"><span data-stu-id="2b14f-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-145">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-145">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 9 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-147">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-147">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 10 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-149">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-149">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 11**</span><span class="sxs-lookup"><span data-stu-id="2b14f-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-151">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-151">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ do \_ ponto de controle da topologia primitiva \_ 12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-153">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-153">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ de \_ \_ correção de \_ ponto de controle \_ \_ da topologia primitiva 13**</span><span class="sxs-lookup"><span data-stu-id="2b14f-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-155">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-155">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 14 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-157">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-157">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**\_Patch da topologia primitiva de D3D11 15 do \_ \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-159">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-159">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**\_Patch da topologia primitiva de D3D11 \_ \_ 16 \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-161">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-161">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 17 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-163">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-163">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ de \_ patch da topologia primitiva de 18 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-165">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-165">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 19 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-167">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-167">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ de \_ \_ \_ \_ patches da topologia \_ primitiva de 20 do ponto de controle**</span><span class="sxs-lookup"><span data-stu-id="2b14f-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-169">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-169">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ de \_ patch da topologia primitiva de \_ 21 \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-171">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-171">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ . \_ patch da topologia primitiva de 22 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-173">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-173">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ . \_ patch da topologia primitiva de 23 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-175">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-175">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**\_ \_ PATCHLIST da topologia D3D11 primitiva \_ 24 do \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-177">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-177">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 25 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-179">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-179">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**\_ \_ PATCHLIST da topologia D3D11 primitiva \_ 26 do \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-181">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-181">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 a \_ topologia de primitiva de 27 do \_ \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-183">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-183">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 28 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-185">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-185">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 da \_ topologia de primitiva de \_ \_ \_ \_ local 29 \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-187">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-187">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**Patch da topologia primitiva de D3D11 de \_ \_ \_ 30 \_ pontos de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-189">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-189">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ de \_ \_ patch do \_ ponto de controle da \_ topologia primitiva de 31 \_**</span><span class="sxs-lookup"><span data-stu-id="2b14f-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-191">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-191">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="2b14f-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 32**</span><span class="sxs-lookup"><span data-stu-id="2b14f-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="2b14f-193">Interprete os dados de vértice como uma lista de patches.</span><span class="sxs-lookup"><span data-stu-id="2b14f-193">Interpret the vertex data as a patch list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b14f-194">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b14f-194">Remarks</span></span>

<span data-ttu-id="2b14f-195">A enumeração de **\_ \_ topologia primitiva D3D11** é do tipo definido no arquivo de cabeçalho D3D11. h como uma enumeração de [**\_ \_ topologia primitiva do D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , que é totalmente definida no arquivo de cabeçalho D3DCommon. h.</span><span class="sxs-lookup"><span data-stu-id="2b14f-195">The **D3D11\_PRIMITIVE\_TOPOLOGY** enumeration is type defined in the D3D11.h header file as a [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) enumeration, which is fully defined in the D3DCommon.h header file.</span></span>
