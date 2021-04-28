---
description: Estrutura D3DXCOLOR (D3dx9math. h) – descreve os valores de cor.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Estrutura D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115924"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>Estrutura D3DXCOLOR (D3dx9math. h)

Descreve os valores de cor.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>Membros

<dl> <dt>

**r**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente vermelho da cor.

</dd> <dt>

**m**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente verde da cor.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente azul da cor.

</dd> <dt>

**um**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente alfa da cor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXCOLOR**](d3dxcolor-extensions.md), que implementam construtores sobrecarregados, bem como operadores de atribuição, unários e binários (incluindo igualdade).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
