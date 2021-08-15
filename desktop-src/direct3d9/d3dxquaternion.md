---
description: Estrutura D3DXQUATERNION (D3dx9math.h) – descreve um quaternion.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Estrutura D3DXQUATERNION (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 9818772163d5286d764c0f025b955a663457dd853c2db0efec8ad0b0a4967c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524608"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>Estrutura D3DXQUATERNION (D3dx9math.h)

Descreve um quaterão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a>Membros

<dl> <dt>

**x**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente y.

</dd> <dt>

**Z**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente z.

</dd> <dt>

**w**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente w.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quaterões adicionam um quarto elemento aos valores x, y, z que definem um vetor, resultando em \[ \] vetores 4D arbitrários. No entanto, o seguinte ilustra como cada elemento de um quaternão de unidade está relacionado a uma rotação de ângulo do eixo (em que q representa um quatternion de unidade (x, y, z, w), eixo é normalizado e theta é a rotação CCW desejada sobre o eixo):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



Os programadores C++ podem aproveitar a sobrecarga do operador e a seleção de tipos com as Extensões [**D3DXQUATERNION**](d3dxquaternion-extensions.md), que implementam construtores sobrecarregados e atribuição, unários e binários (incluindo igualdade).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vetores, vértices e quatérnions (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
