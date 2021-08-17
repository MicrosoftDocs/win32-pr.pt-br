---
title: Função RWByteAddressBuffer::InterlockedMax
description: Localiza o valor máximo, atomicamente.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- Função InterlockedMax HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ca02966843d74aa17c3f5292ee3edf868140ae5722c26f47ec0270722cbbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790271"
---
# <a name="interlockedmax-function"></a>Função InterlockedMax

Localiza o valor máximo, atomicamente.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedMax(
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

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa operação só pode ser executada em recursos digitados int e uint e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa um máximo atômico do valor para o registro de memória compartilhada referenciado por dest. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa um máximo atômico do valor para o local do recurso referenciado por dest. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para um máximo do valor de dest e value, armazenados em dest. A função sobrecarregada tem uma variável de saída adicional que será definida como o valor original de dest. Essa operação sobrecarregada só está disponível quando o R é acessível e pode ser escrito.

Essa função tem suporte nos seguintes tipos de sombreadores:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 