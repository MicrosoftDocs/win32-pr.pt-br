---
description: Essa classe é a classe de tipo de evento que marca o início dos eventos de leitura, gravação e liberação de e/s de disco. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: Classe DiskIo_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501392"
---
# <a name="diskio_typegroup2-class"></a>\_Classe DiskIo TypeGroup2

Essa classe é a classe de tipo de evento que marca o início dos eventos de leitura, gravação e liberação de e/s de disco.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Membros

A classe **DiskIo \_ TypeGroup2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **DiskIo \_ TypeGroup2** tem essas propriedades.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**ponteiro**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Pacote de solicitação de e/s. Essa propriedade identifica a atividade de e/s.

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

O identificador do thread emissor.

**Windows server 2008 R2, Windows server 2008, Windows 7 e Windows Vista:** Não há suporte para essa propriedade.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




