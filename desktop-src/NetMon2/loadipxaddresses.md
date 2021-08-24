---
description: A função LoadIPXAddresses é chamada pelo monitor para preencher uma lista de endereços IPX retirada de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Função LoadIPXAddresses (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ed8bb6948102e8d28150edf102fa261c9c7f7adfcf105e377352054304b352df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677306"
---
# <a name="loadipxaddresses-function"></a>Função LoadIPXAddresses

A **função LoadIPXAddresses** é chamada pelo monitor para preencher uma lista de endereços IPX retirada de uma variável de cadeia de caracteres de configuração HTML.

## <a name="syntax"></a>Sintaxe


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
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

*ppAddresses* \[ out\]
</dt> <dd>

Ponteiro para um ponteiro para uma matriz de endereços. Se a variável especificada em *pVarName* for encontrada e tiver um comprimento não zero, espaço suficiente será alocado (usando **HeapAllocMemory**) e todos os endereços IPX serão armazenados como uma matriz.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Ponteiro para a **variável DWORD** definida como o número de endereços IPX retirados da cadeia de caracteres de configuração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida (o nome da variável foi encontrado e tiver uma cadeia de caracteres de comprimento diferente de zero que representou endereços IPX), o valor de retorno será **TRUE.**

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




