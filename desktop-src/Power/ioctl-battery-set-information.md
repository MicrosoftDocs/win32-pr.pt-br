---
description: Define várias informações de bateria.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION código de controle (Poclass. h)
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
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828370"
---
# <a name="ioctl_battery_set_information-control-code"></a>\_Código de \_ controle de informações do conjunto de baterias do IOCTL \_

Define várias informações de bateria. A estrutura do parâmetro de entrada, [**\_ \_ as informações do conjunto de bateria**](battery-set-information-str.md), indicam quais informações de status da bateria serão definidas.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


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

Um identificador para a bateria na qual as informações serão definidas. Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo. Use **\_ \_ \_ as informações do conjunto de bateria do IOCTL** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de conjunto de bateria**](battery-set-information-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

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

Um ponteiro para uma variável que recebe o tamanho dos dados retornados no buffer *lpOutBuffer* , em bytes.

Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro \_ buffer insuficiente \_ e o número de bytes retornados será zero.

Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**, mesmo se *lpOutBuffer* for **nulo**.

Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**. Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executada como uma operação sobreposta (assíncrona). Se o dispositivo tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.

Se *hDevice* tiver sido aberto sem especificar o \_ sinalizador sobreposto do sinalizador de arquivo \_ , *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Todas as solicitações para definir as informações da bateria serão concluídas com o status do arquivo de erro \_ \_ não \_ encontrado se a marca de bateria da solicitação não corresponder à da marca da bateria atual.

Para as implicações da e/s sobreposta nessa operação, consulte a seção comentários do tópico [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Informações da bateria](battery-information.md)
</dt> <dt>

[Códigos de controle de gerenciamento de energia](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_informações de conjunto de bateria \_**](battery-set-information-str.md)
</dt> <dt>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

