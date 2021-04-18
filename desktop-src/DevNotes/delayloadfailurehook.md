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
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756218"
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

*pszDllName* \[ no\]
</dt> <dd>

O nome da DLL.

</dd> <dt>

*pszProcName* \[ no\]
</dt> <dd>

O nome do processo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 




