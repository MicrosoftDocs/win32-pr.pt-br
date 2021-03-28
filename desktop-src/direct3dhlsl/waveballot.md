---
title: Função WaveActiveBallot
description: Retorna um uint4 contendo uma bitmask da avaliação da expressão booliana para todas as pistas ativas na onda atual.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- HLSL da função WaveActiveBallot
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104499185"
---
# <a name="waveactiveballot-function"></a>Função WaveActiveBallot

Retorna um uint4 contendo uma bitmask da avaliação da expressão booliana para todas as pistas ativas na onda atual. 

## <a name="syntax"></a>Sintaxe

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expr* 
</dt> <dd>

A expressão booliana a ser avaliada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um uint4 que contém um bitmask da avaliação da expressão booliana para todas as pistas ativas na onda atual. O bit menos significativo corresponde à pista com o índice zero. Os bits correspondentes a pistas inativas serão zero. Os bits maiores ou iguais a [**WaveGetLaneCount**](wavegetlanecount.md) serão zero.

## <a name="remarks"></a>Comentários

GPUs diferentes têm larguras de processador SIMD diferentes (contagens de raia). A maioria dessas funções do **WaveXXX** é capaz de operar no nível de abstração em que a largura da máquina SIMD é ocultada. Para maximizar a portabilidade do código entre GPUs, use os intrínsecos que não dependem da largura da máquina. Por exemplo, use:

``` syntax
uint result = WaveActiveCountBits( bBit );
```

Em vez de:

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




