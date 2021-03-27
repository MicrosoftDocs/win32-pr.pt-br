---
description: A classe pai para eventos de cabeçalho de log. Essa classe é sempre a primeira classe de rastreamento de eventos enviada a um consumidor (esse evento não é enviado para consumidores em tempo real). A sintaxe a seguir é simplificada do código MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Classe EventTraceEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967430"
---
# <a name="eventtraceevent-class"></a>Classe EventTraceEvent

A classe pai para eventos de cabeçalho de log. Essa classe é sempre a primeira classe de rastreamento de eventos enviada a um consumidor (esse evento não é enviado para consumidores em tempo real).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **EventTraceEvent** não define nenhum membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_Cabeçalho EventTrace**](eventtrace-header.md)
</dt> </dl>

 

 




