---
title: Melhorias na infraestrutura do Shell Remoto
description: Windows O Gerenciamento Remoto versão 2.0 (WinRM 2.0) oferece muitas melhorias de infraestrutura de shell remoto.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf88a472319b4b4677992f97509a3603cfe4a32f272388caf9db100b6e7457ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121656"
---
# <a name="remote-shell-infrastructure-improvements"></a>Melhorias na infraestrutura do Shell Remoto

Windows O Gerenciamento Remoto versão 2.0 (WinRM 2.0) oferece muitas melhorias de infraestrutura de shell remoto. Os tópicos a seguir descrevem esses aprimoramentos em detalhes:

-   [Suporte a vários saltos](multi-hop-support.md)
-   [Gerenciamento de cotas para shells remotos](quotas.md)

Uma das melhorias na infraestrutura de shell remoto do WinRM é a adição de um gerenciador de shell mais robusto que mantém informações de shell específicas do usuário. Os usuários do WinRM podem criar shells em computadores remotos para executar comandos ou scripts. Além disso, os usuários podem criar vários shells em um computador. Os usuários e administradores precisam da capacidade de gerenciar shells. Os usuários podem enumerar, obter e excluir os shells que eles criaram. Os administradores podem enumerar todos os shells ativos e recuperar detalhes sobre shells específicos em um host local ou remoto. Os administradores também podem excluir qualquer shell ativo em um host local ou remoto.

Quando um usuário ou administrador enumera os shells ativos, as informações a seguir podem ser retornadas pelo serviço WinRM.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId
</dt> <dd>

Especifica o identificador exclusivo para o shell.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variáveis de ambiente
</dt> <dd>

Especifica as variáveis de ambiente definidas pelo usuário.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>Workingdirectory
</dt> <dd>

Especifica o diretório inicial do shell.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>Resourceuri
</dt> <dd>

Especifica o URI do recurso para a operação de shell. O URI do recurso pode ser usado para recuperar a configuração de plug-in específica da instância do shell.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>Idletimeout
</dt> <dd>

Especifica a duração máxima, em milissegundos, que o shell permanecerá aberto sem nenhuma solicitação.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams
</dt> <dd>

Especifica os fluxos de entrada para o shell.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams
</dt> <dd>

Especifica os fluxos de saída para o shell.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Hora de criação do shell
</dt> <dd>

Especifica o timestamp de criação para o shell.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime
</dt> <dd>

Especifica a duração, em milissegundos, de que o shell está ocioso.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>Userid
</dt> <dd>

Especifica a ID de usuário.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nome do host ou endereço IP
</dt> <dd>

Especifica o nome do host ou o endereço IP do computador que criou o shell.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Uso de memória do shell
</dt> <dd>

Especifica a quantidade de memória que foi usada pelo shell.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Número de processos
</dt> <dd>

Especifica o número de processos que foram criados pelo shell.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Enumerando um shell em um host local

O comando a seguir demonstra como usar o utilitário winrm para enumerar shells em um cliente WinRM: **shell de enumeração winrm**.

O exemplo baseado em texto a seguir exibe a saída para enumeração de shell:

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

Para obter mais informações, consulte a ajuda online fornecida executando o seguinte comando: **enumerar winrm -?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Recuperando informações sobre um shell específico

Um administrador ou usuário também pode usar o identificador ShellId para recuperar informações sobre o shell. O comando a seguir demonstra como usar o utilitário winrm para obter informações sobre um shell específico: **winrm get shell? ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.

O exemplo baseado em texto a seguir exibe a saída para informações de shell:

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

Para obter mais informações, consulte a ajuda online fornecida pelo seguinte comando: **winrm get -?**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a vários saltos](multi-hop-support.md)
</dt> <dt>

[Gerenciamento de cotas para shells remotos](quotas.md)
</dt> <dt>

[Referência gerenciada para WS-Management comandos do PowerShell](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




