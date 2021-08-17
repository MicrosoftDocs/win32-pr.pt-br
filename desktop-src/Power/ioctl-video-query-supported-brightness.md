---
description: Recupera os níveis de luz de fundo com suporte.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS código de controle (Ntddvdeo.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 0c41b6773b0ed64160e2ad8850b6092dd5ec987c3e6726ba1cd668909c266311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143389"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a>Código de controle \_ \_ \_ BRIGHTNESS COM SUPORTE PARA CONSULTA DE VÍDEO IOCTL \_

Recupera os níveis de luz de fundo com suporte.

Para executar essa operação, chame a [**função DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um alça para o \\ \\ . \\ Dispositivo LCD. Para recuperar um alça de dispositivo, chame a [**função CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*Dwiocontrolcode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual ela será executada. Use **IOCTL \_ VIDEO \_ QUERY \_ SUPPORTED \_ BRIGHTNESS** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Não usado com essa operação; definido como **NULL.**

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Não usado com essa operação; definido como zero.

</dd> <dt>

*Lpoutbuffer* 
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz dos níveis de energia disponíveis. Esse buffer deve ter 256 bytes de comprimento.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*Lpbytesreturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de saída retornados.

Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro ERROR INSUFFICIENT BUFFER e a contagem de \_ \_ byte retornada será zero.

Se o buffer de saída for muito pequeno para conter todos os dados, mas puder conter algumas entradas, o sistema operacional retornará o máximo que se adequar, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro ERROR MORE DATA e \_ \_ *lpBytesReturned* indicará a quantidade de dados retornados. Seu aplicativo deve chamar [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) novamente com a mesma operação, especificando um novo ponto de partida.

Se *lpOverlapped* for **NULL** (E/S não mapeada), *lpBytesReturned* não poderá ser **NULL.**

Se *lpOverlapped* não for **NULL** (E/S sobrecarregada), *lpBytesReturned* poderá ser **NULL.** Se esta for uma operação sobrecarada, você poderá recuperar o número de bytes retornados chamando a [**função GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice* estiver associado a uma porta de conclusão de E/S, você poderá obter o número de bytes retornados chamando a [**função GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*Lpoverlapped* 
</dt> <dd>

Um ponteiro para uma [**estrutura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice* foi aberto com o sinalizador FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* deverá apontar para uma estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. Nesse caso, a operação é executada como uma operação sobressalo (assíncrona). Se o dispositivo tiver sido aberto com o sinalizador FILE \_ FLAG \_ OVERLAPPED e *lpOverlapped* for **NULL,** a função falhará de maneiras imprevisíveis.

Se *hDevice* tiver sido aberto sem especificar o sinalizador FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* será ignorado e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Cada elemento na *matriz lpOutBuffer* tem um byte de comprimento. Portanto, no retorno, *o parâmetro lpBytesReturned* indica o número de níveis com suporte. Cada nível é um valor de 0 a 100. Quanto maior o valor, maior a luz de fundo. Todos os níveis têm suporte se a fonte de alimentação é AC ou DC.

O arquivo de header usado para criar aplicativos que incluem essa funcionalidade, Ntddvdeo.h, está incluído no DDK (Kit de Desenvolvimento de Driver) do Microsoft Windows. Para obter informações sobre como obter o DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Como alternativa, você pode definir esse código de controle da seguinte maneira:

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP1 \[\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Ntddvdeo.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interface de controle de luz de fundo](backlight-control-interface.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

