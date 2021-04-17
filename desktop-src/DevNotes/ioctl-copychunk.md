---
description: O \_ código de controle COPYCHUNK do IOCTL inicia uma cópia do lado do servidor de um intervalo de dados, também chamado de parte.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK código de controle
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811249"
---
# <a name="ioctl_copychunk-control-code"></a>Código de controle de COPYCHUNK do IOCTL \_

O código de controle **\_ COPYCHUNK do IOCTL** inicia uma cópia do lado do servidor de um intervalo de dados, também chamado de parte.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

Um identificador para o arquivo que é o destino da operação de cópia do lado do servidor. Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ no\]
</dt> <dd>

O código de controle para a operação. Use **o \_ COPYCHUNK do IOCTL** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para o buffer de entrada, uma estrutura de **\_ \_ cópia COPYCHUNK SRV** . Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

*nInBufferSize* \[ no\]
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

</dd> <dt>

*lpOutBuffer* \[ fora\]
</dt> <dd>

Um ponteiro para o buffer de saída, uma estrutura de **\_ \_ resposta de COPYCHUNK SRV** . Para obter mais informações, consulte a seção Comentários.

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
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

Esses membros podem ser descritos da seguinte maneira.



| Membro                                                                                                                                       | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**<br/>                     | O deslocamento, em bytes, desde o início do arquivo de origem até a parte a ser copiada.<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**<br/> | O deslocamento, em bytes, desde o início do arquivo de destino até o local onde a parte deve ser copiada.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Muito**<br/>                                             | O número de bytes de dados na parte a serem copiados. Deve ser maior que zero e menor ou igual a 1 MB. **Comprimento** \* **ChunkCount** deve ser menor ou igual a 16 MB.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | Uma chave que representa o arquivo de origem com os dados a serem copiados. Essa chave é obtida por meio da [**\_ \_ \_ \_ chave de retomada de solicitação do fsctl SRV**](fsctl-srv-request-resume-key.md).<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | O número de partes a serem copiadas. Deve ser maior que zero e menor ou igual a 256.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado**<br/>                                     | Este membro é reservado para uso do sistema; Não use.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Codificação**<br/>                                                 | Uma matriz de estruturas **\_ COPYCHUNK** **ChunkCount** SRV, uma para cada parte a ser copiada. O comprimento, em bytes, dessa matriz deve ser **ChunkCount** \* sizeof (**SRV \_ COPYCHUNK**).<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**<br/>                 | Se a operação falhou com **um \_ \_ parâmetro de erro inválido**, esse valor indica o número máximo de partes que o servidor aceitará em uma única solicitação, que é 256. Caso contrário, esse valor indica o número de partes que foram gravadas com êxito.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | Se a operação falhou com **um \_ \_ parâmetro de erro inválido**, esse valor indica o número máximo de bytes que o servidor permitirá para ser gravado em uma única parte, que é 1 MB. Caso contrário, esse valor indica o número de bytes que foram gravados com êxito na última parte que não foi processada com êxito (se ocorrer uma gravação parcial).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | Se a operação falhou com **um \_ \_ parâmetro de erro inválido**, esse valor indica o número máximo de bytes que o servidor copiará em uma única solicitação, que é 16 MB. Caso contrário, esse valor indica o número de bytes que foram gravados com êxito.<br/>                                                                                                 |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_chave de \_ \_ retomada de solicitação do fsctl SRV \_**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
