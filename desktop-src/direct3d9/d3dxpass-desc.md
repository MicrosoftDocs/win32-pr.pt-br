---
description: Descreve uma passagem para um objeto de efeito.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Estrutura de D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298479"
---
# <a name="d3dxpass_desc-structure"></a>\_Estrutura desc de D3DXPASS

Descreve uma passagem para um objeto de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de cadeia de caracteres usado para a passagem.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

As anotações são dados específicos do usuário que podem ser anexados a qualquer técnica, passagem ou parâmetro. Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Ponteiro para a função de sombreador de vértice. Se um efeito for criado com [D3DXFX \_ não \_ clonável](d3dxfx.md), essa estrutura retornará um ponteiro **nulo** quando for chamado por [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Ponteiro para a função de sombreador de pixel. Se um efeito for criado com [D3DXFX \_ não \_ clonável](d3dxfx.md), essa estrutura retornará um ponteiro **nulo** quando for chamado por [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
