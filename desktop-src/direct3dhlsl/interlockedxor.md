---
title: Função InterlockedXor (referência HLSL)
description: Executa um xor atômico garantido.
ms.assetid: 844ca31f-d051-4713-b9e1-dd6712ad36ca
keywords:
- Função InterlockedXor HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8d71a1fbcfe05ef18ad36d34891adfd05c218247510fa6662846aa6209e41a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906991"
---
# <a name="interlockedxor-function-hlsl-reference"></a>Função InterlockedXor (referência HLSL)

Executa um xor atômico garantido.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedXor(
  in  R dest,
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

*value* \[ Em\]
</dt> <dd>

Tipo: **T**

O valor de entrada.

</dd> <dt>

*valor \_ original* \[ out\]
</dt> <dd>

Tipo: **T**

Opcional. O valor de entrada original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa operação só pode ser executada em recursos digitados int ou uint e variáveis de memória compartilhada. Há dois usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa um XOR atômico de valor para o registro de memória compartilhada referenciado por dest. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa um valor XORof atômico para o local do recurso referenciado por dest. A função sobrecarregada tem uma variável de saída adicional que será definida como o valor original de dest. Essa operação sobrecarregada só está disponível quando o R é acessível e pode ser escrito.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|  x     |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




