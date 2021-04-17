---
description: A função LookupWordSetString retorna a cadeia de caracteres correspondente ao valor solicitado de um conjunto rotulado.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Função LookupWordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501892"
---
# <a name="lookupwordsetstring-function"></a>Função LookupWordSetString

A função **LookupWordSetString** retorna a cadeia de caracteres correspondente ao valor solicitado de um conjunto rotulado.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpSet* 
</dt> <dd>

Rótulo definido a partir do qual você extrai o rótulo do valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de um conjunto rotulado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será uma cadeia de caracteres que corresponde ao valor solicitado.

Se a função não for bem-sucedida, o valor especificado não estará no conjunto, o valor de retorno será **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




