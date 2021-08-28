---
description: Representa uma alteração no brilho de um monitor.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: Classe WmiMonitorBrightnessEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 4affedabdb7fde7cec93d3cf8eb675f343054635eb0b4a504d74d96dc3eb8d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321404"
---
# <a name="wmimonitorbrightnessevent-class"></a>Classe WmiMonitorBrightnessEvent

A **classe de evento WMI WMI WmiMonitorBrightnessEvent** representa uma alteração no brilho de um monitor.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a>Membros

A **classe WmiMonitorBrightnessEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe WmiMonitorBrightnessEvent** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**Brightness**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O brilho atual do monitor como um percentual.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI \\ raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> <dt>

[**WmiMonitorBrightness**](wmimonitorbrightness.md)
</dt> <dt>

[Recebendo um evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

