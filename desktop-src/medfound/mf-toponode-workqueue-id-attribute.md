---
description: Especifica uma fila de trabalho para uma ramificação de topologia.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: Atributo MF_TOPONODE_WORKQUEUE_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090865"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>\_Atributo de \_ ID de fila de TOPONODE MF \_

Especifica uma fila de trabalho para uma ramificação de topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**). O atributo é opcional.

O valor do atributo é um identificador definido pelo aplicativo para a fila de trabalho.

Os aplicativos podem usar esse atributo para atribuir filas de trabalho a ramificações da topologia. Cada nó de origem na topologia define uma ramificação. A ramificação inclui todos os nós de topologia que recebem dados desse nó.

Se você definir esse atributo, chame o método [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) na topologia resolvida. Várias ramificações na topologia podem compartilhar a mesma fila de trabalho e as filas de trabalho podem ser reutilizadas entre as topologias.

> [!Note]  
> O valor desse atributo não é o mesmo que o identificador retornado pela função [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) . O valor do atributo é um identificador definido pelo aplicativo e é usado para associar branches de topologia com filas de trabalho. Quando a sessão de mídia aloca uma nova fila de trabalho, ela armazena o identificador de fila de trabalho real internamente.

 

Se esse atributo for definido, o aplicativo também poderá atribuir a ramificação a uma tarefa do serviço de Agendador de classes de multimídia (MMCSS), definindo o atributo de [**\_ classe MF TOPONODE \_ fila do \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) .

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_classe TOPONODE do MF \_ fila do \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Filas de trabalho](work-queues.md)
</dt> </dl>

 

 




