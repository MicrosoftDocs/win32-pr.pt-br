---
description: Lista os diferentes tipos de notificações que podem ser recebidas por uma inscrição.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767782"
---
# <a name="notification_mask"></a>máscara de notificação \_

Lista os diferentes tipos de notificações que podem ser recebidas por uma inscrição.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_máscara de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Uma máscara que indica todos os bits válidos para uma notificação de transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**prepreparar notificação de transação \_ \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Essa notificação é chamada depois que um cliente chama [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) e nenhum Gerenciador de recursos (RM) dá suporte à confirmação de fase única ou a uma chamada de Gerenciador de transações superior (TM) [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). Essa notificação é recebida pelo RMs, indicando que eles devem concluir qualquer trabalho que poderia fazer com que outro RMs precise se inscrever em uma transação, como liberar seu cache. Depois de concluir essas operações, o RM deve chamar [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Para receber essa notificação, o RM também deve oferecer suporte à **\_ \_ preparação de notificação de transação** e à **\_ \_ confirmação de notificação de transação**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**\_preparação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Essa notificação é chamada depois que o processamento de **\_ \_ prepreparação de notificação de transação** é concluído. Ele sinaliza ao RM para concluir todo o trabalho associado a essa inscrição, de modo que ele possa garantir que uma operação de confirmação possa ser bem sucedido e que uma operação de anulação também tenha sucesso. Normalmente, a maior parte do trabalho de uma transação é feita durante a fase de preparação. Para RMs durável, eles devem registrar seu estado antes de chamar a função [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) . Essa é a última chance para o RM solicitar que a transação seja revertida.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_confirmação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Essa notificação sinaliza o RM para concluir todo o trabalho associado a essa inscrição. Normalmente, o RM libera quaisquer bloqueios, libera Todas as informações necessárias para reverter a transação. O RM deve responder chamando a função [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) quando tiver concluído essas operações.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**reversão de notificação de transação \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Essa notificação sinaliza o RM para desfazer todo o trabalho feito que está associado à transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**prepreparação de notificação de transação \_ \_ \_ concluída**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Essa notificação sinaliza para a TM superior que uma operação de pré-preparação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**preparação de notificação de transação \_ \_ \_ concluída**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Essa notificação sinaliza para a TM superior que uma operação de preparação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**confirmação de notificação de transação \_ \_ \_ concluída**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Essa notificação sinaliza para a TM superior que uma operação de confirmação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**reversão de notificação de transação \_ \_ \_ concluída**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Essa notificação sinaliza para a TM superior que uma operação de reversão foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_recuperação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Essa notificação sinaliza ao RMs que eles devem recuperar seu estado porque um resultado de transação deve ser entregue novamente. Por exemplo, quando um RM é recuperado e quando há transações deixadas em dúvida. Essa notificação é entregue quando o estado incerto é resolvido.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_confirmação de \_ uma \_ fase \_ única de notificação de transação**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Essa notificação sinaliza o RM para concluir e confirmar a transação sem usar um protocolo de confirmação de duas fases. Se o RM quiser usar uma operação de duas fases, ele deverá responder chamando a função [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_confirmação de \_ delegação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



O KTM está sinalizando para a TM superior para executar uma operação de confirmação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_consulta de \_ recuperação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



O KTM está sinalizando para a TM superior para consultar o status de uma transação incerta.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_prepreparar inscrição de notificação de transação \_ \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Essa notificação sinaliza para a TM superior que as notificações de pré-instalação devem ser entregues na inscrição especificada.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ última recuperação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Essa notificação indica que a operação de recuperação foi concluída para este RM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**incerteza de notificação de transação \_ \_**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



A transação especificada está em um estado incerto. O RM recebe essa notificação durante as operações de recuperação quando uma transação é preparada, mas não há Gerenciador de transações (TM) superior disponível. Por exemplo, quando uma transação envolve um TM remoto e esse nó não está disponível, seu nó está indisponível ou o serviço de [Coordenador de transações distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85)) local não está disponível, o estado da transação é incerto.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**notificação de transação do \_ \_ TM \_ online**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



O TM está online e aceitando solicitações.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_resultado da \_ solicitação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Sinaliza ao RMs que há informações de resultado disponíveis e que uma solicitação para essas informações deve ser feita.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_ \_ finalizar confirmação de notificação de transação \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reservado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                            |
| parâmetro<br/>                   | <dl> <dt>KtmTypes. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Constantes do Gerenciador de transações do kernel](kernel-transaction-manager-constants.md)
</dt> <dt>

[**Subinscrição**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**notificação de transação \_**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

