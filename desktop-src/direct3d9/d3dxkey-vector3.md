---
description: Descreve uma chave de vetor para uso na animação de quadro chave. Ele especifica um vetor em um determinado momento. Isso é usado para chaves de escala e de tradução.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Estrutura de D3DXKEY_VECTOR3 (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793993"
---
# <a name="d3dxkey_vector3-structure"></a>\_Estrutura D3DXKEY VECTOR3

Descreve uma chave de vetor para uso na animação de quadro chave. Ele especifica um vetor em um determinado momento. Isso é usado para chaves de escala e de tradução.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a>Membros

<dl> <dt>

**Hora**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Carimbo de data/hora do quadro principal.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

Vetor 3D [**D3DXVECTOR3**](d3dxvector3.md) que fornece valores de escala e/ou translação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
