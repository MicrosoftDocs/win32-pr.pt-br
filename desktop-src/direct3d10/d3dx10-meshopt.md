---
description: Enumeração de D3DX10_MESHOPT-especifica o tipo de otimização de malha a ser executada.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Enumeração de D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105444"
---
# <a name="d3dx10_meshopt-enumeration"></a>\_Enumeração D3DX10 MESHOPT

Especifica o tipo de otimização de malha a ser executada.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ Compact**
</dt> <dd>

Reordena os rostos para remover vértices e faces não utilizados.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**\_Classificação D3DX10 MESHOPT \_ attr \_**
</dt> <dd>

Reordena os rostos para otimizar para menos alterações de estado de pacote de atributo e desempenho de DrawSubset aprimorado.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**\_Cache de \_ vértice D3DX10 MESHOPT \_**
</dt> <dd>

Reordena as faces para aumentar a taxa de acesso do cache de caches de vértice.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**\_REordenar D3DX10 MESHOPT \_ strip \_**
</dt> <dd>

Reordena os rostos para maximizar o comprimento dos triângulos adjacentes.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ ignorar \_ reverte**
</dt> <dd>

Otimizar apenas as faces; Não Otimize os vértices.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ \_ não \_ divide**
</dt> <dd>

Enquanto a classificação de atributo, não divida os vértices compartilhados entre os grupos de atributos.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ dispositivo \_ independente**
</dt> <dd>

Afeta o tamanho do cache de vértice. O uso desse sinalizador especifica um tamanho de cache de vértice padrão que funciona bem em hardware herdado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os \_ sinalizadores de otimização D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE são mutuamente exclusivos.

O \_ sinalizador D3DXMESHOPT SHAREVB foi removido desta enumeração. \_ \_ Em vez disso, use o compartilhamento vb do D3DXMESH, no D3DXMESH.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




