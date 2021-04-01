---
description: Como o UAC (controle de conta de usuário) no Windows Vista restringe os privilégios durante uma instalação, os desenvolvedores de Windows Installer pacotes não devem pressupor que sua instalação sempre tenha acesso a todas as partes do sistema.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Diretrizes para pacotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db228c2dff443d421ddc089074f0fcce6ae93e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828991"
---
# <a name="guidelines-for-packages"></a>Diretrizes para pacotes

Como o UAC ( [*controle de conta de usuário*](u-gly.md) ) no Windows Vista restringe os privilégios durante uma instalação, os desenvolvedores de Windows Installer pacotes não devem pressupor que sua instalação sempre tenha acesso a todas as partes do sistema.

Um pacote do instalador que pode ser implantado com êxito em usuários padrão por meio de [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page) deve, na maioria dos casos, também funcionar com o UAC no Windows Vista. As exceções a isso podem ocorrer se a [tabela InstallUISequence](installuisequence-table.md) contiver a [ação LaunchConditions](launchconditions-action.md) ou a [tabela LaunchCondition](launchcondition-table.md) contiver uma condição baseada na [Propriedade Privileged](privileged.md). Os desenvolvedores de pacotes Windows Installer devem, portanto, aderir às diretrizes a seguir para garantir que seu pacote funcione com o UAC e o Windows Vista.

-   Ao incluir uma condição de [*contexto de instalação*](i-gly.md) com uma ação na [tabela InstallUISequence](installuisequence-table.md), use uma instrução condicional com base na [Propriedade Privileged](privileged.md). Não use uma condição com base na propriedade [**AdminUser**](adminuser.md) .
-   Ao incluir o contexto de instalação com as condições de inicialização de instalação, use um [tipo de ação personalizada 19](custom-action-type-19.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md) e torne a ação personalizada condicional sobre a [Propriedade Privileged](privileged.md). Não use uma ação na [tabela LaunchCondition](launchcondition-table.md) com uma condição baseada na [Propriedade AdminUser](adminuser.md) ou na propriedade privilegiada.
-   Para ler ou modificar a configuração do sistema, use uma [ação personalizada de execução adiada](deferred-execution-custom-actions.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md). Não use ações personalizadas de execução imediata na [tabela InstallUISequence](installuisequence-table.md) para modificar a configuração do sistema.
-   Para modificar partes do sistema que não são específicas do usuário, use uma ação personalizada adiada na [tabela InstallExecuteSequence](installexecutesequence-table.md). Você deve incluir o bit msidbCustomActionTypeNoImpersonate no tipo de ação personalizada.
-   Omita o bit 3 do valor da propriedade de resumo [**contagem de palavras**](word-count-summary.md) para indicar que o pacote pode ser necessário para ser elevado. Não inclua esse bit, a menos que privilégios elevados não sejam necessários para instalar este pacote.
-   Inclua um manifesto com o nível de execução solicitado do aplicativo.
-   Inclua um certificado na tabela [MsiPatchCertificate](msipatchcertificate-table.md) do pacote original e assine todos os patches com o mesmo certificado.
-   Se forem necessários privilégios elevados para instalar um pacote de Windows Installer, o autor do pacote deverá incluir o atributo [ElevationShield](elevationshield-attribute.md) para o [controle de supressão](pushbutton-control.md) usado para iniciar a instalação. Isso alertará o usuário que clicar no botão exibirá a caixa de diálogo UAC solicitando autorização do administrador para continuar a instalação.
-   Defina a propriedade [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) como 1 para indicar ao Windows Installer que o pacote foi criado e testado para estar em conformidade com o UAC no Windows Vista. Se essa propriedade não for definida, o instalador determinará se o pacote está em conformidade com o UAC.

Fora do [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page), a seguinte verificação de conformidade com o UAC pode ser usada no Windows XP.

**Para verificar a conformidade do UAC fora do Política de Grupo**

1.  Faça logon no computador como administrador.
2.  Anuncie o pacote para uma instalação por máquina:

    **msiexec/jm** *package.msi*

3.  Faça logoff do computador.
4.  Faça logon no computador como usuário padrão.
5.  Tentativa de instalar o pacote anunciado:

    **msiexec/i** *package.msi*

6.  Na maioria dos casos, se a instalação for bem-sucedida, o pacote será compatível com o UAC.
7.  Defina a propriedade [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) no pacote como 1.
8.  Teste a instalação correta do pacote usando o Windows Vista.

 

 
