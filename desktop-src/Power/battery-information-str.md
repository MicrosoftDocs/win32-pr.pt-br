---
description: Contém informações da bateria.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION estrutura (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: c449f325e03fb4ea81fe0aa148eaddcf65800b5a56356e22232477e0b6d4fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033006"
---
# <a name="battery_information-structure"></a>Estrutura DE INFORMAÇÕES DO BATTERY \_

Contém informações da bateria. Essa estrutura é retornada pelo código de controle [**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md) quando o nível de informações BatteryInformation é solicitado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Funcionalidades**
</dt> <dd>

As funcionalidades da bateria. Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**BATERIA \_ CAPACIDADE \_ RELATIVA**</dt> <dt>0X40000000</dt> </dl>                    | Indica que a capacidade da bateria e as informações de taxa são relativas e não em unidades específicas. Se esse bit não estiver definido, as unidades de relatório serão miliwatt-horas (mWh) para capacidade e miliwatts (mW) para taxa. Se esse bit estiver definido, todas as referências às unidades na outra documentação da bateria poderão ser ignoradas. Todas as informações de taxa são relatadas em unidades por hora. Por exemplo, se a capacidade totalmente cobrada for relatada como 100, uma taxa de 200 indicará que a bateria usará toda a sua capacidade em meia hora.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**BATERIA \_ É \_ UMA \_ 0X20000000**</dt> <dt></dt> </dl>                               | Indica que a operação normal é para uma função com segurança de falha. Se esse bit não estiver definido, espera-se que a bateria seja usada durante o uso normal do sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**BATERIA \_ SET \_ CHARGE \_ SUPPORTED**</dt> <dt>0X00000001</dt> </dl>          | Indica que as solicitações de informações definidas do tipo BatteryCharge são suportadas por este dispositivo de bateria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**BATERIA \_ DEFINIR \_ A \_ CONFIGURAÇÃO COM**</dt> SUPORTE PARA <dt>0X00000002</dt> </dl> | Indica que as solicitações de informações definidas do tipo BatteryDischarge são suportadas por este dispositivo de bateria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**BATERIA \_ SISTEMA \_ DE BATERIA**</dt> <dt>0X80000000</dt> </dl>                             | Indica que a bateria pode fornecer energia geral para executar o sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Tecnologia**
</dt> <dd>

A tecnologia de bateria. Esse membro pode ser um dos valores a seguir.



| Valor                                                                        | Significado                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Bateria não recarregável, por exemplo, sem energia.<br/> |
| <dl> <dt>1</dt> </dl> | Bateria acessível, por exemplo, acid de lead.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Química**
</dt> <dd>

Uma cadeia de caracteres abreviada que indica a química da bateria. Essa cadeia de caracteres não é necessariamente terminada em zero. Veja a seguir uma lista parcial de abreviações que podem ser retornadas e as químicas associadas.



| Cadeia de caracteres Unicode                                                                                                                                           | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Lead Acid<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**Leão**</dt> </dl>                        | Lithium Ion<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Lithium Ion<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**Nicd**</dt> </dl> | Cadmium de Cadmium<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**Nimh**</dt> </dl> | Nickel Metal Hydride<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**Nizn**</dt> </dl> | Carimão<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Alkaline-Manganese<br/> |



 

Outras químicas podem aparecer no futuro e seu código deve ser capaz de lidar com elas.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

A capacidade teórico da bateria quando nova, em mWh, a menos que BATTERY \_ CAPACITY \_ RELATIVE esteja definido. Nesse caso, as unidades são indefinidas.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

A capacidade atual totalmente carregada da bateria em mWh (ou relativo). Compare esse valor com **DesignedCapacity** para estimar o uso da bateria.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

A capacidade sugerida do fabricante, em mWh, na qual um alerta de bateria fraca deve ocorrer. As definições de baixa variam de fabricante para fabricante. Em geral, um estado de aviso ocorrerá antes de um estado baixo, mas você não deve supor que ele sempre ocorrerá. Para reduzir o risco de perda de dados, esse valor geralmente é usado como a configuração padrão para o alarme de bateria crítico.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

A capacidade sugerida do fabricante, em mWh, na qual um alerta de bateria de aviso deve ocorrer. As definições de aviso variam de fabricante para fabricante. Em geral, um estado de aviso ocorrerá antes de um estado baixo, mas você não deve supor que ele sempre ocorrerá. Para reduzir o risco de perda de dados, esse valor geralmente é usado como a configuração padrão para o alarme de bateria fraca.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Um desvio de zero, em mWh, que é aplicado ao relatório de bateria. Algumas baterias reservam uma pequena carga que é desvio dos valores de capacidade da bateria para mostrar "0" como o nível crítico da bateria. O desvio crítico é análogo à configuração de um medidor de combustível para mostrar "vazio" quando há vários literis de combustível à esquerda.

</dd> <dt>

**CycleCount**
</dt> <dd>

O número de ciclos de carga/descarregamento que a bateria passou. Isso fornece um meio para determinar o uso da bateria. Se a bateria não dá suporte a um contador de ciclo, esse membro é zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Em geral, um estado de aviso ocorre antes de um estado baixo, mas você não deve supor que ocorrerá. É possível sondar uma bateria e descobrir que nenhum nível de alerta ocorreu e sondar a bateria novamente e encontrá-la descarregada até a extensão em que ambos os níveis foram atingidos. Isso pode indicar que você não está sondando com frequência suficiente. Também pode indicar que a bateria não consegue conter uma carga por muito tempo e está sendo descarregada mais rapidamente do que o esperado. Essa bateria pode estar se aproximando do fim de sua vida útil ou pode estar danificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h no Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DE CONSULTA DA BATERIA IOCTL \_ \_ \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




