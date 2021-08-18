---
description: Função D3DXSHDot (D3DX10. h) – computa o produto dot de dois vetores de harmônica esférica (SH).
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: Função D3DXSHDot (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 77595f5aac53572813be72f498944b029dc42491c376410645037dcbfd4c01f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990916"
---
# <a name="d3dxshdot-function-d3dx10h"></a>Função D3DXSHDot (D3DX10. h)

Computa o produto de ponto de dois vetores de harmônica esférica (SH).

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação harmônica esférica (SH). Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*PA* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Aponta para o primeiro vetor SH.

</dd> <dt>

*PB* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Aponta para o segundo vetor SH.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **float**](../winprog/windows-data-types.md)**

SH coeficientes de saída.

## <a name="remarks"></a>Comentários

Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:

-   l é o grau da função base.
-   m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
