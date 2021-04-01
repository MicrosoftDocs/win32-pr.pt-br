---
description: Define um retângulo.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Estrutura D3DRECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664022"
---
# <a name="d3drect-structure"></a>Estrutura D3DRECT

Define um retângulo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a>Membros

<dl> <dt>

**X1**
</dt> <dd>

Tipo: **[ **longo**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada X do canto superior esquerdo do retângulo.

</dd> <dt>

**Y1**
</dt> <dd>

Tipo: **[ **longo**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada y do canto superior esquerdo do retângulo.

</dd> <dt>

**X2**
</dt> <dd>

Tipo: **[ **longo**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada x do canto inferior direito do retângulo.

</dd> <dt>

**Y2**
</dt> <dd>

Tipo: **[ **longo**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada y do canto inferior direito do retângulo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Formatação**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
