---
title: Função InterlockedCompareStore (referência HLSL)
description: Compara atomicamente o destino com o valor de comparação. Se eles são idênticos, o destino é substituído pelo valor de entrada.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- Função InterlockedCompareStore HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dbf13629b9c3b9b38cc3bd72a8a992ab40bd09c0333c155a7c109f71466f23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119240"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>Função InterlockedCompareStore (referência HLSL)

Compara atomicamente o destino com o valor de comparação. Se eles são idênticos, o destino é substituído pelo valor de entrada.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
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

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Compara atomicamente o valor referenciado por *dest*  com *o \_* valor de comparação e armazena o valor no local referenciado *por dest* se os valores corresponderem. Essa operação só pode ser executada em **recursos digitados int** ou **uint** e variáveis de memória compartilhada. Há dois usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado por *dest*. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado *por dest*.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




