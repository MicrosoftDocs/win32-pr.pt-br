---
title: 'Função RWByteAddressBuffer:: interbloqueador'
description: Executa um Atomic ou no valor.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
keywords:
- Função de intercadeado HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07bcaf2ac9d5523949809b22b37f6a31bee1e7ef4243cfef52b1b034ee2e0cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986006"
---
# <a name="interlockedor-function"></a>Função de intercadeado

Executa um Atomic **ou** no valor.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
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

## <a name="return-value"></a>Valor retornado

Nada

## <a name="remarks"></a>Comentários

Esta operação só pode ser executada em recursos tipados **int** ou **uint** e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa um Atomic **ou** com o valor do registro de memória compartilhada referenciado pelo *dest*. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa um Atomic **ou** com o valor do local do recurso referenciado pelo *dest*. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para um **ou** com os valores de *dest* e *Value*. O resultado da operação substitui o valor de *dest*. A função sobrecarregada tem uma variável de saída adicional, que será definida com o valor original de *dest*. Essa operação sobrecarregada está disponível somente quando o R é legível e gravável.

Essa função tem suporte nos seguintes tipos de sombreadores:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 