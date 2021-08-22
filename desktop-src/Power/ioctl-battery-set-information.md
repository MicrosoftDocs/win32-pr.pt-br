---
description: Define várias informações da bateria.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION de controle (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: be6fca1042c4ba381996ccca1740d1662f9795269aaaa8b3e429576d96011dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143489"
---
# <a name="ioctl_battery_set_information-control-code"></a>Código de controle IOCTL \_ BATTERY \_ SET \_ INFORMATION

Define várias informações da bateria. A estrutura do parâmetro de [**entrada, BATTERY \_ SET \_ INFORMATION**](battery-set-information-str.md), indica quais informações de status da bateria devem ser definidas.

Para executar essa operação, chame a [**função DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Uma alça para a bateria na qual as informações devem ser definidas. Para recuperar um alça de dispositivo, chame a [**função CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*Dwiocontrolcode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual ela será executada. Use **IOCTL \_ BATTERY SET \_ \_ INFORMATION** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para uma estrutura [**BATTERY \_ SET \_ INFORMATION.**](battery-set-information-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

</dd> <dt>

*Lpoutbuffer* 
</dt> <dd>

Não usado com essa operação; definido como **NULL.**

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Não usado com essa operação; definido como zero.

</dd> <dt>

*Lpbytesreturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados retornados no buffer *lpOutBuffer,* em bytes.

Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro ERROR INSUFFICIENT BUFFER e a contagem de \_ \_ byte retornada será zero.

Se *lpOverlapped* for **NULL** (E/S não mapeada), *lpBytesReturned* não poderá ser **NULL,** mesmo se *lpOutBuffer* for **NULL.**

Se *lpOverlapped* não for **NULL** (E/S sobrecarregada), *lpBytesReturned* poderá ser **NULL.** Se esta for uma operação sobrecarada, você poderá recuperar o número de bytes retornados chamando a [**função GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice* estiver associado a uma porta de conclusão de E/S, você poderá obter o número de bytes retornados chamando a [**função GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*Lpoverlapped* 
</dt> <dd>

Um ponteiro para uma [**estrutura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice* foi aberto com o sinalizador FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* deverá apontar para uma estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executado como uma operação sobressalo (assíncrona). Se o dispositivo tiver sido aberto com o sinalizador FILE \_ FLAG \_ OVERLAPPED e *lpOverlapped* for **NULL,** a função falhará de maneiras imprevisíveis.

Se *hDevice* tiver sido aberto sem especificar o sinalizador FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Todas as solicitações para definir informações da bateria serão concluídas com o status ARQUIVO DE ERRO NÃO ENCONTRADO se a marca de bateria da solicitação não corresponder à marca \_ \_ da bateria \_ atual.

Para ver as implicações da E/S sobrecarada nessa operação, consulte a seção Comentários do [**tópico DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h no Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Informações da bateria](battery-information.md)
</dt> <dt>

[Códigos de controle de gerenciamento de energia](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**INFORMAÇÕES DO \_ CONJUNTO DE \_ BATERIA**](battery-set-information-str.md)
</dt> <dt>

[**INFORMAÇÕES DE CONSULTA DA BATERIA IOCTL \_ \_ \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**STATUS DA CONSULTA DA BATERIA DE IOCTL \_ \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**MARCA DE \_ CONSULTA IOCTL BATTERY \_ \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

