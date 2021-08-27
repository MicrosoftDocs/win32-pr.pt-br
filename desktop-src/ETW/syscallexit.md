---
description: Essa classe é a classe de tipo de evento para eventos de saída de chamada do sistema. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Classe SysCallExit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: aa297ced8f6c0d17c0c01da9ce11705d30fe7448c8bc2f2ae6358ddc85f653be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102056"
---
# <a name="syscallexit-class"></a>Classe SysCallExit

Essa classe é a classe de tipo de evento para eventos de saída de chamada do sistema.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Membros

A **classe SysCallExit** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe SysCallExit** tem essas propriedades.

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Format("x")
</dt> </dl>

Código de status retornado pela chamada do sistema NT.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 




