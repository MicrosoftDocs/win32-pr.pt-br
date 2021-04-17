---
description: Indica um tipo de alteração de status de serviço para monitoramento e relatório.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Enumeração de SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754114"
---
# <a name="sc_event_type-enumeration"></a>Enumeração de tipo de \_ evento SC \_

Indica um tipo de alteração de status de serviço para monitoramento e relatório.

## <a name="syntax"></a>Syntax


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_alteração do \_ banco de dados de eventos SC \_**
</dt> <dd>

Um serviço foi adicionado ou excluído. O parâmetro *hService* da função [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve ser um identificador para o SCM.

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_alteração da \_ Propriedade do evento SC \_**
</dt> <dd>

Uma ou mais propriedades de serviço foram atualizadas. O parâmetro *hService* da função [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve ser um identificador para o serviço.

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_alteração do \_ status do evento SC \_**
</dt> <dd>

O status de um serviço foi alterado. O parâmetro *hService* da função [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve ser um identificador para o serviço.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl> |



 

 




