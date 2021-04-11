---
description: Define um volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Estrutura D3DBOX (D3D9Types. h)
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
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172951"
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

**Mantida**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição do lado esquerdo da caixa no eixo x.

</dd> <dt>

**Top**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da parte superior da caixa no eixo y.

</dd> <dt>

**Certo**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição do lado direito da caixa no eixo x.

</dd> <dt>

**Inferior**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da parte inferior da caixa no eixo y.

</dd> <dt>

**Front**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da frente da caixa no eixo z.

</dd> <dt>

**Voltar**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição da parte de trás da caixa no eixo z.

</dd> </dl>

## <a name="remarks"></a>Comentários

**D3DBOX** inclui as bordas esquerda, superior e frontal; no entanto, as bordas direita, inferior e traseira não são incluídas. Por exemplo, uma caixa com 100 unidades de largura e começa em 0 (portanto, a inclusão de pontos até e incluindo 99) seria expressa com um valor de 0 para o membro esquerdo e um valor de 100 para o membro correto. Observe que um valor de 99 não é usado para o membro correto.

As restrições de ordenação do lado observado para **D3DBOX** são da esquerda para a direita, de cima para baixo e de frente para trás.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
