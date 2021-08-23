---
description: Lista os intervalos de frequência com suporte no monitor.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Classe WmiMonitorListedFrequencyRanges
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 41b49c293d5661d523138b01c093fce627e5bedf3d1e783dccb8248edf88546c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051134"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>Classe WmiMonitorListedFrequencyRanges

A classe WMI **WmiMonitorListedFrequencyRanges** lista os intervalos de frequência com suporte no monitor. esses intervalos são encontrados na definição de entrada de vídeo da VESA (vídeo Electronics Standard Association) enhanced Display de identificação de vídeo (E-EDID), ou no arquivo INF Windows que contém dados de driver de dispositivo.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorListedFrequencyRanges** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorListedFrequencyRanges** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> <dt>

**MonitorFreqRanges**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **FrequencyRangeDescriptor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de intervalos de frequência de monitor representados por instâncias da classe [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) .

</dd> <dt>

**NumOfMonitorFreqRanges**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de intervalos de frequência de monitor com suporte listados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




