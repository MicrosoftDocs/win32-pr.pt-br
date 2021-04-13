---
description: A função LoadMACAddresses é chamada pelo monitor para preencher uma lista de endereços MAC com endereços extraídos de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Função LoadMACAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501894"
---
# <a name="loadmacaddresses-function"></a>Função LoadMACAddresses

A função **LoadMACAddresses** é chamada pelo monitor para preencher uma lista de endereços MAC com endereços extraídos de uma variável de cadeia de caracteres de configuração html.

## <a name="syntax"></a>Sintaxe


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
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

Ponteiro para um ponteiro para uma matriz de endereços. Se a variável especificada em *pVarName* for encontrada e tiver um comprimento diferente de zero, a função alocará espaço suficiente (usando **HeapAllocMemory**) e armazenará todos os endereços MAC como uma matriz.

</dd> <dt>

*pNumAddresses* \[ fora\]
</dt> <dd>

Ponteiro para a variável **DWORD** que é definido como o número de endereços MAC obtidos da cadeia de caracteres de configuração.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, (o nome da variável foi encontrado e tinha uma cadeia de comprimento diferente de zero que representava endereços MAC), o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




