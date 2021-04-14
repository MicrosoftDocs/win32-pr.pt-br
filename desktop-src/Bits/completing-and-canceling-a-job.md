---
title: Concluindo e cancelando um trabalho
description: Para concluir um trabalho de transferência, chame o método método ibackgroundcopyjob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- transferir BITS de trabalho, cancelando
- Cancelando um trabalho BITS
- transferir BITS de trabalho, concluindo
- Concluindo um trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453530"
---
# <a name="completing-and-canceling-a-job"></a><span data-ttu-id="c9ee0-107">Concluindo e cancelando um trabalho</span><span class="sxs-lookup"><span data-stu-id="c9ee0-107">Completing and Canceling a Job</span></span>

<span data-ttu-id="c9ee0-108">Para concluir um trabalho de transferência, chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="c9ee0-108">To complete a transfer job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="c9ee0-109">Para baixar trabalhos, você pode chamar o método **Complete** antes que todos os arquivos no trabalho tenham sido transferidos (antes de o estado do trabalho ser BG, o \_ estado do trabalho é \_ \_ transferido).</span><span class="sxs-lookup"><span data-stu-id="c9ee0-109">For download jobs, you can call the **Complete** method before all files in the job have been transferred (before the job's state is BG\_JOB\_STATE\_TRANSFERRED).</span></span> <span data-ttu-id="c9ee0-110">Somente os arquivos que o BITS transferiu com êxito para o cliente antes de você ter chamado o método **Complete** estão disponíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-110">Only those files that BITS successfully transferred to the client before you called the **Complete** method are available to the user.</span></span>

<span data-ttu-id="c9ee0-111">Para trabalhos de carregamento, chame o método [**completo**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) somente se o estado do trabalho for BG, \_ estado de trabalho \_ \_ transferido.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-111">For upload jobs, call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method only if the job's state is BG\_JOB\_STATE\_TRANSFERRED.</span></span> <span data-ttu-id="c9ee0-112">Para determinar quando o estado do trabalho é BG, o estado do trabalho é \_ \_ \_ transferido, [sondar](polling-for-the-status-of-the-job.md) a propriedade de estado do trabalho ou registrar-se para receber a notificação de evento de recebimento de \_ tarefa de notificação BG \_ \_ . [](registering-a-com-callback.md)</span><span class="sxs-lookup"><span data-stu-id="c9ee0-112">To determine when the job's state is BG\_JOB\_STATE\_TRANSFERRED, [poll](polling-for-the-status-of-the-job.md) the job's state property or register to receive BG\_NOTIFY\_JOB\_TRANSFERRED [event notification](registering-a-com-callback.md).</span></span>

<span data-ttu-id="c9ee0-113">Para cancelar um trabalho de transferência, chame o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="c9ee0-113">To cancel a transfer job, call the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span> <span data-ttu-id="c9ee0-114">O método **Cancel** remove o trabalho da fila de transferência e remove os arquivos temporários do cliente.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-114">The **Cancel** method removes the job from the transfer queue and removes the temporary files from the client.</span></span> <span data-ttu-id="c9ee0-115">Normalmente, você chamará esse método se não for possível resolver um erro associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-115">Typically, you call this method if you are unable to resolve an error associated with the job.</span></span>

<span data-ttu-id="c9ee0-116">O método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) cancela um upload se o carregamento não for concluído.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-116">The [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method cancels an upload if the upload is not complete.</span></span> <span data-ttu-id="c9ee0-117">Se o upload for concluído e o trabalho for do tipo BG \_ resposta de carregamento do tipo de trabalho \_ \_ \_ , o método cancelará a resposta.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-117">If the upload is complete, and the job is of type BG\_JOB\_TYPE\_UPLOAD\_REPLY, the method cancels the reply.</span></span>

<span data-ttu-id="c9ee0-118">Se você não chamar o método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) dentro de 90 dias ( [JobInactivityTimeout](group-policies.md) padrão política de grupo), o serviço cancelará o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-118">If you do not call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method within 90 days (default [JobInactivityTimeout](group-policies.md) Group Policy), the service cancels the job.</span></span> <span data-ttu-id="c9ee0-119">Se o serviço cancelar o trabalho, os arquivos baixados e o arquivo de resposta não estarão disponíveis para o cliente; o cancelamento do trabalho não afeta os arquivos que foram carregados com êxito.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-119">If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.</span></span> <span data-ttu-id="c9ee0-120">Você sempre deve chamar o método **Complete** ou **Cancel** e não confiar na política JobInactivityTimeout para limpar seus trabalhos.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-120">You should always call the **Complete** or the **Cancel** method and not rely on the JobInactivityTimeout policy to cleanup your jobs.</span></span> <span data-ttu-id="c9ee0-121">Os trabalhos restantes na fila podem impedir que os usuários criem outros trabalhos se o limite da política MaxJobsPerUser ou MaxJobsPerMachine for atingido.</span><span class="sxs-lookup"><span data-stu-id="c9ee0-121">Jobs left in the queue may prevent users from creating other jobs if the MaxJobsPerUser or MaxJobsPerMachine policy limit is reached.</span></span>

 

 




