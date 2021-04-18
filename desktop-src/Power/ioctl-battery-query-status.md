---
description: Recupera o status atual da bateria.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS código de controle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787471"
---
# <a name="ioctl_battery_query_status-control-code"></a>\_Código de \_ controle do status de consulta da bateria do IOCTL \_

Recupera o status atual da bateria.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para a bateria a partir da qual as informações serão retornadas. Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo. Use **o \_ \_ \_ status de consulta da bateria do IOCTL** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ status de espera da bateria**](battery-wait-status-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ status da bateria**](battery-status-str.md) .

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados retornados no buffer *lpOutBuffer* , em bytes.

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

Essa bateria IOCTL recupera o status da bateria no momento em que a operação retorna. A estrutura do parâmetro de entrada, o [**\_ \_ status de espera da bateria**](battery-wait-status-str.md), indica quando o status da bateria deve ser processado e retornado.

As solicitações de status da bateria podem ser para o retorno imediato ou podem ser definidas para aguardar uma determinada condição antes de concluir. Por exemplo, é possível fazer uma solicitação de informações da bateria que aguarde até que a capacidade da bateria atinja um ponto especificado ou o estado da bateria seja alterado.

Todas as solicitações de informações da bateria serão concluídas com o status do **arquivo de erro \_ \_ não \_ encontrado** sempre que o elemento **BatteryTag** da solicitação não corresponder ao da marca da bateria atual. (Consulte [marcas de bateria](battery-information.md) para obter mais informações.) Isso é usado para garantir que as informações de bateria retornadas correspondam àquela da bateria solicitada.

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

[**STATUS da bateria \_**](battery-status-str.md)
</dt> <dt>

[**\_status de espera da bateria \_**](battery-wait-status-str.md)
</dt> <dt>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_informações do \_ conjunto de baterias do IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

