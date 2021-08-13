---
description: Especifica a prioridade de item de trabalho para uma ramificação da topologia.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Atributo MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff67e48bda6ac00baeab9418b80d366c23808713b4689a013949b364f09b6e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739830"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>\_Atributo de \_ prioridade do item da fila de TOPONODE MF \_ \_

Especifica a prioridade de item de trabalho para uma ramificação da topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**). O atributo é opcional.

Esse atributo requer o atributo de ID de fila de TOPONODE do MF no mesmo nó. [ \_ \_ \_ ](mf-toponode-workqueue-id-attribute.md)

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Aprimoramentos na fila de trabalho e threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ID da \_ fila de TOPONODE MF \_**](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




