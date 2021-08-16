---
title: Função RWByteAddressBuffer::InterlockedMin
description: Localiza o valor mínimo, atomicamente.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- Função InterlockedMin HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 062ae6c5fa37b732411891427770761881429069d030e9266ab20adb3e2d3726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509545"
---
# <a name="interlockedmin-function"></a>Função InterlockedMin

Localiza o valor mínimo, atomicamente.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dest* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O endereço de destino.

</dd> <dt>

*value* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O valor de entrada.

</dd> <dt>

*valor \_ original* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O valor original.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nada

## <a name="remarks"></a>Comentários

Essa operação só pode ser executada em recursos digitados int e uint e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa um mínimo atômico do valor para o registro de memória compartilhada referenciado por dest. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa um mínimo atômico do valor para o local do recurso referenciado por dest. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para um mínimo do valor de dest e value, armazenados em dest. A função sobrecarregada tem uma variável de saída adicional que será definida como o valor original de dest. Essa operação sobrecarregada só está disponível quando o R é acessível e pode ser escrito.

Essa função tem suporte nos seguintes tipos de sombreadores:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 