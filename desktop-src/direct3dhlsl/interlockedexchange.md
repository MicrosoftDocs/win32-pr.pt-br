---
title: Função InterlockedExchange (referência de HLSL)
description: Atribui o valor ao dest e retorna o valor original.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- HLSL da função InterlockedExchange
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104967158"
---
# <a name="interlockedexchange-function-hlsl-reference"></a>Função InterlockedExchange (referência de HLSL)

Atribui o valor ao dest e retorna o valor original.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedExchange(
  in  R dest,
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

Esta operação só pode ser executada em recursos de tipo escalar e variáveis de memória compartilhada. Há dois usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo dest. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado pelo dest. Esta operação só está disponível quando o R é legível e gravável.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




