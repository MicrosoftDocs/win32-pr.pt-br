---
description: Retorna o endereço de uma função de retorno de chamada de falha de carregamento de atraso para a DLL e o processo especificados.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: Função DelayLoadFailureHook
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: 8724073a8f5f124cf23d6ba15390c8028d308354aa1e2c896f1d2c9f5030ea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795277"
---
# <a name="delayloadfailurehook-function"></a>Função DelayLoadFailureHook

Retorna o endereço de uma função de retorno de chamada de falha de carregamento de atraso para a DLL e o processo especificados.

## <a name="syntax"></a>Sintaxe


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszDllName* \[ Em\]
</dt> <dd>

O nome da DLL.

</dd> <dt>

*pszProcName* \[ Em\]
</dt> <dd>

O nome do processo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O endereço da função de retorno de chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Ganchos de falha](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




