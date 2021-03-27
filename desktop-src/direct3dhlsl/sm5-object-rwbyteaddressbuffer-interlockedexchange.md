---
title: 'Função RWByteAddressBuffer:: InterlockedExchange'
description: Troca um valor, atomicamente.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
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
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988651"
---
# <a name="interlockedexchange-function"></a>Função InterlockedExchange

Troca um valor, atomicamente.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedExchange(
  in  UINT dest,
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

Esta operação só pode ser executada em recursos de tipo escalar e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo dest. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado pelo dest. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para a operação executada usando operações locais. Esta operação só está disponível quando o R é legível e gravável.

Essa função tem suporte nos seguintes tipos de sombreadores:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
|  x  |  x  |  x  |  x  | x   | x   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 