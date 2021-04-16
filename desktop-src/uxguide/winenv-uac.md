---
title: Controle de conta de usuário (noções básicas de Design)
description: Uma experiência de controle de conta de usuário bem projetada ajuda a impedir alterações indesejadas em todo o sistema de forma previsível e requer esforço mínimo.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b346e5cb581ac83ad2ebffabe73c5fbed636d814
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104551766"
---
# <a name="user-account-control"></a>Controle de Conta de Usuário

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma experiência de controle de conta de usuário bem projetada ajuda a impedir alterações indesejadas em todo o sistema de forma previsível e requer esforço mínimo.

Com o UAC (controle de conta de usuário) totalmente habilitado, os administradores interativos normalmente são executados com privilégios mínimos de usuário, mas podem se elevar automaticamente para executar tarefas administrativas, fornecendo consentimento explícito com a interface do usuário de consentimento. Essas tarefas administrativas incluem a instalação de software e drivers, a alteração de configurações de todo o sistema, a exibição ou a alteração de outras contas de usuário e a execução de ferramentas administrativas.

Em seu estado menos privilegiado, os administradores são chamados de administradores protegidos. Em seu estado elevado, eles são chamados de administradores elevados. Por outro lado, os usuários padrão não podem elevar por conta própria, mas podem pedir que um administrador os eleve usando a interface do usuário da credencial. A conta interna de administrador não requer elevação.

![captura de tela da mensagem de segurança ' permitir programa ' ](images/winenv-uac-image1.png)

A interface do usuário de autorização, usada para elevar os administradores protegidos para ter privilégios administrativos.

![captura de tela da mensagem solicitando senha ](images/winenv-uac-image2.png)

A interface do usuário da credencial, usada para elevar usuários padrão.

O UAC oferece os seguintes benefícios:

-   Ele reduz o número de programas que são executados com privilégios elevados, portanto, ajudando a impedir que os usuários alterem acidentalmente suas configurações do sistema e ajudando a impedir que "malware" Obtenha acesso em todo o sistema. Quando a elevação é negada, o malware só pode afetar os dados do usuário atual. Sem elevação, o malware não pode fazer alterações em todo o sistema nem afetar outros usuários.
-   Para [ambientes gerenciados](glossary.md), as experiências bem projetadas do UAC permitem que os usuários sejam mais produtivos ao serem executados como usuários padrão, removendo restrições desnecessárias.
-   Ele dá aos usuários padrão a capacidade de solicitar que os administradores forneçam permissão para executar tarefas administrativas em sua sessão atual.
-   Para ambientes domésticos, ele permite um melhor controle dos pais sobre as alterações em todo o sistema, incluindo qual software está instalado.

**Desenvolvedores:** Para obter informações de implementação, consulte [reprojetar sua interface do usuário para compatibilidade com UAC](/previous-versions/bb756990(v=msdn.10)).

No Windows Vista, os administradores protegidos podem optar por ser notificados sobre todas as alterações do sistema ou nenhum. A configuração padrão do UAC é notificar sobre todas as alterações, independentemente de qual é sua origem. Quando você for notificado, a área de trabalho ficará esmaecida e você deverá aprovar ou negar a solicitação na caixa de diálogo UAC antes de fazer qualquer outra coisa no computador. O esmaecimento da área de trabalho é chamado de área de [trabalho segura](glossary.md) porque outros programas não podem ser executados enquanto estão esmaecidos.

O Windows 7 introduz duas configurações de UAC intermediárias para administradores protegidos, além dos dois do Windows Vista. A primeira é notificar os usuários somente quando um programa estiver fazendo a alteração, para que os administradores sejam automaticamente elevados quando fizerem uma alteração. Essa é a configuração padrão do UAC no Windows 7 e também utiliza a área de trabalho segura.

A segunda configuração intermediária no Windows 7 é a mesma que a primeira, exceto que ela não usa a área de trabalho segura.

![captura de tela de quatro configurações de UAC no Windows 7 ](images/winenv-uac-image3.png)

O Windows 7 apresenta duas configurações de UAC intermediárias.

**Observação:** As diretrizes relacionadas à gravação de [código para dar suporte ao controle de conta de usuário](/previous-versions/aa905330(v=msdn.10)) são apresentadas em um artigo separado.

## <a name="design-concepts"></a>Conceitos de design

**Metas**

Uma experiência de controle de conta de usuário bem projetada tem os seguintes objetivos:

-   **Elimine a elevação desnecessária.** Os usuários devem ter que elevar apenas para executar tarefas que exigem privilégios administrativos. Todas as outras tarefas devem ser projetadas para eliminar a necessidade de elevação. Geralmente, o software herdado exige privilégios de administrador desnecessariamente gravando nas seções do Registro HKLM ou HKCR, ou nos arquivos de programas ou nas pastas do sistema Windows.
-   **Seja previsível.** Os usuários padrão precisam saber quais tarefas exigem que um administrador execute ou não pode ser realizada em ambientes gerenciados. Os administradores precisam saber quais tarefas exigem elevação. Se não puderem prever a necessidade de elevação com precisão, será mais provável que haja consentimento para tarefas administrativas quando elas não deveriam.
-   **Exigir esforço mínimo.** Tarefas que exigem privilégios administrativos devem ser projetadas para exigir uma única elevação. As tarefas que exigem várias elevações rapidamente se tornam entediantes.
-   **Reverter para privilégios mínimos.** Depois que uma tarefa que requer privilégios administrativos for concluída, o programa deverá reverter para o estado de privilégios mínimos.

**Fluxo de tarefas de elevação**

Quando uma tarefa requer elevação, ela tem as seguintes etapas:

1.  **Ponto de entrada.** Tarefas que exigem elevação imediata quando o UAC está totalmente habilitado têm pontos de entrada marcados com a blindagem do UAC. Nesse caso, os usuários devem esperar ver uma interface do usuário de elevação imediatamente depois de clicar em tais comandos e devem ter cuidado extra quando veem a interface do usuário de elevação de tarefas que não têm uma blindagem.

    ![captura de tela dos ícones do UAC Shield e seus rótulos ](images/winenv-uac-image4.png)

    Neste exemplo, os itens do painel de controle do controle pai e das contas de usuário exigem elevação.

    Quando o UAC é parcialmente habilitado ou desligado completamente, a blindagem do UAC ainda é exibida para indicar que a tarefa envolve alterações no nível do sistema e, portanto, requer elevação, mesmo que o usuário não veja a interface de usuário de elevação. Sempre exibir a blindagem do UAC para tarefas que exigem elevação mantém a interface do usuário simples e previsível.

2.  **Elevação.** Para administradores protegidos, a tarefa solicita consentimento usando a interface do usuário de consentimento. Para usuários padrão, a tarefa solicita credenciais de administrador usando a interface do usuário da credencial.

    ![captura de tela de dois tipos de elevação ](images/winenv-uac-image5.png)

    Esses exemplos mostram a interface do usuário da credencial e a interface do usuário de autorização.

3.  **Separar processo elevado.** Internamente, um novo processo elevado é criado para executar a tarefa.
4.  **Reverter para o privilégio mínimo.** Se necessário, reverta para privilégios mínimos para concluir as etapas que não exigem elevação.

Observe que as tarefas não "se lembram" de Estados elevados. Por exemplo, se o usuário navega para trás e para trás em um ponto de entrada de elevação em um assistente, o usuário deve elevar cada vez.

## <a name="usage-patterns"></a>Padrões de uso

O controle de conta de usuário tem vários padrões de uso (em ordem de preferência):

1.  **Trabalhe para usuários padrão.** Crie o recurso para todos os usuários limitando seu escopo ao usuário atual. Ao limitar as configurações ao usuário atual (em oposição ao sistema todo), você elimina a necessidade de uma interface de usuário de elevação inteiramente e permite que os usuários concluam a tarefa.

    **Incorreto:**

    ![captura de tela da mensagem: você não tem privilégios ](images/winenv-uac-image6.png)

    Neste exemplo, os usuários do Windows XP precisavam ter privilégios administrativos para exibir ou alterar o fuso horário atual.

    **Correto:**

    ![captura de tela da caixa de diálogo de data e hora ](images/winenv-uac-image7.png)

    Neste exemplo, o recurso de fuso horário foi reprojetado no Windows 7 e no Windows Vista para funcionar para todos os usuários.

2.  **Ter elementos de interface do usuário separados para usuários e administradores padrão.** Separe as tarefas de usuário padrão de tarefas administrativas claramente. Conceda a todos os usuários acesso a informações úteis somente leitura. Identifique claramente as tarefas administrativas com o UAC Shield.

    ![gráfico de escudo do UAC mostrando a elevação necessária ](images/winenv-uac-image8.png)

    Neste exemplo, o item do painel de controle do sistema mostra seu estado para todos os usuários, mas alterar as configurações de todo o sistema requer elevação.

3.  **Permitir que usuários padrão tentem a tarefa e aumentem em caso de falha.** Se os usuários padrão puderem exibir as informações e puderem fazer algumas alterações sem elevação, permita que elas acessem a interface do usuário e que elas sejam elevadas somente se a tarefa falhar. Essa abordagem é adequada quando os usuários padrão têm acesso limitado, como com propriedades de seus próprios arquivos no Windows Explorer. Ele também é adequado para configurações nas páginas do Hub híbrido do painel de controle.

    ![mensagem de captura de tela de acesso negada ](images/winenv-uac-image9.png)

    Neste exemplo, o usuário tentou alterar as propriedades do arquivo de programa, mas não tinha privilégios suficientes. O usuário pode elevar e tentar novamente.

4.  **Trabalhe somente para administradores.** Use essa abordagem somente para programas e recursos do administrador! Se um recurso for destinado apenas a administradores (e não tiver nenhum caminho de navegação ou informações de somente leitura úteis para usuários padrão), você poderá solicitar credenciais de administrador no ponto de entrada antes de mostrar qualquer interface do usuário. Use essa abordagem para assistentes longos e [fluxos de página](glossary.md) quando todos os caminhos exigirem privilégios administrativos.

    Se o programa inteiro for somente para administradores, marque-o para solicitar credenciais de administrador para iniciar. O Windows exibe esses ícones de programa com a sobreposição do UAC Shield.

    ![captura de tela do logotipo do Windows e da sobreposição do UAC Shield ](images/winenv-uac-image10.png)

    Neste exemplo, o programa requer privilégios administrativos para ser iniciado.

## <a name="guidelines"></a>Diretrizes

### <a name="uac-shield-icon"></a>Ícone de escudo do UAC

-   **Exibe controles com o escudo do UAC para indicar que a tarefa requer elevação imediata quando o UAC está totalmente habilitado,** mesmo que o UAC não esteja totalmente habilitado no momento. Se todos os caminhos de um assistente e o [fluxo de página](glossary.md) exigirem elevação, exiba a blindagem do UAC no ponto de entrada da tarefa. O uso adequado da blindagem do UAC ajuda os usuários a prever quando a elevação é necessária.
-   **Se o programa der suporte a várias versões do Windows, exiba a blindagem do UAC se pelo menos uma versão exigir elevação.** Como o Windows XP nunca requer elevação, considere remover as blindagens do UAC para o Windows XP se você puder fazer isso consistentemente e sem prejudicar o desempenho.
-   **Não exiba a blindagem do UAC para tarefas que não exigem elevação na maioria dos contextos.** Como essa abordagem às vezes será enganosa, a abordagem preferida é usar um comando contextual blindado adequadamente.

    ![captura de tela de arquivos de fotos no Windows Explorer ](images/winenv-uac-image11.png)

    Como o comando de nova pasta requer elevação somente quando usado em pastas do sistema, ele é exibido sem um escudo do UAC.

-   A blindagem do UAC pode ser exibida nos seguintes controles:

    **Botões de comando:**

    ![captura de tela do botão de comando com o ícone de escudo do UAC ](images/winenv-uac-image12.png)

    Um botão de comando que requer elevação imediata.

    **Links de comando:**

    ![captura de tela do link de comando com o ícone de escudo do UAC ](images/winenv-uac-image13.png)

    Um link de comando que requer elevação imediata.

    **Vincule**

    ![captura de tela do link alterar conta com o UAC Shield ](images/winenv-uac-image14.png)

    Um link que requer elevação imediata.

    **Completos**

    ![captura de tela de menu com o UAC Shield ](images/winenv-uac-image15.png)

    Um menu suspenso que requer elevação imediata.

-   Como as tarefas não se lembram de Estados elevados, **não altere o escudo do UAC para refletir o estado.**
-   **Exibir a blindagem do UAC mesmo que o controle de conta de usuário tenha sido desativado ou o usuário esteja usando a conta de administrador interna.** A exibição consistente da blindagem do UAC é mais fácil de programar e fornece aos usuários informações sobre a natureza da tarefa.

### <a name="elevation"></a>Elevação

-   **Sempre que possível, as tarefas de design serão executadas por usuários padrão sem elevação.** Conceda a todos os usuários acesso a informações úteis somente leitura.
-   **Eleve-se por tarefa, não por configuração.** Não misture configurações de usuário padrão com configurações administrativas em uma única página ou caixa de diálogo. Por exemplo, se os usuários padrão puderem alterar algumas, mas não todas as configurações, dividir essas configurações como uma superfície de interface do usuário separada.

    **Incorreto:**

    ![captura de tela da caixa de diálogo Configurações de data e hora ](images/winenv-uac-image16.png)

    Neste exemplo, as configurações de usuário padrão são misturadas incorretamente com configurações administrativas.

    **Correto:**

    ![captura de tela da mesma caixa de diálogo sem escudos do UAC ](images/winenv-uac-image17.png)

    Neste exemplo, as configurações para alterar a data e hora estão em uma caixa de diálogo separada, disponível somente para administradores. As configurações de fuso horário estão disponíveis para usuários padrão e não são misturadas com configurações administrativas.

-   **Não considere a necessidade de elevar ao determinar se um controle deve ser exibido ou desabilitado.** Isso ocorre porque:
    -   Em ambientes não gerenciados, suponha que os usuários padrão pudessem se elevar solicitando um administrador. A desabilitação de controles que exigem elevação impede que os usuários tenham os administradores em elevação.
    -   Em ambientes gerenciados, suponha que os usuários padrão não possam elevar. A remoção de controles que exigem elevação impede que os usuários saibam quando parar de procurar.
-   **Para eliminar a elevação desnecessária:**
    -   **Se uma tarefa puder exigir elevação, eleve o mais tarde possível.** Se uma tarefa precisar de uma [confirmação](mess-confirm.md), exiba a interface do usuário de elevação somente depois que o usuário tiver confirmado. Se uma tarefa sempre exigir elevação, eleve-a em seu ponto de entrada.
    -   **Uma vez com privilégios elevados, mantenha-se elevado até que privilégios elevados não sejam mais necessários.** Os usuários não devem ter que elevar várias vezes para executar uma única tarefa.
    -   **Se os usuários precisarem elevar para fazer uma alteração, mas optar por não fazer nenhuma alteração, deixe os botões de confirmação positivos habilitados, mas manipule a confirmação como um cancelamento.** Isso elimina os usuários que têm que se elevar apenas para fechar uma janela.
    -   **Incorreto:**
    -   ![captura de tela da janela com apenas um botão ativo ](images/winenv-uac-image18.png)
    -   Neste exemplo, o botão Salvar alterações é desabilitado para evitar uma elevação desnecessária, mas fica habilitado quando os usuários alteram a seleção. No entanto, o botão de confirmação desabilitado faz parecer que os usuários realmente não têm uma opção.
-   **Não exibir uma mensagem de erro quando as tarefas falharem porque os usuários optaram por não elevar.** Suponha que os usuários preferiam intencionalmente não continuar, portanto, não consideram essa situação como um erro.

    **Incorreto:**

    ![captura de tela de mensagem: a Fabrikam Restore não pode ser executada ](images/winenv-uac-image19.png)

    Neste exemplo, a Fabrikam Restore retorna incorretamente uma mensagem de erro quando o usuário decide não elevar.

-   **Não exiba avisos para explicar que os usuários podem precisar elevar seus privilégios para executar tarefas.** Permita que os usuários descubram esse fato por conta própria.
-   **Exiba a interface do usuário do protetor de UAC e elevação com base na tabela a seguir:**

    |                       |                                                                                                                                                                  |                                                                                                                                                                                                                       |                                                                                                      |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **Objeto**      | **Circunstâncias**                                                                                                                                                | **Onde colocar o UAC Shield**                                                                                                                                                                               | **Quando elevar**                                                                            |
    | Programa<br/>    | O programa inteiro é apenas para administradores.<br/>                                                                                                            | ![captura de tela do logotipo do Windows e da sobreposição do UAC Shield ](images/winenv-uac-image10.png)<br/> Sobreposição do UAC Shield no ícone do programa.<br/>                                                                       | Exibir a interface do usuário de elevação na inicialização.<br/>                                                           |
    | Comando<br/>    | O comando inteiro é apenas para administradores.<br/>                                                                                                            | ![captura de tela do link da conta de alteração e da blindagem do UAC ](images/winenv-uac-image14.png)<br/> Botão de comando ou link do UAC Shield on.<br/>                                                                      | Exibir a interface do usuário de elevação quando um link ou botão de comando for clicado, mas após qualquer confirmação.<br/> |
    | Comando<br/>    | O comando exibe informações úteis somente leitura apropriadas para todos os usuários, mas as alterações exigem privilégios administrativos.<br/>                               | ![captura de tela do link de configurações de alteração e da blindagem do UAC ](images/winenv-uac-image8.png)<br/> Complemento do UAC no botão de comando ou link para fazer alterações.<br/>                                                      | Exibir a interface do usuário de elevação quando o botão de comando for clicado, mas após qualquer confirmação.<br/>         |
    | Comando<br/>    | Os usuários padrão podem exibir as informações e possivelmente fazer algumas alterações sem elevação. permitir que os usuários padrão tentem e se elevem em caso de falha.<br/> | ![captura de tela de erro com o ícone do UAC no botão de repetição ](images/winenv-uac-image9.png)<br/> Não mostrar a blindagem do UAC para o comando, mas mostrá-la para o ponto de entrada de elevação se o comando falhar.<br/> | Exibir a interface do usuário de elevação quando o usuário tentar novamente o comando.<br/>                                       |
    | Etapa da tarefa<br/>  | Todas as etapas subsequentes exigem elevação.<br/>                                                                                                               | ![captura de tela do próximo botão de comando com o UAC Shield ](images/winenv-uac-image20.png)<br/> Escudo do UAC no botão próximo (ou equivalente).<br/>                                                                | Exibe a interface do usuário de elevação quando o botão de confirmação próximo ou outro é clicado.<br/>                         |
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

## <a name="text"></a>Texto

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

