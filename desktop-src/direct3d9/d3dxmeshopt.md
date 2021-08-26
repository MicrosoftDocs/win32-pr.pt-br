---
description: Enumeração D3DXMESHOPT – especifica o tipo de otimização de malha a ser executada.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumeração D3DXMESHOPT (D3dx9mesh.h)
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
ms.openlocfilehash: d4d26538832a698909ace59da42b13ae51aef93d2d4d622b687f324a62d8361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986486"
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

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**
</dt> <dd>

Reordena faces para remover vértices e rostos nãoutilados.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

Reordena rostos para otimizar para menos alterações de estado do pacote de atributos e desempenho Aprimorado [**ID3DXBaseMesh::D rawSubset.**](id3dxbasemesh--drawsubset.md)

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

Reordena rostos para aumentar a taxa de acertos de cache de caches de vértice.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

Reordena faces para maximizar o comprimento de triângulos adjacentes.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

Otimizar apenas as faces; não otimize os vértices.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

Durante a classificação de atributo, não divida os vértices compartilhados entre grupos de atributos.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**
</dt> <dd>

Afeta o tamanho do cache de vértice. Usar esse sinalizador especifica um tamanho de cache de vértice padrão que funciona bem no hardware herdado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os sinalizadores de otimização \_ DE VERTEXCACHE D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ são mutuamente exclusivos.

O sinalizador D3DXMESHOPT \_ SHAREVB foi removido dessa enumeração. Use d3DXMESH VB SHARE em vez \_ \_ disso, [**em D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
