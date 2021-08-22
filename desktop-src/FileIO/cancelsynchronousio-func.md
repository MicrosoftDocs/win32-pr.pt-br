---
description: Marca as operações de E/S síncronas pendentes emitidas pelo thread especificado como canceladas.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Função CancelSynchronousIo (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 1bdae4682bcbabb09778bdf5f5d3421c16af17587eda72813c9103eb16f7037f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582546"
---
# <a name="cancelsynchronousio-function"></a>Função CancelSynchronousIo

Marca as operações de E/S síncronas pendentes emitidas pelo thread especificado como canceladas.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hThread* \[ Em\]
</dt> <dd>

Um alça para o thread.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor de retorno será 0 (zero). Para obter informações de erro estendidas, chame a [**função GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Se essa função não puder encontrar uma solicitação para cancelar, o valor de retorno será 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **retornará ERROR \_ NOT \_ FOUND**.

## <a name="remarks"></a>Comentários

O chamador deve ter o [direito de acesso THREAD \_ TERMINATE.](/windows/desktop/ProcThread/thread-security-and-access-rights)

Se houver operações de E/S pendentes em andamento para o thread especificado, a função **CancelSynchronousIo** as marcará para cancelamento. A maioria dos tipos de operações pode ser cancelada imediatamente; outras operações podem continuar até a conclusão antes que elas sejam realmente canceladas e o chamador seja notificado. A **função CancelSynchronousIo** não aguarda a conclusão de todas as operações canceladas. Para obter mais informações, consulte [Diretrizes de conclusão/cancelamento de E/S.](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)

A operação que está sendo cancelada é concluída com um dos três status; você deve verificar o status de conclusão para determinar o estado de conclusão. Os três status são:

-   **A operação foi concluída normalmente.** Isso pode ocorrer mesmo que a operação tenha sido cancelada, porque a solicitação de cancelamento pode não ter sido enviada a tempo de cancelar a operação.
-   **A operação foi cancelada.** A [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **ERROR OPERATION \_ \_ ABORTED**.
-   **A operação falhou com outro erro.** A [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro relevante.

No Windows 8 e Windows Server 2012, essa função é suportada pelas tecnologias a seguir.



| Tecnologia                                           | Com suporte      |
|------------------------------------------------------|----------------|
| Protocolo SMB 3.0<br/>   | Sim<br/> |
| TFO (Failover Transparente) do SMB 3.0<br/>        | Sim<br/> |
| SMB 3.0 com SO (Compartilhamentos de Arquivos de Escalação Out)<br/>   | Sim<br/> |
| Volume Compartilhado Clusterizado sistema de arquivos (CsvFS)<br/> | Sim<br/> |
| ReFS (Sistema de Arquivos Resiliente)<br/>              | Sim<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                                                                                                                                                                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                                                                                                                                                                                    |
| Cabeçalho<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h no Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista (inclua Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[E/S síncrona e assíncrona](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

