---
title: 'Função RWByteAddressBuffer:: InterlockedCompareExchange'
description: Compara a entrada com o valor de comparação e troca o resultado, atomicamente.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
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
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641560"
---
# <a name="interlockedcompareexchange-function"></a>Função InterlockedCompareExchange

Compara a entrada com o valor de comparação e troca o resultado, atomicamente.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dest* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O endereço de destino.

</dd> <dt>

*comparar \_ valor* \[ em\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O valor de comparação.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O valor de entrada.

</dd> <dt>

*\_ valor original* \[\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O valor original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Compara atomicamente o valor no *dest* para *comparar \_* o valor, armazena o valor no *dest* se os valores corresponderem, retorna o valor original do *dest* no *\_ valor original*. Esta operação só pode ser executada em recursos tipados **int** ou *uint* e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo *dest*. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado pelo *dest*. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para a operação executada usando operações locais. Esta operação só está disponível quando o R é legível e gravável.

> [!Note]  
> Se você chamar **InterlockedCompareExchange** em um loop [**for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) Compute Shader, para compilar corretamente, você deverá usar o atributo **\[ Allow \_ UAV \_ Condition \]** nesse loop.

 

Essa função tem suporte nos seguintes tipos de sombreadores:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 