---
description: Especifica a prioridade de thread relativa para um branch da topologia.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1b131e6c8b0f379e5e7951498c52f7c0d7a3eab83b75fed4ab9e8100721668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874789"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>Atributo MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY

Especifica a prioridade de thread relativa para um branch da topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos nós de origem **(NÓ SOURCESTREAM DA \_ \_ TOPOLOGIA \_ do MF).** O atributo é opcional.

Esse atributo requer os atributos [MF \_ TOPNODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) e [MF \_ TOPNODE \_ WORKQUEUE \_ MMCSS \_ CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) no mesmo nó.

O valor do atributo é a prioridade de thread relativa da fila de trabalho para esse branch da topologia. O [MMCSS (Serviço](../procthread/multimedia-class-scheduler-service.md) de Agendador de Classes Multimídia) usa a prioridade relativa quando define a prioridade do thread. Para obter mais informações, [**consulte AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Melhorias na fila de trabalho e threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ID DE \_ WORKQUEUE DO MF TOPONODE \_**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
