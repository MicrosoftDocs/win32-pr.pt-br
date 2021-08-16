---
description: Descreve um objeto de efeito.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: D3DXEFFECT_DESC (D3dx9effect.h)
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
ms.openlocfilehash: 0b30ad0348a5c799690d668e036724d30808c2998eee9d762fa2ad3fc8106c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298589"
---
# <a name="d3dxeffect_desc-structure"></a>Estrutura D3DXEFFECT \_ DESC

Descreve um objeto de efeito.

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

Cadeia de caracteres que contém o nome do criador do efeito.

</dd> <dt>

**Parâmetros**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de parâmetros usados para efeito.

</dd> <dt>

**Técnicas**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de técnicas que podem renderizar o efeito.

</dd> <dt>

**Funções**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de funções que podem renderizar o efeito.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um objeto de efeito pode conter várias técnicas de renderização e parâmetros para o mesmo efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
