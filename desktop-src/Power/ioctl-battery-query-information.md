---
description: Recupera uma variedade de informações para a bateria.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION de controle (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: a48514b81ddf5d8f7c0d84d4404eb01752413e73ade43db089fbb6dade673bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143521"
---
# <a name="ioctl_battery_query_information-control-code"></a>Código de controle \_ IOCTL BATTERY \_ QUERY \_ INFORMATION

Recupera uma variedade de informações para a bateria.

Para executar essa operação, chame a [**função DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
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

Uma alça para a bateria na qual as informações devem ser retornadas. Para recuperar um alça de dispositivo, chame a [**função CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*Dwiocontrolcode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual ela será executada. Use **INFORMAÇÕES DE CONSULTA \_ IOCTL BATTERY \_ \_** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para uma estrutura [**DE INFORMAÇÕES DE CONSULTA \_ \_ BATTERY.**](battery-query-information-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

</dd> <dt>

*Lpoutbuffer* 
</dt> <dd>

Um ponteiro para o buffer de retorno. O tipo de dados (e, portanto, o tamanho) do buffer de retorno depende das informações solicitadas no membro **BATTERY \_ QUERY \_ INFORMATION \_ LEVEL** da estrutura DE INFORMAÇÕES DE CONSULTA BATTERY de [**\_ \_**](battery-query-information-str.md) entrada.

A tabela a seguir mostra os dados retornados por um determinado nível de informações.



| Nível de informações                 | Dados retornados                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | **Cadeia de** caracteres Unicode terminada em nulo que especifica o nome da bateria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | Um **ULONG que** especifica o tempo estimado de duração da bateria, em segundos. Se a taxa de dreno fornecida no membro **AtRate** da estrutura [**BATTERY \_ QUERY \_ INFORMATION**](battery-query-information-str.md) for zero, esse cálculo será baseado na taxa atual de dreno. Se **AtRate** for menor que zero, o tempo retornado será o tempo de run time esperado para a taxa determinada. Se o tempo estimado for desconhecido (por exemplo, a bateria não está sendo descarregada e **AtRate** é zero), **BATTERY UNKNOWN \_ \_ TIME** é retornado. Observe que esse valor não é muito preciso em alguns sistemas de bateria. O valor pode variar muito dependendo do uso de energia atual, que pode ser afetado pela atividade de disco e outros fatores. Não há nenhum mecanismo de notificação para alterações nesse valor. |
| **BatteryGranularityInformation** | Uma matriz de comprimento variável de estruturas [**BATTERY \_ REPORTING \_ SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) que contém a granularidade de relatório para a capacidade da bateria retornada do STATUS DA CONSULTA [**IOCTL \_ BATTERY \_ \_**](ioctl-battery-query-status.md). Várias entradas são retornadas quando a granularidade depende da capacidade atual da bateria. Consulte **BATTERY \_ REPORTING \_ SCALE** para ver a interpretação da matriz de entradas. O número de entradas é indicado pelo tamanho do buffer retornado e pode ser calculado como (*lpBytesReturned/sizeof* (**BATTERY REPORTING \_ \_ SCALE**)). O número máximo de entradas que serão retornadas é quatro.                                                                                                |
| **BatteryInformation**            | Uma [**estrutura DE INFORMAÇÕES \_ DA**](battery-information-str.md) BATERIA.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Uma [**estrutura DE DATA DE \_ \_ FABRICAÇÃO DE**](battery-manufacture-date-str.md) BATERIA.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | **Cadeia de** caracteres Unicode terminada em nulo que contém o nome do fabricante da bateria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | **Cadeia de** caracteres Unicode terminada em nulo que contém o número de série da bateria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | Um **ULONG** que contém a temperatura atual da bateria, em 10ºs de um grau Dem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | **Cadeia de** caracteres Unicode terminada em nulo que identifica exclusivamente a bateria. Esse valor pode ser usado para acompanhar uma bateria específica. No caso de baterias inteligentes, essa ID será a concatenação do nome do fabricante, do nome do dispositivo, da data de fabricação e de uma representação imprimível do número de série. Esse valor não se destina a ser exibido ao usuário.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

O tamanho do buffer de saída em bytes. Dependendo do nível de informações dos dados solicitados, esse pode ser um buffer de tamanho variavel.

</dd> <dt>

*Lpbytesreturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados retornados no buffer *lpOutBuffer,* em bytes.

Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro **ERROR INSUFFICIENT \_ \_ BUFFER** e a contagem de byte retornada será zero.

Se *lpOverlapped* for **NULL** (E/S não mapeada), *lpBytesReturned* não poderá ser **NULL.**

Se *lpOverlapped* não for **NULL** (E/S sobrecarregada), *lpBytesReturned* poderá ser **NULL.** Se esta for uma operação sobrecarada, você poderá recuperar o número de bytes retornados chamando a [**função GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice* estiver associado a uma porta de conclusão de E/S, você poderá obter o número de bytes retornados chamando a [**função GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*Lpoverlapped* 
</dt> <dd>

Um ponteiro para uma [**estrutura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice* foi aberto com o sinalizador **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* deverá apontar para uma estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executado como uma operação sobressalo (assíncrona). Se o dispositivo tiver sido aberto com o sinalizador **FILE \_ FLAG \_ OVERLAPPED** e *lpOverlapped* for **NULL,** a função falhará de maneiras imprevisíveis.

Se *hDevice* tiver sido aberto sem especificar o sinalizador **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Algumas informações sobre baterias são opcionais ou podem não ter sentido para algumas baterias. Se o tipo específico de dados solicitado não estiver disponível para a bateria atual, **ERROR \_ INVALID \_ FUNCTION** será retornado.

Todas as solicitações de informações de bateria serão concluídas com o status ARQUIVO DE ERRO **\_ \_ NÃO \_** ENCONTRADO sempre que o elemento **BatteryTag** da solicitação não corresponder ao da marca de bateria atual. Isso garante que as informações de bateria retornadas corresponde às da bateria solicitada. (Consulte [Marcas de bateria](battery-information.md) para obter mais informações.)

## <a name="remarks"></a>Comentários

Esse IOCTL da bateria recupera uma variedade de informações para a bateria. A estrutura do parâmetro de [**entrada, BATTERY \_ QUERY \_ INFORMATION**](battery-query-information-str.md), indica o tipo de informação a ser retornado e quando as informações da bateria devem ser retornadas. O tipo de dados e o conteúdo do buffer de saída variam de acordo com os dados solicitados.

Para ver as implicações da E/S sobrecarada nessa operação, consulte a seção Comentários do [**tópico DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Exemplos

Para ver um exemplo, consulte [Enumerando dispositivos de bateria](enumerating-battery-devices.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h no Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Informações da bateria](battery-information.md)
</dt> <dt>

[Códigos de controle de gerenciamento de energia](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**INFORMAÇÕES \_ DE CONSULTA DA \_ BATERIA**](battery-query-information-str.md)
</dt> <dt>

[**\_escala de relatório de bateria \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_informações do \_ conjunto de baterias do IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

