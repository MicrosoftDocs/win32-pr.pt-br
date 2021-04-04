---
description: Descreve um objeto Effect.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Estrutura de D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664007"
---
# <a name="d3dxeffect_desc-structure"></a>\_Estrutura desc de D3DXEFFECT

Descreve um objeto Effect.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Criador**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Cadeia de caracteres que contém o nome do criador de efeito.

</dd> <dt>

**Parâmetros**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de parâmetros usados para efeito.

</dd> <dt>

**Técnicas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de técnicas que podem renderizar o efeito.

</dd> <dt>

**Funções**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de funções que podem renderizar o efeito.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um objeto Effect pode conter várias técnicas de renderização e parâmetros para o mesmo efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
