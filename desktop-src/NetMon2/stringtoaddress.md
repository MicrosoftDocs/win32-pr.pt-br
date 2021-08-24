---
description: A função StringToAddress converte uma cadeia de caracteres em um endereço.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Função StringToAddress (Netmon.h)
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
ms.openlocfilehash: 9dbac01f5df9d32a65fe5afb1c1437064f6dd0d4480c95dacd0fe8f7d58e2fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676686"
---
# <a name="stringtoaddress-function"></a>Função StringToAddress

A **função StringToAddress** converte uma cadeia de caracteres em um endereço.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpAddress* \[ out\]
</dt> <dd>

Ponteiro para o endereço em que a cadeia de caracteres é convertida.

</dd> <dt>

*cadeia de caracteres* \[ Em\]
</dt> <dd>

Cadeia de caracteres convertida em um endereço.

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



 

 




