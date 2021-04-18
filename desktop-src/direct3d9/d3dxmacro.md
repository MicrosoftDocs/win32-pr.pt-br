---
description: Descreve as definições de pré-processador usadas por um objeto de efeito.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Estrutura D3DXMACRO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784625"
---
# <a name="d3dxmacro-structure"></a>Estrutura D3DXMACRO

Descreve as definições de pré-processador usadas por um objeto de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome do pré-processador.

</dd> <dt>

**Definição**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome da definição.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar **D3DXMACRO** s em mais de uma linha, Prefixe cada caractere de nova linha com uma barra invertida (como uma \# definição na linguagem C). Por exemplo:


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



Observe os 3 caracteres de barra invertida no final da linha. Os dois primeiros são necessários para gerar um único ' \\ ', seguido pelo caractere de nova linha " \\ n". Opcionalmente, você também pode querer encerrar suas linhas usando " \\ \\ \\ r \\ n".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
