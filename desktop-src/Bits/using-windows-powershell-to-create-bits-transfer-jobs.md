---
title: Usando o Windows PowerShell para criar trabalhos de transferência do BITS
description: Você pode usar cmdlets do PowerShell para criar trabalhos de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS) síncronos e assíncronos.
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af4879d1fc8f1b25fa0b1b51816432aad3bed8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646401"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a><span data-ttu-id="a478b-103">Usando o Windows PowerShell para criar trabalhos de transferência do BITS</span><span class="sxs-lookup"><span data-stu-id="a478b-103">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>

<span data-ttu-id="a478b-104">Você pode usar cmdlets do PowerShell para criar trabalhos de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS) síncronos e assíncronos.</span><span class="sxs-lookup"><span data-stu-id="a478b-104">You can use PowerShell cmdlets to create synchronous and asynchronous Background Intelligent Transfer Service (BITS) transfer jobs.</span></span>

<span data-ttu-id="a478b-105">Todos os exemplos neste tópico usam o cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="a478b-105">All of the examples in this topic use the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="a478b-106">Para usar o cmdlet, certifique-se de importar o módulo primeiro.</span><span class="sxs-lookup"><span data-stu-id="a478b-106">To use the cmdlet, be sure to import the module first.</span></span> <span data-ttu-id="a478b-107">Para instalar o módulo, execute o seguinte comando: Import-Module BitsTransfer.</span><span class="sxs-lookup"><span data-stu-id="a478b-107">To install the module, run the following command: Import-Module BitsTransfer.</span></span> <span data-ttu-id="a478b-108">Para obter mais informações, digite **Get-Help Start-BitsTransfer** no prompt do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a478b-108">For more information, type **Get-Help Start-BitsTransfer** at the PowerShell prompt.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="a478b-109">Quando você usa cmdlets [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) de dentro de um processo executado em um contexto não interativo, como um serviço do Windows, talvez não seja possível adicionar arquivos aos trabalhos do bits, o que pode resultar em um estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="a478b-109">When you use [\*-BitsTransfer](/previous-versions//dd819413(v=technet.10)) cmdlets from within a process that runs in a noninteractive context, such as a Windows service, you may not be able to add files to BITS jobs, which can result in a suspended state.</span></span> <span data-ttu-id="a478b-110">Para que o trabalho continue, a identidade que foi usada para criar um trabalho de transferência deve estar conectada.</span><span class="sxs-lookup"><span data-stu-id="a478b-110">For the job to proceed, the identity that was used to create a transfer job must be logged on.</span></span> <span data-ttu-id="a478b-111">Por exemplo, ao criar um trabalho BITS em um script do PowerShell que foi executado como um trabalho Agendador de Tarefas, a transferência BITS nunca será concluída, a menos que a configuração de tarefa do Agendador de Tarefas "executar somente quando o usuário estiver conectado" esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="a478b-111">For example, when creating a BITS job in a PowerShell script that was executed as a Task Scheduler job, the BITS transfer will never complete unless the Task Scheduler's task setting "Run only when user is logged on" is enabled.</span></span>

 

-   [<span data-ttu-id="a478b-112">Para criar um trabalho de transferência de BITS síncrono</span><span class="sxs-lookup"><span data-stu-id="a478b-112">To create a synchronous BITS transfer job</span></span>](#to-create-a-synchronous-bits-transfer-job)
-   [<span data-ttu-id="a478b-113">Para criar um trabalho de transferência de BITS síncrono com vários arquivos</span><span class="sxs-lookup"><span data-stu-id="a478b-113">To create a synchronous BITS transfer job with multiple files</span></span>](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [<span data-ttu-id="a478b-114">Para criar um trabalho de transferência de BITS síncrono e especificar credenciais para um servidor remoto</span><span class="sxs-lookup"><span data-stu-id="a478b-114">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [<span data-ttu-id="a478b-115">Para criar um trabalho de transferência de BITS síncrono a partir de um arquivo CSV</span><span class="sxs-lookup"><span data-stu-id="a478b-115">To create a synchronous BITS transfer job from a CSV file</span></span>](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [<span data-ttu-id="a478b-116">Para criar um trabalho de transferência de BITS assíncrono</span><span class="sxs-lookup"><span data-stu-id="a478b-116">To create an asynchronous BITS transfer job</span></span>](#to-create-an-asynchronous-bits-transfer-job)
-   [<span data-ttu-id="a478b-117">Para gerenciar sessões remotas do PowerShell</span><span class="sxs-lookup"><span data-stu-id="a478b-117">To manage PowerShell Remote sessions</span></span>](#to-manage-powershell-remote-sessions)
-   [<span data-ttu-id="a478b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a478b-118">Related topics</span></span>](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a><span data-ttu-id="a478b-119">Para criar um trabalho de transferência de BITS síncrono</span><span class="sxs-lookup"><span data-stu-id="a478b-119">To create a synchronous BITS transfer job</span></span>


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> <span data-ttu-id="a478b-120">O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="a478b-120">The grave-accent character (\`) is used to indicate a line break.</span></span>

 

<span data-ttu-id="a478b-121">No exemplo anterior, os nomes local e remoto do arquivo são especificados nos parâmetros de *origem* e *destino* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a478b-121">In the preceding example, the local and remote names of the file are specified in the *Source* and *Destination* parameters, respectively.</span></span> <span data-ttu-id="a478b-122">O prompt de comando volta a aparecer quando a transferência do arquivo é concluída ou quando ela entra em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="a478b-122">The command prompt returns when the file transfer is complete or when it enters an error state.</span></span>

<span data-ttu-id="a478b-123">O tipo de transferência padrão é download.</span><span class="sxs-lookup"><span data-stu-id="a478b-123">The default transfer type is Download.</span></span> <span data-ttu-id="a478b-124">Quando você carrega arquivos em um local HTTP, o parâmetro *transfertype* deve ser definido para upload.</span><span class="sxs-lookup"><span data-stu-id="a478b-124">When you upload files to an HTTP location, the *TransferType* parameter must be set to Upload.</span></span>

<span data-ttu-id="a478b-125">Como a posição do parâmetro é imposta para o cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) , os nomes de parâmetro não precisam ser especificados para os parâmetros de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="a478b-125">Because parameter position is enforced for the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet, the parameter names do not need to be specified for the Source and Destination parameters.</span></span> <span data-ttu-id="a478b-126">Portanto, esse comando pode ser simplificado da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a478b-126">Therefore, this command can be simplified as follows.</span></span>


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a><span data-ttu-id="a478b-127">Para criar um trabalho de transferência de BITS síncrono com vários arquivos</span><span class="sxs-lookup"><span data-stu-id="a478b-127">To create a synchronous BITS transfer job with multiple files</span></span>


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



<span data-ttu-id="a478b-128">No exemplo anterior, o comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cria um novo trabalho de transferência de bits.</span><span class="sxs-lookup"><span data-stu-id="a478b-128">In the preceding example, the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job.</span></span> <span data-ttu-id="a478b-129">Todos os arquivos são adicionados a esse trabalho e transferidos sequencialmente para o cliente.</span><span class="sxs-lookup"><span data-stu-id="a478b-129">All of the files are added to this job and transferred sequentially to the client.</span></span>

> [!Note]  
> <span data-ttu-id="a478b-130">O caminho de destino não pode usar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="a478b-130">The destination path cannot use wildcard characters.</span></span> <span data-ttu-id="a478b-131">O caminho de destino dá suporte a diretórios relativos, caminhos raiz ou diretórios implícitos (ou seja, o diretório atual).</span><span class="sxs-lookup"><span data-stu-id="a478b-131">The destination path supports relative directories, root paths, or implicit directories (that is, the current directory).</span></span> <span data-ttu-id="a478b-132">Os arquivos de destino não podem ser renomeados usando um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="a478b-132">Destination files cannot be renamed by using a wildcard character.</span></span> <span data-ttu-id="a478b-133">Além disso, as URLs HTTP e HTTPS não funcionam com curingas.</span><span class="sxs-lookup"><span data-stu-id="a478b-133">Additionally, HTTP and HTTPS URLs do not work with wildcards.</span></span> <span data-ttu-id="a478b-134">Os curingas são válidos somente para caminhos UNC e diretórios locais.</span><span class="sxs-lookup"><span data-stu-id="a478b-134">Wildcards are only valid for UNC paths and local directories.</span></span>

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a><span data-ttu-id="a478b-135">Para criar um trabalho de transferência de BITS síncrono e especificar credenciais para um servidor remoto</span><span class="sxs-lookup"><span data-stu-id="a478b-135">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



<span data-ttu-id="a478b-136">No exemplo anterior, um usuário cria um trabalho de transferência de BITS para baixar um arquivo de um servidor que requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="a478b-136">In the preceding example, a user creates a BITS transfer job to download a file from a server that requires authentication.</span></span> <span data-ttu-id="a478b-137">As credenciais do usuário são solicitadas e o parâmetro *Credential* passa um objeto Credential para o cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="a478b-137">The user is prompted for credentials, and the *Credential* parameter passes a credential object to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="a478b-138">O usuário define um proxy explícito e o trabalho de transferência BITS usa apenas os proxies que são definidos pelo parâmetro *ProxyList* .</span><span class="sxs-lookup"><span data-stu-id="a478b-138">The user sets an explicit proxy, and the BITS transfer job uses only the proxies that are defined by the *ProxyList* parameter.</span></span> <span data-ttu-id="a478b-139">O parâmetro *DisplayName* fornece ao trabalho de transferência de bits um nome de exibição exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a478b-139">The *DisplayName* parameter gives the BITS transfer job a unique display name.</span></span>

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a><span data-ttu-id="a478b-140">Para criar um trabalho de transferência de BITS síncrono a partir de um arquivo CSV</span><span class="sxs-lookup"><span data-stu-id="a478b-140">To create a synchronous BITS transfer job from a CSV file</span></span>


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> <span data-ttu-id="a478b-141">O " \| " é o caractere de pipe.</span><span class="sxs-lookup"><span data-stu-id="a478b-141">The "\|" is the pipe character.</span></span>

 

<span data-ttu-id="a478b-142">No exemplo anterior, um usuário cria um trabalho de transferência de BITS que carrega vários arquivos de um cliente.</span><span class="sxs-lookup"><span data-stu-id="a478b-142">In the preceding example, a user creates a BITS transfer job that uploads multiple files from a client.</span></span> <span data-ttu-id="a478b-143">O cmdlet [Import-CSV](/previous-versions//dd347665(v=technet.10)) importa os locais do arquivo de origem e de destino e os canaliza para o comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="a478b-143">The [Import-CSV](/previous-versions//dd347665(v=technet.10)) cmdlet imports the source and destination file locations and pipes them to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command.</span></span> <span data-ttu-id="a478b-144">O comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cria um novo trabalho de transferência de bits para cada arquivo, adiciona os arquivos ao trabalho e os transfere sequencialmente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a478b-144">The [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job for each file, adds the files to the job, and then transfers them sequentially to the server.</span></span>

<span data-ttu-id="a478b-145">O conteúdo do arquivo de Filelist.txt deve estar no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a478b-145">The contents of the Filelist.txt file should be in the following format:</span></span>

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a><span data-ttu-id="a478b-146">Para criar um trabalho de transferência de BITS assíncrono</span><span class="sxs-lookup"><span data-stu-id="a478b-146">To create an asynchronous BITS transfer job</span></span>


```PowerShell
$Job = Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip `
       -Destination d:\temp\downloads\ -Asynchronous

while (($Job.JobState -eq "Transferring") -or ($Job.JobState -eq "Connecting")) `
       { sleep 5;} # Poll for status, sleep for 5 seconds, or perform an action.

Switch($Job.JobState)
{
    "Transferred" {Complete-BitsTransfer -BitsJob $Job}
    "Error" {$Job | Format-List } # List the errors.
    default {"Other action"} #  Perform corrective action.
}

```



<span data-ttu-id="a478b-147">No exemplo anterior, o trabalho de transferência BITS foi atribuído à variável $Job.</span><span class="sxs-lookup"><span data-stu-id="a478b-147">In the preceding example, the BITS transfer job was assigned to the $Job variable.</span></span> <span data-ttu-id="a478b-148">Os arquivos são baixados em sequência.</span><span class="sxs-lookup"><span data-stu-id="a478b-148">The files are downloaded sequentially.</span></span> <span data-ttu-id="a478b-149">Depois que o trabalho de transferência for concluído, os arquivos estarão imediatamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a478b-149">After the transfer job is complete, the files are immediately available.</span></span> <span data-ttu-id="a478b-150">Se $Job. JobState retornar "transferidad", o objeto $Job será enviado ao cmdlet [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="a478b-150">If $Job.JobState returns "Transferred", the $Job object is sent to the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="a478b-151">Se $Job. JobState retornar "Error", o objeto $Job será enviado ao cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) para listar os erros.</span><span class="sxs-lookup"><span data-stu-id="a478b-151">If $Job.JobState returns "Error", the $Job object is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet to list the errors.</span></span>

## <a name="to-manage-powershell-remote-sessions"></a><span data-ttu-id="a478b-152">Para gerenciar sessões remotas do PowerShell</span><span class="sxs-lookup"><span data-stu-id="a478b-152">To manage PowerShell Remote sessions</span></span>

<span data-ttu-id="a478b-153">A partir do Windows 10, versão 1607, você pode executar cmdlets do PowerShell, BITSAdmin ou outros aplicativos que usam as [interfaces](bits-interfaces.md) do bits de uma linha de comando remota do PowerShell conectada a outro computador (físico ou virtual).</span><span class="sxs-lookup"><span data-stu-id="a478b-153">Starting with Windows 10, version 1607, you can run PowerShell Cmdlets, BITSAdmin, or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="a478b-154">Esse recurso não está disponível ao usar uma linha de comando [direto do PowerShell](/virtualization/hyper-v-on-windows/user_guide/vmsession) para uma máquina virtual no mesmo computador físico e não está disponível ao usar os cmdlets do WinRM.</span><span class="sxs-lookup"><span data-stu-id="a478b-154">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>

<span data-ttu-id="a478b-155">Um trabalho do BITS criado a partir de uma sessão remota do PowerShell é executado sob o contexto da conta de usuário da sessão e só fará o progresso quando houver pelo menos uma sessão de logon local ativa ou uma sessão remota do PowerShell associada a essa conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="a478b-155">A BITS Job created from a Remote PowerShell session runs under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="a478b-156">Você pode usar as PSSessions persistentes do PowerShell para executar comandos remotos sem a necessidade de manter uma janela do PowerShell aberta para cada trabalho para continuar a progredir, conforme descrito em [noções básicas do PowerShell: gerenciamento remoto](https://techgenix.com/remote-management-powershell-part1/).</span><span class="sxs-lookup"><span data-stu-id="a478b-156">You can use PowerShell's persistent PSSessions to run remote commands without the need to keep a PowerShell window open for each job to continue making progress, as described in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span></span>

-   <span data-ttu-id="a478b-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) cria uma sessão do PowerShell remota persistente.</span><span class="sxs-lookup"><span data-stu-id="a478b-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) creates a persistent Remote PowerShell session.</span></span> <span data-ttu-id="a478b-158">Depois de criados, os objetos PSSession persistem no computador remoto até que sejam explicitamente excluídos.</span><span class="sxs-lookup"><span data-stu-id="a478b-158">Once created, the PSSession objects persist in the remote machine until explicitly deleted.</span></span> <span data-ttu-id="a478b-159">Todos os trabalhos do BITS iniciados em uma sessão ativa farão o andamento da transferência de dados, mesmo depois que o cliente tiver se desconectado da sessão.</span><span class="sxs-lookup"><span data-stu-id="a478b-159">Any BITS jobs initiated in an active session will make progress transferring data, even after the client has disconnected from the session.</span></span>
-   <span data-ttu-id="a478b-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) desconecta o computador cliente de uma sessão remota do PowerShell e o estado da sessão continua a ser mantido pelo computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a478b-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnects the client machine from a Remote PowerShell session and the session’s state continues to be maintained by the remote machine.</span></span> <span data-ttu-id="a478b-161">O mais importante é que os processos da sessão remota continuarão em execução, e os trabalhos do BITS continuarão a progredir.</span><span class="sxs-lookup"><span data-stu-id="a478b-161">Most importantly, the remote session’s processes will continue executing, and BITS jobs will continue to make progress.</span></span> <span data-ttu-id="a478b-162">O computador cliente pode até mesmo reinicializar e/ou desligar depois de chamar Disconnect-PSSession.</span><span class="sxs-lookup"><span data-stu-id="a478b-162">The client machine can even reboot and/or turn off after calling Disconnect-PSSession.</span></span>
-   <span data-ttu-id="a478b-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) reconecta o computador cliente a uma sessão remota do PowerShell ativa.</span><span class="sxs-lookup"><span data-stu-id="a478b-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) re-connects the client machine to an active Remote PowerShell session.</span></span>
-   <span data-ttu-id="a478b-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) destrói uma sessão remota do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a478b-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) tears down a Remote PowerShell session.</span></span>

<span data-ttu-id="a478b-165">O exemplo a seguir mostra como usar o PowerShell remoto para trabalhar com trabalhos de transferência de BITS assíncronos de uma maneira que permite que o trabalho continue a progredir mesmo quando você não estiver conectado ativamente à sessão remota.</span><span class="sxs-lookup"><span data-stu-id="a478b-165">The example below shows how to use PowerShell Remote to work with asynchronous BITS transfer jobs in a way that allows the job to continue to make progress even when you are not actively connected to the remote session.</span></span>


```PowerShell
# Establish a PowerShell Remote session in Server01 with name 'MyRemoteSession'
New-PSSession -ComputerName Server01 -Name MyRemoteSession -Credential Domain01\User01

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# While running in the context of the PowerShell Remote session, start a new BITS transfer
Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip -Destination c:\temp\downloads\ -Asynchronous

# Exit the PowerShell Remote session's context
Exit-PSSession

# Disconnect the 'MyRemoteSession' PowerShell Remote session from the current PowerShell window
# After this command, it is safe to close the current PowerShell window and turn off the local machine
Disconnect-PSSession -Name MyRemoteSession


# The commands below can be executed from a different PowerShell window, even after rebooting the local machine
# Connect the 'MyRemoteSession' PowerShell Remote session to the current PowerShell window
Connect-PSSession -ComputerName Server01 -Name MyRemoteSession

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# Manage BITS transfers on the remote machine via Complete-BitsTransfer, Remove-BitsTransfer, etc.

# Exit the PowerShell Remote session's context
Exit-PSSession

# Destroy the 'MyRemoteSession' PowerShell Remote session when no longer needed
Remove-PSSession -Name MyRemoteSession
```



## <a name="related-topics"></a><span data-ttu-id="a478b-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a478b-166">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a478b-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="a478b-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="a478b-168">[Concluir-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="a478b-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span></span>
</dt> </dl>

 

 
