---
description: Especifica a prioridade de thread relativa para uma ramificação da topologia.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Atributo MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090864"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>\_Atributo de \_ prioridade MF TOPONODE fila do \_ MMCSS \_

Especifica a prioridade de thread relativa para uma ramificação da topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**). O atributo é opcional.

Esse atributo requer os atributos de classe [MF \_ TOPONODE \_ fila \_ ](mf-toponode-workqueue-id-attribute.md) e [MF \_ TOPONODE \_ fila do \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) no mesmo nó.

O valor do atributo é a prioridade de thread relativa da fila de trabalho para essa ramificação da topologia. O [serviço do Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) usa a prioridade relativa quando define a prioridade do thread. Para obter mais informações, consulte [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

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
</dt> <dt>

[**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
