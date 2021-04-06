---
description: A função MacTypeToAddressType converte um determinado tipo de MAC em um tipo de endereço.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Função MacTypeToAddressType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827259"
---
# <a name="mactypetoaddresstype-function"></a>Função MacTypeToAddressType

A função **MacTypeToAddressType** converte um determinado tipo de Mac em um tipo de endereço.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MacType* \[ no\]
</dt> <dd>

Tipo de MAC a ser convertido. Especifique um dos seguintes valores:

MAC \_ tipo \_ Ethernet Mac \_ tipo \_ TOKENRING Mac \_ tipo \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um dos seguintes tipos de endereço.

tipo de endereço \_ \_ Ethernet tipo de endereço \_ \_ TOKENRING tipo de endereço \_ \_ FDDI

Se a função não for bem-sucedida, o tipo de MAC será desconhecido, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **MacTypeToAddressType** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




