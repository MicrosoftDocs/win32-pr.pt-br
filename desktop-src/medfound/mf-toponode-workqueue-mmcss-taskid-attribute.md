---
description: Especifica um identificador de tarefa do serviço de Agendador de classes de multimídia (MMCSS) para uma ramificação de topologia.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Atributo MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502108"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>\_Atributo TOPONODE da \_ fila de \_ \_ tarefas do MF MMCSS

Especifica um identificador de tarefa do serviço de Agendador de classes de multimídia (MMCSS) para uma ramificação de topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**). Esse atributo é opcional.

Esse atributo é ignorado, a menos que os seguintes atributos também sejam definidos:

-   [**\_ID da \_ fila de TOPONODE MF \_**](mf-toponode-workqueue-id-attribute.md)
-   [**\_classe TOPONODE do MF \_ fila do \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md)

Se o aplicativo registrar um de seus próprios threads com o MMCSS, você poderá usar esse atributo para associar a fila de trabalho de topologia ao grupo do MMCSS do aplicativo. Defina o valor do atributo igual ao identificador da tarefa que o aplicativo recebeu quando registrado com o MMCSS. (O identificador de tarefa é retornado no parâmetro *TaskIndex* da função [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) . Para obter mais informações, consulte o tópico [processo e funções de thread](../procthread/process-and-thread-functions.md).)

Se você quiser que o MMCSS atribua um novo identificador de tarefa para a topologia, defina o atributo de [**\_ classe MF TOPONODE \_ fila do \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) , mas não defina o atributo **MF TOPONODE da fila de \_ \_ \_ \_ tarefas do MMCSS** .

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

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[Filas de trabalho](work-queues.md)
</dt> </dl>

 

 
