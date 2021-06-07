---
title: Controle de Conta de Usuário (noções básicas de design)
description: Uma experiência de Controle de Conta de Usuário bem projetada ajuda a evitar alterações indesejadas em todo o sistema de maneira previsível e requer esforço mínimo.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: bb1424254a91f935073e57bbde2c7124fd838b32
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443207"
---
# <a name="user-account-control"></a>Controle de Conta de Usuário

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma experiência de Controle de Conta de Usuário bem projetada ajuda a evitar alterações indesejadas em todo o sistema de maneira previsível e requer esforço mínimo.

Com o UAC (Controle de Conta de Usuário) totalmente habilitado, os administradores interativos normalmente são executados com privilégios mínimos de usuário, mas podem se auto elevar para executar tarefas administrativas dando consentimento explícito com a interface do usuário de Consentimento. Essas tarefas administrativas incluem a instalação de software e drivers, alteração de configurações em todo o sistema, exibição ou alteração de outras contas de usuário e execução de ferramentas administrativas.

Em seu estado menos privilegiado, os administradores são chamados de Administradores protegidos. Em seu estado elevado, eles são chamados de Administradores elevados. Por outro lado, os usuários Padrão não podem elevar por conta própria, mas podem pedir a um administrador para elevá-los usando a interface do usuário de credencial. A conta de Administrador Integrado não requer elevação.

![captura de tela da mensagem de segurança 'permitir programa' ](images/winenv-uac-image1.png)

A interface do usuário de Consentimento, usada para elevar os administradores protegidos para ter privilégios administrativos.

![captura de tela da mensagem solicitando senha ](images/winenv-uac-image2.png)

A interface do usuário de credencial, usada para elevar os usuários Padrão.

O UAC oferece os seguintes benefícios:

-   Ele reduz o número de programas executados com privilégios elevados, ajudando, portanto, a impedir que os usuários mudem acidentalmente suas configurações do sistema e ajudando a impedir que "malware" obtenha acesso em todo o sistema. Quando a elevação é negada, o malware só pode afetar os dados do usuário atual. Sem elevação, o malware não pode fazer alterações em todo o sistema nem afetar outros usuários.
-   Para [ambientes gerenciados,](glossary.md)as experiências de UAC bem projetadas permitem que os usuários sejam mais produtivos ao executar como usuários Padrão removendo restrições desnecessárias.
-   Ele dá aos usuários standard a capacidade de pedir aos administradores para que eles deem permissão para executar tarefas administrativas em sua sessão atual.
-   Para ambientes domésticos, ele permite um melhor controle dos pais sobre alterações em todo o sistema, incluindo qual software está instalado.

**Desenvolvedores:** Para obter informações de implementação, [consulte Redesign Your UI for UAC Compatibility](/previous-versions/bb756990(v=msdn.10)).

No Windows Vista, os administradores protegidos podem optar por ser notificados sobre todas as alterações do sistema ou nenhuma. A configuração padrão do UAC é notificar sobre todas as alterações, independentemente de sua origem. Quando você for notificado, sua área de trabalho ficará esmaecida e você deverá aprovar ou negar a solicitação na caixa de diálogo UAC antes de poder fazer qualquer outra coisa em seu computador. A esmaecimento da área [](glossary.md) de trabalho é conhecida como área de trabalho segura porque outros programas não podem ser executados enquanto estão esmaecidas.

O Windows 7 apresenta duas configurações intermediárias de UAC para administradores protegidos, além das duas do Windows Vista. A primeira é notificar os usuários somente quando um programa estiver fazendo a alteração, para que os administradores sejam automaticamente elevados quando fizerem uma alteração por conta própria. Essa é a configuração padrão do UAC no Windows 7 e também usa a área de trabalho segura.

A segunda configuração intermediária no Windows 7 é a mesma que a primeira, exceto que ela não usa a área de trabalho segura.

![captura de tela de quatro configurações de uac no Windows 7 ](images/winenv-uac-image3.png)

O Windows 7 apresenta duas configurações de UAC intermediárias.

**Observação:** As diretrizes relacionadas à escrita [de código para dar](/previous-versions/aa905330(v=msdn.10)) suporte ao Controle de Conta de Usuário são apresentadas em um artigo separado.

## <a name="design-concepts"></a>Conceitos de design

**Metas**

Uma experiência de Controle de Conta de Usuário bem projetada tem as seguintes metas:

-   **Elimine a elevação desnecessária.** Os usuários devem ter que elevar apenas para executar tarefas que exigem privilégios administrativos. Todas as outras tarefas devem ser projetadas para eliminar a necessidade de elevação. Geralmente, o software herdado requer privilégios de administrador desnecessariamente escrevendo nas seções do registro HKLM ou HKCR ou nas pastas Arquivos de Programas ou Sistema Windows.
-   **Ser previsível.** Os usuários padrão precisam saber quais tarefas exigem que um administrador execute ou não podem ser executadas em ambientes gerenciados. Os administradores precisam saber quais tarefas exigem elevação. Se eles não puderem prever a necessidade de elevação com precisão, é mais provável que eles deem consentimento para tarefas administrativas quando não deveriam.
-   **Exigir esforço mínimo.** As tarefas que exigem privilégios administrativos devem ser projetadas para exigir uma única elevação. Tarefas que exigem várias elevações rapidamente se tornam entediantes.
-   **Reverta para privilégios mínimos.** Depois que uma tarefa que exige privilégios administrativos for concluída, o programa deverá reverter para o estado de privilégio mínimo.

**Fluxo de tarefas de elevação**

Quando uma tarefa requer elevação, ela tem as seguintes etapas:

1.  **Ponto de entrada.** Tarefas que exigem elevação imediata quando o UAC está totalmente habilitado têm pontos de entrada marcados com a blindagem UAC. Nesse caso, os usuários devem esperar ver uma interface do usuário de elevação imediatamente após clicar nesses comandos e devem ter cuidado extra quando veem a interface do usuário de elevação de tarefas que não têm um blindagem.

    ![captura de tela de ícones de blindagem uac e seus rótulos ](images/winenv-uac-image4.png)

    Neste exemplo, os itens do painel de controle de contas de usuário e controle dos pais exigem elevação.

    Quando o UAC está parcialmente habilitado ou completamente desligado, o blindagem UAC ainda é exibido para indicar que a tarefa envolve alterações no nível do sistema e, portanto, requer elevação, mesmo que o usuário possa não ver a interface do usuário de elevação. Sempre exibir o blindagem UAC para tarefas que exigem elevação mantém a interface do usuário simples e previsível.

2.  **Elevação.** Para Administradores Protegidos, a tarefa solicita consentimento usando a interface do usuário de Consentimento. Para usuários Padrão, a tarefa solicita credenciais de administrador usando a interface do usuário de credencial.

    ![captura de tela de dois tipos de elevação ](images/winenv-uac-image5.png)

    Esses exemplos mostram a interface do usuário de credencial e a interface do usuário de consentimento.

3.  **Processo elevado separado.** Internamente, um novo processo elevado é criado para executar a tarefa.
4.  **Reverta para privilégios mínimos.** Se necessário, reverta para o privilégio mínimo para concluir as etapas que não exigem elevação.

Observe que as tarefas não "se lembram" dos estados elevados. Por exemplo, se o usuário navegar para frente e para trás sobre um ponto de entrada de elevação em um assistente, o usuário deverá elevar cada vez.

## <a name="usage-patterns"></a>Padrões de uso

O Controle de Conta de Usuário tem vários padrões de uso (em ordem de preferência):

1.  **Trabalhe para usuários Standard.** Projete o recurso para todos os usuários limitando seu escopo ao usuário atual. Limitando as configurações para o usuário atual (em vez de todo o sistema), você elimina a necessidade de uma interface do usuário de elevação inteiramente e permite que os usuários concluam a tarefa.

    **Incorreto:**

    ![captura de tela da mensagem: você não tem privilégio ](images/winenv-uac-image6.png)

    Neste exemplo, os usuários do Windows XP tinham que ter privilégios administrativos para exibir ou alterar o fuso horário atual.

    **Correto:**

    ![captura de tela da caixa de diálogo de data e hora ](images/winenv-uac-image7.png)

    Neste exemplo, o recurso de fuso horário foi reprojetado no Windows 7 e no Windows Vista para funcionar para todos os usuários.

2.  **Ter elementos de interface do usuário separados para usuários e administradores Standard.** Separe claramente tarefas de usuário Padrão de tarefas administrativas. Dê a todos os usuários acesso a informações úteis somente leitura. Identifique claramente as tarefas administrativas com o blindagem UAC.

    ![gráfico do uac shield mostrando a elevação necessária ](images/winenv-uac-image8.png)

    Neste exemplo, o item do painel de controle Sistema mostra seu estado para todos os usuários, mas alterar as configurações de todo o sistema requer elevação.

3.  **Permitir que os usuários padrão tentem a tarefa e elevem-se em caso de falha.** Se os usuários Standard puderem exibir as informações e puderem fazer algumas alterações sem elevação, permita que eles acessem a interface do usuário e os elevem somente se a tarefa falhar. Essa abordagem é adequada quando os usuários Standard têm acesso limitado, como com propriedades de seus próprios arquivos Windows Explorer. Ele também é adequado para configurações em Painel de Controle de hub híbrido.

    ![captura de tela da mensagem de acesso negado ](images/winenv-uac-image9.png)

    Neste exemplo, o usuário tentou alterar as propriedades do arquivo de programa, mas não tinha privilégios suficientes. O usuário pode elevar e tentar novamente.

4.  **Trabalhe apenas para administradores.** Use essa abordagem somente para programas e recursos de administrador! Se um recurso for destinado somente para administradores (e não tiver nenhum caminho de navegação ou informações úteis somente leitura para usuários Standard), você poderá solicitar credenciais de administrador no ponto de entrada antes de mostrar qualquer interface do usuário. Use essa abordagem para assistentes longos e fluxos [de página](glossary.md) quando todos os caminhos exigirem privilégios administrativos.

    Se o programa inteiro for apenas para administradores, marque-o para solicitar credenciais de administrador para iniciar. O Windows exibe esses ícones de programa com a sobreposição de blindagem UAC.

    ![captura de tela do logotipo do Windows e sobreposição de blindagem uac ](images/winenv-uac-image10.png)

    Neste exemplo, o programa requer privilégios administrativos para iniciar.

## <a name="guidelines"></a>Diretrizes

### <a name="uac-shield-icon"></a>Ícone de blindagem UAC

-   **Exibir controles com o blindagem UAC** para indicar que a tarefa requer elevação imediata quando o UAC está totalmente habilitado, mesmo que o UAC não está totalmente habilitado no momento. Se todos os caminhos de um assistente e fluxo [de página](glossary.md) exigirem elevação, ex exibirá a blindagem UAC no ponto de entrada da tarefa. O uso adequado da blindagem UAC ajuda os usuários a prever quando a elevação é necessária.
-   **Se o programa for compatível com várias versões do Windows, ex exibirá a blindagem UAC se pelo menos uma versão exigir elevação.** Como o Windows XP nunca requer elevação, considere remover os blindagem UAC para Windows XP se você puder fazer isso de forma consistente e sem prejudicar o desempenho.
-   **Não ex exibir o blindagem UAC para tarefas que não exigem elevação na maioria dos contextos.** Como essa abordagem às vezes será enganosa, a abordagem preferencial é usar um comando contextual devidamente blindado.

    ![captura de tela de arquivos de fotos no Windows Explorer ](images/winenv-uac-image11.png)

    Como o comando Nova pasta requer elevação somente quando usado em pastas do sistema, ele é exibido sem uma blindagem UAC.

-   O blindagem UAC pode ser exibido nos seguintes controles:

    **Botões de comando:**

    ![captura de tela do botão de comando com o ícone de blindagem uac ](images/winenv-uac-image12.png)

    Um botão de comando que requer elevação imediata.

    **Links de comando:**

    ![captura de tela do link de comando com o ícone de blindagem uac ](images/winenv-uac-image13.png)

    Um link de comando que requer elevação imediata.

    **Links:**

    ![captura de tela do link alterar conta com o uac shield ](images/winenv-uac-image14.png)

    Um link que requer elevação imediata.

    **Menus:**

    ![captura de tela do menu com o uac shield ](images/winenv-uac-image15.png)

    Um menu suspenso que requer elevação imediata.

-   Como as tarefas não se recordam de estados **elevados, não altere a blindagem UAC para refletir o estado.**
-   **Exibir o blindagem UAC mesmo se o Controle de Conta de Usuário tiver sido desligado ou se o usuário estiver usando a conta de Administrador Interna.** Exibir consistentemente a blindagem UAC é mais fácil de programar e fornece aos usuários informações sobre a natureza da tarefa.

### <a name="elevation"></a>Elevação

-   **Sempre que possível, projete tarefas a serem executadas por usuários Padrão sem elevação.** Dê a todos os usuários acesso a informações úteis somente leitura.
-   **Elevar por tarefa, não por configuração.** Não misture configurações de usuário padrão com configurações administrativas em uma única página ou caixa de diálogo. Por exemplo, se os usuários Standard puderem alterar algumas, mas não todas as configurações, divida essas configurações como uma superfície de interface do usuário separada.

    **Incorreto:**

    ![captura de tela da caixa de diálogo de configurações de data e hora ](images/winenv-uac-image16.png)

    Neste exemplo, as configurações de usuário padrão são misturadas incorretamente com configurações administrativas.

    **Correto:**

    ![captura de tela da mesma caixa de diálogo sem blindagem uac ](images/winenv-uac-image17.png)

    Neste exemplo, as configurações para alterar a data e a hora estão em uma caixa de diálogo separada, disponível somente para administradores. As configurações de fuso horário estão disponíveis para usuários Standard e não são misturadas com configurações administrativas.

-   **Não considere a necessidade de elevar ao determinar se um controle deve ser exibido ou desabilitado.** Isso ocorre porque:
    -   Em ambientes não controlados, suponha que os usuários Padrão podem elevar solicitando um administrador. Desabilitar controles que exigem elevação impediria que os usuários elevem os administradores.
    -   Em ambientes gerenciados, suponha que os usuários Padrão não possam elevar. Remover controles que exigem elevação impediria que os usuários saibam quando parar de procurar.
-   **Para eliminar a elevação desnecessária:**
    -   **Se uma tarefa puder exigir elevação, eleve o mais tarde possível.** Se uma tarefa precisar de [uma confirmação](mess-confirm.md), exibirá a interface do usuário de elevação somente depois que o usuário tiver confirmado. Se uma tarefa sempre exigir elevação, eleve-a em seu ponto de entrada.
    -   **Depois de elevado, mantenha-se elevado até que os privilégios elevados não sejam mais necessários.** Os usuários não devem ter que elevar várias vezes para executar uma única tarefa.
    -   **Se os usuários devem elevar para fazer uma alteração, mas optar por não fazer nenhuma alteração, deixe os botões de confirmação positivos habilitados, mas tratar a confirmação como um cancelamento.** Isso elimina os usuários que têm que elevar apenas para fechar uma janela.
    -   **Incorreto:**
    -   ![captura de tela da janela com apenas um botão ativo ](images/winenv-uac-image18.png)
    -   Neste exemplo, o botão Salvar Alterações é desabilitado para evitar uma elevação desnecessária, mas fica habilitado quando os usuários alteram a seleção. No entanto, o botão de confirmação desabilitado faz com que pareça que os usuários realmente não têm uma opção.
-   **Não exibir uma mensagem de erro quando as tarefas falharem porque os usuários optaram por não elevar.** Suponha que os usuários intencionalmente optaram por não prosseguir, portanto, eles não considerarão essa situação como um erro.

    **Incorreto:**

    ![captura de tela da mensagem: restauração fabrikam não pode ser executado ](images/winenv-uac-image19.png)

    Neste exemplo, a Restauração fabrikam fornece incorretamente uma mensagem de erro quando o usuário decide não elevar.

-   **Não exibir avisos para explicar que os usuários talvez precisem elevar seus privilégios para executar tarefas.** Permitir que os usuários descubram esse fato por conta própria.
-   **Ex exibir a interface do usuário de elevação e blindagem UAC com base na tabela a seguir:**

    | Objeto | Circunstância | Onde colocar o blindagem UAC | Quando elevar |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | Programa<br/>    | O programa inteiro é somente para administradores.<br/>                                                                                                            | ![captura de tela do logotipo do Windows e sobreposição de blindagem uac ](images/winenv-uac-image10.png)<br/> Sobreposição de blindagem UAC no ícone do programa.<br/>                                                                       | Exibir a interface do usuário de elevação no início.<br/>                                                           |
    | Comando<br/>    | O comando inteiro é apenas para administradores.<br/>                                                                                                            | ![captura de tela do link da conta de alteração e do uac Shield ](images/winenv-uac-image14.png)<br/> Blindagem UAC no botão de comando ou link.<br/>                                                                      | Exibir a interface do usuário de elevação quando o botão de comando ou o link for clicado, mas após quaisquer confirmações.<br/> |
    | Comando<br/>    | O comando exibe informações úteis somente leitura apropriadas para todos os usuários, mas as alterações exigem privilégios administrativos.<br/>                               | ![captura de tela do link de configurações de alteração e do uac Shield ](images/winenv-uac-image8.png)<br/> Blindagem UAC no botão de comando ou link para fazer alterações.<br/>                                                      | Exibe a interface do usuário de elevação quando o botão de comando é clicado, mas após quaisquer confirmações.<br/>         |
    | Comando<br/>    | Os usuários padrão podem exibir as informações e, possivelmente, fazer algumas alterações sem elevação. permitir que os usuários padrão tentem e elevem em caso de falha.<br/> | ![captura de tela de erro com o ícone uac no botão tentar novamente ](images/winenv-uac-image9.png)<br/> Não mostre o blindagem UAC para o comando, mas mostre-o para o ponto de entrada de elevação se o comando falhar.<br/> | Exibe a interface do usuário de elevação quando o usuário recupera o comando.<br/>                                       |
    | Etapa da tarefa<br/>  | Todas as etapas subsequentes exigem elevação.<br/>                                                                                                               | ![captura de tela do próximo botão de comando com o uac shield ](images/winenv-uac-image20.png)<br/> Blindagem UAC no botão Próximo (ou equivalente).<br/>                                                                | Exibe a interface do usuário de elevação quando o botão Próximo ou outro commit é clicado.<br/>                         |
    | Etapa da tarefa<br/>  | Algumas ramificações exigem elevação.<br/>                                                                                                                      | ![captura de tela do link de comando com a blindagem do UAC ](images/winenv-uac-image21.png)<br/> O UAC Shield nos links de comando que exigem elevação.<br/>                                                              | Exibir a interface do usuário de elevação quando os links de comando com o UAC Shield forem clicados.<br/>                      |

    

     

### <a name="elevation-ui"></a>IU de elevação

-   **Se o usuário fornece uma conta que não é válida (nome ou senha) ou não tem privilégios de administrador, basta reexibir a interface do usuário da credencial.** Não exibir uma mensagem de erro.
-   **Se o usuário cancelar a interface do usuário da credencial, retorne o usuário de volta para a interface de usuário original.** Não exibir uma mensagem de erro.
-   Se o controle de conta de usuário tiver sido desativado e um usuário padrão tentar executar uma tarefa que requer elevação, forneça uma mensagem de erro afirmando "esta tarefa requer privilégios de administrador. Para executar essa tarefa, você deve fazer logon usando uma conta de administrador. "

![captura de tela da tarefa requer a mensagem de privilégios ](images/winenv-uac-image22.png)

Neste exemplo, o controle de conta de usuário foi desativado, portanto, uma mensagem de erro explica que o usuário deve usar uma conta de administrador.

### <a name="wizards"></a>Assistentes

-   **Não eleve várias vezes.** Depois que um assistente é elevado, ele deve ficar elevado.
-   Se a tarefa for executada dentro do assistente, coloque uma blindagem do UAC no botão "Avançar" da página de confirmação (que deve receber um [rótulo mais específico](win-wizards.md)). Quando o usuário confirmar:
    -   Se a próxima página for uma página de progresso, avance para essa página e exiba a interface do usuário de elevação de moda. Após a elevação bem-sucedida, execute a tarefa.
    -   Se a próxima página for uma página de conclusão, avance para essa página (mas substitua temporariamente seu conteúdo por "aguardando permissão...") e exiba a interface do usuário de elevação de moda restrita. Após a elevação bem-sucedida, execute a tarefa e exiba o conteúdo da página de conclusão.
    -   Se o usuário cancelar a interface do usuário de elevação, retorne à página de confirmação. Isso permite que o usuário tente novamente.
-   Se a tarefa for executada após a conclusão do assistente, coloque uma blindagem do UAC no botão "Concluir" da página de confirmação (que deve receber um [rótulo mais específico](win-wizards.md)). Quando o usuário confirmar:
    -   Permanecer na página de confirmação e exibir de moda restrita a interface do usuário de elevação. Após a elevação bem-sucedida, feche o assistente.
    -   Se o usuário cancelar a interface do usuário de elevação, retorne à página de confirmação. Isso permite que o usuário tente novamente.
-   Para assistentes longos destinados apenas a administradores, você pode solicitar credenciais de administrador no ponto de entrada antes de mostrar qualquer interface do usuário.

## <a name="text"></a>Text

-   **Não use reticências apenas porque um comando requer elevação.** A necessidade de elevar é indicada com a blindagem do UAC.

## <a name="documentation"></a>Documentação

Ao fazer referência ao controle de conta de usuário:

-   Consulte o recurso como controle de conta de usuário (na primeira menção) ou UAC (em menção posterior), não conta de usuário com privilégios mínimos ou LUA.
-   Consulte não administradores como usuários padrão.
-   Consulte administradores de computadores internos como administradores internos.

Na documentação do usuário:

-   Consulte o ato de dar consentimento para executar uma tarefa administrativa como concedendo permissão.

Em programação e outras documentações técnicas:

-   Consulte o ato de dar consentimento para executar uma tarefa administrativa como elevação.
-   No contexto do UAC, consulte administradores como administradores protegidos quando não elevados e administradores elevados após a elevação.
-   Consulte a caixa de diálogo usada para inserir senhas como a interface do usuário da credencial. Consulte a caixa de diálogo usada para dar consentimento como a interface do usuário de consentimento. Consulte ambos geralmente como interface do usuário de elevação.

