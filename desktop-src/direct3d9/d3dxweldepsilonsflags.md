---
description: Opções de soldagem em vértices.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Enumeração D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298657"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a>Enumeração D3DXWELDEPSILONSFLAGS

Opções de soldagem em vértices.

## <a name="syntax"></a>Syntax


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**
</dt> <dd>

A solda em todos os vértices que estão no mesmo local. O uso desse sinalizador evita uma comparação de Épsilon entre componentes de vértice.

</dd> <dt>

<span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**
</dt> <dd>

Se um determinado componente de vértice estiver dentro de épsilon, modifique os vértices parcialmente correspondentes para que ambos os componentes sejam idênticos. Se todos os componentes forem iguais, remova um dos vértices.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**
</dt> <dd>

Instrui a solda para permitir apenas modificações em vértices e não na remoção. Esse sinalizador só será válido se D3DXWELDEPSILONS \_ WELDPARTIALMATCHES for definido. É útil modificar vértices para que sejam iguais, mas não permitir que os vértices sejam removidos.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**
</dt> <dd>

Instrui a solda não a dividir os vértices que estão em grupos de atributos separados. Quando o método [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) é chamado com o \_ sinalizador D3DXMESHOPT ATTRSORT, o sinalizador D3DXMESHOPT \_ DONOTSPLIT também será definido. A definição desse sinalizador pode tornar o processamento de vértice de software lento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 




