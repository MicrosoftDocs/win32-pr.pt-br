---
description: A função HTMLValueToUnicode converte uma \_ cadeia de caracteres HTML CP UTF8 em uma cadeia de caracteres Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Função HTMLValueToUnicode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646791"
---
# <a name="htmlvaluetounicode-function"></a>Função HTMLValueToUnicode

A função **HTMLValueToUnicode** converte uma \_ cadeia de caracteres HTML CP UTF8 em uma cadeia de caracteres Unicode.

## <a name="syntax"></a>Sintaxe


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valores* \[ entrada, saída\]
</dt> <dd>

Na entrada, ponteiro para a cadeia de caracteres HTML fornecida pelo MCSVC.

Na saída, ponteiro para a cadeia de caracteres Unicode convertida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o equivalente Unicode da cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




