---
title: Função WavePrefixCountBits
description: Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as pistas ativas com índices menores que a raia atual.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- HLSL da função WavePrefixCountBits
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008603"
---
# <a name="waveprefixcountbits-function"></a>Função WavePrefixCountBits

Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as pistas ativas com índices menores que a raia atual.

## <a name="syntax"></a>Sintaxe


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bBit* 
</dt> <dd>

As variáveis Booleanas especificadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A soma de todas as variáveis Booleanas especificadas definidas como true em todas as pistas ativas com índices menores que a pista atual.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

O código a seguir descreve como implementar uma gravação compactada em um fluxo ordenado em que o número de elementos gravados por Lane é 1 ou 0.

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




