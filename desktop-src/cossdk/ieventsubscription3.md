---
description: Armazena e recupera informações sobre assinaturas de evento. Essa interface estende a interface IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interface IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: cbb6c5b19ed6116c59642e8dc5c0aa8eabf4800b066904f2132c7d182f2b7bbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070626"
---
# <a name="ieventsubscription3-interface"></a>Interface IEventSubscription3

Armazena e recupera informações sobre assinaturas de evento. Essa interface estende a interface [**IEventSubscription2.**](ieventsubscription2.md)

## <a name="when-to-implement"></a>Quando implementar

Você não precisa implementar a interface **IEventSubscription3.** Uma classe de objeto de evento fornecida pelo sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription3.**

## <a name="when-to-use"></a>Quando usar

O [sistema eventos COM+](com--events.md) usa essa interface para obter informações sobre assinaturas individuais.

## <a name="members"></a>Membros

A interface **IEventSubscription3** herda de **IEventSubscription2**. **IEventSubscription3** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IEventSubscription3** tem essas propriedades.



| Propriedade                                                                                  | Tipo de acesso           | Descrição                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | Leitura/gravação<br/> | O GUID do aplicativo do objeto da classe de evento.<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Leitura/gravação<br/> | O GUID de partição do objeto da classe de evento.<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Leitura/gravação<br/> | O GUID do aplicativo do assinante.<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Leitura/gravação<br/> | O GUID de partição do assinante.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




