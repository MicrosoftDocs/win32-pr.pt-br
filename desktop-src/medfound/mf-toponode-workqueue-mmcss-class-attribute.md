---
description: Especifica uma tarefa do serviço de Agendador de classes de multimídia (MMCSS) para uma ramificação de topologia.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: Atributo MF_TOPONODE_WORKQUEUE_MMCSS_CLASS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766559"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a>\_Atributo de classe MF TOPONODE \_ fila \_ MMCSS \_

Especifica uma tarefa do [serviço de Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para uma ramificação de topologia.

## <a name="data-type"></a>Tipo de dados

Cadeia de caracteres largos

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**). Esse atributo é opcional.

Esse atributo requer o atributo de [ID de fila de TOPONODE do MF \_ \_ \_ ](mf-toponode-workqueue-id-attribute.md) . Se você definir esse atributo, defina também o atributo de **\_ ID de \_ fila \_ de teleTOPONODE MF** definido no mesmo nó.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ID da \_ fila de TOPONODE MF \_**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Filas de trabalho](work-queues.md)
</dt> </dl>

 

 
