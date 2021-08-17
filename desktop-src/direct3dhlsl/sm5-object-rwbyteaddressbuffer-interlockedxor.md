---
title: 'Função RWByteAddressBuffer:: InterlockedXor'
description: Executa um XOR atômico no valor.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- HLSL da função InterlockedXor
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b9e0c719bb72116ba84a33f46c81cf243773d4c66e5ff0997066e7228b19db1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905793"
---
# <a name="interlockedxor-function"></a>Função InterlockedXor

Executa um **XOR** atômico no valor.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedXor(
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

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta operação só pode ser executada em recursos tipados **int** ou **uint** e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa um **XOR** atômico com o valor do registro de memória compartilhada referenciado pelo *dest*. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa um **XOR** atômico com o valor do local do recurso referenciado pelo *dest*. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para um **XOR** dos valores de *dest* e *Value*. O resultado da operação substitui o valor no *dest*. A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de *dest*. Essa operação sobrecarregada está disponível somente quando o R é legível e gravável.

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

 

 