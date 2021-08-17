---
description: Descreve uma faixa de animação e especifica o peso, a velocidade e a posição da mistura para a faixa em um determinado momento.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: cddabb3ea79951e35831c2cdc32e11baeb5c7c1c4ce174fd29d9382edb391953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731113"
---
# <a name="d3dxtrack_desc-structure"></a>Estrutura D3DXTRACK \_ DESC

Descreve uma faixa de animação e especifica o peso, a velocidade e a posição da mistura para a faixa em um determinado momento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Prioridade**
</dt> <dd>

Tipo: **[ **D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)**

</dd> <dd>

Tipo de prioridade, conforme definido [**em D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de peso. O peso determina a proporção dessa faixa para combinar com outras faixas.

</dd> <dt>

**Velocidade**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de velocidade. Isso é usado de forma semelhante a um multiplicador para dimensionar o período da faixa.

</dd> <dt>

**Posição**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição de hora da faixa, no período local de seu conjunto de animação atual.

</dd> <dt>

**Habilitar**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Acompanhe habilitar/desabilitar. Para habilitar, de definido como **TRUE.** Para desabilitar, de definido como **FALSE.**

</dd> </dl>

## <a name="remarks"></a>Comentários

As faixas com a mesma prioridade são mescladas e os dois valores resultantes são então mesclados usando o fator de combinação de prioridade. Uma faixa deve ter um conjunto de animação (armazenado separadamente) associado a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
