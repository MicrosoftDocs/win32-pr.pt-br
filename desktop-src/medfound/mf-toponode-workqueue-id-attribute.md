---
description: Especifica uma fila de trabalho para um branch de topologia.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: MF_TOPONODE_WORKQUEUE_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ba4ab55d2a70b4b0c081544ab43a78719fab537fbf478519bde1e65dfc9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955086"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>Atributo MF \_ TOPONODE \_ WORKQUEUE \_ ID

Especifica uma fila de trabalho para um branch de topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos nós de origem **(NÓ SOURCESTREAM DA \_ \_ TOPOLOGIA \_ do MF).** O atributo é opcional.

O valor do atributo é um identificador definido pelo aplicativo para a fila de trabalho.

Os aplicativos podem usar esse atributo para atribuir filas de trabalho a branches da topologia. Cada nó de origem na topologia define um branch. O branch inclui todos os nós de topologia que recebem dados desse nó.

Se você definir esse atributo, chame o método [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) na topologia resolvida. Vários branches na topologia podem compartilhar a mesma fila de trabalho e as filas de trabalho podem ser re usadas entre topologias.

> [!Note]  
> O valor desse atributo não é o mesmo que o identificador retornado pela [**função MFAllocateWorkQueue.**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) O valor do atributo é um identificador definido pelo aplicativo e é usado para associar branches de topologia a filas de trabalho. Quando a Sessão de Mídia aloca uma nova fila de trabalho, ela armazena o identificador real da fila de trabalho internamente.

 

Se esse atributo for definido, o aplicativo também poderá atribuir o branch a uma tarefa MMCSS (Serviço de Agendador de Classes Multimídia), definindo o atributo [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS.**](mf-toponode-workqueue-mmcss-class-attribute.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**CLASSE MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Filas de Trabalho](work-queues.md)
</dt> </dl>

 

 




