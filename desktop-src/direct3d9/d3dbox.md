---
description: Define um volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Estrutura D3DBOX (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9b7e01641348594e962f546a431700db799600a08571bbb7cfaf13396e671036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805509"
---
# <a name="d3dbox-structure"></a>Estrutura D3DBOX

Define um volume.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a>Membros

<dl> <dt>

**Left**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição do lado esquerdo da caixa no eixo x.

</dd> <dt>

**Top**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da parte superior da caixa no eixo y.

</dd> <dt>

**Right**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição do lado direito da caixa no eixo x.

</dd> <dt>

**Menor**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da parte inferior da caixa no eixo y.

</dd> <dt>

**Front**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da frente da caixa no eixo z.

</dd> <dt>

**Voltar**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da parte traseira da caixa no eixo z.

</dd> </dl>

## <a name="remarks"></a>Comentários

**D3DBOX** inclui as bordas esquerda, superior e frontal; no entanto, as bordas direita, inferior e traseira não são incluídas. Por exemplo, uma caixa com 100 unidades de largura e começa em 0 (portanto, incluindo os pontos até e incluindo 99) seria expressa com um valor de 0 para o membro Left e um valor de 100 para o membro Right. Observe que um valor de 99 não é usado para o membro Right.

As restrições de ordenação lateral observadas para **D3DBOX** são da esquerda para a direita, de cima para baixo e de frente para trás.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
