---
title: Função WaveActiveCountBits
description: Conta o número de variáveis boolianas que são avaliadas como true em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- HLSL da função WaveActiveCountBits
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e1642cbd5cbdef162511185e9d2c05e849d78486b82e8219623286f33e39223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504931"
---
# <a name="waveactivecountbits-function"></a>Função WaveActiveCountBits

Conta o número de variáveis boolianas que são avaliadas como true em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda.

## <a name="syntax"></a>Sintaxe


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bBit* 
</dt> <dd>

As variáveis Booleanas a serem avaliadas. Fornecer um valor booliano verdadeiro explícito retorna o número de pistas ativas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O número de que é avaliado como true em todas as pistas ativas na onda atual.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

Isso pode ser implementado com mais eficiência do que um WaveActiveSum completo, conforme descrito no exemplo a seguir:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




