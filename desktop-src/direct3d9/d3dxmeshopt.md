---
description: Especifica o tipo de otimização de malha a ser executada.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumeração D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810624"
---
# <a name="d3dxmeshopt-enumeration"></a>Enumeração D3DXMESHOPT

Especifica o tipo de otimização de malha a ser executada.

## <a name="syntax"></a>Syntax


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**
</dt> <dd>

Reordena os rostos para remover vértices e faces não utilizados.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

Reordena os rostos para otimizar para menos alterações de estado de pacote de atributo e ID3DXBaseMesh aprimorada [**::D rawsubset**](id3dxbasemesh--drawsubset.md) desempenho.

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

Reordena as faces para aumentar a taxa de acesso do cache de caches de vértice.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

Reordena os rostos para maximizar o comprimento dos triângulos adjacentes.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

Otimizar apenas as faces; Não Otimize os vértices.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

Enquanto a classificação de atributo, não divida os vértices compartilhados entre os grupos de atributos.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**
</dt> <dd>

Afeta o tamanho do cache de vértice. O uso desse sinalizador especifica um tamanho de cache de vértice padrão que funciona bem em hardware herdado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os \_ sinalizadores de otimização D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE são mutuamente exclusivos.

O \_ sinalizador D3DXMESHOPT SHAREVB foi removido desta enumeração. \_ \_ Em vez disso, use o compartilhamento vb do D3DXMESH, no [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
