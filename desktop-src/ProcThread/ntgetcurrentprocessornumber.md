---
description: Recupera o número do processador em que o thread atual estava em execução durante a chamada para essa função.
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
ms.openlocfilehash: f45ee39e9599e2d77d77131eb64c2a9037de1f4ba31f907ac5c9ea562a706c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032186"
---
# <a name="ntgetcurrentprocessornumber-function"></a>Função NtGetCurrentProcessorNumber

\[**NtGetCurrentProcessorNumber** pode ser alterado ou não disponível em versões futuras do Windows. Os aplicativos devem usar [**a função GetCurrentProcessorNumber.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)\]

Recupera o número do processador em que o thread atual estava em execução durante a chamada para essa função.

## <a name="syntax"></a>Sintaxe


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

A função retorna o número atual do processador.

## <a name="remarks"></a>Comentários

Essa função é usada para fornecer informações para estimar o desempenho do processo.

Essa função não tem nenhuma biblioteca de importação associada. Você deve usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

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

 

 
