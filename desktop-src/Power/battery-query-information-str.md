---
description: Contém informações de consulta de bateria.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: Estrutura de BATTERY_QUERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 9049517108cbb31df1164cc88640a78e104e2902d3a8a4b8dec4b8bfb48e8a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143679"
---
# <a name="battery_query_information-structure"></a>Estrutura de informações de \_ consulta de bateria \_

Contém informações de consulta de bateria. Essa estrutura é usada com o código de controle de [**\_ \_ \_ informações de consulta da bateria do IOCTL**](ioctl-battery-query-information.md) para especificar o tipo de informações a serem retornadas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BATTERY_QUERY_INFORMATION {
  ULONG                           BatteryTag;
  BATTERY_QUERY_INFORMATION_LEVEL InformationLevel;
  LONG                            AtRate;
} BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**BatteryTag**
</dt> <dd>

A marca de bateria atual para a bateria. Somente informações para uma bateria que correspondem à marca podem ser retornadas. Sempre que esse valor não corresponder à marca atual da bateria, a solicitação de IOCTL será concluída com o \_ arquivo de erro \_ não \_ encontrado. Isso indica ao chamador que a bateria associada à marca existe mais. O chamador pode optar por usar a operação de [**\_ \_ \_ marca de consulta da bateria do IOCTL**](ioctl-battery-query-tag.md) para determinar a marca da bateria recém-instalada, se existir uma. (Consulte [marcas de bateria](battery-information.md) para obter mais informações.)

Quando uma solicitação de informações de consulta é feita, esse valor é verificado. Além disso, se a solicitação estiver em andamento enquanto esse valor for alterado, a solicitação será anulada com o status do \_ arquivo de erro \_ não \_ encontrado.

</dd> <dt>

**InformationLevel**
</dt> <dd>

O nível das informações da bateria que estão sendo consultadas. Os dados retornados pelo IOCTL dependem desse valor. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | Cadeia de caracteres Unicode terminada em nulo que contém o nome da bateria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | Um **ULONG** que especifica o tempo de execução de bateria estimado, em segundos. Se a taxa de dreno fornecida no membro **AtRate** da estrutura de **\_ \_ informações de consulta da bateria** for zero, esse cálculo será baseado na taxa atual de drenagem. Se **AtRate** for diferente de zero, o tempo retornado será o tempo de execução esperado para a taxa determinada. Se o tempo estimado for desconhecido (por exemplo, a bateria não está sendo descarregada e o **AtRate** especificado for zero), o valor de retorno será o tempo de bateria \_ desconhecido \_ . Observe que esse valor não é muito preciso em alguns sistemas de bateria e pode variar muito dependendo do consumo de energia presente, que poderia ser afetado pela atividade de disco e por outros fatores. Não há nenhum mecanismo de notificação para alterações nesse valor.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | Uma matriz de estruturas de [**\_ \_ escala de relatório de bateria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) , nunca mais do que quatro entradas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | Uma estrutura de [**\_ informações da bateria**](battery-information-str.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | Uma estrutura de [**\_ \_ data de fabricação de bateria**](battery-manufacture-date-str.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | Cadeia de caracteres Unicode terminada em nulo que especifica o nome do fabricante da bateria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | Cadeia de caracteres Unicode terminada em nulo que especifica o número de série da bateria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | Um **ULONG** que especifica a temperatura atual da bateria, em 10 ° de um grau Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | Cadeia de caracteres Unicode terminada em nulo que identifica exclusivamente a bateria. Esse valor pode ser usado para rastrear uma bateria específica. No caso de baterias inteligentes, essa ID seria a concatenação do nome do fabricante, do nome do dispositivo, da data de fabricação e de uma representação imprimível do número de série. <br/> Esse valor não deve ser exibido para o usuário.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

Esse membro será usado somente se **InformationLevel** for BatteryEstimatedTime.

Se esse membro for diferente de zero, será uma taxa de drenagem que será usada para calcular o tempo até que a bateria seja descarregada para o BatteryEstimatedTime de uma bateria individual. Ele deve ser especificado em mW e deve ser um valor negativo para representar uma taxa de descarga da bateria.

</dd> </dl>

## <a name="remarks"></a>Comentários

Algumas informações sobre baterias são opcionais ou podem não fazer sentido para algumas baterias. Se o tipo específico de dados solicitado não estiver disponível para a bateria atual, a \_ função erro inválido \_ será retornada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                                                                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Poclass. h;</dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações da bateria \_**](battery-information-str.md)
</dt> <dt>

[**\_data de fabricação da bateria \_**](battery-manufacture-date-str.md)
</dt> <dt>

[**\_escala de relatório de bateria \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




