---
description: D3DX10_MESHOPT enumeração - especifica o tipo de otimização de malha a ser executada.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT enumeração (D3DX10Mesh.h)
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
ms.openlocfilehash: 193bf832f00c9812a515ae9b5c478f6baed637d87605e9f8d04349a12d79aac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989216"
---
# <a name="d3dx10_meshopt-enumeration"></a>Enumeração D3DX10 \_ MESHOPT

Especifica o tipo de otimização de malha a ser executada.

## <a name="syntax"></a>Syntax


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

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**
</dt> <dd>

Reordena faces para remover vértices e rostos nãoutilados.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ SORT**
</dt> <dd>

Reordena rostos para otimizar para menos alterações de estado do pacote de atributos e desempenho aprimorado de DrawSubset.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**CACHE DE \_ \_ VÉRTICE D3DX10 MESHOPT \_**
</dt> <dd>

Reordena rostos para aumentar a taxa de acertos de cache de caches de vértice.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10 \_ MESHOPT \_ STRIP \_ REORDER**
</dt> <dd>

Reordena faces para maximizar o comprimento de triângulos adjacentes.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ IGNORE \_ VERTS**
</dt> <dd>

Otimizar apenas as faces; não otimize os vértices.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ NÃO \_ \_ DIVIDE**
</dt> <dd>

Durante a classificação de atributo, não divida os vértices compartilhados entre grupos de atributos.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ DEVICE \_ INDEPENDENT**
</dt> <dd>

Afeta o tamanho do cache de vértice. Usar esse sinalizador especifica um tamanho de cache de vértice padrão que funciona bem no hardware herdado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os sinalizadores de otimização \_ DE VERTEXCACHE D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ são mutuamente exclusivos.

O sinalizador D3DXMESHOPT \_ SHAREVB foi removido dessa enumeração. Use d3DXMESH \_ VB \_ SHARE em vez disso, em D3DXMESH.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




