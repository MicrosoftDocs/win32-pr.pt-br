---
description: Descreve um plano.
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
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298780"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
