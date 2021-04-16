---
description: Recupera o número do processador no qual o thread atual estava sendo executado durante a chamada para essa função.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Função NtGetCurrentProcessorNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757744"
---
# <a name="ntgetcurrentprocessornumber-function"></a>Função NtGetCurrentProcessorNumber

\[O **NtGetCurrentProcessorNumber** pode ser alterado ou indisponível em versões futuras do Windows. Em vez disso, os aplicativos devem usar a função [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) .\]

Recupera o número do processador no qual o thread atual estava sendo executado durante a chamada para essa função.

## <a name="syntax"></a>Sintaxe


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

A função retorna o número de processador atual.

## <a name="remarks"></a>Comentários

Essa função é usada para fornecer informações para estimar o desempenho do processo.

Esta função não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vários processadores](multiple-processors.md)
</dt> <dt>

[Funções de thread e processo](process-and-thread-functions.md)
</dt> <dt>

[Processos](child-processes.md)
</dt> </dl>

 

 
