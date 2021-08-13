---
title: Considerações de segurança para tecnologias assistenciais
description: tecnologias assistenciais são aplicativos executados no Windows desktop e ajudam os usuários de acessibilidade a interagir com o sistema operacional e outros aplicativos em execução no computador, incluindo aplicativos na nova interface do usuário do Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- atributo uiAccess
- Automação da interface do usuário, atributo uiAccess
- segurança, atributo uiAccess
- marca de requestedExecutionLevel
- Automação da interface do usuário, marca requestedExecutionLevel
- Automação da interface do usuário, considerações de segurança
- Automação da interface do usuário, arquivos de manifesto
- arquivos de manifesto
- controle de conta de usuário
- segurança, controle de conta de usuário
- segurança, arquivos de manifesto
- segurança, marca requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88ba97be98795be3725efaf76cf01297d7a00a2bb0112b0211581b3e0e4035f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563959"
---
# <a name="security-considerations-for-assistive-technologies"></a>Considerações de segurança para tecnologias assistenciais

tecnologias assistenciais são aplicativos executados na área de trabalho do Windows e ajudam os usuários de acessibilidade a interagir com o sistema operacional e outros aplicativos em execução no computador, incluindo aplicativos na nova interface do usuário do Windows. Os aplicativos de tecnologia assistencial funcionam recuperando informações do sistema operacional e de outros aplicativos e, em seguida, apresentando as informações de uma maneira que possa ser acessada pelo usuário. Um aplicativo de tecnologia assistencial também pode "impulsionar" de forma programática o sistema operacional e outros aplicativos com base na entrada do usuário.

A natureza dos aplicativos de tecnologia assistencial exige que eles entrem em limites de processo e que tenham acesso a processos executados em um nível de integridade mais alto (IL) do que em si. (Um aplicativo de tecnologia assistencial é executado em IL médio.) por exemplo, quando o usuário tenta executar uma tarefa que exige privilégios administrativos, Windows apresenta uma caixa de diálogo solicitando que o usuário tenha consentimento para continuar. Essa caixa de diálogo é executada em um IL superior para protegê-la da comunicação entre processos, para que o software mal-intencionado não possa simular a entrada do usuário. Da mesma forma, a tela de logon da área de trabalho é executada em um IL superior para impedir que ele seja acessado por outros processos.

Aplicativos de tecnologia assistencial normalmente precisam de acesso aos elementos de interface do usuário do sistema protegido ou a outros processos que podem estar sendo executados em um nível de privilégio mais alto. Portanto, os aplicativos de tecnologia assistencial devem ser confiáveis pelo sistema e devem ser executados com privilégios especiais.

Para obter acesso a processos de IL mais altos, um aplicativo de tecnologia assistencial deve definir o sinalizador UIAccess no manifesto do aplicativo e ser iniciado por um usuário com privilégios de administrador.

> [!NOTE]
> Os privilégios de acesso são restritos da seguinte maneira:
>
> - Um aplicativo que não tem o UIAccess no manifesto começa com IL médio e não pode acessar a interface do usuário de processo com privilégios elevados ("média +" IL).
> - Um aplicativo que tem o UIAccess no manifesto e é iniciado por um usuário que não está no grupo Administradores, começa como IL "médio +" e não pode acessar a interface do usuário elevada (nada executando como IL "alta", como aplicativos iniciados por meio de um **clique com o botão direito do mouse > executar como administrador**).
> - Um aplicativo tem acesso à interface de usuário e é iniciado por um usuário administrador inicia como IL "alta" e pode acessar a interface do usuário elevada porque ele tem o mesmo IL.
>
> O UIAccess não é suficiente para que um processo avance pelo limite de IL.

Além de ter acesso a processos de IL mais altos, um aplicativo de tecnologia assistencial com esses privilégios pode ser executado como o aplicativo mais alto na ordem z a qualquer momento, o que significa que um aplicativo de tecnologia assistencial pode ficar visível e disponível sempre que o usuário precisar.

> [!Important]
> Nenhum dos cenários listados anteriormente fornece acesso à interface do usuário em execução no IL do sistema. Isso só será possível se o processo for iniciado na área de trabalho do UAC (controle de conta de usuário) em sistema (e IL do sistema). Nesse caso, a definição de UIAccess não tem nenhum efeito.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>Requisitos de UIAccess para aplicativos de tecnologia assistencial

um aplicativo de tecnologia assistencial é um aplicativo Windows Windows desktop que interage com outros processos em execução na área de trabalho e na nova interface do usuário do Windows para obter informações do sistema e dos aplicativos. O aplicativo de tecnologia assistencial pode fornecer as informações aos usuários de acessibilidade.

Um aplicativo de tecnologia assistencial obtém acesso a outros processos definindo o sinalizador UIAccess no manifesto do aplicativo. Para usar o sinalizador UIAccess, um aplicativo de tecnologia assistencial deve atender aos seguintes requisitos.

-   Exigir para exibir, interagir ou refletir informações de outro aplicativo para fornecer informações para um cenário de acessibilidade e/ou
-   Exigir a execução como a janela superior para obter ou exibir essas informações.

Para usar o UIAccess, um aplicativo de tecnologia assistencial precisa:

-   Ser assinado com um certificado para interagir com aplicativos em execução em um nível de privilégio mais alto.
-   Seja confiável pelo sistema. O aplicativo deve ser instalado em um local seguro que exija um prompt de controle de conta de usuário (UAC) para acesso. Por exemplo, a pasta arquivos de programas.
-   Seja criado com um arquivo de manifesto que inclui o sinalizador uiAccess.

O UIAccess não deve ser usado:

-   Por aplicativos que não são tecnologias assistenciais.
-   Por aplicativos de tecnologia assistencial que exibem informações ou interface do usuário que não são relevantes para o cenário de acessibilidade que eles visam.
-   por aplicativos que só desejam aparecer acima de outros aplicativos na nova interface do usuário Windows.
    > [!Note]  
    > os aplicativos desenvolvidos para a nova interface do usuário Windows não têm o UIAccess como uma opção disponível.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Definindo o UIAccess no arquivo de manifesto do aplicativo

Para obter acesso à interface do usuário do sistema protegido, os aplicativos devem ser criados com um arquivo de manifesto que inclui um atributo especial no arquivo de manifesto. Esse atributo **UIAccess** é incluído na marca **requestedExecutionLevel** , conforme mostrado no exemplo de código a seguir.


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



O valor do atributo **Level** neste código é apenas um exemplo.

O **UIAccess** é "false" por padrão. Se o atributo for omitido ou se não houver nenhum manifesto, o aplicativo não poderá obter acesso à interface do usuário protegida.

para obter mais informações sobre Windows segurança, em aplicativos de assinatura e sobre como criar manifestos, consulte [a história do desenvolvedor do Windows vista e do Windows Server 2008: Windows os requisitos de desenvolvimento de aplicativos do vista para o UAC (controle de conta de usuário)](/previous-versions/aa905330(v=msdn.10)) no MSDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md)
</dt> </dl>

 

 