---
description: Estrutura que contém os atributos de uma malha de patch.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Estrutura D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298478"
---
# <a name="d3dxpatchinfo-structure"></a>Estrutura D3DXPATCHINFO

Estrutura que contém os atributos de uma malha de patch.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Patchtype**
</dt> <dd>

Tipo: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**

</dd> <dd>

O tipo de patch. Para obter informações sobre tipos de patch, consulte [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).

</dd> <dt>

**Grau**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Grau das curvas usadas para construir o patch. Para obter informações sobre os graus com suporte, consulte [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

**Base**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Tipo de curva usado para construir o patch. Para obter informações sobre os tipos de base com suporte, consulte [**D3DBASISTYPE**](./d3dbasistype.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma malha é um conjunto de faces, cada uma delas é descrita por um polígono simples. Os objetos podem ser criados Conectando várias malhas juntas. Uma malha de patch é construída A partir de patches. Um patch é uma parte com quatro lados da geometria construída com base nas curvas. O tipo de curva usado e a ordem da curva podem ser variados para que a superfície do patch caiba quase qualquer forma de superfície.

Há suporte para os seguintes tipos de combinações de patch:



| Tipo de patch | Base       | Grau |
|------------|-------------|--------|
| Retângulo  | Bézier      | 2, 3, 5  |
| Retângulo  | B-spline    | 2, 3, 5  |
| Retângulo  | Catmull-Rom | 3      |
| Triangle   | Bézier      | 2, 3, 5  |
| N-patch    | N/D         | 3      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**Informações de D3DRECTPATCH \_**](d3drectpatch-info.md)
</dt> <dt>

[**Informações de D3DTRIPATCH \_**](d3dtripatch-info.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
