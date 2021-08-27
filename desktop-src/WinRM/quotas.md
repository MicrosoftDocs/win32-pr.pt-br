---
title: Gerenciamento de cota para shells remotos
description: O gerenciamento de cotas permite que os usuários gerenciem recursos do sistema com mais eficiência.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8cfa177d6f09552238471ff29d81d0ac0b7351
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883216"
---
# <a name="quota-management-for-remote-shells"></a>Gerenciamento de cota para shells remotos

O gerenciamento de cotas permite que os usuários gerenciem recursos do sistema com mais eficiência. Windows O gerenciamento remoto (WinRM) adicionou um conjunto específico de cotas que fornecem uma melhor qualidade de serviço, ajudam a evitar problemas de negação de serviço e aloca recursos de servidor para usuários simultâneos. o conjunto de cotas do WinRM é baseado na infraestrutura de cota que é implementada para o serviço de Serviços de Informações da Internet (IIS).

A implementação de cotas ajudará a evitar a degradação do desempenho e a negação de problemas de serviço fazendo o seguinte:

-   Limitando o número de shells e processos de shell que um usuário pode criar
-   Limitando o número máximo de usuários simultâneos
-   Gerenciando a quantidade de memória alocada para um shell
-   Definindo um tempo limite para shells que estão inativos

## <a name="quota-settings"></a>Configurações de cota

As cotas a seguir precisam ser impostas para o gerenciamento remoto de Shell. Essas cotas podem ser configuradas por meio do utilitário WinRM ou por meio de configurações de Política de Grupo. Configurações configurado por um Política de Grupo substituir as cotas definidas pelo utilitário winrm. para obter mais informações sobre como definir políticas de grupo para o WinRM, consulte [instalação e configuração para Gerenciamento Remoto do Windows](installation-and-configuration-for-windows-remote-management.md).

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

O tempo máximo em milissegundos antes que um shell remoto inativo seja excluído. O padrão é 180000 milissegundos. O tempo mínimo é de 1000 milissegundos.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

O número máximo de processos permitidos por shell, incluindo os processos filho do Shell. O padrão é 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

A quantidade máxima de memória alocada por shell, incluindo os processos filho do Shell. O padrão é 1024 MB.

> [!Note]  
> O comportamento não será suportado se MaxMemoryPerShellMB for definido como um valor menor que o padrão.

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

O número máximo de shells por usuário. O padrão é 30.

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

O número máximo de usuários simultâneos que podem abrir shells. O padrão é 10.

</dd> </dl>

## <a name="deprecated-quotas"></a>Cotas preteridas

O WinRM 2,0 define a cota de MaxShellRunTime como somente leitura. Alterar o valor dessa cota não terá nenhum efeito nos shells remotos.

## <a name="retrieving-quota-configuration-information"></a>Recuperando informações de configuração de cota

Para verificar as definições de configuração de cota, digite **WinRM Get WinRM/config**.

O trecho a seguir é um exemplo baseado em texto de uma configuração do WinRM com as configurações de cota padrão.

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a>Configurando cotas do Shell

As cotas podem ser definidas por meio de uma configuração de Política de Grupo ou manualmente. para obter mais informações sobre definições de configuração específicas, consulte [instalação e configuração para Gerenciamento Remoto do Windows](installation-and-configuration-for-windows-remote-management.md).

**Para definir uma cota com Política de Grupo**

1.  Abra uma janela de Prompt de comando como administrador.
2.  No prompt de comando, digite **gpedit. msc**. A janela **Editor de objeto de política de grupo** é aberta.
3.  localize o **Gerenciamento Remoto do Windows** e Windows objetos de Política de Grupo do **Shell remoto** (GPO) em **configuração do computador \\ Modelos Administrativos \\ componentes Windows**.
4.  Na guia **estendida** , selecione uma configuração para ver uma descrição. Clique duas vezes em uma configuração para editá-la.

**Para definir uma cota manualmente**

1.  Abra uma janela de Prompt de comando como administrador.
2.  No prompt de comando, digite **WinRM Set WinRM/config/WinRS ' @ {**_&lt; quota &gt;_*_= "_*_&lt; valor &gt;_*_"} '_*

Por exemplo, para aumentar o número máximo de shells por usuário de 5 para 7, digite **WinRM Set WinRM/config/WinRS ' @ {MaxShellsPerUser = "7"} '**.

 

 




