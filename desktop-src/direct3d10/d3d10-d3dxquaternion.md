---
description: Estrutura D3DXQUATERNION (D3DX10Math. h) – descreve um Quaternion.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Estrutura D3DXQUATERNION (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103244"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>Estrutura D3DXQUATERNION (D3DX10Math. h)

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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
