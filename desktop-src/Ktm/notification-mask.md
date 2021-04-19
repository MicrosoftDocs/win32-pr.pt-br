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
# <a name="notification_mask"></a><span data-ttu-id="7c99e-103">máscara de notificação \_</span><span class="sxs-lookup"><span data-stu-id="7c99e-103">NOTIFICATION\_MASK</span></span>

<span data-ttu-id="7c99e-104">Lista os diferentes tipos de notificações que podem ser recebidas por uma inscrição.</span><span class="sxs-lookup"><span data-stu-id="7c99e-104">Lists the different types of notifications that can be received by an enlistment.</span></span>

<dl> <dt>

<span data-ttu-id="7c99e-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_máscara de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION\_NOTIFY\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-106">0x3FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="7c99e-106">0x3FFFFFFF</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-107">Uma máscara que indica todos os bits válidos para uma notificação de transação.</span><span class="sxs-lookup"><span data-stu-id="7c99e-107">A mask that indicates all valid bits for a transaction notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**prepreparar notificação de transação \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**TRANSACTION\_NOTIFY\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7c99e-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-110">Essa notificação é chamada depois que um cliente chama [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) e nenhum Gerenciador de recursos (RM) dá suporte à confirmação de fase única ou a uma chamada de Gerenciador de transações superior (TM) [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span><span class="sxs-lookup"><span data-stu-id="7c99e-110">This notification is called after a client calls [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) and either no resource manager (RM) supports single-phase commit or a superior transaction manager (TM) calls [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span></span> <span data-ttu-id="7c99e-111">Essa notificação é recebida pelo RMs, indicando que eles devem concluir qualquer trabalho que poderia fazer com que outro RMs precise se inscrever em uma transação, como liberar seu cache.</span><span class="sxs-lookup"><span data-stu-id="7c99e-111">This notification is received by the RMs indicating that they should complete any work that could cause other RMs to need to enlist in a transaction, such as flushing its cache.</span></span> <span data-ttu-id="7c99e-112">Depois de concluir essas operações, o RM deve chamar [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span><span class="sxs-lookup"><span data-stu-id="7c99e-112">After completing these operations the RM must call [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span></span> <span data-ttu-id="7c99e-113">Para receber essa notificação, o RM também deve oferecer suporte à **\_ \_ preparação de notificação de transação** e à **\_ \_ confirmação de notificação de transação**.</span><span class="sxs-lookup"><span data-stu-id="7c99e-113">To receive this notification the RM must also support **TRANSACTION\_NOTIFY\_PREPARE** and **TRANSACTION\_NOTIFY\_COMMIT**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**\_preparação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION\_NOTIFY\_PREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7c99e-115">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-116">Essa notificação é chamada depois que o processamento de **\_ \_ prepreparação de notificação de transação** é concluído.</span><span class="sxs-lookup"><span data-stu-id="7c99e-116">This notification is called after the **TRANSACTION\_NOTIFY\_PREPREPARE** processing is complete.</span></span> <span data-ttu-id="7c99e-117">Ele sinaliza ao RM para concluir todo o trabalho associado a essa inscrição, de modo que ele possa garantir que uma operação de confirmação possa ser bem sucedido e que uma operação de anulação também tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="7c99e-117">It signals the RM to complete all the work that is associated with this enlistment so that it can guarantee that a commit operation could succeed and an abort operation could also succeed.</span></span> <span data-ttu-id="7c99e-118">Normalmente, a maior parte do trabalho de uma transação é feita durante a fase de preparação.</span><span class="sxs-lookup"><span data-stu-id="7c99e-118">Typically, the bulk of the work for a transaction is done during the prepare phase.</span></span> <span data-ttu-id="7c99e-119">Para RMs durável, eles devem registrar seu estado antes de chamar a função [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) .</span><span class="sxs-lookup"><span data-stu-id="7c99e-119">For durable RMs, they must log their state prior to calling the [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) function.</span></span> <span data-ttu-id="7c99e-120">Essa é a última chance para o RM solicitar que a transação seja revertida.</span><span class="sxs-lookup"><span data-stu-id="7c99e-120">This is the last chance for the RM to request that the transaction be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_confirmação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION\_NOTIFY\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7c99e-122">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-123">Essa notificação sinaliza o RM para concluir todo o trabalho associado a essa inscrição.</span><span class="sxs-lookup"><span data-stu-id="7c99e-123">This notification signals the RM to complete all the work that is associated with this enlistment.</span></span> <span data-ttu-id="7c99e-124">Normalmente, o RM libera quaisquer bloqueios, libera Todas as informações necessárias para reverter a transação.</span><span class="sxs-lookup"><span data-stu-id="7c99e-124">Typically, the RM releases any locks, releases any information necessary to roll back the transaction.</span></span> <span data-ttu-id="7c99e-125">O RM deve responder chamando a função [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) quando tiver concluído essas operações.</span><span class="sxs-lookup"><span data-stu-id="7c99e-125">The RM must respond by calling the [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) function when it has finished these operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**reversão de notificação de transação \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION\_NOTIFY\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-127">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7c99e-127">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-128">Essa notificação sinaliza o RM para desfazer todo o trabalho feito que está associado à transação.</span><span class="sxs-lookup"><span data-stu-id="7c99e-128">This notification signals the RM to undo all the work it has done that is associated with the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**prepreparação de notificação de transação \_ \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="7c99e-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-130">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c99e-130">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-131">Essa notificação sinaliza para a TM superior que uma operação de pré-preparação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="7c99e-131">This notification signals to the superior TM that a pre-prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**preparação de notificação de transação \_ \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="7c99e-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-133">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7c99e-133">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-134">Essa notificação sinaliza para a TM superior que uma operação de preparação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="7c99e-134">This notification signals to the superior TM that a prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**confirmação de notificação de transação \_ \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="7c99e-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-136">0x00000040</span><span class="sxs-lookup"><span data-stu-id="7c99e-136">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-137">Essa notificação sinaliza para a TM superior que uma operação de confirmação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="7c99e-137">This notification signals to the superior TM that a commit operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**reversão de notificação de transação \_ \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="7c99e-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="7c99e-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-140">Essa notificação sinaliza para a TM superior que uma operação de reversão foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="7c99e-140">This notification signals to the superior TM that a rollback operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_recuperação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION\_NOTIFY\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="7c99e-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-143">Essa notificação sinaliza ao RMs que eles devem recuperar seu estado porque um resultado de transação deve ser entregue novamente.</span><span class="sxs-lookup"><span data-stu-id="7c99e-143">This notification signals to RMs that they should recover their state because a transaction outcome must be redelivered.</span></span> <span data-ttu-id="7c99e-144">Por exemplo, quando um RM é recuperado e quando há transações deixadas em dúvida.</span><span class="sxs-lookup"><span data-stu-id="7c99e-144">For example, when an RM is recovered, and when there are transactions left in-doubt.</span></span> <span data-ttu-id="7c99e-145">Essa notificação é entregue quando o estado incerto é resolvido.</span><span class="sxs-lookup"><span data-stu-id="7c99e-145">This notification is delivered once the in-doubt state is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_confirmação de \_ uma \_ fase \_ única de notificação de transação**</span><span class="sxs-lookup"><span data-stu-id="7c99e-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION\_NOTIFY\_SINGLE\_PHASE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-147">0x00000200</span><span class="sxs-lookup"><span data-stu-id="7c99e-147">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-148">Essa notificação sinaliza o RM para concluir e confirmar a transação sem usar um protocolo de confirmação de duas fases.</span><span class="sxs-lookup"><span data-stu-id="7c99e-148">This notification signals the RM to complete and commit the transaction without using a two-phase commit protocol.</span></span> <span data-ttu-id="7c99e-149">Se o RM quiser usar uma operação de duas fases, ele deverá responder chamando a função [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .</span><span class="sxs-lookup"><span data-stu-id="7c99e-149">If the RM wants to use a two-phase operation, it must respond by calling the [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_confirmação de \_ delegação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION\_NOTIFY\_DELEGATE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-151">0x00000400</span><span class="sxs-lookup"><span data-stu-id="7c99e-151">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-152">O KTM está sinalizando para a TM superior para executar uma operação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="7c99e-152">KTM is signaling to the superior TM to perform a commit operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_consulta de \_ recuperação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION\_NOTIFY\_RECOVER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-154">0x00000800</span><span class="sxs-lookup"><span data-stu-id="7c99e-154">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-155">O KTM está sinalizando para a TM superior para consultar o status de uma transação incerta.</span><span class="sxs-lookup"><span data-stu-id="7c99e-155">KTM is signaling to the superior TM to query the status of an in-doubt transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_prepreparar inscrição de notificação de transação \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION\_NOTIFY\_ENLIST\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-157">0x00001000</span><span class="sxs-lookup"><span data-stu-id="7c99e-157">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-158">Essa notificação sinaliza para a TM superior que as notificações de pré-instalação devem ser entregues na inscrição especificada.</span><span class="sxs-lookup"><span data-stu-id="7c99e-158">This notification signals to the superior TM that pre-prepare notifications must be delivered on the specified enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ última recuperação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION\_NOTIFY\_LAST\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="7c99e-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-161">Essa notificação indica que a operação de recuperação foi concluída para este RM.</span><span class="sxs-lookup"><span data-stu-id="7c99e-161">This notification indicates that the recovery operation is complete for this RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**incerteza de notificação de transação \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION\_NOTIFY\_INDOUBT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-163">0x00004000</span><span class="sxs-lookup"><span data-stu-id="7c99e-163">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-164">A transação especificada está em um estado incerto.</span><span class="sxs-lookup"><span data-stu-id="7c99e-164">The specified transaction is in an in-doubt state.</span></span> <span data-ttu-id="7c99e-165">O RM recebe essa notificação durante as operações de recuperação quando uma transação é preparada, mas não há Gerenciador de transações (TM) superior disponível.</span><span class="sxs-lookup"><span data-stu-id="7c99e-165">The RM receives this notification during recovery operations when a transaction has been prepared, but there is no superior transaction manager (TM) available.</span></span> <span data-ttu-id="7c99e-166">Por exemplo, quando uma transação envolve um TM remoto e esse nó não está disponível, seu nó está indisponível ou o serviço de [Coordenador de transações distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85)) local não está disponível, o estado da transação é incerto.</span><span class="sxs-lookup"><span data-stu-id="7c99e-166">For example, when a transaction involves a remote TM and that node is unavailable, its node is unavailable, or the local [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) service is unavailable, the transaction state is in-doubt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**notificação de transação do \_ \_ TM \_ online**</span><span class="sxs-lookup"><span data-stu-id="7c99e-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION\_NOTIFY\_TM\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-168">0x02000000</span><span class="sxs-lookup"><span data-stu-id="7c99e-168">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-169">O TM está online e aceitando solicitações.</span><span class="sxs-lookup"><span data-stu-id="7c99e-169">The TM is online and accepting requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_resultado da \_ solicitação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**TRANSACTION\_NOTIFY\_REQUEST\_OUTCOME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-171">0x20000000</span><span class="sxs-lookup"><span data-stu-id="7c99e-171">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-172">Sinaliza ao RMs que há informações de resultado disponíveis e que uma solicitação para essas informações deve ser feita.</span><span class="sxs-lookup"><span data-stu-id="7c99e-172">Signals to RMs that there is outcome information available, and that a request for that information should be made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c99e-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_ \_ finalizar confirmação de notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION\_NOTIFY\_COMMIT\_FINALIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c99e-174">0x40000000</span><span class="sxs-lookup"><span data-stu-id="7c99e-174">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="7c99e-175">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7c99e-175">Reserved.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c99e-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c99e-176">Requirements</span></span>



| <span data-ttu-id="7c99e-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c99e-177">Requirement</span></span> | <span data-ttu-id="7c99e-178">Valor</span><span class="sxs-lookup"><span data-stu-id="7c99e-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c99e-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c99e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="7c99e-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c99e-180">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="7c99e-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c99e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="7c99e-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c99e-182">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="7c99e-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c99e-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c99e-184"><dt>KtmTypes. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c99e-184"><dt>KtmTypes.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c99e-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c99e-185">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c99e-186">[Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c99e-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7c99e-187">Constantes do Gerenciador de transações do kernel</span><span class="sxs-lookup"><span data-stu-id="7c99e-187">Kernel Transaction Manager Constants</span></span>](kernel-transaction-manager-constants.md)
</dt> <dt>

[<span data-ttu-id="7c99e-188">**Subinscrição**</span><span class="sxs-lookup"><span data-stu-id="7c99e-188">**CreateEnlistment**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[<span data-ttu-id="7c99e-189">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="7c99e-189">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[<span data-ttu-id="7c99e-190">**GetNotificationResourceManager**</span><span class="sxs-lookup"><span data-stu-id="7c99e-190">**GetNotificationResourceManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[<span data-ttu-id="7c99e-191">**GetNotificationResourceManagerAsync**</span><span class="sxs-lookup"><span data-stu-id="7c99e-191">**GetNotificationResourceManagerAsync**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[<span data-ttu-id="7c99e-192">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="7c99e-192">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[<span data-ttu-id="7c99e-193">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="7c99e-193">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[<span data-ttu-id="7c99e-194">**notificação de transação \_**</span><span class="sxs-lookup"><span data-stu-id="7c99e-194">**TRANSACTION\_NOTIFICATION**</span></span>](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

