---
description: A função MacTypeToAddressType converte um determinado tipo MAC em um tipo de endereço.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Função MacTypeToAddressType (Netmon.h)
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
ms.openlocfilehash: fe02cb6f0bec62a3bda35eabe288eafc2d5c3c15e422b7d68dc0b488546b83b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742316"
---
# <a name="mactypetoaddresstype-function"></a>Função MacTypeToAddressType

A **função MacTypeToAddressType** converte um determinado tipo MAC em um tipo de endereço.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MacType* \[ Em\]
</dt> <dd>

Tipo MAC a ser convertido. Especifique um dos seguintes valores:

MAC \_ TYPE \_ ETHERNET MAC \_ TYPE \_ TOKENRING MAC \_ TYPE \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um dos seguintes tipos de endereço.

TIPO \_ DE ENDEREÇO TIPO DE ENDEREÇO ETHERNET \_ \_ \_ TOKENING ADDRESS TYPE \_ \_ FDDI

Se a função não for bem-sucedida, o tipo MAC for desconhecido, o valor de retorno será -1.

## <a name="remarks"></a>Comentários

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função MacTypeToAddressType.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




