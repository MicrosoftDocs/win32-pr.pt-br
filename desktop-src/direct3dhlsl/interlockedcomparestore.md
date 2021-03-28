---
title: Função InterlockedCompareStore (referência de HLSL)
description: Compara atomicamente o destino com o valor de comparação. Se forem idênticos, o destino será substituído pelo valor de entrada.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- HLSL da função InterlockedCompareStore
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104365458"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>Função InterlockedCompareStore (referência de HLSL)

Compara atomicamente o destino com o valor de comparação. Se forem idênticos, o destino será substituído pelo valor de entrada.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dest* \[ no\]
</dt> <dd>

Tipo: **R**

O endereço de destino.

</dd> <dt>

*comparar \_ valor* \[ em\]
</dt> <dd>

Tipo: **T**

O valor de comparação.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **T**

O valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Compara atomicamente o valor referenciado pelo *dest* com o *\_ valor de comparação* e armazena o *valor* no local referenciado pelo *dest* se os valores correspondem. Esta operação só pode ser executada em recursos tipados **int** ou **uint** e variáveis de memória compartilhada. Há dois usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo *dest*. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado pelo *dest*.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




