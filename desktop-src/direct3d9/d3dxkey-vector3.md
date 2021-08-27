---
description: Descreve uma chave de vetor para uso na animação de quadro-chave. Especifica um vetor em um determinado momento. Isso é usado para chaves de escala e tradução.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: D3DXKEY_VECTOR3 estrutura (D3dx9anim.h)
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
ms.openlocfilehash: 0214582b3fb1267caeb30a6cca905cbf7243ecf5dd1af40365841b315359317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119176"
---
# <a name="d3dxkey_vector3-structure"></a>Estrutura D3DXKEY \_ VECTOR3

Descreve uma chave de vetor para uso na animação de quadro-chave. Especifica um vetor em um determinado momento. Isso é usado para chaves de escala e tradução.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Carimbo de data/hora do quadro-chave.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

[**Vetor 3DXVECTOR3**](d3dxvector3.md) 3D que fornece valores de escala e/ou tradução.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
