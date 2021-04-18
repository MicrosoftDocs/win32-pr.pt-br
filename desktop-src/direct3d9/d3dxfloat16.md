---
description: Descreve um vetor de ponto flutuante de 16 bits.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Estrutura D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814577"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>Estrutura D3DXFLOAT16 (D3dx9math. h)

Descreve um vetor de ponto flutuante de 16 bits.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>Membros

<dl> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Os dados de 16 bits.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXFLOAT16**](d3dxfloat16-extensions.md), que implementam construtores sobrecarregados e operadores de atribuição, unários e binários (incluindo igualdade).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
