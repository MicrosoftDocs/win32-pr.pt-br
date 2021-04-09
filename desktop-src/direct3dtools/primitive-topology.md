---
description: Uma enumeração usada para indicar a topologia de uma malha. Consulte MeshDataVertCallback.
MS-HAID: vspixengine.PRIMITIVE\_TOPOLOGY
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração de PRIMITIVE_TOPOLOGY
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A845DD10-C735-4EA1-82D3-07F3B26508E7
api_name:
- PRIMITIVE_TOPOLOGY
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e448fcaaeaa2b1b50bd77b18ac4b3ac3f5e122a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010056"
---
# <a name="span-idvspixengineprimitive_topologyspanprimitive_topology-enumeration"></a><span data-ttu-id="b5a3b-104"><span id="vspixengine.primitive_topology"></span>\_Enumeração de topologia primitiva</span><span class="sxs-lookup"><span data-stu-id="b5a3b-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="b5a3b-105">Uma enumeração usada para indicar a topologia de uma malha.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-105">An enum used to indicate the topology of a mesh.</span></span> <span data-ttu-id="b5a3b-106">Consulte MeshDataVertCallback.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-106">See MeshDataVertCallback.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a3b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5a3b-107">Syntax</span></span>


```C++
} PRIMITIVE_TOPOLOGY;
```

## <a name="constants"></a><span data-ttu-id="b5a3b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b5a3b-108">Constants</span></span>

<span data-ttu-id="b5a3b-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**\_topologia primitiva \_ indefinida**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>  
<span data-ttu-id="b5a3b-110">A topologia da malha é indefinida.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-110">The topology of the mesh is undefined.</span></span>

<span data-ttu-id="b5a3b-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**\_ponto da topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>  
<span data-ttu-id="b5a3b-112">A topologia da malha é uma lista de pontos.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-112">The topology of the mesh is a point list.</span></span>

<span data-ttu-id="b5a3b-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**\_linhalist da topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>  
<span data-ttu-id="b5a3b-114">A topologia da malha é uma lista de linhas.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-114">The topology of the mesh is a line list.</span></span>

<span data-ttu-id="b5a3b-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**\_LINESTRIP de topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>  
<span data-ttu-id="b5a3b-116">A topologia da malha é uma faixa de linha.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-116">The topology of the mesh is a line strip.</span></span>

<span data-ttu-id="b5a3b-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**\_TRIângulolist da topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>  
<span data-ttu-id="b5a3b-118">A topologia da malha é uma lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-118">The topology of the mesh is a triangle list.</span></span>

<span data-ttu-id="b5a3b-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**\_TRIANGLESTRIP de topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>  
<span data-ttu-id="b5a3b-120">A topologia da malha é uma faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-120">The topology of the mesh is a triangle strip.</span></span>

<span data-ttu-id="b5a3b-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**\_TRIANGLEFAN de topologia primitiva \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLEFAN**</span></span>  
<span data-ttu-id="b5a3b-122">A topologia da malha é um ventilador de triângulo.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-122">The topology of the mesh is a triangle fan.</span></span>

<span data-ttu-id="b5a3b-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**linha da topologia de primitiva de \_ \_ linhas \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>  
<span data-ttu-id="b5a3b-124">A topologia da malha é uma lista de linhas com adjacências.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-124">The topology of the mesh is a line list with adjacency.</span></span>

<span data-ttu-id="b5a3b-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**\_LINESTRIP de topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>  
<span data-ttu-id="b5a3b-126">A topologia da malha é uma faixa de linhas com adjacências.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-126">The topology of the mesh is a line strip with adjacency.</span></span>

<span data-ttu-id="b5a3b-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**\_BIângulolist da topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>  
<span data-ttu-id="b5a3b-128">A topologia da malha é uma lista de triângulos com adjacências.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-128">The topology of the mesh is a triangle list with adjacency.</span></span>

<span data-ttu-id="b5a3b-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**\_TRIANGLESTRIP de topologia primitiva \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>  
<span data-ttu-id="b5a3b-130">A topologia da malha é uma faixa de triângulo com adjacência.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-130">The topology of the mesh is a triangle strip with adjacency.</span></span>

<span data-ttu-id="b5a3b-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 1 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-132">A topologia da malha é uma lista de patches com um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-132">The topology of the mesh is a patch list with 1 control point.</span></span>

<span data-ttu-id="b5a3b-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 2 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-134">A topologia da malha é uma lista de patches com dois pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-134">The topology of the mesh is a patch list with 2 control points.</span></span>

<span data-ttu-id="b5a3b-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 3 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-136">A topologia da malha é uma lista de patches com 3 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-136">The topology of the mesh is a patch list with 3 control points.</span></span>

<span data-ttu-id="b5a3b-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 4 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-138">A topologia da malha é uma lista de patches com 4 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-138">The topology of the mesh is a patch list with 4 control points.</span></span>

<span data-ttu-id="b5a3b-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**Patch da primitiva de \_ ponto de controle da topologia \_ 5 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-140">A topologia da malha é uma lista de patches com 5 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-140">The topology of the mesh is a patch list with 5 control points.</span></span>

<span data-ttu-id="b5a3b-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 6 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-142">A topologia da malha é uma lista de patches com 6 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-142">The topology of the mesh is a patch list with 6 control points.</span></span>

<span data-ttu-id="b5a3b-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 7 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-144">A topologia da malha é uma lista de patches com 7 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-144">The topology of the mesh is a patch list with 7 control points.</span></span>

<span data-ttu-id="b5a3b-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 8 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-146">A topologia da malha é uma lista de patches com 8 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-146">The topology of the mesh is a patch list with 8 control points.</span></span>

<span data-ttu-id="b5a3b-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 9 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-148">A topologia da malha é uma lista de patches com 9 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-148">The topology of the mesh is a patch list with 9 control points.</span></span>

<span data-ttu-id="b5a3b-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**Patch da primitiva de \_ ponto de controle da topologia \_ 10 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-150">A topologia da malha é uma lista de patches com 10 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-150">The topology of the mesh is a patch list with 10 control points.</span></span>

<span data-ttu-id="b5a3b-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 11 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-152">A topologia da malha é uma lista de patches com 11 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-152">The topology of the mesh is a patch list with 11 control points.</span></span>

<span data-ttu-id="b5a3b-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**Corpatch da \_ topologia primitiva 12 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-154">A topologia da malha é uma lista de patches com 12 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-154">The topology of the mesh is a patch list with 12 control points.</span></span>

<span data-ttu-id="b5a3b-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**\_Correção de \_ \_ ponto de \_ controle \_ da topologia primitiva 13**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-156">A topologia da malha é uma lista de patches com 13 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-156">The topology of the mesh is a patch list with 13 control points.</span></span>

<span data-ttu-id="b5a3b-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**\_Patch de \_ \_ ponto de \_ controle \_ da topologia primitiva 14**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-158">A topologia da malha é uma lista de patches com 14 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-158">The topology of the mesh is a patch list with 14 control points.</span></span>

<span data-ttu-id="b5a3b-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**Corpatch da \_ topologia primitiva 15 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-160">A topologia da malha é uma lista de patches com 15 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-160">The topology of the mesh is a patch list with 15 control points.</span></span>

<span data-ttu-id="b5a3b-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**Corpatch da \_ topologia primitiva 16 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-162">A topologia da malha é uma lista de patches com 16 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-162">The topology of the mesh is a patch list with 16 control points.</span></span>

<span data-ttu-id="b5a3b-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**\_Correção de \_ \_ ponto de \_ controle \_ da topologia primitiva 17**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-164">A topologia da malha é uma lista de patches com 17 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-164">The topology of the mesh is a patch list with 17 control points.</span></span>

<span data-ttu-id="b5a3b-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**\_Correção de \_ \_ ponto de \_ controle \_ da topologia do primitivo 18**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-166">A topologia da malha é uma lista de patches com 18 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-166">The topology of the mesh is a patch list with 18 control points.</span></span>

<span data-ttu-id="b5a3b-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**Corpatch da topologia de primitiva de \_ \_ 19 do \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-168">A topologia da malha é uma lista de patches com 19 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-168">The topology of the mesh is a patch list with 19 control points.</span></span>

<span data-ttu-id="b5a3b-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**\_Aplicação de patch da topologia primitiva \_ 20 \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-170">A topologia da malha é uma lista de patches com 20 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-170">The topology of the mesh is a patch list with 20 control points.</span></span>

<span data-ttu-id="b5a3b-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**\_Aplicação de \_ \_ patch de \_ ponto de controle \_ da topologia primitiva 21**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-172">A topologia da malha é uma lista de patches com 21 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-172">The topology of the mesh is a patch list with 21 control points.</span></span>

<span data-ttu-id="b5a3b-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**\_Aplicação de \_ \_ patch de \_ ponto de controle \_ da topologia primitiva 22**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-174">A topologia da malha é uma lista de patches com 22 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-174">The topology of the mesh is a patch list with 22 control points.</span></span>

<span data-ttu-id="b5a3b-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**\_Aplicação de patch da topologia primitiva 23 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-176">A topologia da malha é uma lista de patches com 23 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-176">The topology of the mesh is a patch list with 23 control points.</span></span>

<span data-ttu-id="b5a3b-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**\_Correção de \_ \_ ponto de \_ controle \_ de topologia de primitiva 24**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-178">A topologia da malha é uma lista de patches com 24 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-178">The topology of the mesh is a patch list with 24 control points.</span></span>

<span data-ttu-id="b5a3b-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**\_Patch do \_ \_ ponto de \_ controle \_ da topologia primitiva 25**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-180">A topologia da malha é uma lista de patches com 25 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-180">The topology of the mesh is a patch list with 25 control points.</span></span>

<span data-ttu-id="b5a3b-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 26 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-182">A topologia da malha é uma lista de patches com 26 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-182">The topology of the mesh is a patch list with 26 control points.</span></span>

<span data-ttu-id="b5a3b-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**\_Aplicação de \_ \_ patch de \_ ponto de controle \_ da topologia primitiva 27**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-184">A topologia da malha é uma lista de patches com 27 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-184">The topology of the mesh is a patch list with 27 control points.</span></span>

<span data-ttu-id="b5a3b-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**Retalho da \_ topologia primitiva 28 do \_ \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-186">A topologia da malha é uma lista de patches com 28 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-186">The topology of the mesh is a patch list with 28 control points.</span></span>

<span data-ttu-id="b5a3b-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**Retalho da topologia primitiva, \_ \_ \_ \_ PATCHLIST do ponto de controle \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-188">A topologia da malha é uma lista de patches com 29 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-188">The topology of the mesh is a patch list with 29 control points.</span></span>

<span data-ttu-id="b5a3b-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**Patch da topologia primitiva de \_ \_ 30 \_ pontos de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-190">A topologia da malha é uma lista de patches com 30 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-190">The topology of the mesh is a patch list with 30 control points.</span></span>

<span data-ttu-id="b5a3b-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**Patch da topologia primitiva de \_ \_ 31 \_ ponto de controle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-192">A topologia da malha é uma lista de patches com 31 pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-192">The topology of the mesh is a patch list with 31 control points.</span></span>

<span data-ttu-id="b5a3b-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**\_ \_ \_ \_ PATCHLIST do ponto de controle da topologia primitiva 32 \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b5a3b-194">A topologia da malha é uma lista de patches com pontos de controle de 32.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-194">The topology of the mesh is a patch list with 32 control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a3b-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a3b-195">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b5a3b-196">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5a3b-196">Header</span></span></p></td><td><span data-ttu-id="b5a3b-197">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b5a3b-197">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



