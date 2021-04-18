---
description: A função loaddword é chamada pelo monitor para definir uma variável DWORD com um valor extraído de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Função loaddword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778537"
---
# <a name="loaddword-function"></a>Função loaddword

A função **loaddword** é chamada pelo monitor para definir uma variável **DWORD** com um valor extraído de uma variável de cadeia de caracteres de configuração html.

## <a name="syntax"></a>Sintaxe


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pConfig* \[ no\]
</dt> <dd>

Ponteiro para a cadeia de caracteres de configuração HTML passado para o monitor pelo método [Imonitor::D oconfigure](imonitor-doconfigure.md) .

</dd> <dt>

*pVarName* \[ no\]
</dt> <dd>

Ponteiro para o nome da variável na cadeia de caracteres de configuração.

</dd> <dt>

*valores* \[ no\]
</dt> <dd>

Ponteiro para a variável **DWORD** que é definida como o valor da variável de cadeia de caracteres de configuração.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (se o nome da variável tiver sido encontrado e tiver uma cadeia de caracteres que não seja de comprimento zero), o **DWORD** será inserido e o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




