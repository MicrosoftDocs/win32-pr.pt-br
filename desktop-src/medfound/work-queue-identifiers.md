---
description: As constantes a seguir identificam as filas de trabalho do Media Foundation padrão.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificadores de fila de trabalho (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d454e8b2a199a9c132bf6ea287f31d7d3e5102
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470223"
---
# <a name="work-queue-identifiers"></a>Identificadores de fila de trabalho

As constantes a seguir identificam as filas de trabalho do Media Foundation padrão.

Os aplicativos devem usar \_ \_ a fila \_ de retorno de chamada MFASYNC multithread ou usar uma fila de trabalho Obtida de [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) se desejarem controlar a prioridade de execução. Observe que as prioridades da fila de trabalho da plataforma padrão podem ser alteradas dinamicamente quando um aplicativo chama [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss). Para obter mais informações sobre filas de trabalho, consulte [filas de trabalho](work-queues.md).




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt><dt>0x00000001</dt></dl> | Na maioria dos casos, os aplicativos devem usar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> Esta fila de trabalho é usada para operações síncronas. Usar a fila de trabalho padrão pode correr o risco de deadlock. Os aplicativos podem criar uma fila síncrona privada na parte superior da fila multi-threaded usando <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt><dt>0x00000002</dt></dl> | Não para uso geral do aplicativo.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt><dt>0x00000003</dt></dl> | Não para uso geral do aplicativo.<br /> Essa fila de trabalho é usada internamente para operações de e/s, como leitura de arquivos e leitura da rede.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt><dt>0x00000004</dt></dl> | Não para uso geral do aplicativo.<br /> Essa fila de trabalho é usada para retornos de chamada periódicos e itens de trabalho agendados. As seguintes funções colocam itens de trabalho nesta fila:<br /><ul><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li></ul> | 
| <span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt><dt>0x00000005</dt></dl> | Essa fila de trabalho multi-threaded deve ser usada na maioria dos casos. <br /> Essa fila de trabalho é usada para operações assíncronas durante Media Foundation.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt><dt>0x00000007</dt></dl> | Não para uso geral do aplicativo. Em vez disso, os aplicativos devem usar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> | 




Além disso, as constantes a seguir são usadas em conexão com as filas de trabalho.



| Constante/valor                                                                                                                                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_ Fila de retorno de chamada \_ \_ indefinida**</dt> <dt>0x00000000</dt> </dl>           | Fila de trabalho indefinida.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_ 0xFFFF0000 \_ de \_ \_ máscara privada da fila de retorno de chamada**</dt> <dt></dt> </dl> | Máscara de bits para distinguir as filas de trabalho da plataforma daquelas criadas chamando [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).<br/> Para uma fila de trabalho criada pelo [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), o seguinte valor é diferente de zero:<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_ Fila de retorno de chamada \_ \_ todos**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Todas as filas de trabalho da plataforma.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> <dt>

[Filas de trabalho](work-queues.md)
</dt> <dt>

[Aprimoramentos na fila de trabalho e threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




