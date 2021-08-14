---
description: A função AddressToString converte um endereço em uma cadeia de caracteres.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Função AddressToString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 58c105fb8fa646fbffcc7d7d4a3f1dad3a9cd86e7bb6ef8cc426dc982873f720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796366"
---
# <a name="addresstostring-function"></a>Função AddressToString

A **função AddressToString** converte um endereço em uma cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cadeia de caracteres* \[ out\]
</dt> <dd>

Cadeia de caracteres em que o endereço é convertido.

</dd> <dt>

*lpAddress* \[ Em\]
</dt> <dd>

O endereço impresso.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um ponteiro para a cadeia de caracteres convertida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




