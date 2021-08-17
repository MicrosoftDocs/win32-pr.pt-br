---
description: a classe HWConfig é a classe pai para eventos de configuração de hardware no Windows XP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Classe HWConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1d4b8f69784729ffe5d51f3068b03fc0b4154182b2d05f2896e4556a05f7eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394676"
---
# <a name="hwconfig-class"></a>Classe HWConfig

a classe **HWConfig** é a classe pai para eventos de configuração de hardware no Windows XP.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **HWConfig** não define nenhum membro.

## <a name="remarks"></a>Comentários

Esses eventos fornecem a configuração de hardware do computador. Ao contrário de outros eventos de agente de log do NT, a sessão de kernel gera automaticamente eventos de configuração de hardware; Você não habilita esses eventos ao iniciar a sessão do agente de log do NT kernel.

**Windows 2000:** Sem suporte.

para eventos de configuração de hardware no Windows Vista e no Windows Server 2003, consulte a classe [SystemConfig](systemconfig.md) .

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de configuração de hardware chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os seguintes tipos de evento para identificar o evento de configuração de hardware real ao consumir eventos.



| Tipo de evento                                                                      | Descrição                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ CPU**(o valor do tipo de evento é 10)<br/>          | Evento de configuração de CPU. As classes MOF de [**\_ CPU do HWConfig**](hwconfig-cpu.md) definem os dados do evento para esse evento.                            |
| **Evento \_ de Configuração do tipo de rastreamento \_ \_ \_ LOGICALDISK**(o valor do tipo de evento é 12)<br/>  | Evento de configuração de disco lógico. A classe MOF [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) MOF classes define os dados do evento para esse evento. |
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ NIC**(o valor do tipo de evento é 13)<br/>          | Evento de configuração de NIC. As classes MOF do [**\_ NIC HWConfig**](hwconfig-nic.md) definem os dados do evento para esse evento.                            |
| **Evento \_ de Configuração de tipo de rastreamento \_ \_ \_ PHYSICALDISK**(o valor do tipo de evento é 11)<br/> | Evento de configuração de disco físico. As classes [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF definem os dados do evento para esse evento.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**HWConfig \_ CPU**](hwconfig-cpu.md)
</dt> <dt>

[**HWConfig \_ LogDisk**](hwconfig-logdisk.md)
</dt> <dt>

[**\_NIC HWConfig**](hwconfig-nic.md)
</dt> <dt>

[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
