---
description: Lista os modos de origem com suporte para um monitor de vídeo em seu descritor de monitor, se existir algum.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Classe WmiMonitorListedSupportedSourceModes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785196"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a>Classe WmiMonitorListedSupportedSourceModes

O **WmiMonitorListedSupportedSourceModes** lista os modos de origem com suporte para um monitor de vídeo em seu descritor de monitor, se existir algum. Para monitores que não têm nenhuma descrição, essa lista de modos é gerada com base no tipo de monitor, conforme especificado pelo driver do barramento do monitor.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorListedSupportedSourceModes** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorListedSupportedSourceModes** tem essas propriedades.

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

**MonitorSourceModes**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **VideoModeDescriptor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista modos de origem do monitor representados por instâncias da classe [**VideoModeDescriptor**](videomodedescriptor.md) .

</dd> <dt>

**NumOfMonitorSourceModes**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de modo de origem do monitor com suporte listado.

</dd> <dt>

**PreferredMonitorSourceModeIndex**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Índice de modo de origem do monitor preferencial.

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

 

 




