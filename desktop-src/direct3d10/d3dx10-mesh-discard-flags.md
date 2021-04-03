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
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>\_Enumeração de \_ sinalizadores de descarte de malha D3DX10 \_

Especifica quais partes de dados de malha descartar do dispositivo. Usado com [**ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_Buffer de \_ atributo de descarte de malha D3DX10 \_ \_**
</dt> <dd>

Descartar o buffer de atributo.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_Tabela de \_ atributos de descarte de malha D3DX10 \_ \_**
</dt> <dd>

Descartar a tabela de atributos.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**\_POINTREPS de \_ descarte de malha D3DX10 \_**
</dt> <dd>

Descartar o buffer de representantes do ponteiro.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**\_Adjacência de \_ descarte de malha D3DX10 \_**
</dt> <dd>

Descartar o buffer de adjacência.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**\_ \_ \_ Buffers de dispositivo de descarte de malha D3DX10 \_**
</dt> <dd>

Descarte os buffers confirmados para o dispositivo (com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




