---
description: Recupera a marca atual das baterias.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG código de controle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759354"
---
# <a name="ioctl_battery_query_tag-control-code"></a>\_Código de \_ controle de marca de consulta da bateria do IOCTL \_

Recupera a marca atual da bateria.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para a bateria da qual a marca deve ser recuperada. Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo. Use **a \_ \_ \_ marca de consulta da bateria do IOCTL** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para um buffer de entrada **ULONG** . O valor indica o número de milissegundos a esperar se não houver bateria. Um valor de-1 indica que a solicitação aguardará indefinidamente (ou até ser cancelada por algum outro evento).

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Um ponteiro para um buffer de saída **ULONG** . Em caso de sucesso, esse buffer contém a marca de bateria atual, que pode ser qualquer valor, exceto a marca de bateria \_ \_ inválida. Em caso de falha, se [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornar o arquivo de erro de código de erro **\_ \_ não \_ encontrado**, esse buffer conterá a marca de bateria de valor **\_ \_ inválida**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer *lpOutBuffer* , em bytes.

Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro **\_ \_ buffer insuficiente** e o número de bytes retornados será zero.

Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**.

Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**. Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executada como uma operação sobreposta (assíncrona). Se o dispositivo tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.

Se *hDevice* tiver sido aberto sem especificar o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** , *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Esta bateria IOCTL recupera a marca atual da bateria. A marca de bateria é um valor exclusivo diferente de zero que muda quando a bateria física é reinserida, substituída ou passa por alterações de características. Consulte a seção marcas de bateria no tópico Visão geral [das informações da bateria](battery-information.md) para obter mais detalhes sobre quando uma marca de bateria é alterada, como detectar a alteração e como um aplicativo deve continuar após uma alteração na marca da bateria. Quando uma bateria não estiver presente, essa solicitação aguardará o horário indicado e, se ainda não houver bateria presente, ela retornará o arquivo de **erro \_ \_ não \_ encontrado** e definirá a marca de bateria como a **marca de bateria é \_ \_ inválida**. (Consulte informações da bateria para obter mais informações.)

Todas as solicitações para outras informações de bateria exigem que o chamador forneça a marca de bateria correspondente. Isso garante que o chamador esteja recebendo informações para a mesma bateria para cada solicitação e garante que o chamador esteja ciente das alterações de bateria sem sondagem constante.

Para as implicações da e/s sobreposta nessa operação, consulte a seção comentários do tópico [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [enumerando dispositivos de bateria](enumerating-battery-devices.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>BatClass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Informações da bateria](battery-information.md)
</dt> <dt>

[Códigos de controle de gerenciamento de energia](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_informações do \_ conjunto de baterias do IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

