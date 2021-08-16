---
title: 'Função RWByteAddressBuffer:: InterlockedCompareStore'
description: Ccompares a entrada para o valor de comparação, atomicamente.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- HLSL da função InterlockedCompareStore
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb19358f98c1280ddb180b7381fb7714d28cc7db145ca36577f5f97f70c9f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509685"
---
# <a name="interlockedcomparestore-function"></a>Função InterlockedCompareStore

Ccompares a entrada para o valor de comparação, atomicamente.

## <a name="syntax"></a>Sintaxe

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
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

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta operação só pode ser executada em recursos tipados int ou uint e variáveis de memória compartilhada. Há três usos possíveis para essa função. A primeira é quando R é um tipo de variável de memória compartilhada. Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo dest. O segundo cenário é quando R é um tipo de variável de recurso. Nesse cenário, a função executa a operação no local do recurso referenciado pelo dest. Por fim, o terceiro cenário é quando R é um tipo de variável local. Nesse cenário, a função reduz para a operação executada usando operações locais.

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

 

 