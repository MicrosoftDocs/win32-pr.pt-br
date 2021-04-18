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
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814004"
---
# <a name="ieventsubscription3-interface"></a>Interface IEventSubscription3

Armazena e recupera informações sobre assinaturas de evento. Essa interface estende a interface [**IEventSubscription2**](ieventsubscription2.md) .

## <a name="when-to-implement"></a>Quando implementar

Você não precisa implementar a interface **IEventSubscription3** . Uma classe de objeto de evento fornecida pelo sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription3**.

## <a name="when-to-use"></a>Quando usar

O sistema de [eventos com+](com--events.md) usa essa interface para obter informações sobre assinaturas individuais.

## <a name="members"></a>Membros

A interface **IEventSubscription3** herda de **IEventSubscription2**. **IEventSubscription3** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IEventSubscription3** tem essas propriedades.



| Propriedade                                                                                  | Tipo de acesso           | Descrição                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | Leitura/gravação<br/> | O GUID do aplicativo do objeto da classe de evento.<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Leitura/gravação<br/> | O GUID da partição do objeto de classe de evento.<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Leitura/gravação<br/> | O GUID do aplicativo do Assinante.<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Leitura/gravação<br/> | O GUID da partição do Assinante.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




