---
description: Descreve uma faixa de animação e especifica o peso, a velocidade e a posição de mesclagem para a faixa em um determinado momento.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Estrutura de D3DXTRACK_DESC (D3dx9anim. h)
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
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802053"
---
# <a name="d3dxtrack_desc-structure"></a>\_Estrutura desc de D3DXTRACK

Descreve uma faixa de animação e especifica o peso, a velocidade e a posição de mesclagem para a faixa em um determinado momento.

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

Tipo: **[ **\_ tipo de D3DXPRIORITY**](./d3dxpriority-type.md)**

</dd> <dd>

Tipo de prioridade, conforme definido [**no \_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de peso. O peso determina a proporção dessa faixa para misturar com outras faixas.

</dd> <dt>

**Velocidade**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de velocidade. Isso é usado da mesma forma que um multiplicador para dimensionar o período da faixa.

</dd> <dt>

**Posição**
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição de hora da faixa, no período de tempo local do conjunto de animações atual.

</dd> <dt>

**Habilitar**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Controle habilitar/desabilitar. Para habilitar, defina como **true**. Para desabilitar, defina como **false**.

</dd> </dl>

## <a name="remarks"></a>Comentários

As faixas com a mesma prioridade são mescladas e os dois valores resultantes são mesclados usando o fator de mesclagem de prioridade. Uma faixa deve ter uma animação definida (armazenada separadamente) associada a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
