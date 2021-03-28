---
title: 'Função RWByteAddressBuffer:: InterlockedAdd'
description: Adiciona o valor, atomicamente.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- HLSL da função InterlockedAdd
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988666"
---
# <a name="interlockedadd-function"></a>Função InterlockedAdd

Adiciona o valor, atomicamente.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedAdd(
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

Esta operação só pode ser executada em recursos tipados int ou uint e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa uma adição atômica de valor para o registro de memória compartilhada referenciado pelo dest. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa uma adição atômica do valor para o local do recurso referenciado pelo dest. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para uma soma do valor de dest e Value, armazenado no dest. A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de dest. Essa operação sobrecarregada só está disponível quando o R é legível e gravável.

Essa função tem suporte nos seguintes tipos de sombreadores:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="requirements"></a>Requisitos




## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

