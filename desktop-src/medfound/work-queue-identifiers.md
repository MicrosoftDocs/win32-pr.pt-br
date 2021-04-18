---
description: As constantes a seguir identificam as filas de trabalho do Media Foundation padrão.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificadores de fila de trabalho (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756787"
---
# <a name="work-queue-identifiers"></a><span data-ttu-id="0846b-103">Identificadores de fila de trabalho</span><span class="sxs-lookup"><span data-stu-id="0846b-103">Work Queue Identifiers</span></span>

<span data-ttu-id="0846b-104">As constantes a seguir identificam as filas de trabalho do Media Foundation padrão.</span><span class="sxs-lookup"><span data-stu-id="0846b-104">The following constants identify the standard Media Foundation work queues.</span></span>

<span data-ttu-id="0846b-105">Os aplicativos devem usar \_ \_ a fila \_ de retorno de chamada MFASYNC multithread ou usar uma fila de trabalho Obtida de [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) se desejarem controlar a prioridade de execução.</span><span class="sxs-lookup"><span data-stu-id="0846b-105">Applications should use MFASYNC\_CALLBACK\_QUEUE\_MULTITHREADED or use a work queue obtained from [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) if they want to control the execution priority.</span></span> <span data-ttu-id="0846b-106">Observe que as prioridades da fila de trabalho da plataforma padrão podem ser alteradas dinamicamente quando um aplicativo chama [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span><span class="sxs-lookup"><span data-stu-id="0846b-106">Note that the default platform work queue priorities can dynamically change when an application calls [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span></span> <span data-ttu-id="0846b-107">Para obter mais informações sobre filas de trabalho, consulte [filas de trabalho](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="0846b-107">For more information about work queues, see [Work Queues](work-queues.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0846b-108">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="0846b-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0846b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0846b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <span data-ttu-id="0846b-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="0846b-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0846b-111">Na maioria dos casos, os aplicativos devem usar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="0846b-111">In most cases, applications should use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/> <span data-ttu-id="0846b-112">Esta fila de trabalho é usada para operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="0846b-112">This work queue is used for synchronous operations.</span></span> <span data-ttu-id="0846b-113">Usar a fila de trabalho padrão pode correr o risco de deadlock.</span><span class="sxs-lookup"><span data-stu-id="0846b-113">Using the standard work queue may run the risk of deadlocking.</span></span> <span data-ttu-id="0846b-114">Os aplicativos podem criar uma fila síncrona privada na parte superior da fila multi-threaded usando <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0846b-114">Applications can create a private synchronous queue on top of the multithreaded queue by using <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <span data-ttu-id="0846b-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="0846b-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0846b-116">Não para uso geral do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0846b-116">Not for general application use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <span data-ttu-id="0846b-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span><span class="sxs-lookup"><span data-stu-id="0846b-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0846b-118">Não para uso geral do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0846b-118">Not for general application use.</span></span><br/> <span data-ttu-id="0846b-119">Essa fila de trabalho é usada internamente para operações de e/s, como leitura de arquivos e leitura da rede.</span><span class="sxs-lookup"><span data-stu-id="0846b-119">This work queue is used internally for I/O operations such as reading files and reading from the network.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <span data-ttu-id="0846b-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="0846b-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0846b-121">Não para uso geral do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0846b-121">Not for general application use.</span></span><br/> <span data-ttu-id="0846b-122">Essa fila de trabalho é usada para retornos de chamada periódicos e itens de trabalho agendados.</span><span class="sxs-lookup"><span data-stu-id="0846b-122">This work queue is used for periodic callbacks and scheduled work items.</span></span> <span data-ttu-id="0846b-123">As seguintes funções colocam itens de trabalho nesta fila:</span><span class="sxs-lookup"><span data-stu-id="0846b-123">The following functions put work items in this queue:</span></span><br/>
<ul>
<li><span data-ttu-id="0846b-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0846b-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span></span></li>
<li><span data-ttu-id="0846b-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="0846b-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span></span></li>
<li><span data-ttu-id="0846b-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="0846b-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <span data-ttu-id="0846b-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span><span class="sxs-lookup"><span data-stu-id="0846b-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0846b-128">Essa fila de trabalho multi-threaded deve ser usada na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="0846b-128">This multithreaded work queue should be used in most cases.</span></span> <br/> <span data-ttu-id="0846b-129">Essa fila de trabalho é usada para operações assíncronas durante Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0846b-129">This work queue is used for asynchronous operations throughout Media Foundation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <span data-ttu-id="0846b-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span><span class="sxs-lookup"><span data-stu-id="0846b-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0846b-131">Não para uso geral do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0846b-131">Not for general application use.</span></span> <span data-ttu-id="0846b-132">Em vez disso, os aplicativos devem usar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="0846b-132">Applications should instead use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="0846b-133">Além disso, as constantes a seguir são usadas em conexão com as filas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0846b-133">In addition, the following constants are used in connection with work queues.</span></span>



| <span data-ttu-id="0846b-134">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="0846b-134">Constant/value</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0846b-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="0846b-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <span data-ttu-id="0846b-136"><dt>**MFASYNC \_ Fila de retorno de chamada \_ \_ indefinida**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0846b-136"><dt>**MFASYNC\_CALLBACK\_QUEUE\_UNDEFINED**</dt> <dt>0x00000000</dt></span></span> </dl>           | <span data-ttu-id="0846b-137">Fila de trabalho indefinida.</span><span class="sxs-lookup"><span data-stu-id="0846b-137">Undefined work queue.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <span data-ttu-id="0846b-138"><dt>**MFASYNC \_ 0xFFFF0000 \_ de \_ \_ máscara privada da fila de retorno de chamada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0846b-138"><dt>**MFASYNC\_CALLBACK\_QUEUE\_PRIVATE\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl> | <span data-ttu-id="0846b-139">Máscara de bits para distinguir as filas de trabalho da plataforma daquelas criadas chamando [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="0846b-139">Bit mask to distinguish platform work queues from those created by calling [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span><br/> <span data-ttu-id="0846b-140">Para uma fila de trabalho criada pelo [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), o seguinte valor é diferente de zero:</span><span class="sxs-lookup"><span data-stu-id="0846b-140">For a work queue created by [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), the following value is nonzero:</span></span><br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <span data-ttu-id="0846b-141"><dt>**MFASYNC \_ Fila de retorno de chamada \_ \_ todos**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="0846b-141"><dt>**MFASYNC\_CALLBACK\_QUEUE\_ALL**</dt> <dt>0xFFFFFFFF</dt></span></span> </dl>                             | <span data-ttu-id="0846b-142">Todas as filas de trabalho da plataforma.</span><span class="sxs-lookup"><span data-stu-id="0846b-142">All platform work queues.</span></span><br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="0846b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0846b-143">Requirements</span></span>



| <span data-ttu-id="0846b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0846b-144">Requirement</span></span> | <span data-ttu-id="0846b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="0846b-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0846b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0846b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0846b-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0846b-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0846b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0846b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0846b-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0846b-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0846b-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0846b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0846b-151"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0846b-151"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0846b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0846b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0846b-153">Media Foundation constantes</span><span class="sxs-lookup"><span data-stu-id="0846b-153">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="0846b-154">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="0846b-154">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="0846b-155">Aprimoramentos na fila de trabalho e threading</span><span class="sxs-lookup"><span data-stu-id="0846b-155">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




