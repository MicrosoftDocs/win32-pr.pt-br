---
description: Sinalizadores usados para especificar as opções de criação para uma malha.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: Enumeração de D3DX10_MESH (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786959"
---
# <a name="d3dx10_mesh-enumeration"></a>\_Enumeração de malha D3DX10

Sinalizadores usados para especificar as opções de criação para uma malha.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 de \_ malha de \_ 32 \_ bits**
</dt> <dd>

A malha tem índices de 32 bits em vez de índices de 16 bits. Consulte Observações.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**\_Adjacência da malha D3DX10 \_ GS \_**
</dt> <dd>

Sinaliza que a malha contém dados de adjacência do sombreador de geometria.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma malha de 32 bits (D3DXMESH \_ 32bit) pode teoricamente dar suporte a (2 ³ ²)-1 rostos e vértices. No entanto, a alocação de memória para uma malha grande em um sistema operacional de 32 bits não é prática.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




