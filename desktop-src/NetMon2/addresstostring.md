---
description: A função AddressToString converte um endereço em uma cadeia de caracteres.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Função AddressToString (Netmon. h)
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
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091794"
---
# <a name="addresstostring-function"></a>Função AddressToString

A função **AddressToString** converte um endereço em uma cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cadeia de caracteres* \[ fora\]
</dt> <dd>

Cadeia de caracteres para a qual o endereço é convertido.

</dd> <dt>

*lpAddress* \[ no\]
</dt> <dd>

O endereço que é impresso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um ponteiro para a cadeia de caracteres convertida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




