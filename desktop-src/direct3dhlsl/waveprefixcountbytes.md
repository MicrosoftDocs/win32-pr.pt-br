---
title: Função WavePrefixCountBits
description: Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as faixas ativas com índices menores que a faixa atual.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- Função WavePrefixCountBits HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 048b63d24e87d97f0e0223083a91694c0471b9e38ad21afbc487c02d711d720d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504672"
---
# <a name="waveprefixcountbits-function"></a>Função WavePrefixCountBits

Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as faixas ativas com índices menores que a faixa atual.

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

As variáveis boolianas especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A soma de todas as variáveis boolianas especificadas definidas como true em todas as faixas ativas com índices menores que a faixa atual.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6.0 em todos os estágios do sombreador. 



 

## <a name="examples"></a>Exemplos

O código a seguir descreve como implementar uma gravação compactada em um fluxo ordenado em que o número de elementos gravados por faixa é 1 ou 0.

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

[Visão geral do Modelo de Sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




