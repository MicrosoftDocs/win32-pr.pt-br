---
description: Define um retângulo.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Estrutura D3DRECT (D3D9Types.h)
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
ms.openlocfilehash: 5e202ae058cdc30b79e2cc579a064b597d0013f7447e70f0fd6d996d9740a830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732280"
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

**x1**
</dt> <dd>

Tipo: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada X do canto superior esquerdo do retângulo.

</dd> <dt>

**y1**
</dt> <dd>

Tipo: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada y do canto superior esquerdo do retângulo.

</dd> <dt>

**x2**
</dt> <dd>

Tipo: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada X do canto inferior direito do retângulo.

</dd> <dt>

**y2**
</dt> <dd>

Tipo: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

A coordenada Y do canto inferior direito do retângulo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Limpar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
