---
title: Função InterlockedCompareExchange (referência HLSL)
description: Compara atomicamente o destino com o valor de comparação. Se eles são idênticos, o destino é substituído pelo valor de entrada. O valor original é definido como o valor original do destino.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- Função InterlockedCompareExchange HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46cf8c3fb0e3bc0b21c5bf8bc3d946851ce213b765731518d252495250071228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119250"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>Função InterlockedCompareExchange (referência HLSL)

Compara atomicamente o destino com o valor de comparação. Se eles são idênticos, o destino é substituído pelo valor de entrada. O valor original é definido como o valor original do destino.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dest* \[ Em\]
</dt> <dd>

Tipo: **R**

O endereço de destino.

</dd> <dt>

*comparar \_ valor* \[ em\]
</dt> <dd>

Tipo: **T**

O valor de comparação.

</dd> <dt>

*value* \[ Em\]
</dt> <dd>

Tipo: **T**

O valor de entrada.

</dd> <dt>

*valor \_ original* \[ out\]
</dt> <dd>

Tipo: **T**

O valor original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Compara atomicamente o valor referenciado por dest  com o valor de comparação *\_ ,* armazena o valor no local referenciado *por dest* se os valores corresponderem, retorna o valor original *de dest* no valor  *original \_*. Essa operação só pode ser executada em **recursos digitados int** ou **uint** e variáveis de memória compartilhada. Há dois usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado por *dest*. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado *por dest*. Essa operação só está disponível quando o R é acessível e pode ser escrito.

> [!Note]  
> Se você chamar **InterlockedCompareExchange** [](dx-graphics-hlsl-while.md) em um loop para ou durante [**o**](dx-graphics-hlsl-for.md) sombreador de computação, para compilar corretamente, você deverá usar o atributo **\[ allow \_ uav \_ condition \]** nesse loop.

 

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




