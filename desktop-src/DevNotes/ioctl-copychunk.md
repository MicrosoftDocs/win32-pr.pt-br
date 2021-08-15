---
description: O código de controle COPYCHUNK de IOCTL inicia uma cópia do lado do servidor de um intervalo de \_ dados, também chamado de parte.
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
ms.openlocfilehash: 415e94d8ed19d3248beb31d8a5e6327e1adc11078483d4f60fcd42699e4dab89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001726"
---
# <a name="ioctl_copychunk-control-code"></a>Código de controle COPYCHUNK IOCTL \_

O **código de controle \_ COPYCHUNK de IOCTL** inicia uma cópia do lado do servidor de um intervalo de dados, também chamado de parte.

Para executar essa operação, chame a [**função DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


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

*hDevice* \[ Em\]
</dt> <dd>

Um handle para o arquivo que é o destino da operação de cópia do lado do servidor. Para obter esse handle, chame a [**função CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ Em\]
</dt> <dd>

O código de controle para a operação. Use **IOCTL \_ COPYCHUNK** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para o buffer de entrada, uma **estrutura \_ COPYCHUNK \_ COPY SRV.** Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

*nInBufferSize* \[ Em\]
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Um ponteiro para o buffer de saída, uma **estrutura SRV \_ COPYCHUNK \_ RESPONSE.** Para obter mais informações, consulte a seção Comentários.

</dd> <dt>

*nOutBufferSize* \[ Em\]
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.

Se o buffer de saída for muito pequeno, a chamada falhará, a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) **retornará ERROR \_ INSUFFICIENT \_ BUFFER** e *lpBytesReturned* será zero.

Se o *parâmetro lpOverlapped* for **NULL,** *lpBytesReturned* não poderá ser **NULL.** Mesmo quando uma operação não retorna dados de saída e o *parâmetro lpOutBuffer* é **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned*. Após essa operação, o valor de *lpBytesReturned* não tem sentido.

Se *lpOverlapped não* for **NULL,** *lpBytesReturned* poderá ser **NULL.** Se *lpOverlapped* não for **NULL** e a operação retornar dados, *lpBytesReturned* não terá sentido até que a operação sobrecarregada seja concluída. Para recuperar o número de bytes retornados, chame a [**função GetOverlappedResult.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) Se o *parâmetro hDevice* estiver associado a uma porta de conclusão de E/S, você poderá recuperar o número de bytes retornados chamando a [**função GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Se o *parâmetro hDevice* tiver sido aberto sem especificar **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* será ignorado.

Se *hDevice* tiver sido aberto com o sinalizador **FILE FLAG \_ \_ OVERLAPPED,** a operação será executada como uma operação sobressalo (assíncrona). Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento. Caso contrário, a função falhará de maneiras imprevisíveis.

Para operações sobreporadas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída. Caso contrário, a função não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Esse código de controle não tem nenhum arquivo de header associado. Você deve definir o código de controle e as estruturas de dados da seguinte forma.

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

Esses membros podem ser descritos da seguinte forma.



| Membro                                                                                                                                       | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**Sourceoffset**<br/>                     | O deslocamento, em bytes, do início do arquivo de origem para a parte a ser copiada.<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**Destinationoffset**<br/> | O deslocamento, em bytes, do início do arquivo de destino para o local em que a parte deve ser copiada.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Comprimento**<br/>                                             | O número de bytes de dados na parte a ser copiada. Deve ser maior que zero e menor ou igual a 1 MB. **Comprimento** \* **ChunkCount** deve ser menor ou igual a 16 MB.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**Sourcefile**<br/>                             | Uma chave que representa o arquivo de origem com os dados a serem copiados. Essa chave é obtida por meio de [**FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY**](fsctl-srv-request-resume-key.md).<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | O número de partes a serem copiadas. Deve ser maior que zero e menor ou igual a 256.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservados**<br/>                                     | Esse membro é reservado para uso do sistema; não use.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Pedaço**<br/>                                                 | Uma matriz de estruturas **\_ COPYCHUNK** **de ChunkCount** SRV, uma para cada parte a ser copiada. O comprimento, em bytes, dessa matriz deve ser **ChunkCount** \* sizeof(**SRV \_ COPYCHUNK**).<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**<br/>                 | Se a operação falhou com **ERROR \_ INVALID \_ PARAMETER**, esse valor indica o número máximo de partes que o servidor aceitará em uma única solicitação, que é 256. Caso contrário, esse valor indica o número de partes que foram escritas com êxito.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | Se a operação falhou com **ERROR \_ INVALID \_ PARAMETER**, esse valor indica o número máximo de bytes que o servidor permitirá que seja gravado em uma única parte, que é de 1 MB. Caso contrário, esse valor indica o número de bytes que foram gravados com êxito na última parte que não foi processada com êxito (se ocorreu uma gravação parcial).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | Se a operação falhou com **ERROR \_ INVALID \_ PARAMETER**, esse valor indica o número máximo de bytes que o servidor copiará em uma única solicitação, que é de 16 MB. Caso contrário, esse valor indica o número de bytes que foram gravados com êxito.<br/>                                                                                                 |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**CHAVE DE RETOMADA DA \_ SOLICITAÇÃO SRV FSCTL \_ \_ \_**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
