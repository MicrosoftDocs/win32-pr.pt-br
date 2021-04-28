---
description: Estrutura D3DXQUATERNION (D3dx9math. h) – descreve um Quaternion.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Estrutura D3DXQUATERNION (D3dx9math. h)
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
ms.openlocfilehash: f67acc6389ce809c1aa5f4987d9502735fe61e49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115674"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>Estrutura D3DXQUATERNION (D3dx9math. h)

Descreve um Quaternion.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente y.

</dd> <dt>

**z**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente z.

</dd> <dt>

**w**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente w-.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os quaternions adicionam um quarto elemento aos \[ valores x, y, z \] que definem um vetor, resultando em vetores de 4D arbitrários. No entanto, o seguinte ilustra como cada elemento de uma unidade Quaternion está relacionado a uma rotação de ângulo angular (em que q representa uma unidade Quaternion (x, y, z, w), o eixo é normalizado e teta é a rotação do CCW desejada sobre o eixo):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXQUATERNION**](d3dxquaternion-extensions.md), que implementam construtores sobrecarregados e operadores de atribuição, unários e binários (incluindo igualdade).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vetores, vértices e quaternions (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
