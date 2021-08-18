---
description: Estrutura D3DXCOLOR (D3dx9math.h) – descreve valores de cor.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Estrutura D3DXCOLOR (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 28f170814988317cd1cdf3300e4cbb3c2a97fa0fac7a43b2231767914a9b103a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988716"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>Estrutura D3DXCOLOR (D3dx9math.h)

Descreve valores de cor.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>Membros

<dl> <dt>

**r**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente vermelho da cor.

</dd> <dt>

**G**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente verde da cor.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente azul da cor.

</dd> <dt>

**Um**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente alfa da cor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os programadores C++ podem aproveitar a sobrecarga do operador e a seleção de tipo com as Extensões [**D3DXCOLOR**](d3dxcolor-extensions.md), que implementam construtores sobrecarregados, bem como operadores de atribuição, unários e binários (incluindo igualdade).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
