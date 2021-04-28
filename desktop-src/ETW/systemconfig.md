---
description: Classe SystemConfig – essa classe é a classe pai para eventos de configuração de hardware. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: Classe SystemConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 232214aa2c33485d909525d54965f59fdc891a29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105864"
---
# <a name="systemconfig-class"></a>Classe SystemConfig

Essa classe é a classe pai para eventos de configuração de hardware.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **SystemConfig** não define nenhum membro.

## <a name="remarks"></a>Comentários

Esses eventos fornecem a configuração de hardware do computador. Ao contrário de outros eventos de agente de log do NT, a sessão de kernel gera automaticamente eventos de configuração de hardware; Você não habilita esses eventos ao iniciar a sessão do agente de log do NT kernel.

Para eventos de configuração de hardware no Windows XP, consulte a classe [HWConfig](hwconfig.md) .

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de configuração de hardware chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os seguintes tipos de evento para identificar o evento de configuração de hardware real ao consumir eventos.



| Tipo de evento                                                                      | Descrição                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ CPU**(o valor do tipo de evento é 10)<br/>          | Evento de configuração de CPU. As classes MOF de [**\_ CPU do SystemConfig**](systemconfig-cpu.md) definem os dados do evento para esse evento.                                                       |
| **Evento \_ de Tipo de rastreamento \_ \_ config \_ IDECHANNEL**(o valor do tipo de evento é 23)<br/>   | Evento de configuração de canal IDE primário e secundário. A classe MOF [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) MOF classes define os dados do evento para esse evento. |
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ IRQ**(o valor do tipo de evento é 21)<br/>          | Evento de solicitação de interrupção (IRQ). A classe MOF de [**SystemConfig \_ IRQ**](systemconfig-irq.md) do MOF classes define os dados do evento para esse evento.                                       |
| **Evento \_ de Configuração do tipo de rastreamento \_ \_ \_ LOGICALDISK**(o valor do tipo de evento é 12)<br/>  | Evento de configuração de disco lógico. A classe MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) MOF classes define os dados do evento para esse evento.                            |
| **Evento \_ de Tipo de rastreamento \_ \_ config \_ NetInfo**(o valor do tipo de evento é 17)<br/>      | Evento de Iformation de rede. A classe MOF de [**\_ rede SystemConfig**](systemconfig-network.md) define os dados de evento para esse evento.                                                |
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ NIC**(o valor do tipo de evento é 13)<br/>          | Evento de configuração de NIC. As classes MOF do [**\_ NIC SystemConfig**](systemconfig-nic.md) definem os dados do evento para esse evento.                                                       |
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ PHYSICALDISK**(o valor do tipo de evento é 11)<br/> | Evento de configuração de disco físico. As classes [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) MOF definem os dados do evento para esse evento.                                     |
| **Evento \_ de Tipo de rastreamento \_ \_ config \_ PNP**(o valor do tipo de evento é 22)<br/>          | Evento plug and Play. A classe [**SystemConfig \_ PNP**](systemconfig-pnp.md) MOF classes MOF define os dados do evento para esse evento.                                                 |
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ Power**(o valor do tipo de evento é 16)<br/>        | Evento de configuração de energia. A classe [**SystemConfig \_ Power**](systemconfig-power.md) MOF define os dados do evento para esse evento.                                                   |
| **Evento \_ de \_Serviços de \_ configuração \_ de tipo de rastreamento**(o valor do tipo de evento é 15)<br/>     | Evento de configuração de serviços. A classe MOF [**\_ dos serviços SystemConfigs**](systemconfig-services.md) define os dados do evento para esse evento.                                          |
| **Evento \_ de \_Vídeo de \_ configuração \_ do tipo de rastreamento**(o valor do tipo de evento é 14)<br/>        | Evento de configuração do adaptador de gráficos. A classe MOF de [**\_ vídeo SystemConfig**](systemconfig-video.md) define os dados de evento para esse evento.                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig \_ CPU**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md)
</dt> <dt>

[**\_IRQ SystemConfig**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md)
</dt> <dt>

[**\_Rede SystemConfig**](systemconfig-network.md)
</dt> <dt>

[**\_NIC SystemConfig**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md)
</dt> <dt>

[**\_PNP SystemConfig**](systemconfig-pnp.md)
</dt> <dt>

[**SystemConfig \_ Power**](systemconfig-power.md)
</dt> <dt>

[**Serviços SystemConfigs \_**](systemconfig-services.md)
</dt> <dt>

[**Vídeo do SystemConfig \_**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 
