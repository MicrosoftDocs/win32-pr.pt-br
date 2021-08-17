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
ms.openlocfilehash: 15b529076660eec093df370df47823fb21aa13e53cce61565fe82de7fbb7e017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364714"
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

## <a name="return-value"></a>Valor retornado

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



 

 




