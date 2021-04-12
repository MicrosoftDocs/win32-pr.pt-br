---
title: Usar os cmdlets do Windows PowerShell do WinRM para gerenciar trabalhos de transferência do BITS
description: Gerenciamento Remoto do Windows cmdlets do PowerShell podem gerenciar trabalhos de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500982"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a><span data-ttu-id="74634-103">Usar os cmdlets do Windows PowerShell do WinRM para gerenciar trabalhos de transferência do BITS</span><span class="sxs-lookup"><span data-stu-id="74634-103">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>

<span data-ttu-id="74634-104">Gerenciamento Remoto do Windows cmdlets do PowerShell podem gerenciar trabalhos de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS).</span><span class="sxs-lookup"><span data-stu-id="74634-104">Windows Remote Management PowerShell cmdlets can manage Background Intelligent Transfer Service (BITS) transfer jobs.</span></span> <span data-ttu-id="74634-105">Para obter mais informações sobre gerenciamento remoto de BITS, consulte [provedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider) e [classes de provedor bits]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74634-105">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

<span data-ttu-id="74634-106">Os exemplos a seguir exigem o [provedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider).</span><span class="sxs-lookup"><span data-stu-id="74634-106">The following examples require the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider).</span></span> <span data-ttu-id="74634-107">O provedor de BITS está disponível após a instalação do BITS Compact Server.</span><span class="sxs-lookup"><span data-stu-id="74634-107">The BITS provider is available after the BITS Compact server is installed.</span></span> <span data-ttu-id="74634-108">Para obter informações sobre como instalar o Compact Server, consulte a documentação do [bits Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="74634-108">For information about installing the Compact server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="74634-109">Criar um trabalho de transferência de BITS.</span><span class="sxs-lookup"><span data-stu-id="74634-109">Create a BITS transfer job.</span></span>

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="74634-110">O cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita as credenciais do usuário para se conectar ao computador remoto e atribui as credenciais ao objeto $cred.</span><span class="sxs-lookup"><span data-stu-id="74634-110">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="74634-111">O cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cria o trabalho de transferência bits em CLIENT1 criando uma instância da classe [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) e usando as informações na tabela de hash definida no parâmetro *ValueSet* .</span><span class="sxs-lookup"><span data-stu-id="74634-111">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cmdlet creates the BITS transfer job on Client1 by creating an instance of the [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) class and using the information in the hash table defined in the *Valueset* parameter.</span></span> <span data-ttu-id="74634-112">O parâmetro *ValueSet* especifica as informações necessárias para popular os parâmetros do método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="74634-112">The *Valueset* parameter specifies the information needed to populate the parameters of the [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span> <span data-ttu-id="74634-113">No exemplo anterior, o usuário define o parâmetro de *tipo* como 0 (download).</span><span class="sxs-lookup"><span data-stu-id="74634-113">In the preceding example, the user is sets the *Type* parameter to 0 (download).</span></span> <span data-ttu-id="74634-114">O usuário também especifica o nome dos arquivos remotos e locais para o trabalho de download.</span><span class="sxs-lookup"><span data-stu-id="74634-114">The user also specifies the name of both the remote and local files for the download job.</span></span> <span data-ttu-id="74634-115">Para obter mais informações sobre como criar trabalhos de transferência do BITS e obter informações detalhadas sobre parâmetros, consulte método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="74634-115">For more information about creating BITS transfer jobs and for detailed information about parameters, see [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span>

    <span data-ttu-id="74634-116">O cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) atribui o resultado à variável $Result.</span><span class="sxs-lookup"><span data-stu-id="74634-116">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet assigns the result to the $result variable.</span></span>

    > [!Note]  
    > <span data-ttu-id="74634-117">O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="74634-117">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="74634-118">Defina a prioridade do trabalho de transferência de BITS.</span><span class="sxs-lookup"><span data-stu-id="74634-118">Set the Priority of the BITS transfer job.</span></span>

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="74634-119">O cmdlet [set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) altera a nova prioridade do trabalho de transferência de bits para 0 (**BG \_ \_ \_ primeiro plano de prioridade do trabalho**).</span><span class="sxs-lookup"><span data-stu-id="74634-119">The [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cmdlet changes the new BITS transfer job priority to 0 (**BG\_JOB\_PRIORITY\_FOREGROUND**).</span></span> <span data-ttu-id="74634-120">Para obter mais informações sobre os níveis de prioridade, consulte a enumeração de [**\_ \_ prioridade de trabalho BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .</span><span class="sxs-lookup"><span data-stu-id="74634-120">For more information about the priority levels, see the [**BG\_JOB\_PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) enumeration.</span></span>

3.  <span data-ttu-id="74634-121">Retome o trabalho de transferência do BITS.</span><span class="sxs-lookup"><span data-stu-id="74634-121">Resume the BITS transfer job.</span></span>

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="74634-122">O cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , que define o estado do trabalho como 2 (retomar o trabalho).</span><span class="sxs-lookup"><span data-stu-id="74634-122">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method, which sets the job state to 2 (Resume the Job).</span></span>

4.  <span data-ttu-id="74634-123">Gerenciar o trabalho de transferência de BITS.</span><span class="sxs-lookup"><span data-stu-id="74634-123">Manage the BITS transfer job.</span></span>

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    <span data-ttu-id="74634-124">O exemplo anterior é um script para sondar o status do trabalho e tomar uma ação com base no status.</span><span class="sxs-lookup"><span data-stu-id="74634-124">The preceding example is a script to poll the status of the job and take an action based on the status.</span></span> <span data-ttu-id="74634-125">As seguintes ações são possíveis:</span><span class="sxs-lookup"><span data-stu-id="74634-125">The following actions are possible:</span></span>

    -   <span data-ttu-id="74634-126">Se $result. O estado é 4 **( \_ BG \_ \_ erro de estado do trabalho**), o cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e cancela o trabalho.</span><span class="sxs-lookup"><span data-stu-id="74634-126">If $result.State is 4 (**BG\_JOB\_STATE\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="74634-127">Se $result. O estado é 5 (o **BG \_ \_ \_ \_ erro transitório do estado do trabalho**), o cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e cancela o trabalho.</span><span class="sxs-lookup"><span data-stu-id="74634-127">If $result.State is 5 (**BG\_JOB\_STATE\_TRANSIENT\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="74634-128">Se $result. O estado é 6 (**BG \_ estado do trabalho \_ \_ transferido**), o cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e define o estado como Complete.</span><span class="sxs-lookup"><span data-stu-id="74634-128">If $result.State is 6 (**BG\_JOB\_STATE\_TRANSFERRED**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and sets the state to complete.</span></span>

    <span data-ttu-id="74634-129">Para obter mais informações sobre os Estados de trabalho, consulte a enumeração de [**\_ \_ estado do trabalho BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .</span><span class="sxs-lookup"><span data-stu-id="74634-129">For more information about job states, see the [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74634-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74634-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="74634-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="74634-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

[<span data-ttu-id="74634-132">Invoke-WSManAction</span><span class="sxs-lookup"><span data-stu-id="74634-132">Invoke-WsmanAction</span></span>](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[<span data-ttu-id="74634-133">Set-WsmanInstance</span><span class="sxs-lookup"><span data-stu-id="74634-133">Set-WsmanInstance</span></span>](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
