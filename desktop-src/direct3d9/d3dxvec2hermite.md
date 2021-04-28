---
description: Função D3DXVec2Hermite (D3dx9math. h) – executa uma interpolação de spline Hermite, usando os vetores 2D especificados.
ms.assetid: 30eb9490-bc01-4449-adfb-1c552e8ad3e7
title: Função D3DXVec2Hermite (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88073e23826362e1f9a753f411ac89ac1e272fc6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097984"
---
# <a name="d3dxvec2hermite-function-d3dx9mathh"></a>Função D3DXVec2Hermite (D3dx9math. h)

Executa uma interpolação de spline Hermite, usando os vetores 2D especificados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem, um vetor de posição.

</dd> <dt>

*pT1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem, um vetor tangente.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem, um vetor de posição.

</dd> <dt>

*pT2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem, um vetor tangente.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da interpolação Hermite spline.

## <a name="remarks"></a>Comentários

A função **D3DXVec2Hermite** interpola de (positiona, tangentea) a (PositionB, tangentB) usando a interpolação Hermite spline.

A interpolação de spline é uma generalização da spline de fácil entrada, de fácil saída. A rampa é uma função de Q (s) com as propriedades a seguir.

Q (s) = as ³ + BS ² + CS + D (e, portanto, Q ' s) = 3As ² + 2Bs + C)

a) Q (0) = v1, portanto, Q ' (0) = T1

b) Q (1) = v2, portanto Q ' (1) = T2

v1 é o conteúdo de pV1, V2 no conteúdo de pV2, T1 é o conteúdo de pT1 e T2 é o conteúdo de pT2.

Essas propriedades são usadas para resolver para A, B, C, D.

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

Conecte as soluções para a, B, C e D para gerar Q (s).

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Isso resulta em:

Q (s) = (2v1-2v2 + T2 + T1) s ³ + (3v2-3V1-2T1-T2) s ² + T1s + v1

Que pode ser reorganizado como:

Q (s) = (2S ³-3S ² + 1) V1 + (-2S ³ + 3S ²) V2 + (s ³-2s ² + s) T1 + (s ³-s ²) T2

As Hermites são úteis para controlar a animação porque a curva é executada por todos os pontos de controle. Além disso, como a posição e a tangente são especificadas explicitamente nas extremidades de cada segmento, é fácil criar uma curva contínua C2, contanto que você verifique se a posição inicial e a tangente correspondem aos valores finais do último segmento.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função **D3DXVec2Hermite** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
