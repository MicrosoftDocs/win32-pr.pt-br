---
description: Gira o vetor harmônica (SH) esférico pela matriz especificada.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: Função D3DXSHRotate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747864"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a>Função D3DXSHRotate (D3dx9math. h)

Gira o vetor harmônica (SH) esférico pela matriz especificada.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para os coeficientes de saída harmônicas (SH). A avaliação gera coeficientes do Order ². Esse ponteiro não deve ser alias com *pIn*. Consulte Observações.

</dd> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*pMatrix* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a matriz de rotação. A submatriz de rotação deve ser ortogonal, com um determinante de unidade.

</dd> <dt>

*fixar* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Ponteiro para de doeficientes de forma girada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para SH coeficientes de saída.

## <a name="remarks"></a>Comentários

Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:

-   l é o grau da função base.
-   m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferência radiante de computação (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
