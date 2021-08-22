---
description: Armazena e recupera informações sobre assinaturas de evento. Essa interface estende a interface IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interface IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 332f123756d1340352524852aa5bcb38fce09612f52554facaf6e5c8c2398e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047474"
---
# <a name="ieventsubscription2-interface"></a>Interface IEventSubscription2

Armazena e recupera informações sobre assinaturas de evento. Essa interface estende a interface [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .

## <a name="when-to-implement"></a>Quando implementar

Você não precisa implementar a interface **IEventSubscription2** . Uma classe de objeto de evento fornecida pelo sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription2**.

## <a name="when-to-use"></a>Quando usar

O sistema de [eventos com+](com--events.md) usa essa interface para obter informações sobre assinaturas individuais.

## <a name="members"></a>Membros

A interface **IEventSubscription2** herda de **IEventSubscription**. **IEventSubscription2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IEventSubscription2** tem essas propriedades.



| Propriedade                                                                      | Tipo de acesso           | Descrição                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**FilterCriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Leitura/gravação<br/> | Os critérios de filtro que regem a assinatura.<br/> |
| [**SubscriberMoniker**](ieventsubscription2-subscribermoniker.md)<br/> | Leitura/gravação<br/> | O moniker do Assinante.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




