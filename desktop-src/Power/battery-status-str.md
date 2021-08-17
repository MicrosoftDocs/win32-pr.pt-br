---
description: Contém o estado atual da bateria.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: Estrutura de BATTERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 28b75a8eb1c7abf647f3f8ea61b29dedb40978f3ea639fc505364a12ae5e57cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143599"
---
# <a name="battery_status-structure"></a>Estrutura de status da bateria \_

Contém o estado atual da bateria. Essa estrutura é usada pelo código de controle do [**\_ \_ \_ status de consulta da bateria do IOCTL**](ioctl-battery-query-status.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**PowerState**
</dt> <dd>

O estado da bateria. Esse membro pode ser zero, um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Bateria \_ CARREGANDO**</dt> <dt>0x00000004</dt> </dl>                  | Indica que a bateria está carregando no momento.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Bateria \_**</dt> <dt>0x00000008</dt> crítico </dl>                  | Indica que a falha da bateria é iminente. Consulte a seção Comentários para obter mais informações.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Bateria \_ Descarregando**</dt> <dt>0x00000002</dt> </dl>         | Indica que a bateria está sendo descarregada no momento.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Bateria \_ LIGAR \_ a \_ linha**</dt> <dt>0x00000001</dt> </dl> | Indica que o sistema tem acesso à energia AC, portanto, nenhuma bateria está sendo descarregada.<br/>   |



 

</dd> <dt>

**Capacidade**
</dt> <dd>

A capacidade atual da bateria, em mWh (ou relativa). Esse valor pode ser usado para gerar uma exibição de "medidor de gás" dividindo-a pelo membro **FullChargedCapacity** da estrutura de [**\_ informações da bateria**](battery-information-str.md) . Se a capacidade não estiver disponível, esse membro será de \_ capacidade desconhecida da bateria \_ .

</dd> <dt>

**Voltagem**
</dt> <dd>

A voltagem da bateria atual entre os terminais da bateria, em milivolts (MV). Se a tensão não estiver disponível, esse membro será a \_ tensão desconhecida da bateria \_ .

</dd> <dt>

**Tarifa**
</dt> <dd>

A taxa atual de carga ou descarga da bateria. Esse valor estará em miliwatts, a menos que as informações de taxa de bateria sejam relativas, caso em que elas estarão em unidades arbitrárias por hora. Para determinar se as informações da bateria são relativas, examine o \_ sinalizador relativo da capacidade da bateria \_ no membro de **recursos** da estrutura de [**\_ informações da bateria**](battery-information-str.md) . Uma taxa positiva diferente de zero indica cobrança; uma taxa negativa indica o descarregamento. Algumas baterias relatam apenas taxas de descarregamento. Se a taxa não estiver disponível, esse membro será uma \_ taxa de bateria desconhecida \_ . Se o estado da bateria ou fonte de energia for alterado, a taxa poderá ficar disponível.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ sinalizador de bateria crítica no membro do **PowerState** dessa estrutura indica uma condição de "bateria crítica" de hardware. Esse nível crítico é definido pelo fabricante da bateria, não pelo usuário no "alarme de bateria crítica". Geralmente, isso significa que o sistema de bateria calculou que a bateria está totalmente descarregada, e qualquer energia que esteja sendo desenhada está além do esperado.

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

[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




