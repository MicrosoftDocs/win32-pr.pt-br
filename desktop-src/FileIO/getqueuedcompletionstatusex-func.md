---
description: Recupera várias entradas de porta de conclusão simultaneamente.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Função GetQueuedCompletionStatusEx (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f81bc0c997e3637fa941cb5a23f6394ba1f585566c8d633cadb00c9fd75ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696116"
---
# <a name="getqueuedcompletionstatusex-function"></a>Função GetQueuedCompletionStatusEx

Recupera várias entradas de porta de conclusão simultaneamente. Ele aguarda a conclusão das operações de E/S pendentes associadas à porta de conclusão especificada.

Para desassoar pacotes de conclusão de E/S um de cada vez, use a [**função GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CompletionPort* \[ Em\]
</dt> <dd>

Um alça para a porta de conclusão. Para criar uma porta de conclusão, use a [**função CreateIoCompletionPort.**](createiocompletionport.md)

</dd> <dt>

*lpCompletionPortEntries* \[ out\]
</dt> <dd>

Na entrada, aponta para uma matriz pré-alocada de [**estruturas OVERLAPPED \_ ENTRY.**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)

Na saída, recebe uma matriz de estruturas [**OVERLAPPED \_ ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) que mantém as entradas. O número de elementos de matriz é fornecido por *ulNumEntriesRemoved*.

O número de bytes transferidos durante cada E/S, a chave de conclusão que indica em qual arquivo cada E/S ocorreu e o endereço de estrutura sobressalo usado em cada E/S original são retornados na matriz *lpCompletionPortEntries.*

</dd> <dt>

*ulCount* \[ Em\]
</dt> <dd>

O número máximo de entradas a remover.

</dd> <dt>

*ulNumEntriesRemoved* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de entradas realmente removidas.

</dd> <dt>

*dwMilliseconds* \[ Em\]
</dt> <dd>

O número de milissegundos que o chamador está disposto a aguardar até que um pacote de conclusão apareça na porta de conclusão. Se um pacote de conclusão não aparecer dentro do tempo especificado, a função temporização e **retornará FALSE.**

Se *dwMilliseconds* for **INFINITE** (0xFFFFFFFF), a função nunca passará do tempo. Se *dwMilliseconds* for zero e não houver nenhuma operação de E/S para desem fila, a função passará do tempo de atividade imediatamente.

</dd> <dt>

*fAlertable* \[ Em\]
</dt> <dd>

Se esse parâmetro for **FALSE,** a função não retornará até que o período de tempo decorrido ou uma entrada seja recuperada.

Se o parâmetro for **TRUE** e não houver entradas disponíveis, a função executará uma espera alertável. O thread retorna quando o sistema enfileira uma rotina de conclusão de E/S ou APC para o thread e o thread executa a função.

Uma rotina de conclusão é enxuada quando a função [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) na qual ela foi especificada foi concluída e o thread de chamada é o thread que iniciou a operação. Um APC é enfileirodo quando você chama [**QueueUserAPC.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero (**TRUE**) se for bem-sucedido ou zero (**FALSE**) caso contrário.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Essa função associa um thread à porta de conclusão especificada. Um thread pode ser associado a no máximo uma porta de conclusão.

Essa função retorna **TRUE quando** pelo menos uma E/S pendente é concluída, mas é possível que uma ou mais operações de E/S falhem. Observe que cabe ao usuário dessa função verificar a lista de entradas retornadas no parâmetro *lpCompletionPortEntries* para determinar qual delas corresponde a todas as possíveis operações de E/S com falha observando o status contido no membro **lpOverlapped** em cada ENTRADA SOBRELAVADA . [**\_**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)

Essa função retorna **FALSE** quando nenhuma operação de E/S foi desaqueada. Normalmente, isso significa que ocorreu um erro durante o processamento dos parâmetros para essa chamada ou que o handle *CompletionPort* foi fechado ou, de outra forma, inválido. A [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fornece informações de erro estendidas.

Se uma chamada para [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) falhar porque o handle associado a ele está fechado, a função retornará **FALSE** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará **ERROR ABANDONED WAIT \_ \_ \_ 0**.

Os aplicativos de servidor podem ter vários threads chamando a **função GetQueuedCompletionStatusEx** para a mesma porta de conclusão. À medida que as operações de E/S são concluídas, elas são en na fila para essa porta na ordem de primeira entrada. Se um thread estiver aguardando ativamente essa chamada, uma ou mais solicitações na fila concluirão a chamada somente para esse thread.

Para obter mais informações sobre a teoria da porta de conclusão de [E/S,](i-o-completion-ports.md)o uso e as funções associadas, consulte Portas de conclusão de E/S .

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
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                                                                                                                                                                                                                   |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                                                                                                                                                                                                             |
| Cabeçalho<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h no Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista (inclua Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Tópicos de visão geral**
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[Portas de conclusão de E/S](i-o-completion-ports.md)
</dt> <dt>

[Usando os Windows de dados](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Funções**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**Createiocompletionport**](createiocompletionport.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**Waitcommevent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

