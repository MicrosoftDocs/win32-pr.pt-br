---
description: Especifica quais partes de dados de malha descartar do dispositivo. Usado com ID3DX10Mesh::D iscard.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: Enumeração de D3DX10_MESH_DISCARD_FLAGS (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930702"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a><span data-ttu-id="0a1e6-104">\_Enumeração de \_ sinalizadores de descarte de malha D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="0a1e6-104">D3DX10\_MESH\_DISCARD\_FLAGS enumeration</span></span>

<span data-ttu-id="0a1e6-105">Especifica quais partes de dados de malha descartar do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-105">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="0a1e6-106">Usado com [**ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md).</span><span class="sxs-lookup"><span data-stu-id="0a1e6-106">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a1e6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a1e6-107">Syntax</span></span>


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="0a1e6-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0a1e6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0a1e6-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_Buffer de \_ atributo de descarte de malha D3DX10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-110">Descartar o buffer de atributo.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-110">Discard the attribute buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0a1e6-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_Tabela de \_ atributos de descarte de malha D3DX10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_TABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-112">Descartar a tabela de atributos.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-112">Discard the attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="0a1e6-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**\_POINTREPS de \_ descarte de malha D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10\_MESH\_DISCARD\_POINTREPS**</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-114">Descartar o buffer de representantes do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-114">Discard the pointer reps buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0a1e6-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**\_Adjacência de \_ descarte de malha D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10\_MESH\_DISCARD\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-116">Descartar o buffer de adjacência.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-116">Discard the adjacency buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0a1e6-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**\_ \_ \_ Buffers de dispositivo de descarte de malha D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10\_MESH\_DISCARD\_DEVICE\_BUFFERS**</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-118">Descarte os buffers confirmados para o dispositivo (com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="0a1e6-118">Discard the buffers committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a1e6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a1e6-119">Requirements</span></span>



| <span data-ttu-id="0a1e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a1e6-120">Requirement</span></span> | <span data-ttu-id="0a1e6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0a1e6-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1e6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a1e6-122">Header</span></span><br/> | <dl> <span data-ttu-id="0a1e6-123"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-123"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a1e6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a1e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1e6-125">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="0a1e6-125">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




