---
title: Usar os cmdlets do Windows PowerShell do WinRM para gerenciar trabalhos de transferência do BITS
description: Windows Os cmdlets do PowerShell de gerenciamento remoto podem gerenciar trabalhos de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f24f4776d8a8431ac8c910fb8145633961bf353721698f8c3e5b4737ee0a1c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004636"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Usar os cmdlets do Windows PowerShell do WinRM para gerenciar trabalhos de transferência do BITS

Windows Os cmdlets do PowerShell de gerenciamento remoto podem gerenciar trabalhos de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS). Para obter mais informações sobre gerenciamento remoto de BITS, consulte [provedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider) e [classes de provedor bits]( /previous-versions//dd904507(v=vs.85)).

Os exemplos a seguir exigem o [provedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider). O provedor de BITS está disponível após a instalação do BITS Compact Server. Para obter informações sobre como instalar o Compact Server, consulte a documentação do [bits Compact Server](bits-compact-server.md) .

1.  Criar um trabalho de transferência de BITS.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    O cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita as credenciais do usuário para se conectar ao computador remoto e atribui as credenciais ao objeto $cred.

    O cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cria o trabalho de transferência bits em CLIENT1 criando uma instância da classe [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) e usando as informações na tabela de hash definida no parâmetro *ValueSet* . O parâmetro *ValueSet* especifica as informações necessárias para popular os parâmetros do método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) . No exemplo anterior, o usuário define o parâmetro de *tipo* como 0 (download). O usuário também especifica o nome dos arquivos remotos e locais para o trabalho de download. Para obter mais informações sobre como criar trabalhos de transferência do BITS e obter informações detalhadas sobre parâmetros, consulte método [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .

    O cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) atribui o resultado à variável $Result.

    > [!Note]  
    > O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.

     

2.  Defina a prioridade do trabalho de transferência de BITS.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    O cmdlet [set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) altera a nova prioridade do trabalho de transferência de bits para 0 (**BG \_ \_ \_ primeiro plano de prioridade do trabalho**). Para obter mais informações sobre os níveis de prioridade, consulte a enumeração de [**\_ \_ prioridade de trabalho BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .

3.  Retome o trabalho de transferência do BITS.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    O cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , que define o estado do trabalho como 2 (retomar o trabalho).

4.  Gerenciar o trabalho de transferência de BITS.

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

    

    O exemplo anterior é um script para sondar o status do trabalho e tomar uma ação com base no status. As seguintes ações são possíveis:

    -   Se $result. O estado é 4 **( \_ BG \_ \_ erro de estado do trabalho**), o cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e cancela o trabalho.
    -   Se $result. O estado é 5 (o **BG \_ \_ \_ \_ erro transitório do estado do trabalho**), o cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e cancela o trabalho.
    -   Se $result. O estado é 6 (**BG \_ estado do trabalho \_ \_ transferido**), o cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) chama o método [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) e define o estado como Complete.

    Para obter mais informações sobre os Estados de trabalho, consulte a enumeração de [**\_ \_ estado do trabalho BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
