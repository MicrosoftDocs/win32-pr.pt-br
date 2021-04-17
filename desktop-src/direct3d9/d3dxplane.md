---
description: Descreve um plano.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Estrutura D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812076"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>Estrutura D3DXPLANE (D3dx9math. h)

Descreve um plano.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Membros

<dl> <dt>

**um**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente de recorte na equação do plano geral. Consulte Observações.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente b do plano de recorte na equação do plano geral. Consulte Observações.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente de c do plano de recorte na equação do plano geral. Consulte Observações.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente d do plano de recorte na equação do plano geral. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros da estrutura **D3DXPLANE** assumem a forma da equação de plano geral. Eles se enquadram na equação do plano geral para que **um** x + **b** y + **c** z + **d** w = 0.

Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXPLANE**](d3dxplane-extensions.md) que implementam construtores sobrecarregados e operadores de atribuição, unários e binários (incluindo igualdade).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
