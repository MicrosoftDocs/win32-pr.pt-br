---
description: A função LoadIPXAddresses é chamada pelo monitor para preencher uma lista de endereços IPX Obtida de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Função LoadIPXAddresses (Netmon. h)
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
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171286"
---
# <a name="loadipxaddresses-function"></a>Função LoadIPXAddresses

A função **LoadIPXAddresses** é chamada pelo monitor para preencher uma lista de endereços IPX Obtida de uma variável de cadeia de caracteres de configuração html.

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

*pConfig* \[ no\]
</dt> <dd>

Ponteiro para a cadeia de caracteres de configuração HTML passado para o monitor pelo método [Imonitor::D oconfigure](imonitor-doconfigure.md) .

</dd> <dt>

*pVarName* \[ no\]
</dt> <dd>

Ponteiro para o nome da variável na cadeia de caracteres de configuração.

</dd> <dt>

*ppAddresses* \[ fora\]
</dt> <dd>

Ponteiro para um ponteiro para uma matriz de endereços. Se a variável especificada em *pVarName* for encontrada e tiver um comprimento diferente de zero, o espaço suficiente será alocado (usando **HeapAllocMemory**) e todos os endereços IPX serão armazenados como uma matriz.

</dd> <dt>

*pNumAddresses* \[ fora\]
</dt> <dd>

Ponteiro para a variável **DWORD** que é definido como o número de endereços IPX extraídos da cadeia de caracteres de configuração.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (o nome da variável foi encontrado e tiver uma cadeia de caracteres que não seja de comprimento zero que representou endereços IPX), o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




