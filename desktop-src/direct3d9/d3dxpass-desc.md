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
ms.openlocfilehash: 9666f0385c592adbc4378cbc693a5ce7a628092bbbb1695fd39527817c7ca04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894046"
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

 

 
