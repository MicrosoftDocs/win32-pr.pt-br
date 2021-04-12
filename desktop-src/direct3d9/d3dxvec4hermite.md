---
description: Executa uma interpolação de spline Hermite, usando os vetores de 4D especificados.
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: Função D3DXVec4Hermite (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85cf60150606a37c2e68ebf72bd4a3772d346660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173039"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a>Função D3DXVec4Hermite (D3dx9math. h)

Executa uma interpolação de spline Hermite, usando os vetores de 4D especificados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor de posição.

</dd> <dt>

*pT1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor tangente.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor de posição.

</dd> <dt>

*pT2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem, um vetor tangente.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da interpolação Hermite spline.

## <a name="remarks"></a>Comentários

A função **D3DXVec4Hermite** interpola de (positiona, tangentea) a (PositionB, tangentB) usando a interpolação Hermite spline.

A interpolação de spline é uma generalização da spline de fácil entrada, de fácil saída. A rampa é uma função de Q (s) com as propriedades a seguir.

Q (s) = as ³ + BS ² + CS + D (e, portanto, Q ' s) = 3As ² + 2Bs + C)

a) Q (0) = v1, portanto, Q ' (0) = T1

b) Q (1) = v2, portanto Q ' (1) = T2

v1 é o conteúdo de pV1, V2 no conteúdo de pV2, T1 é o conteúdo de pT1 e T2 é o conteúdo de pT2.

Essas propriedades são usadas para resolver para A, B, C, D.

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

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função **D3DXVec4Hermite** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
