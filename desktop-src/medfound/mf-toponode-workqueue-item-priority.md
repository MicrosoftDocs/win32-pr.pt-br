---
description: Especifica a prioridade de item de trabalho para uma ramificação da topologia.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Atributo MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164759"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                               |
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

 

 




