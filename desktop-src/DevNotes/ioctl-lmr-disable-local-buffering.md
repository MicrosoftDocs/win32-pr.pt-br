---
description: O LMR do IOCTL \_ \_ desabilitar o \_ \_ código de controle de buffer local desabilita o cache de dados na memória local do lado do cliente ao ler ou gravar dados em um arquivo remoto. Este é um código de controle definido internamente não disponível em um cabeçalho público.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING código de controle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749711"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>IOCTL \_ LMR \_ desabilitar \_ o \_ código de controle de buffer local

O LMR do IOCTL desabilitar o código de controle de **\_ \_ \_ \_ buffer local** desabilita o cache de dados na memória local do lado do cliente ao ler ou gravar dados em um arquivo remoto. Este é um código de controle definido internamente não disponível em um cabeçalho público.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* \[ no\]
</dt> <dd>

Um identificador para o arquivo remoto. Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ no\]
</dt> <dd>

O código de controle para a operação. Use o valor 0x140390 para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Não usado, deve ser **nulo**.

</dd> <dt>

*nInBufferSize* \[ no\]
</dt> <dd>

O tamanho do buffer de entrada, em bytes. Deve ser zero.

</dd> <dt>

*lpOutBuffer* \[ fora\]
</dt> <dd>

Não usado, deve ser **nulo**.

</dd> <dt>

*nOutBufferSize* \[ no\]
</dt> <dd>

O tamanho do buffer de saída em bytes. Deve ser zero.

</dd> <dt>

*lpBytesReturned* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.

Se o buffer de saída for muito pequeno, a chamada falhará, a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **\_ \_ buffer insuficiente de erro** e *lpBytesReturned* será zero.

Se o parâmetro *lpOverlapped* for **NULL**, *lpBytesReturned* não poderá ser **nulo**. Mesmo quando uma operação não retorna dados de saída e o parâmetro *lpOutBuffer* é **nulo**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*. Após tal operação, o valor de *lpBytesReturned* é inútil.

Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**. Se *lpOverlapped* não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída. Para recuperar o número de bytes retornados, chame a função [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Se o parâmetro *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.

Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona). Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento. Caso contrário, a função falhará de maneiras imprevisíveis.

Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída. Caso contrário, a função não retorna até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

O código de controle de **\_ \_ \_ \_ buffer local de LMR de IOCTL desabilitado** é definido internamente pelo sistema como 0x140390 e não em um arquivo de cabeçalho público. Ele é usado por aplicativos de finalidade especial para desabilitar o cache de dados na memória local do lado do cliente ao ler ou gravar dados em um arquivo remoto. Depois que o buffer local é desabilitado, a configuração permanece em vigor até que todos os identificadores abertos para o arquivo sejam fechados e o redirecionador Limpe suas estruturas de dados internas.

Os aplicativos de uso geral não devem usar o **IOCTL \_ LMR \_ desabilitar o \_ \_ buffer local**, pois isso pode resultar em excesso de tráfego de rede e perda associada de desempenho. O LMR de dados do IOCTL desabilitar o código de controle de **\_ \_ \_ \_ buffer local** deve ser usado somente em aplicativos especializados que movem grandes quantidades de dados pela rede ao tentar maximizar o uso da largura de banda da rede. Por exemplo, as funções [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) usam o **IOCTL \_ LMR \_ desabilitar o \_ \_ buffer local** para melhorar o desempenho de cópia de arquivo grande.

**IOCTL \_ LMR \_ desabilitar \_ o \_ buffer local** não é implementado por sistemas de arquivos locais e falhará com a **função erro de erro \_ inválida \_**. A emissão do código de controle de **\_ \_ \_ \_ buffer local LMR de IOCTL de desativação** em identificadores de diretório remoto falhará, com o erro de erro **\_ não \_ suportado**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
