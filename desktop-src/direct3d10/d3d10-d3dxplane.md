---
description: Estrutura D3DXPLANE (D3DX10Math. h) – descreve um plano.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Estrutura D3DXPLANE (D3DX10Math. h)
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
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103324"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>Estrutura D3DXPLANE (D3DX10Math. h)

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

**um**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente de recorte na equação do plano geral. Consulte Observações.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente b do plano de recorte na equação do plano geral. Consulte Observações.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente de c do plano de recorte na equação do plano geral. Consulte Observações.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O coeficiente d do plano de recorte na equação do plano geral. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros da estrutura **D3DXPLANE** assumem a forma da equação de plano geral. Eles se encaixam na equação do plano geral para que o AX + por + cz + DW = 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
