---
description: Função D3DXVec4Hermite (D3dx9math.h) – executa uma interpolação de spline hermite, usando os vetores 4D especificados.
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: Função D3DXVec4Hermite (D3dx9math.h)
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
ms.openlocfilehash: a62d96181b4242073b9e6a2176d841add86cbfeab4238bfb4cbb538bfd88e1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730724"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a>Função D3DXVec4Hermite (D3dx9math.h)

Executa uma interpolação de spline hermite usando os vetores 4D especificados.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR4 de**](d3dxvector4.md) origem, um vetor de posição.

</dd> <dt>

*pT1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR4 de**](d3dxvector4.md) origem, um vetor tangente.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR4 de**](d3dxvector4.md) origem, um vetor de posição.

</dd> <dt>

*pT2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR4 de**](d3dxvector4.md) origem, um vetor tangente.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é o resultado da interpolação de spline hermite.

## <a name="remarks"></a>Comentários

A **função D3DXVec4Hermite** interpola de (positionA, tangentA) para (positionB, tangentB) usando a interpolação de spline hermite.

A interpolação de spline é uma generalização do spline fácil de entrar e sair. A rampa é uma função de P(s) com as propriedades a seguir.

P(s) = As(s) = As(s) + Bs(s) + Cs + D (e, portanto, Q(s) = 3As(s) + 2Bs + C)

a) Q(0) = v1, portanto, Q'(0) = t1

b) Q(1) = v2, portanto, Q'(1) = t2

v1 é o conteúdo de pV1, v2 no conteúdo de pV2, t1 é o conteúdo de pT1 e t2 é o conteúdo de pT2.

Essas propriedades são usadas para resolver A, B, C, D.

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

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a **função D3DXVec4Hermite** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
