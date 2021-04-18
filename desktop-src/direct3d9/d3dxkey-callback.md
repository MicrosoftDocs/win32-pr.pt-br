---
description: Descreve uma chave de retorno de chamada para uso na animação de quadro chave.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: Estrutura de D3DXKEY_CALLBACK (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807285"
---
# <a name="d3dxkey_callback-structure"></a>\_Estrutura de retorno de chamada D3DXKEY

Descreve uma chave de retorno de chamada para uso na animação de quadro chave.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a>Membros

<dl> <dt>

**Hora**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Carimbo de data/hora do quadro principal.

</dd> <dt>

**pCallbackData**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para dados de retorno de chamada do usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
