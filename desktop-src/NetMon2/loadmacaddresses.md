---
description: A função LoadMACAddresses é chamada pelo monitor para preencher uma lista de endereços MAC com endereços retirados de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Função LoadMACAddresses (Netmon.h)
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
ms.openlocfilehash: 2de609ef0a1e820785ee7d62cbbe1e6af32c633aa29b133974f6f5f6f2a649b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742716"
---
# <a name="loadmacaddresses-function"></a>Função LoadMACAddresses

A **função LoadMACAddresses** é chamada pelo monitor para preencher uma lista de endereços MAC com endereços retirados de uma variável de cadeia de caracteres de configuração HTML.

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

Ponteiro para um ponteiro para uma matriz de endereços. Se a variável especificada em *pVarName* for encontrada e tiver um comprimento não zero, a função aloca espaço suficiente (usando **HeapAllocMemory**) e armazena todos os endereços MAC como uma matriz.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Ponteiro para a **variável DWORD** definida como o número de endereços MAC retirados da cadeia de caracteres de configuração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida (o nome da variável foi encontrado e tinha uma cadeia de caracteres de comprimento diferente de zero que representou endereços MAC), o valor de retorno será **TRUE.**

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




