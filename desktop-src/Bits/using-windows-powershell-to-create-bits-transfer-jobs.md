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
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>Usando o Windows PowerShell para criar trabalhos de transferência do BITS

Você pode usar cmdlets do PowerShell para criar trabalhos de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS) síncronos e assíncronos.

Todos os exemplos neste tópico usam o cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . Para usar o cmdlet, certifique-se de importar o módulo primeiro. Para instalar o módulo, execute o seguinte comando: Import-Module BitsTransfer. Para obter mais informações, digite **Get-Help Start-BitsTransfer** no prompt do PowerShell.

> [!IMPORTANT]
>
> Quando você usa cmdlets [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) de dentro de um processo executado em um contexto não interativo, como um serviço do Windows, talvez não seja possível adicionar arquivos aos trabalhos do bits, o que pode resultar em um estado suspenso. Para que o trabalho continue, a identidade que foi usada para criar um trabalho de transferência deve estar conectada. Por exemplo, ao criar um trabalho BITS em um script do PowerShell que foi executado como um trabalho Agendador de Tarefas, a transferência BITS nunca será concluída, a menos que a configuração de tarefa do Agendador de Tarefas "executar somente quando o usuário estiver conectado" esteja habilitada.

 

-   [Para criar um trabalho de transferência de BITS síncrono](#to-create-a-synchronous-bits-transfer-job)
-   [Para criar um trabalho de transferência de BITS síncrono com vários arquivos](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [Para criar um trabalho de transferência de BITS síncrono e especificar credenciais para um servidor remoto](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [Para criar um trabalho de transferência de BITS síncrono a partir de um arquivo CSV](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [Para criar um trabalho de transferência de BITS assíncrono](#to-create-an-asynchronous-bits-transfer-job)
-   [Para gerenciar sessões remotas do PowerShell](#to-manage-powershell-remote-sessions)
-   [Tópicos relacionados](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>Para criar um trabalho de transferência de BITS síncrono


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.

 

No exemplo anterior, os nomes local e remoto do arquivo são especificados nos parâmetros de *origem* e *destino* , respectivamente. O prompt de comando volta a aparecer quando a transferência do arquivo é concluída ou quando ela entra em um estado de erro.

O tipo de transferência padrão é download. Quando você carrega arquivos em um local HTTP, o parâmetro *transfertype* deve ser definido para upload.

Como a posição do parâmetro é imposta para o cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) , os nomes de parâmetro não precisam ser especificados para os parâmetros de origem e destino. Portanto, esse comando pode ser simplificado da seguinte maneira.


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>Para criar um trabalho de transferência de BITS síncrono com vários arquivos


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



No exemplo anterior, o comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cria um novo trabalho de transferência de bits. Todos os arquivos são adicionados a esse trabalho e transferidos sequencialmente para o cliente.

> [!Note]  
> O caminho de destino não pode usar caracteres curinga. O caminho de destino dá suporte a diretórios relativos, caminhos raiz ou diretórios implícitos (ou seja, o diretório atual). Os arquivos de destino não podem ser renomeados usando um caractere curinga. Além disso, as URLs HTTP e HTTPS não funcionam com curingas. Os curingas são válidos somente para caminhos UNC e diretórios locais.

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>Para criar um trabalho de transferência de BITS síncrono e especificar credenciais para um servidor remoto


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



No exemplo anterior, um usuário cria um trabalho de transferência de BITS para baixar um arquivo de um servidor que requer autenticação. As credenciais do usuário são solicitadas e o parâmetro *Credential* passa um objeto Credential para o cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . O usuário define um proxy explícito e o trabalho de transferência BITS usa apenas os proxies que são definidos pelo parâmetro *ProxyList* . O parâmetro *DisplayName* fornece ao trabalho de transferência de bits um nome de exibição exclusivo.

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>Para criar um trabalho de transferência de BITS síncrono a partir de um arquivo CSV


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> O " \| " é o caractere de pipe.

 

No exemplo anterior, um usuário cria um trabalho de transferência de BITS que carrega vários arquivos de um cliente. O cmdlet [Import-CSV](/previous-versions//dd347665(v=technet.10)) importa os locais do arquivo de origem e de destino e os canaliza para o comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . O comando [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cria um novo trabalho de transferência de bits para cada arquivo, adiciona os arquivos ao trabalho e os transfere sequencialmente para o servidor.

O conteúdo do arquivo de Filelist.txt deve estar no seguinte formato:

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>Para criar um trabalho de transferência de BITS assíncrono


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



No exemplo anterior, o trabalho de transferência BITS foi atribuído à variável $Job. Os arquivos são baixados em sequência. Depois que o trabalho de transferência for concluído, os arquivos estarão imediatamente disponíveis. Se $Job. JobState retornar "transferidad", o objeto $Job será enviado ao cmdlet [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .

Se $Job. JobState retornar "Error", o objeto $Job será enviado ao cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) para listar os erros.

## <a name="to-manage-powershell-remote-sessions"></a>Para gerenciar sessões remotas do PowerShell

A partir do Windows 10, versão 1607, você pode executar cmdlets do PowerShell, BITSAdmin ou outros aplicativos que usam as [interfaces](bits-interfaces.md) do bits de uma linha de comando remota do PowerShell conectada a outro computador (físico ou virtual). Esse recurso não está disponível ao usar uma linha de comando [direto do PowerShell](/virtualization/hyper-v-on-windows/user_guide/vmsession) para uma máquina virtual no mesmo computador físico e não está disponível ao usar os cmdlets do WinRM.

Um trabalho do BITS criado a partir de uma sessão remota do PowerShell é executado sob o contexto da conta de usuário da sessão e só fará o progresso quando houver pelo menos uma sessão de logon local ativa ou uma sessão remota do PowerShell associada a essa conta de usuário. Você pode usar as PSSessions persistentes do PowerShell para executar comandos remotos sem a necessidade de manter uma janela do PowerShell aberta para cada trabalho para continuar a progredir, conforme descrito em [noções básicas do PowerShell: gerenciamento remoto](https://techgenix.com/remote-management-powershell-part1/).

-   [New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) cria uma sessão do PowerShell remota persistente. Depois de criados, os objetos PSSession persistem no computador remoto até que sejam explicitamente excluídos. Todos os trabalhos do BITS iniciados em uma sessão ativa farão o andamento da transferência de dados, mesmo depois que o cliente tiver se desconectado da sessão.
-   [Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) desconecta o computador cliente de uma sessão remota do PowerShell e o estado da sessão continua a ser mantido pelo computador remoto. O mais importante é que os processos da sessão remota continuarão em execução, e os trabalhos do BITS continuarão a progredir. O computador cliente pode até mesmo reinicializar e/ou desligar depois de chamar Disconnect-PSSession.
-   [Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) reconecta o computador cliente a uma sessão remota do PowerShell ativa.
-   [Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) destrói uma sessão remota do PowerShell.

O exemplo a seguir mostra como usar o PowerShell remoto para trabalhar com trabalhos de transferência de BITS assíncronos de uma maneira que permite que o trabalho continue a progredir mesmo quando você não estiver conectado ativamente à sessão remota.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[Concluir-BitsTransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
