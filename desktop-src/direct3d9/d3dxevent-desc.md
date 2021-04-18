---
description: Descreve um evento de animação.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Estrutura de D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796116"
---
# <a name="d3dxevent_desc-structure"></a>\_Estrutura desc de D3DXEVENT

Descreve um evento de animação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXEVENT**](./d3dxevent-type.md)**

</dd> <dd>

Tipo de evento, conforme definido [**no \_ tipo D3DXEVENT**](./d3dxevent-type.md).

</dd> <dt>

**Rastrear**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de faixa de eventos.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

</dd> <dd>

Hora de início do evento em tempo global.

</dd> <dt>

**Duration**
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

</dd> <dd>

Duração do evento em tempo global.

</dd> <dt>

**Transição**
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md)**

</dd> <dd>

Estilo de transição do evento, conforme definido no [**\_ tipo D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Controle o peso do evento.

</dd> <dt>

**Velocidade**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Controlar a velocidade do evento.

</dd> <dt>

**Posição**
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da faixa para o evento.

</dd> <dt>

**Habilitar**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Habilitar sinalizador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
