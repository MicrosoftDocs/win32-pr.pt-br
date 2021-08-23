---
description: Função D3DXSHAdd (D3DX10.h) – adiciona dois vetores de sh (ataque esférico); em outras palavras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Função D3DXSHAdd (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f59d0d83424039af6d2ca5d4ea6ca25702d6fc50039502fb0af0eae3ab782ec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990926"
---
# <a name="d3dxshadd-function-d3dx10h"></a>Função D3DXSHAdd (D3DX10.h)

Adiciona dois vetores esféricos (SH); em outras palavras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para coeficientes de saída sh. A avaliação gera coeficientes orderâmicos. Consulte Observações.

</dd> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH. Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*pA* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ponteiro para o primeiro vetor SH.

</dd> <dt>

*pB* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ponteiro para o segundo vetor SH.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para coeficientes de saída sh.

## <a name="remarks"></a>Comentários

Cada coeficiente da função de base Ylm é armazenado no local de memória lá + m + l, em que:

-   l é o grau da função base.
-   m é o índice de função base para o valor l e intervalos de -l a l, inclusive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
