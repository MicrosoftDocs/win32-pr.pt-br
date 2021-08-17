---
description: Função D3DXVec2Hermite (D3dx9math.h) – executa uma interpolação de spline hermite, usando os vetores 2D especificados.
ms.assetid: 30eb9490-bc01-4449-adfb-1c552e8ad3e7
title: Função D3DXVec2Hermite (D3dx9math.h)
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
ms.openlocfilehash: 052174ba85370c62dc8a4618b44880f1e750801a78cf61963d863a9057c10568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804047"
---
# <a name="d3dxvec2hermite-function-d3dx9mathh"></a>Função D3DXVec2Hermite (D3dx9math.h)

Executa uma interpolação de spline Hermite usando os vetores 2D especificados.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem, um vetor de posição.

</dd> <dt>

*pT1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem, um vetor tangente.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem, um vetor de posição.

</dd> <dt>

*pT2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem, um vetor tangente.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é o resultado da interpolação de spline hermite.

## <a name="remarks"></a>Comentários

A **função D3DXVec2Hermite** interpola de (positionA, tangentA) a (positionB, tangentB) usando a interpolação de spline hermite.

A interpolação de spline é uma generalização do spline fácil de entrar e sair. A rampa é uma função de P(s) com as propriedades a seguir.

P(s) = As(s) = As(s) + Bs(s) + Cs + D (e, portanto, Q(s) = 3As(s) + 2Bs + C)

a) Q(0) = v1, portanto, Q'(0) = t1

b) Q(1) = v2, portanto, Q'(1) = t2

v1 é o conteúdo de pV1, v2 no conteúdo de pV2, t1 é o conteúdo de pT1 e t2 é o conteúdo de pT2.

Essas propriedades são usadas para resolver A, B, C, D.

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

Conecte as soluções para A, B, C e D para gerar P(s).

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Isso resulta em:

Q(s) = (2v1 - 2v2 + t2 + t1)sÁ + (3v2 - 3v1 - 2t1 - t2)sU + t1s + v1

Que pode ser reorganizar como:

Q(s) = (2s polegadas - 3su + 1)v1 + (-2s polegada + 3s)v2 + (sá - 2sU + s)t1 + (sá - su)t2

Splines de hermite são úteis para controlar a animação porque a curva é executado em todos os pontos de controle. Além disso, como a posição e a tangente são especificadas explicitamente nas extremidades de cada segmento, é fácil criar uma curva contínua C2, desde que você certifique-se de que a posição inicial e a tangente corresponderão aos valores finais do último segmento.

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a **função D3DXVec2Hermite** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
