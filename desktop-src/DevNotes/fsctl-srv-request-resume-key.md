---
description: O \_ código de \_ controle de chave de retomada de solicitação SRV fsctl \_ \_ é usado para recuperar uma referência de arquivo opaco para uso com o \_ código de controle COPYCHUNK do IOCTL.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY código de controle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826160"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>FSCTL \_ SRV \_ solicitar \_ retomar \_ código de controle de chave

O código de controle de **\_ \_ \_ \_ chave de retomada de solicitação SRV fsctl** é usado para recuperar uma referência de arquivo opaco para uso com o código de controle [**\_ COPYCHUNK do IOCTL**](ioctl-copychunk.md) .

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* \[ no\]
</dt> <dd>

Um identificador para o arquivo para o qual a chave do arquivo de origem deve ser solicitada. Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ no\]
</dt> <dd>

O código de controle para a operação. Use **a \_ \_ \_ \_ chave de retomada de solicitação do fsctl SRV** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Não usado com esta operação; Defina como **nulo**.

</dd> <dt>

*nInBufferSize* \[ no\]
</dt> <dd>

Não usado com esta operação; definido como zero.

</dd> <dt>

*lpOutBuffer* \[ fora\]
</dt> <dd>

Um ponteiro para o buffer de saída, **uma \_ solicitação \_ SRV \_ retomar** estrutura de chave. Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

*nOutBufferSize* \[ no\]
</dt> <dd>

O tamanho do buffer de saída em bytes.

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

Este código de controle não tem nenhum arquivo de cabeçalho associado. Você deve definir o código de controle e as estruturas de dados da seguinte maneira.

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

Esses membros podem ser descritos da seguinte maneira.



| Membro                                                                                                                       | DESCRIÇÃO                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**<br/>                 | Um valor opaco que identifica o arquivo de origem para o servidor.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Estampa**<br/>                 | Um valor opaco que identifica a hora em que o arquivo foi aberto.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pessoal**<br/>                                         | Um valor opaco que identifica o processo que abriu o arquivo.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Chaves**<br/>                                         | Uma estrutura de **\_ \_ chave de retomada SRV** . Para executar uma operação de cópia do lado do servidor, use essa estrutura com o código de controle [**\_ COPYCHUNK do IOCTL**](ioctl-copychunk.md) .<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**<br/> | Este membro é reservado para uso do sistema; Não use.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Noticioso**<br/>                         | Este membro é reservado para uso do sistema; Não use.<br/>                                                                                                              |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**COPYCHUNK de IOCTL \_**](ioctl-copychunk.md)
</dt> </dl>

 

 
