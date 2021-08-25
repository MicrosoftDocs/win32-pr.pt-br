---
description: A função LoadTCHAR é chamada pelos monitores para definir uma variável de cadeia de caracteres como uma cadeia de caracteres retirada de uma cadeia de caracteres de configuração HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Função LoadTCHAR (Netmon.h)
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
ms.openlocfilehash: 2d85419485e2442f82c94948b832914fa30e44396f266eed10cd1545b4cc28ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890282"
---
# <a name="loadtchar-function"></a>Função LoadTCHAR

A **função LoadTCHAR é** chamada pelos monitores para definir uma variável de cadeia de caracteres como uma cadeia de caracteres retirada de uma cadeia de caracteres de configuração HTML.

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

*pConfig* \[ Em\]
</dt> <dd>

Ponteiro para a cadeia de caracteres de configuração HTML passada para o monitor pelo [método IMonitor::D oConfigure.](imonitor-doconfigure.md)

</dd> <dt>

*pVarName* \[ Em\]
</dt> <dd>

Ponteiro para o nome da variável na cadeia de caracteres de configuração.

</dd> <dt>

*ppszString* \[ out\]
</dt> <dd>

Ponteiro para um ponteiro de cadeia de caracteres. Se o nome da variável solicitada for encontrado, a cadeia de caracteres será alocada e atribuída a esse ponteiro. É responsabilidade do usuário liberar a memória associada à cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida (se o nome da variável tiver sido encontrado e tiver uma cadeia de caracteres de comprimento diferente de zero), o valor de retorno será **TRUE.**

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




