---
description: Recupera os níveis de luz de realce com suporte.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS código de controle (Ntddvdeo. h)
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
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757489"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a>\_Código de \_ controle de \_ brilho com suporte da consulta de vídeo do IOCTL \_

Recupera os níveis de luz de realce com suporte.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


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

Um identificador para o \\ \\ . \\ Dispositivo LCD. Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo. Use o **brilho de consulta de vídeo do IOCTL \_ \_ \_ com suporte \_** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Não usado com esta operação; Defina como **nulo**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Não usado com esta operação; definido como zero.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz dos níveis de energia disponíveis. Esse buffer deve ter 256 bytes de comprimento.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de saída retornados.

Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro \_ buffer insuficiente \_ e o número de bytes retornados será zero.

Se o buffer de saída for muito pequeno para conter todos os dados, mas puder conter algumas entradas, o sistema operacional retornará o máximo que se ajustar, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro com \_ mais \_ dados e *lpBytesReturned* indicará a quantidade de dados retornados. Seu aplicativo deve chamar [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) novamente com a mesma operação, especificando um novo ponto de partida.

Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**.

Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**. Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. Nesse caso, a operação é executada como uma operação sobreposta (assíncrona). Se o dispositivo tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.

Se *hDevice* tiver sido aberto sem especificar o \_ sinalizador sobreposto do sinalizador de arquivo \_ , *lpOverlapped* será ignorado e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Cada elemento na matriz *lpOutBuffer* tem um byte de comprimento. Portanto, após o retorno, o parâmetro *lpBytesReturned* indica o número de níveis com suporte. Cada nível é um valor de 0 a 100. Quanto maior o valor, mais claro a luz. Todos os níveis têm suporte se a fonte de energia for AC ou DC.

O arquivo de cabeçalho usado para criar aplicativos que incluem essa funcionalidade, Ntddvdeo. h, está incluído no Microsoft Windows Driver Development Kit (DDK). Para obter informações sobre como obter o DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Como alternativa, você pode definir esse código de controle da seguinte maneira:

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos do Windows Vista, Windows XP com SP1 para \[ Desktop\]<br/>                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interface de controle de luz Invista](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

