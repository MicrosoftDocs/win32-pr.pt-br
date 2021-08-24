---
description: A função LoadIPAddresses é chamada pelo monitor para preencher uma lista de endereços IP com endereços retirados de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Função LoadIPAddresses (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f56517fd0caf4762be2848ac9a6f3094ed5e3194b2eb84123bf2fcc2bf67bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742666"
---
# <a name="loadipaddresses-function"></a>Função LoadIPAddresses

A **função LoadIPAddresses** é chamada pelo monitor para preencher uma lista de endereços IP com endereços retirados de uma variável de cadeia de caracteres de configuração HTML.

## <a name="syntax"></a>Sintaxe


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
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

Ponteiro para um ponteiro para uma matriz de endereços. Se a variável especificada em *pVarName* for encontrada e tiver um comprimento não zero, a função alocará espaço suficiente e armazenará todos os endereços IP como uma matriz.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Ponteiro para a **variável DWORD** definida como o número de endereços IP retirados da cadeia de caracteres de configuração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida (o nome da variável foi encontrado e tiver uma cadeia de caracteres de comprimento diferente de zero que representou endereços IP), o valor de retorno será **TRUE.**

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

Os endereços IP devem estar no formato x.x.x.x (por exemplo, 127.0.0.1).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




