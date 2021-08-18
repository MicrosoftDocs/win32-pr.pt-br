---
description: Lista os diferentes tipos de notificações que podem ser recebidas por uma inscrever-se.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17391d2b406b3f7a3ee9a3a868bc1b6734050c787fdbb432785e5be0b917468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146539"
---
# <a name="notification_mask"></a>MÁSCARA DE \_ NOTIFICAÇÃO

Lista os diferentes tipos de notificações que podem ser recebidas por uma inscrever-se.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**MÁSCARA DE \_ NOTIFICAÇÃO \_ DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Uma máscara que indica todos os bits válidos para uma notificação de transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**\_PREPREPARE DE \_ NOTIFICAÇÃO DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Essa notificação é chamada depois que um cliente chama [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) e nenhum RM (gerenciador de recursos) dá suporte a confirmação de fase única ou a um TM (gerenciador de transações superior) chama [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment). Essa notificação é recebida pelas RMs, indicando que elas devem concluir qualquer trabalho que possa fazer com que outras RMs precisem se inscrever em uma transação, como liberar seu cache. Depois de concluir essas operações, o RM deve chamar [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete). Para receber essa notificação, o RM também deve dar suporte **a TRANSACTION \_ NOTIFY \_ PREPARE** e **TRANSACTION NOTIFY \_ \_ COMMIT.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**PREPARAÇÃO \_ DE NOTIFICAÇÃO \_ DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Essa notificação é chamada depois que o processamento **\_ DE \_ PREPREPARE TRANSACTION NOTIFY** é concluído. Ele sinaliza ao RM para concluir todo o trabalho associado a essa inslistação para que ele possa garantir que uma operação de confirmação seja bem-sucedida e que uma operação de anulação também possa ser bem-sucedida. Normalmente, a maior parte do trabalho para uma transação é feita durante a fase de preparação. Para RMs duráveis, eles devem registrar seu estado antes de chamar a [**função PrepareComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) Essa é a última chance do RM solicitar que a transação seja relembolsada.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**COMMIT \_ DE NOTIFICAÇÃO \_ DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Essa notificação sinaliza o RM para concluir todo o trabalho associado a essa inscrever-se. Normalmente, o RM libera todos os bloqueios, libera todas as informações necessárias para reverter a transação. O RM deve responder chamando a [**função CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) quando tiver concluído essas operações.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**ROLLBACK \_ DE \_ NOTIFICAÇÃO DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Essa notificação sinaliza o RM para desfazer todo o trabalho que ele fez associado à transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_ \_ PRÉ-PREPARAÇÃO DA NOTIFICAÇÃO DE TRANSAÇÃO \_ CONCLUÍDA**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Essa notificação sinaliza ao TM superior que uma operação de pré-preparação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**CONCLUSÃO \_ DA PREPARAÇÃO DA \_ NOTIFICAÇÃO DE \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Essa notificação sinaliza ao TM superior que uma operação de preparação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**COMMIT \_ DE \_ NOTIFICAÇÃO DE TRANSAÇÃO \_ CONCLUÍDO**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Essa notificação sinaliza ao TM superior que uma operação de confirmação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**RE \_ \_ ROLLBACK DE NOTIFICAÇÃO DE TRANSAÇÃO \_ CONCLUÍDA**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Essa notificação sinaliza ao TM superior que uma operação de reação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**RECUPERAÇÃO \_ DE NOTIFICAÇÃO \_ DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Essa notificação sinaliza às RMs que elas devem recuperar seu estado porque um resultado da transação deve ser entregue de novo. Por exemplo, quando um RM é recuperado e quando há transações deixadas em dúvida. Essa notificação é entregue depois que o estado de dúvida é resolvido.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**COMMIT \_ DE FASE ÚNICA DE \_ \_ NOTIFICAÇÃO DE \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Essa notificação sinaliza o RM para concluir e fazer commit da transação sem usar um protocolo de confirmação em duas fases. Se o RM quiser usar uma operação de duas fases, ele deverá responder chamando a [**função SinglePhaseReject.**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**COMMIT \_ DO DELEGADO DE \_ NOTIFICAÇÃO DE \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



O KTM está sinalizando para o TM superior para executar uma operação de confirmação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**CONSULTA \_ DE \_ RECUPERAÇÃO DE \_ NOTIFICAÇÃO DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



O KTM está sinalizando para o TM superior para consultar o status de uma transação em dúvida.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_PREPREPARE DE \_ \_ NOTIFICAÇÃO DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Essa notificação sinaliza para o TM superior que as notificações de pré-preparação devem ser entregues na inscrições especificada.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**NOTIFICAÇÃO \_ DA TRANSAÇÃO ÚLTIMA \_ \_ RECUPERAÇÃO**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Essa notificação indica que a operação de recuperação está concluída para este RM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**NOTIFICAÇÃO \_ \_ DE TRANSAÇÃO INDOUBT**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



A transação especificada está em um estado de dúvida. O RM recebe essa notificação durante as operações de recuperação quando uma transação foi preparada, mas não há nenhum TM (gerenciador de transações superior) disponível. Por exemplo, quando [uma](/previous-versions/windows/desktop/ms684146(v=vs.85)) transação envolve um TM remoto e esse nó não está disponível, seu nó não está disponível ou o serviço Coordenador de Transações Distribuídas local não está disponível, o estado da transação está em dúvida.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**NOTIFICAÇÃO \_ DE \_ TRANSAÇÃO TM \_ ONLINE**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



O TM está online e aceitando solicitações.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**RESULTADO DA \_ \_ SOLICITAÇÃO DE NOTIFICAÇÃO \_ DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Sinaliza às RMs que há informações de resultado disponíveis e que uma solicitação para essas informações deve ser feita.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION \_ NOTIFY \_ COMMIT \_ FINALIZE**
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
| Cabeçalho<br/>                   | <dl> <dt>KtmTypes.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Constantes do Gerenciador de Transações do Kernel](kernel-transaction-manager-constants.md)
</dt> <dt>

[**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
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

[**NOTIFICAÇÃO DE \_ TRANSAÇÃO**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

