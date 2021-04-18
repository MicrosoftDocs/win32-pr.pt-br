---
description: Recupera simultaneamente várias entradas de porta de conclusão.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Função GetQueuedCompletionStatusEx (IoAPI. h)
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
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757159"
---
# <a name="getqueuedcompletionstatusex-function"></a>Função GetQueuedCompletionStatusEx

Recupera simultaneamente várias entradas de porta de conclusão. Ele aguarda que as operações de e/s pendentes associadas à porta de conclusão especificada sejam concluídas.

Para remover os pacotes de conclusão de e/s da fila um de cada vez, use a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

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

*CompletionPort* \[ no\]
</dt> <dd>

Um identificador para a porta de conclusão. Para criar uma porta de conclusão, use a função [**CreateIoCompletionPort**](createiocompletionport.md) .

</dd> <dt>

*lpCompletionPortEntries* \[ fora\]
</dt> <dd>

Na entrada, aponta para uma matriz pré-configurada de estruturas de [**\_ entrada sobrepostas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .

Na saída, recebe uma matriz de estruturas de [**\_ entrada sobrepostas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) que contêm as entradas. O número de elementos de matriz é fornecido por *ulNumEntriesRemoved*.

O número de bytes transferidos durante cada e/s, a chave de conclusão que indica em qual arquivo cada e/s ocorreu e o endereço da estrutura sobreposta usado em cada e/s original são todos retornados na matriz *lpCompletionPortEntries* .

</dd> <dt>

*ulCount* \[ no\]
</dt> <dd>

O número máximo de entradas a serem removidas.

</dd> <dt>

*ulNumEntriesRemoved* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de entradas realmente removidas.

</dd> <dt>

*dwMilliseconds* \[ no\]
</dt> <dd>

O número de milissegundos que o chamador está disposto a aguardar a exibição de um pacote de conclusão na porta de conclusão. Se um pacote de conclusão não aparecer dentro do tempo especificado, a função expirará e retornará **false**.

Se *dwMilliseconds* for **infinito** (0xFFFFFFFF), a função nunca atingirá o tempo limite. Se *dwMilliseconds* for zero e não houver nenhuma operação de e/s para remover da fila, a função atingirá o tempo limite imediatamente.

</dd> <dt>

*fAlertable* \[ no\]
</dt> <dd>

Se esse parâmetro for **false**, a função não retornará até que o período de tempo limite tenha decorrido ou uma entrada seja recuperada.

Se o parâmetro for **true** e não houver entradas disponíveis, a função executará uma espera alertável. O thread retorna quando o sistema enfileira uma rotina de conclusão de e/s ou a APC para o thread e o thread executa a função.

Uma rotina de conclusão é enfileirada quando a função [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) na qual ela foi especificada foi concluída, e o thread de chamada é o thread que iniciou a operação. Uma APC é enfileirada quando você chama [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero (**true**) se for bem-sucedido ou zero (**false**) caso contrário.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Essa função associa um thread à porta de conclusão especificada. Um thread pode ser associado a no máximo uma porta de conclusão.

Essa função retorna **true** quando pelo menos uma e/s pendente é concluída, mas é possível que uma ou mais operações de e/s tenham falhado. Observe que cabe ao usuário dessa função verificar a lista de entradas retornadas no parâmetro *lpCompletionPortEntries* para determinar quais delas correspondem a quaisquer possíveis operações de e/s com falha examinando o status contido no membro **lpOverlapped** em cada [**\_ entrada sobreposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).

Essa função retorna **false** quando nenhuma operação de e/s foi removida da fila. Isso normalmente significa que ocorreu um erro durante o processamento dos parâmetros para esta chamada ou que o identificador *CompletionPort* foi fechado ou é inválido. A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fornece informações de erro estendidas.

Se uma chamada para [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) falhar porque o identificador associado a ela está fechado, a função retornará **false** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o **erro \_ abandonado \_ aguardando \_ 0**.

Os aplicativos de servidor podem ter vários threads chamando a função **GetQueuedCompletionStatusEx** para a mesma porta de conclusão. À medida que as operações de e/s são concluídas, elas são enfileiradas para essa porta na ordem de primeiro a entrar, primeiro a sair. Se um thread estiver aguardando ativamente nesta chamada, uma ou mais solicitações enfileiradas concluirão a chamada somente para esse thread.

Para obter mais informações sobre a teoria, uso e funções associadas da porta de conclusão de e/s, consulte [portas de conclusão de e/s](i-o-completion-ports.md).

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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                                                                                                                                                                                                                   |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                                                                                                                                                                                                             |
| parâmetro<br/>                   | <dl> <dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Tópicos de visão geral**
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[Portas de conclusão de e/s](i-o-completion-ports.md)
</dt> <dt>

[Usando os cabeçalhos do Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Funções**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
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

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

