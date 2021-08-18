---
description: Função D3DXSHScale (D3DX10. h) – dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: Função D3DXSHScale (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 46018d83a473202066ac22c9e4bda88a096154ffd6fc79b13c604d8937d1140c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990746"
---
# <a name="d3dxshscale-function-d3dx10h"></a>Função D3DXSHScale (D3DX10. h)

Dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para os coeficientes de saída harmônicas (SH). A avaliação gera coeficientes do Order ². Consulte Observações.

</dd> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*fixar* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Ponteiro para o vetor SH a ser dimensionado.

</dd> <dt>

*Escala* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md)**

Ponteiro para o valor de escala.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para SH coeficientes de saída.

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

 

 
