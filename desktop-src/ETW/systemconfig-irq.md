---
description: Essa classe é a classe de tipo de evento para eventos irQ (solicitação de interrupção). A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: SystemConfig_IRQ classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3da720de11aa7dbbd759131a521e44e546b7cad6d2525565c81d0aa6920dd0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078286"
---
# <a name="systemconfig_irq-class"></a>Classe IRQ SystemConfig \_

Essa classe é a classe de tipo de evento para eventos irQ (solicitação de interrupção).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a>Membros

A **classe SYSTEMConfig \_ IRQ** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe SYSTEMConfig \_ IRQ** tem essas propriedades.

<dl> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Descrição do dispositivo ou software que está fazendo a solicitação.

</dd> <dt>

**DeviceDescriptionLen**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

Comprimento, em caracteres, da cadeia de caracteres **em DeviceDescription.**

</dd> <dt>

**IRQAffinity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Format("x")
</dt> </dl>

Máscara de afinidade irq. A máscara de afinidade identifica os processadores específicos (ou grupos de processadores) que podem receber o IRQ.

</dd> <dt>

**IRQNum**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

Número da linha de solicitação de interrupção.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




