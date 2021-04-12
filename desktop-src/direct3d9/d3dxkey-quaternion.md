---
description: Descreve uma chave do Quaternion para uso na animação do quadro chave. Uma chave Quaternion é um valor de Quaternion em um determinado momento.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: Estrutura de D3DXKEY_QUATERNION (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298611"
---
# <a name="d3dxkey_quaternion-structure"></a>\_Estrutura de QUATERNION D3DXKEY

Descreve uma chave do Quaternion para uso na animação do quadro chave. Uma chave Quaternion é um valor de Quaternion em um determinado momento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Hora**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O valor temporal.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)**

</dd> <dd>

[**D3DXQUATERNION**](d3dxquaternion.md) Quaternion que fornece valores de rotação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
