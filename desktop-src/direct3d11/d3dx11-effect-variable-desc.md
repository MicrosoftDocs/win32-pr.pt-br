---
title: Estrutura de D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Descreve uma variável de efeito.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- Estrutura D3DX11_EFFECT_VARIABLE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989397"
---
# <a name="d3dx11_effect_variable_desc-structure"></a>\_ \_ Estrutura desc da variável de efeito D3DX11 \_

Descreve uma variável de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome desta variável, anotação ou membro de estrutura.

</dd> <dt>

**Semântico**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Cadeia de caracteres semântica dessa variável ou membro de estrutura (NULL para anotações ou se não estiver presente).

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sinalizadores opcionais para variáveis de efeito.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotações nessa variável (sempre 0 para anotações).

</dd> <dt>

**BufferOffset**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Offset em contendo CBuffer ou tbuffers (sempre 0 para anotações ou variáveis que não estão em buffers constantes).

</dd> <dt>

**ExplicitBindPoint**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Usado se a variável tiver sido explicitamente associada usando a palavra-chave Register. Verifique os sinalizadores para \_ o \_ \_ ponto de ligação explícito da variável de efeito D3DX11 \_ \_ .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ A variável de efeito D3DX11 \_ DESC é usada com [**ID3DX11EffectVariable:: GetDesc**](id3dx11effectvariable-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

