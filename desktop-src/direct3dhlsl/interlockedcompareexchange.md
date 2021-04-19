---
title: Função InterlockedCompareExchange (referência de HLSL)
description: Compara atomicamente o destino com o valor de comparação. Se forem idênticos, o destino será substituído pelo valor de entrada. O valor original é definido como o valor original do destino.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- HLSL da função InterlockedCompareExchange
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104988642"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>Função InterlockedCompareExchange (referência de HLSL)

Compara atomicamente o destino com o valor de comparação. Se forem idênticos, o destino será substituído pelo valor de entrada. O valor original é definido como o valor original do destino.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
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

</dd> <dt>

*\_ valor original* \[\]
</dt> <dd>

Tipo: **T**

O valor original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Compara atomicamente o valor referenciado *pelo dest* com o *\_ valor de comparação* *, armazena o valor no* local referenciado pelo *dest* se os valores forem correspondentes, retorna o valor original do *dest* no *\_ valor original*. Esta operação só pode ser executada em recursos tipados **int** ou **uint** e variáveis de memória compartilhada. Há dois usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo *dest*. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado pelo *dest*. Esta operação só está disponível quando o R é legível e gravável.

> [!Note]  
> Se você chamar **InterlockedCompareExchange** em um loop [**for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) Compute Shader, para compilar corretamente, você deverá usar o atributo **\[ Allow \_ UAV \_ Condition \]** nesse loop.

 

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




