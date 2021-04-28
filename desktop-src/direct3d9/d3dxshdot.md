---
description: Função D3DXSHDot (D3dx9math. h) – computa o produto dot de dois vetores de harmônica esférica (SH).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Função D3DXSHDot (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093924"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a>Função D3DXSHDot (D3dx9math. h)

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

Ordem da avaliação harmônica esférica (SH). Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

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
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferência radiante de computação (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
