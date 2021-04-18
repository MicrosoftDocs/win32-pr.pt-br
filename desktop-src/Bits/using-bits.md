---
title: Usando BITS
description: Usando BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- BITS
- Serviço de Transferência Inteligente em Segundo Plano, tarefas
- BITS de transferência de arquivo
- Usando BITS bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753001"
---
# <a name="using-bits"></a><span data-ttu-id="2241a-107">Usando BITS</span><span class="sxs-lookup"><span data-stu-id="2241a-107">Using BITS</span></span>

<span data-ttu-id="2241a-108">As etapas a seguir mostram como executar uma transferência de arquivo usando as  [interfaces](bits-interfaces.md)do serviço de transferência inteligente em segundo plano (bits).</span><span class="sxs-lookup"><span data-stu-id="2241a-108">The following steps show how to perform a file transfer using the Background Intelligent Transfer Service (BITS)  [interfaces](bits-interfaces.md).</span></span>

<span data-ttu-id="2241a-109">**Para executar uma transferência de arquivo**</span><span class="sxs-lookup"><span data-stu-id="2241a-109">**To perform a file transfer**</span></span>

1.  [<span data-ttu-id="2241a-110">Conectar-se ao serviço BITS</span><span class="sxs-lookup"><span data-stu-id="2241a-110">Connect to the BITS service</span></span>](connecting-to-the-bits-service.md)
2.  [<span data-ttu-id="2241a-111">Criar um trabalho de transferência</span><span class="sxs-lookup"><span data-stu-id="2241a-111">Create a transfer job</span></span>](creating-a-job.md)
3.  [<span data-ttu-id="2241a-112">Adicionar arquivos ao trabalho</span><span class="sxs-lookup"><span data-stu-id="2241a-112">Add files to the job</span></span>](adding-files-to-a-job.md)
4.  [<span data-ttu-id="2241a-113">Iniciar o trabalho</span><span class="sxs-lookup"><span data-stu-id="2241a-113">Start the job</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [<span data-ttu-id="2241a-114">Determinar se o BITS transferiu com êxito os arquivos</span><span class="sxs-lookup"><span data-stu-id="2241a-114">Determine if BITS successfully transferred the files</span></span>](determining-the-status-of-a-job.md)
6.  [<span data-ttu-id="2241a-115">Concluir o trabalho</span><span class="sxs-lookup"><span data-stu-id="2241a-115">Complete the job</span></span>](completing-and-canceling-a-job.md)

<span data-ttu-id="2241a-116">As etapas anteriores mostram como transferir arquivos usando os valores de propriedade padrão para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="2241a-116">The previous steps show how to transfer files using the default property values for a job.</span></span> <span data-ttu-id="2241a-117">Você pode alterar o comportamento padrão alterando um ou mais dos valores de Propriedade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2241a-117">You can change the default behavior by changing one or more of the job's property values.</span></span> <span data-ttu-id="2241a-118">Por exemplo, você pode alterar a prioridade em que o trabalho é processado em relação a outros trabalhos na fila, especificar sua própria configuração de proxy e registrar para receber a notificação de eventos quando o BITS transferiu os arquivos.</span><span class="sxs-lookup"><span data-stu-id="2241a-118">For example, you can change the priority that the job is processed relative to other jobs in the queue, specify your own proxy setting, and register to receive event notification when BITS has transferred the files.</span></span> <span data-ttu-id="2241a-119">Para obter mais informações, consulte [Configurando e recuperando as propriedades de um trabalho](setting-and-retrieving-the-properties-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="2241a-119">For more information, see [Setting and Retrieving the Properties of a Job](setting-and-retrieving-the-properties-of-a-job.md).</span></span>

<span data-ttu-id="2241a-120">O Windows PowerShell fornece um mecanismo simples para gerenciar muitas tarefas de BITS.</span><span class="sxs-lookup"><span data-stu-id="2241a-120">Windows PowerShell provides a simple mechanism to manage many BITS tasks.</span></span> <span data-ttu-id="2241a-121">Esta seção contém os seguintes tópicos que mostram como usar os cmdlets do Windows PowerShell com BITS:</span><span class="sxs-lookup"><span data-stu-id="2241a-121">This section contains the following topics that show how to use Windows PowerShell cmdlets with BITS:</span></span>

-   [<span data-ttu-id="2241a-122">Usar o Windows PowerShell para criar trabalhos de transferência do BITS</span><span class="sxs-lookup"><span data-stu-id="2241a-122">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [<span data-ttu-id="2241a-123">Usar os cmdlets do Windows PowerShell do WinRM para gerenciar trabalhos de transferência do BITS</span><span class="sxs-lookup"><span data-stu-id="2241a-123">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [<span data-ttu-id="2241a-124">Usando os cmdlets WMI do Windows PowerShell para gerenciar o BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="2241a-124">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> <span data-ttu-id="2241a-125">A partir do Windows 10, versão 1607, você também pode executar cmdlets do PowerShell e usar o BITSAdmin ou outros aplicativos que usam as [interfaces](bits-interfaces.md) bits de uma linha de comando remota do PowerShell conectada a outro computador (físico ou virtual).</span><span class="sxs-lookup"><span data-stu-id="2241a-125">Starting with Windows 10, version 1607, you can also run PowerShell Cmdlets and use BITSAdmin or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="2241a-126">Esse recurso não está disponível ao usar uma linha de comando [direto do PowerShell](/virtualization/hyper-v-on-windows/user_guide/vmsession) para uma máquina virtual no mesmo computador físico e não está disponível ao usar os cmdlets do WinRM.</span><span class="sxs-lookup"><span data-stu-id="2241a-126">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>
>
> <span data-ttu-id="2241a-127">Um trabalho do BITS criado a partir de uma sessão remota do PowerShell será executado sob o contexto da conta de usuário da sessão e só fará o progresso quando houver pelo menos uma sessão de logon local ativa ou uma sessão remota do PowerShell associada a essa conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="2241a-127">A BITS Job created from a Remote PowerShell session will run under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="2241a-128">Para obter mais informações, consulte [para gerenciar sessões remotas do PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="2241a-128">For more information, see [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md).</span></span>

 

<span data-ttu-id="2241a-129">Esta seção também contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="2241a-129">This section also contains the following topics:</span></span>

-   [<span data-ttu-id="2241a-130">Práticas recomendadas ao usar o BITS</span><span class="sxs-lookup"><span data-stu-id="2241a-130">Best Practices When Using BITS</span></span>](best-practices-when-using-bits.md)
-   [<span data-ttu-id="2241a-131">Enumerando trabalhos na fila de transferência</span><span class="sxs-lookup"><span data-stu-id="2241a-131">Enumerating jobs in the transfer queue</span></span>](enumerating-jobs-in-the-transfer-queue.md)
-   [<span data-ttu-id="2241a-132">Enumerando arquivos em um trabalho</span><span class="sxs-lookup"><span data-stu-id="2241a-132">Enumerating files in a job</span></span>](enumerating-files-in-a-job.md)
-   [<span data-ttu-id="2241a-133">Tratando erros</span><span class="sxs-lookup"><span data-stu-id="2241a-133">Handling errors</span></span>](handling-errors.md)
-   [<span data-ttu-id="2241a-134">Recuperar a resposta de um trabalho de resposta de upload</span><span class="sxs-lookup"><span data-stu-id="2241a-134">Retrieve the reply from an upload-reply job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)

<span data-ttu-id="2241a-135">Para obter o código de exemplo que usa as interfaces BITS, consulte [exemplos e ferramentas do bits](bits-samples-and-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2241a-135">For sample code that uses the BITS interfaces, see [BITS Samples and Tools](bits-samples-and-tools.md).</span></span>

 

 