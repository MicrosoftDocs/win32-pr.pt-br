---
description: A função StringToAddress converte uma cadeia de caracteres em um endereço.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Função StringToAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760042"
---
# <a name="stringtoaddress-function"></a>Função StringToAddress

A função **StringToAddress** converte uma cadeia de caracteres em um endereço.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpAddress* \[ fora\]
</dt> <dd>

Ponteiro para o endereço para o qual a cadeia de caracteres é convertida.

</dd> <dt>

*cadeia de caracteres* \[ no\]
</dt> <dd>

Cadeia de caracteres que é convertida em um endereço.

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



 

 




