---
description: A função LookupByteSetString retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Função LookupByteSetString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 208f7cef1a658ae321d7ce03aaee763e5387b5a45985d59134418a4d136e0b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742496"
---
# <a name="lookupbytesetstring-function"></a>Função LookupByteSetString

A **função LookupByteSetString** retorna a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpSet* 
</dt> <dd>

Ponteiro para um conjunto rotulado, do qual você pode extrair o rótulo do valor.

</dd> <dt>

*Valor* 
</dt> <dd>

Valor de um conjunto rotulado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será uma cadeia de caracteres correspondente ao valor fornecido.

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




