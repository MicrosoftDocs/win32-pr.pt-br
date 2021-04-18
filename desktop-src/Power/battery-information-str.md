---
description: Contém informações sobre a bateria.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: Estrutura de BATTERY_INFORMATION (Poclass. h)
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
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756695"
---
# <a name="battery_information-structure"></a>Estrutura de informações da bateria \_

Contém informações sobre a bateria. Essa estrutura é retornada pelo código de controle de [**\_ \_ \_ informações de consulta da bateria do IOCTL**](ioctl-battery-query-information.md) quando o nível de informações BatteryInformation é solicitado.

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

Os recursos da bateria. Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**Bateria \_ 0x40000000 \_ relativa à capacidade**</dt> <dt></dt> </dl>                    | Indica que a capacidade da bateria e as informações de taxa são relativas, e não em unidades específicas. Se esse bit não for definido, as unidades de relatório serão milliwatt (mWh) para a capacidade e miliwatts (mW) para taxa. Se esse bit for definido, todas as referências a unidades na outra documentação da bateria poderão ser ignoradas. Todas as informações de taxa são relatadas em unidades por hora. Por exemplo, se a capacidade totalmente carregada for relatada como 100, uma taxa de 200 indica que a bateria usará toda a sua capacidade em meia hora.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**Bateria \_ É 0x20000000 de \_ curto \_ prazo**</dt> <dt></dt> </dl>                               | Indica que a operação normal é para uma função com falha. Se esse bit não for definido, espera-se que a bateria seja usada durante o uso normal do sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**Bateria \_ DEFINIR \_ cobrança \_ com suporte**</dt> <dt>0x00000001</dt> </dl>          | Indica que as solicitações Set Information do tipo BatteryCharge são suportadas por esse dispositivo de bateria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**Bateria \_ DEFINIR a \_ descarga \_ suportada como**</dt> <dt>0x00000002</dt> </dl> | Indica que as solicitações Set Information do tipo BatteryDischarge são suportadas por esse dispositivo de bateria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**Bateria \_ \_Bateria do sistema**</dt> <dt>0x80000000</dt> </dl>                             | Indica que a bateria pode fornecer energia geral para executar o sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Tecnologia**
</dt> <dd>

A tecnologia da bateria. Esse membro pode ser um dos valores a seguir.



| Valor                                                                        | Significado                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Bateria Nonrechargeable, por exemplo, Alkaline.<br/> |
| <dl> <dt>1</dt> </dl> | Bateria recarregáveis, por exemplo, chumbo em acid.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Química**
</dt> <dd>

Uma cadeia de caracteres abreviada que indica a química da bateria. Essa cadeia de caracteres não é necessariamente terminada em zero. A seguir está uma lista parcial de abreviações que podem ser retornadas e o chemistries associado.



| Cadeia de caracteres Unicode                                                                                                                                           | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Acid de chumbo<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**LION**</dt> </dl>                        | Íon de lítio<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Íon de lítio<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**NiCd**</dt> </dl> | Cádmio de níquel<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**NiMH**</dt> </dl> | Hydride de metal de níquel<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**NiZn**</dt> </dl> | Zinc de níquel<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Alkaline-Manganese recarregáveis<br/> |



 

Outros chemistries podem aparecer no futuro e seu código deve ser capaz de tratá-los.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

A capacidade teórica da bateria quando nova, em mWh, a menos que a capacidade da bateria \_ \_ relativa esteja definida. Nesse caso, as unidades são indefinidas.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

A capacidade totalmente carregada atual da bateria em mWh (ou relativa). Compare esse valor com **DesignedCapacity** para estimar o desgaste da bateria.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

A capacidade sugerida do fabricante, em mWh, em que um alerta de bateria baixa deve ocorrer. Definições de baixo variam de fabricante para fabricante. Em geral, um estado de aviso ocorrerá antes de um estado baixo, mas você não deve presumir que ele sempre será. Para reduzir o risco de perda de dados, esse valor geralmente é usado como a configuração padrão para o alarme de bateria crítico.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

A capacidade sugerida do fabricante, em mWh, na qual um alerta de bateria de aviso deve ocorrer. As definições de aviso variam de fabricante para fabricante. Em geral, um estado de aviso ocorrerá antes de um estado baixo, mas você não deve presumir que ele sempre será. Para reduzir o risco de perda de dados, esse valor geralmente é usado como a configuração padrão para o alarme de bateria fraca.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Uma tendência de zero, em mWh, que é aplicada ao relatório de bateria. Algumas baterias reservam um pequeno encargo que se ajusta dos valores de capacidade da bateria para mostrar "0" como o nível de bateria crítico. A diferença crítica é análoga à definição de um medidor de combustível para mostrar "vazio" quando há vários litros de combustível deixados.

</dd> <dt>

**CycleCount**
</dt> <dd>

O número de ciclos de cobrança/descarga que a bateria experimentou. Isso fornece um meio para determinar o desgaste da bateria. Se a bateria não oferecer suporte a um contador de ciclo, esse membro será zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Geralmente, um estado de aviso ocorre antes de um estado baixo, mas você não deve presumir isso. É possível sondar uma bateria e descobrir que nenhum nível de alerta ocorreu e sondar a bateria novamente e encontrá-la descarregada na medida em que os dois níveis foram atingidos. Isso pode indicar que você não está sondando com frequência suficiente. Isso também pode indicar que a bateria não pode manter uma cobrança por muito tempo e está descarregando mais rapidamente do que o esperado. Essa bateria pode estar se aproximando do fim de sua vida útil ou pode estar danificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




