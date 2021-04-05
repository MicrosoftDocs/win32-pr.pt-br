---
description: Recupera uma variedade de informações para a bateria.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION código de controle (Poclass. h)
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
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921724"
---
# <a name="ioctl_battery_query_information-control-code"></a>\_Código de \_ controle de informações de consulta da bateria do IOCTL \_

Recupera uma variedade de informações para a bateria.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


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

Um identificador para a bateria em que as informações serão retornadas. Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

O código de controle para a operação. Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo. Use **\_ \_ \_ as informações de consulta da bateria do IOCTL** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de consulta de bateria**](battery-query-information-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

O tamanho do buffer de entrada, em bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Um ponteiro para o buffer de retorno. O tipo de dados (e, portanto, tamanho) do buffer de retorno depende das informações solicitadas no membro do nível de informações de consulta da bateria da estrutura de [**\_ \_ informações de consulta da bateria**](battery-query-information-str.md) de entrada. **\_ \_ \_**

A tabela a seguir mostra os dados retornados por um determinado nível de informação.



| Nível de informações                 | Dados retornados                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | Cadeia de caracteres Unicode terminada em **nulo** que especifica o nome da bateria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | Um **ULONG** que especifica o tempo de execução de bateria estimado, em segundos. Se a taxa de dreno fornecida no membro **AtRate** da estrutura de [**\_ \_ informações de consulta da bateria**](battery-query-information-str.md) for zero, esse cálculo será baseado na taxa atual de drenagem. Se **AtRate** for diferente de zero, o tempo retornado será o tempo de execução esperado para a taxa determinada. Se o tempo estimado for desconhecido (por exemplo, a bateria não está sendo descarregada e **AtRate** for zero), o **\_ \_ tempo de bateria desconhecido** será retornado. Observe que esse valor não é muito preciso em alguns sistemas de bateria. O valor pode variar muito, dependendo do consumo de energia presente, que pode ser afetado pela atividade de disco e por outros fatores. Não há nenhum mecanismo de notificação para alterações nesse valor. |
| **BatteryGranularityInformation** | Uma matriz de comprimento variável de estruturas de [**\_ \_ escala de relatório de bateria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) que contém a granularidade do relatório para a capacidade da bateria retornada do [**\_ \_ \_ status da consulta da bateria do IOCTL**](ioctl-battery-query-status.md). Várias entradas são retornadas quando a granularidade depende da capacidade presente da bateria. Consulte **\_ \_ escala de relatório de bateria** para a interpretação da matriz de entradas. O número de entradas é indicado pelo tamanho do buffer retornado e pode ser calculado como (*lpBytesReturned* /sizeof (**escala de relatório de \_ bateria \_**)). O número máximo de entradas que serão retornadas é quatro.                                                                                                |
| **BatteryInformation**            | Uma estrutura de [**\_ informações da bateria**](battery-information-str.md) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Uma estrutura de [**\_ \_ data de fabricação de bateria**](battery-manufacture-date-str.md) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | Cadeia de caracteres Unicode terminada em **nulo** que contém o nome do fabricante da bateria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | Cadeia de caracteres Unicode terminada em **nulo** que contém o número de série da bateria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | Um **ULONG** que contém a temperatura atual da bateria, em 10 ° de um grau Kelvin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | Cadeia de caracteres Unicode terminada em **nulo** que identifica exclusivamente a bateria. Esse valor pode ser usado para rastrear uma bateria específica. No caso de baterias inteligentes, essa ID será a concatenação do nome do fabricante, do nome do dispositivo, da data de fabricação e de uma representação imprimível do número de série. Esse valor não deve ser exibido para o usuário.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

O tamanho do buffer de saída em bytes. Dependendo do nível de informação dos dados solicitados, esse pode ser um buffer de tamanho de variavelmente.

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

Algumas informações sobre baterias são opcionais ou podem não fazer sentido para algumas baterias. Se o tipo específico de dados solicitado não estiver disponível para a bateria atual, a **\_ \_ função erro inválido** será retornada.

Todas as solicitações de informações da bateria serão concluídas com o status do **arquivo de erro \_ \_ não \_ encontrado** sempre que o elemento **BatteryTag** da solicitação não corresponder ao da marca da bateria atual. Isso garante que as informações de bateria retornadas correspondam àquela da bateria solicitada. (Consulte [marcas de bateria](battery-information.md) para obter mais informações.)

## <a name="remarks"></a>Comentários

Essa bateria IOCTL recupera uma variedade de informações para a bateria. A estrutura do parâmetro de entrada, [**\_ \_ as informações de consulta da bateria**](battery-query-information-str.md), indicam o tipo de informações a serem retornadas e quando as informações da bateria devem ser retornadas. O tipo de dados e o conteúdo do buffer de saída variam com base nos dados solicitados.

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

[**\_informações de consulta de bateria \_**](battery-query-information-str.md)
</dt> <dt>

[**\_escala de relatório de bateria \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_informações do \_ conjunto de baterias do IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

