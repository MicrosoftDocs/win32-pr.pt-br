---
description: Contém informações sobre as condições sob as quais o status da bateria deve ser recuperado.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: Estrutura de BATTERY_WAIT_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756694"
---
# <a name="battery_wait_status-structure"></a>Estrutura de status de \_ espera da bateria \_

Contém informações sobre as condições sob as quais o status da bateria deve ser recuperado. Essa estrutura é usada pelo código de controle do [**\_ \_ \_ status de consulta da bateria do IOCTL**](ioctl-battery-query-status.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**BatteryTag**
</dt> <dd>

A marca de bateria atual para a bateria. Somente informações para uma bateria que correspondem à marca podem ser retornadas. Sempre que esse valor não corresponder à marca atual da bateria, a operação [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) falhará com um código de erro de \_ arquivo de erro \_ não \_ encontrado, que indica ao chamador que a bateria para a qual ela tem uma marca não está mais instalada, o chamador pode optar por usar a operação de [**\_ \_ \_ marca de consulta da bateria do IOCTL**](ioctl-battery-query-tag.md) para determinar a marca da bateria recém-instalada, se houver. Além disso, se a solicitação estiver em andamento quando a bateria for removida ou a marca for alterada, a operação será anulada com o status do \_ arquivo de erro \_ não \_ encontrado. (Consulte [marcas de bateria](battery-information.md) para obter mais informações.)

</dd> <dt>

**Tempo Limite**
</dt> <dd>

O número de milissegundos que a solicitação aguardará pela condição especificada pelos membros **PowerState**, **LowCapacity** e **HighCapacity** antes de concluir. Um valor de-1 indica que a solicitação aguardará indefinidamente que as condições sejam satisfeitas. Um valor de zero indica que as informações de bateria solicitadas serão retornadas imediatamente, independentemente das outras condições. Qualquer outro valor indica que a solicitação deve aguardar esse período de tempo ou até que qualquer uma das outras condições seja satisfeita.

Se o computador tiver inserido o modo de suspensão, o relógio continuará a ser executado, mas o esgotamento da contagem não ativará o computador. Se a contagem for esgotada quando o computador for acordado e outras condições forem satisfeitas, a chamada retornará imediatamente na ativação.

</dd> <dt>

**PowerState**
</dt> <dd>

Zero, um ou mais dos seguintes bits de status, que indicam o estado da bateria. É idêntico ao membro **PowerState** da estrutura de [**\_ status da bateria**](battery-status-str.md) .



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Bateria \_ CARREGANDO**</dt> <dt>0x00000004</dt> </dl>                  | Indica que a bateria está carregando no momento.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Bateria \_**</dt> <dt>0x00000008</dt> crítico </dl>                  | Indica que a falha da bateria é iminente. Consulte a seção Comentários para obter mais informações.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Bateria \_ Descarregando**</dt> <dt>0x00000002</dt> </dl>         | Indica que a bateria está sendo descarregada no momento.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Bateria \_ LIGAR \_ a \_ linha**</dt> <dt>0x00000001</dt> </dl> | Indica que a bateria tem acesso à energia AC.<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

A capacidade atual da bateria, em mWh (ou relativa). Esse valor é idêntico ao membro de **capacidade** da estrutura [**de \_ status da bateria**](battery-status-str.md) .

</dd> <dt>

**HighCapacity**
</dt> <dd>

A capacidade atual da bateria, em mWh (ou relativa). Esse valor é idêntico ao membro de **capacidade** da estrutura [**de \_ status da bateria**](battery-status-str.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

As solicitações de informações da bateria são adiadas até que ocorra um dos seguintes:

-   O tempo limite expira (supondo que o **tempo limite** não seja-1).
-   O status atual da bateria não corresponde ao **PowerState**.
-   A capacidade da bateria está abaixo de **LowCapacity**.
-   A capacidade da bateria está acima de **HighCapacity**.
-   A marca de bateria é alterada.

Quando qualquer uma dessas condições é satisfeita, os dados são coletados e a operação retorna. Isso permite que os aplicativos monitorem informações de baterias dinâmicas típicas sem sondar o dispositivo.

Antes de usar qualquer uma das duas condições de capacidade, verifique se a bateria dá suporte a elas usando o código de controle de [**\_ \_ \_ status de consulta da bateria do IOCTL**](ioctl-battery-query-status.md) com um tempo limite de zero. Examine os resultados para determinar se o membro de **capacidade** tem suporte (ou seja, sem \_ capacidade de bateria desconhecida \_ ).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**STATUS da bateria \_**](battery-status-str.md)
</dt> <dt>

[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

