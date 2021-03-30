---
description: A função LookupDwordSetString retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Função LookupDwordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647321"
---
# <a name="lookupdwordsetstring-function"></a>Função LookupDwordSetString

A função **LookupDwordSetString** retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpSet* 
</dt> <dd>

Conjunto rotulado, do qual você pode extrair o rótulo do valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de um conjunto rotulado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será a cadeia de caracteres que corresponde ao valor especificado.

Se a função não for bem-sucedida, o valor especificado não estará no conjunto, o valor de retorno será **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




