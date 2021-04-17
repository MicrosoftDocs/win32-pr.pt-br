---
description: A função LoadTCHAR é chamada por monitores para definir uma variável de cadeia de caracteres para uma cadeia de caracteres Obtida de uma cadeia de caracteres de configuração HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Função LoadTCHAR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790011"
---
# <a name="loadtchar-function"></a>Função LoadTCHAR

A função **LoadTCHAR** é chamada por monitores para definir uma variável de cadeia de caracteres para uma cadeia de caracteres Obtida de uma cadeia de caracteres de configuração html.

## <a name="syntax"></a>Sintaxe


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
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

*ppszString* \[ fora\]
</dt> <dd>

Ponteiro para um ponteiro de cadeia de caracteres. Se o nome de variável solicitado for encontrado, a cadeia de caracteres será alocada e atribuída a esse ponteiro. É responsabilidade do usuário liberar a memória associada à cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (se o nome da variável tiver sido encontrado e tiver uma cadeia de caracteres que não seja de comprimento zero), o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




