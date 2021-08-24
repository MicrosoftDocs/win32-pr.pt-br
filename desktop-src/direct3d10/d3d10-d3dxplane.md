---
description: Estrutura D3DXPLANE (D3DX10Math.h) – descreve um plano.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Estrutura D3DXPLANE (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ccdc8644f63bdb048f6caa97ef635165a11a4473f549214410558583c8f807c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754256"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>Estrutura D3DXPLANE (D3DX10Math.h)

Descreve um plano.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Um**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente do plano de recorte na equação geral do plano. Consulte Observações.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente b do plano de recorte na equação geral do plano. Consulte Observações.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente c do plano de recorte na equação geral do plano. Consulte Observações.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente d do plano de recorte na equação geral do plano. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros da estrutura **D3DXPLANE** assumirão a forma da equação geral do plano. Eles se encaixam na equação geral do plano para que ax + por + cz + dw = 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
