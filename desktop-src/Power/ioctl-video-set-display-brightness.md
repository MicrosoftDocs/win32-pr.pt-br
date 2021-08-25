---
description: Define os níveis atuais de luz de CA e CC.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS código de controle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: ec4bb5200378f9f530913f26d33bfbd485d81ae184c7b478a51c90bca18d95da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961846"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>Conjunto de vídeos do IOCTL \_ \_ \_ Exibir \_ código de controle de brilho

Define os níveis atuais de luz de CA e CC.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo. Use **o \_ vídeo do IOCTL \_ definir \_ \_ brilho de vídeo** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ brilho de vídeo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

O tamanho do buffer apontado por *lpOutBuffer*, em bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Não usado com esta operação; Defina como **nulo**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Não usado com esta operação; definido como zero.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe a contagem real de bytes retornados pela função no buffer de saída.

Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* será usado internamente e não poderá ser **nulo**.

Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. Nesse caso, a operação é executada como uma operação sobreposta (assíncrona). Se o dispositivo tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.

Se *hDevice* tiver sido aberto sem especificar o \_ sinalizador sobreposto do sinalizador de arquivo \_ , *lpOverlapped* será ignorado e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Os valores especificados nos membros **ucACBrightness** e **ucDCBrightness** da estrutura de [**\_ brilho de vídeo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) devem ter sido retornados anteriormente pelo [**\_ \_ \_ \_ brilho suportado pela consulta de vídeo do IOCTL**](ioctl-video-query-supported-brightness.md). Por exemplo, se os valores com suporte forem 10, 20, 30, 40, 50, 60, 70, 80, 90 e 100, o uso de um valor de 33 seria um erro.

o arquivo de cabeçalho usado para criar aplicativos que incluem essa funcionalidade, Ntddvdeo. h, está incluído no Microsoft Windows Driver Development Kit (DDK). Para obter informações sobre como obter o DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Como alternativa, você pode definir esse código de controle da seguinte maneira:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, somente Windows XP com \[ aplicativos de área de trabalho do SP1\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interface de controle de luz Invista](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**brilho da tela \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**\_brilho de \_ exibição de consulta de vídeo do IOCTL \_ \_**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**\_ \_ \_ brilho com suporte para consulta de vídeo do IOCTL \_**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

