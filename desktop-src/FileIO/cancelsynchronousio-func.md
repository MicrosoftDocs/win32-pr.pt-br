---
description: Marca as operações de e/s síncronas pendentes emitidas pelo thread especificado como canceladas.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Função CancelSynchronousIo (IoAPI. h)
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
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506178"
---
# <a name="cancelsynchronousio-function"></a>Função CancelSynchronousIo

Marca as operações de e/s síncronas pendentes emitidas pelo thread especificado como canceladas.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hThread* \[ no\]
</dt> <dd>

Um identificador para o thread.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor de retorno será 0 (zero). Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Se essa função não puder localizar uma solicitação para cancelar, o valor de retorno será 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o **erro \_ não \_ encontrado**.

## <a name="remarks"></a>Comentários

O chamador deve ter o direito de acesso de [ \_ término de thread](/windows/desktop/ProcThread/thread-security-and-access-rights) .

Se houver alguma operação de e/s pendente em andamento para o thread especificado, a função **CancelSynchronousIo** as marcará para cancelamento. A maioria dos tipos de operações pode ser cancelada imediatamente; outras operações podem continuar na conclusão antes de serem realmente canceladas e o chamador é notificado. A função **CancelSynchronousIo** não aguarda a conclusão de todas as operações canceladas. Para obter mais informações, consulte [diretrizes de conclusão/cancelamento de e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

A operação que está sendo cancelada é concluída com um dos três status; Você deve verificar o status de conclusão para determinar o estado de conclusão. Os três status são:

-   **A operação foi concluída normalmente.** Isso pode ocorrer mesmo que a operação tenha sido cancelada, porque a solicitação de cancelamento pode não ter sido enviada a tempo para cancelar a operação.
-   **A operação foi cancelada.** A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna a **operação de erro \_ \_ anulada**.
-   **A operação falhou com outro erro.** A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro relevante.

No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.



| Tecnologia                                           | Com suporte      |
|------------------------------------------------------|----------------|
| Protocolo SMB (Server Message Block) 3,0<br/>   | Yes<br/> |
| Failover transparente SMB 3,0 (TFO)<br/>        | Yes<br/> |
| SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)<br/>   | Yes<br/> |
| Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)<br/> | Yes<br/> |
| ReFS (Sistema de Arquivos Resiliente)<br/>              | Yes<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                                                                                                                                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                                                                                                                                    |
| parâmetro<br/>                   | <dl> <dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluir Windows. h)</dt> </dl> |
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

[E/s síncrona e síncrona](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

