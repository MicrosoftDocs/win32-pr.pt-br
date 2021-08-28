---
title: Área de notificação
description: A área de notificação fornece notificações e status. Programas bem projetados usam a área de notificação adequadamente, sem ser entediantes ou desalocar.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c580d80bd95684cc80dc24e59273553f4a08e11f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985449"
---
# <a name="notification-area"></a>Área de notificação

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

A área de notificação fornece notificações e status. Programas bem projetados usam a área de notificação adequadamente, sem ser entediantes ou desalocar.

A área de notificação é uma parte da barra de tarefas que fornece uma fonte temporária para notificações e status. Ele também pode ser usado para exibir ícones para recursos do sistema e do programa que não têm presença na área de trabalho.

Os itens na área de notificação são chamados de ícones de área de notificação ou simplesmente ícones se o contexto da área de notificação já estiver claramente estabelecido.

![captura de tela da área de notificação, hora e data ](images/winenv-notification-image1.png)

A área de notificação.

Para dar aos usuários controle da área de trabalho Windows 7, nem todos os ícones de área de notificação são exibidos por padrão. Em vez disso, os ícones são exibidos no estouro da área de notificação, a menos que sejam promovidos para a área de notificação pelo usuário.

![Captura de tela que mostra uma área de notificação e estouro.](images/winenv-notification-image2.png)

O estouro da área de notificação.

**Observação:** Diretrizes relacionadas à barra [de tarefas,](winenv-taskbar.md) [notificações](mess-notif.md) e [balão são apresentadas](ctrl-balloons.md) em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **Seu programa precisa exibir uma notificação?** Se sim, você deve usar um ícone de área de notificação.
-   **O ícone é exibido temporariamente para mostrar uma alteração de status?** Em caso positivo, um ícone de área de notificação pode ser apropriado, dependendo dos seguintes fatores:

    -   **O status é útil e relevante?** Ou seja, os usuários provavelmente monitorarão o ícone e alterarão seu comportamento como resultado dessas informações? Caso não seja, não exibe o status ou coloca-o em um arquivo de log.

        **Incorreto:**

        ![captura de tela da área de notificação com o ícone de unidade ](images/winenv-notification-image3.png)

        Neste exemplo, o ícone de atividade de unidade de disco é inadequado porque é improvável que os usuários alterem seu comportamento com base nele.

    -   **O status é crítico? A ação imediata é necessária?** Nesse caso, exibe as informações de uma forma que exige atenção e não pode ser facilmente ignorada, como uma caixa [de diálogo](win-dialog-box.md).

    Os programas projetados para Windows 7 podem usar ícones de sobreposição no botão da barra de tarefas do programa para mostrar a alteração do status, bem como barras de progresso do botão da barra de tarefas para mostrar o progresso das tarefas de execução longa.

-   **O recurso já tem "presença da área de trabalho"?** Ou seja, quando executado, o recurso aparece em uma janela na área de trabalho (possivelmente minimizado)? Nesse caso, exibe o status na barra de status do programa, em outra área de [status](ctrl-status-bars.md)ou, Windows 7, diretamente no botão da barra de tarefas. Se o recurso não tiver presença na área de trabalho, você poderá usar um ícone para acesso ao programa e para mostrar o status.
-   **O ícone é principalmente para iniciar um programa ou acessar seus recursos ou configurações rapidamente?** Em caso afirmativos, use o menu Iniciar para iniciar programas. A área de notificação não se destina ao acesso rápido de programa ou comando.

    ![captura de tela da barra de ferramentas de início rápido ](images/winenv-notification-image4.png)

    Neste exemplo do Windows Vista, Início Rápido é usado para iniciar o Windows Explorer e Windows Internet Explorer rapidamente.

    Para programas projetados para Windows 7, os usuários podem fixar botões de barra de tarefas para acesso rápido ao programa. Os programas podem usar uma Lista de Atalhos ou uma barra de ferramentas em miniatura para acessar comandos usados com frequência diretamente do botão de barra de ferramentas de um programa. A Início Rápido não é exibida por padrão no Windows 7.

    ![captura de tela da barra de tarefas e da lista de saltos com ícones ](images/winenv-notification-image5.png)

    Neste exemplo, um Lista de Atalhos é usado para acesso rápido a comandos.

## <a name="design-concepts"></a>Conceitos de design

### <a name="the-windows-desktop"></a>A área Windows desktop

A Windows desktop tem os seguintes pontos de acesso do programa:

-   **Área de trabalho.** A área na tela em que os usuários podem executar seu trabalho, bem como armazenar programas, documentos e seus atalhos. Embora tecnicamente a área de trabalho inclua a barra de tarefas, na maioria dos contextos, ela se refere apenas à área de trabalho.
-   **botão Iniciar.** O ponto de acesso para todos os programas e locais Windows especiais (Documentos, Imagens, Música, Jogos, Computador, Painel de Controle), com listas "usadas mais recentemente" para acesso rápido a documentos e programas usados recentemente.
-   **Início Rápido.** Um ponto de acesso direto para programas selecionados pelo usuário. Início Rápido foi removido do Windows 7.
-   **Taskbar.** O ponto de acesso para executar programas que têm presença na área de trabalho. Embora tecnicamente a barra de tarefas abrange toda a barra do botão Iniciar até a área de notificação, na maioria dos contextos, a barra de tarefas refere-se à área entre elas, contendo os botões da barra de tarefas. Às vezes, essa área é conhecida como o grupo de tarefas.
-   **Faixas de mesa. Não recomendado.**
-   **Área de notificação.** Uma fonte de curto prazo para notificações e status, bem como um ponto de acesso para recursos relacionados ao sistema e ao programa que não têm presença na área de trabalho.

![captura de tela identificando pontos de acesso da área de trabalho ](images/winenv-notification-image6.png)

Os Windows de acesso à área de trabalho incluem a botão Iniciar, a barra de tarefas e a área de notificação. Observe o recurso em miniatura do botão da barra de tarefas.

**A área de trabalho é um recurso compartilhado limitado que é o ponto de entrada do usuário para Windows.** Deixe os usuários no controle. Você deve usar as áreas de trabalho conforme pretendido qualquer outro uso deve ser considerado um abuso. Por exemplo, nunca veja áreas de trabalho como maneiras de promover seu programa ou sua [marca](exper-branding.md).

### <a name="using-the-notification-area-appropriately"></a>Usando a área de notificação adequadamente

A área de notificação foi originalmente destinada como uma fonte temporária para notificações e status. Sua eficiência e conveniência incentivam os desenvolvedores a dar a ele outras finalidades, como iniciar programas e executar comandos. Infelizmente, ao longo do tempo, essas adições tornou a área de notificação muito grande e com muitos nós e confundiram sua finalidade com os outros pontos de acesso da área de trabalho.

Windows O XP abordou o problema de escala tornando a área relegível e ocultando os ícones nãoutilados. Windows O Vista abordou o ruído removendo notificações desnecessárias e entediantes. Windows 7 foi um passo além concentrando a notificação em sua finalidade original de ser uma fonte de notificação. **A maioria dos ícones está oculta por padrão Windows 7, mas pode ser promovida para a área de notificação manualmente pelo usuário. Para manter os usuários no controle de suas áreas de trabalho, não é possível que seu programa execute essa promoção automaticamente.** Windows ainda exibe notificações para ícones ocultos, promovendo-os temporariamente.

![captura de tela da área de notificação e estouro ](images/winenv-notification-image7.png)

No Windows 7, a maioria dos ícones de área de notificação está oculta por padrão.

Além disso, Windows 7 dá suporte a muitos recursos diretamente nos botões da barra de tarefas. Especificamente, você pode usar:

-   Jump Lists e barras de ferramentas em miniatura para acessar rapidamente os comandos usados com frequência.
-   Ícones de sobreposição para mostrar o status de programas em execução.
-   Barras de progresso do botão da barra de tarefas para mostrar o progresso de tarefas de execução longa.

Em resumo, se o programa tiver presença na área de trabalho, aproveite ao máximo os recursos da barra de tarefas Windows 7 para essas finalidades. **Mantenha os ícones da área de notificação focados em exibir notificações e status.**

### <a name="keeping-users-in-control"></a>Mantendo os usuários no controle

Manter os usuários no controle se estende além do uso correto da área de notificação. Dependendo da natureza do ícone, talvez você queira permitir que os usuários faça o seguinte:

-   **Remova o ícone.** Seu ícone pode fornecer status relevante e útil, mas, mesmo assim, os usuários podem não querer vê-lo. Windows permite que os usuários o ocultam ícones, mas esse recurso não é facilmente descoberto. Para manter os usuários no controle, forneça uma **opção Ícone de** exibição na área de notificação no menu de contexto do ícone. Observe que remover um ícone não precisa afetar o programa, o recurso ou o processo subjacente.
-   **Selecione os tipos de notificações a exibir.** Sua notificação deve ser útil e relevante, mas pode haver notificações que os usuários não querem ver. Isso é especialmente verdadeiro para [notificações](mess-notif.md)do FYI. Permita que os usuários optem por habilitar os menos importantes.
-   **Suspender recursos opcionais.** Os ícones são usados para exibir o status de recursos sem presença na área de trabalho. Esses recursos tendem a ser execução demorada, tarefas em segundo plano opcionais, como impressão, indexação, verificação ou sincronização. Os usuários podem querer suspender esses recursos para aumentar o desempenho do sistema, reduzir o consumo de energia ou porque estão offline.
-   **Encerre o programa.** Forneça as opções mais adequadas:
    -   **Encerre o programa temporariamente.** o programa é interrompido e reiniciado quando Windows é reiniciado. Essa abordagem é adequada para utilitários de sistema importantes, como programas de segurança.
    -   **Encerre o programa permanentemente.** o programa é interrompido e não é reiniciado quando Windows é reiniciado (a menos que o usuário opte por reiniciar mais tarde). O usuário não deseja mais executar o programa ou deseja executar o programa sob demanda, talvez para melhorar o desempenho do sistema.

Embora seja uma boa ideia fornecer a maioria dessas configurações no menu de contexto do ícone, a experiência padrão do programa deve ser adequada para a maioria dos usuários. Não ative tudo por padrão e espere que os usuários Desativem os recursos. Em vez disso, ative os recursos importantes por padrão e permita que os usuários habilitem recursos adicionais conforme desejado.

**Se você fizer apenas quatro coisas...**

1.  Não se preocupe com a área de notificação. Use-o apenas como uma fonte para notificações e status e para recursos sem presença na área de trabalho.
2.  Mantenha os usuários no controle. Forneça as opções apropriadas para controlar o ícone, suas notificações e os recursos subjacentes.
3.  Apresente uma experiência padrão adequada para a maioria dos usuários. Permita que os usuários habilitem os recursos desejados em vez de esperar que eles desabilitem aqueles indesejados.
4.  aproveite ao máximo os recursos do botão da barra de tarefas do Windows 7 para mostrar o status e tornar as tarefas executadas com mais frequência do programa eficientes.

## <a name="usage-patterns"></a>Padrões de uso

Os ícones da área de notificação têm vários padrões de uso:




| Rótulo | Valor |
|--------|-------|
| <strong>Status do sistema e acesso</strong><br /> Exibido continuamente para mostrar o status do sistema importante, mas não crítico, e para fornecer acesso a recursos e configurações relevantes. <br /> | Os recursos do sistema que precisam de ícones da área de notificação não têm presença de área de trabalho persistente. Também pode ser usado como uma fonte de notificação. <br /><img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br /> Neste exemplo, os ícones de bateria, rede e volume são exibidos continuamente quando aplicável.<br /> | 
| <strong>Status e acesso da tarefa em segundo plano</strong><br /> Exibido enquanto uma tarefa em segundo plano está em execução para mostrar o status e fornecer acesso a recursos e configurações. <br /> | Os processos em segundo plano precisam de ícones da área de notificação quando não têm presença na área de trabalho. Também pode ser usado como uma fonte de notificação. <br /><img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br /> Neste exemplo, o ícone da central de ações permite que os usuários verifiquem seu status mesmo quando não há presença na área de trabalho.<br /> | 
| <strong>Status do evento temporário</strong><br /> Programas com presença na área de trabalho podem exibir ícones temporariamente para mostrar eventos importantes ou alterações no status. <br /> | <img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br /> Neste exemplo, os ícones para impressão e instalação de atualizações são exibidos temporariamente para mostrar eventos importantes ou alterações no status.<br /> | 
| <strong>Origem de notificação temporária</strong><br /> Exibido temporariamente para mostrar uma notificação. Removido após um tempo limite ou quando o problema subjacente é resolvido ou a tarefa foi executada. <br /> | Ícones temporários são preferenciais para fontes de notificação puras. Não exiba um ícone que não forneça um status útil, relevante e dinâmico apenas porque um recurso pode precisar exibir uma notificação no futuro. <br /><img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br /> Neste exemplo, o ícone de plug-and-Play é exibido enquanto uma nova notificação de hardware detectado é mostrada.<br /> | 
| <strong>Aplicativo de instância única minimizada</strong><br /> Para reduzir a aglomeração da barra de tarefas, um aplicativo de instância única e de execução longa pode ser minimizado para um ícone da área de notificação. <br /> | <img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br /> neste exemplo do Windows Vista, Outlook e Windows Live Messenger são aplicativos de instância única que minimizam para ícones da área de notificação.<br /> Considere o uso desse padrão somente se todos os itens a seguir se aplicarem: <br /><ul><li>O aplicativo pode ter apenas uma única instância.</li><li>O aplicativo é executado por um longo período de tempo.</li><li>O ícone mostra o status.</li><li>O ícone pode ser uma fonte de notificação.</li><li>Isso é opcional e os usuários devem <a href="glossary.md">aceitar</a>.</li></ul>Se todas essas condições se aplicarem, a minimização para um ícone eliminará a existência de dois pontos de acesso quando apenas um for necessário. <br /><strong>Observação:</strong> esse padrão de ícone não é mais recomendado para o Windows 7. Use botões normais da barra de tarefas se o seu programa tiver presença na área de trabalho.<br /><img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br /> neste exemplo do Windows 7, um botão de barra de tarefas normal ocupa pouco espaço, mas beneficia-se dos recursos do botão da barra de tarefas do Windows 7, incluindo listas de atalhos, ícones de sobreposição e miniaturas sofisticadas.<br /> | 




 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Forneça apenas um ícone da área de notificação por componente.**
-   **Use um ícone com as versões 16x16, 20x20 e 24x24 pixel.** As versões maiores são usadas em modos de exibição de alto dpi.

### <a name="when-to-show"></a>Quando mostrar

-   Para o padrão de origem de notificação temporária:
    -   Windows exibe o ícone quando a notificação é exibida.
    -   Remova o ícone com base em seu padrão de [design de notificação](mess-notif.md) :



    | Padrão                                     | Quando remover                                         |
    |--------------------------------------|------------------------------------------|
    | Êxito na ação<br/>            | Quando a notificação é removida.<br/> |
    | Falha na ação<br/>            | Quando o problema é resolvido.<br/>     |
    | Evento não crítico do sistema<br/> | Quando o problema é resolvido.<br/>     |
    | Tarefa opcional do usuário<br/>        | Quando a tarefa é concluída.<br/>            |
    | CONHECIMENTO<br/>                       | Quando a notificação é removida.<br/> |



 

-   **Para o padrão de status de evento temporário, exiba o ícone enquanto o evento estiver acontecendo.**
-   Para todos os outros padrões, **exiba o ícone quando o programa, o recurso ou o processo estiver em execução e o ícone for relevante** , a menos que o usuário tenha apagado seu **ícone de exibição na opção área de notificação** (para obter mais informações, consulte menus de [contexto](#context-menus)). a maioria dos ícones fica oculta por padrão no Windows 7, mas pode ser promovida para a área de notificação pelo usuário.
-   **Não exiba ícones destinados a administradores a usuários padrão.** registre as informações no log de eventos Windows.

### <a name="where-to-show"></a>Onde mostrar

-   **Janelas de exibição iniciadas de ícones da área de notificação próximo à área de notificação.**

![Figura de uma janela próxima à área de notificação ](images/winenv-notification-image14.png)

Windows iniciado a partir de ícones da área de notificação são exibidos próximo à área de notificação.

### <a name="icons"></a>Ícones

-   **Escolha o ícone com base em seu padrão de design:**

    | Padrão                                                 | Tipo de ícone                                   |
    |--------------------------------------------------|------------------------------------|
    | Status do sistema e acesso<br/>              | Ícone de recurso do sistema<br/>     |
    | Status e acesso da tarefa em segundo plano<br/>     | Ícone de programa ou recurso<br/> |
    | Origem de notificação temporária<br/>         | Ícone de programa ou recurso<br/> |
    | Status do evento temporário<br/>                | Ícone de programa ou recurso<br/> |
    | Aplicativo de instância única minimizado<br/> | Ícone do programa<br/>            |

    

     

    ![captura de tela da área de notificação e ícones do Outlook ](images/winenv-notification-image15.png)

    Neste exemplo, o Outlook usa um ícone de recurso de email para uma fonte de notificação temporária e seu ícone de aplicativo para o aplicativo minimizado.

-   **Escolha um design de ícone facilmente reconhecível.** Prefira ícones com contornos exclusivos em vez de ícones em forma de quadrado ou retangular. Mantenha os designs simples preferir símbolos em vez de imagens realistas. Aplique as outras [diretrizes de ícone de estilo Aero](vis-icons.md) também.
-   **Use variações de ícone ou sobreposições para indicar alterações de status ou status.** Use variações de ícone para mostrar alterações em quantidades ou pontos fortes. Para outros tipos de status, use as sobreposições padrão a seguir. Use apenas uma única sobreposição e localize-a no canto inferior direito para consistência. 

    | Sobreposição                                                                                                       | Status                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![captura de tela do ícone de aviso pequeno ](images/winenv-notification-image16.png)<br/>               | Aviso<br/>               |
    | ![captura de tela do ícone de erro pequeno ](images/winenv-notification-image17.png)<br/>                 | Erro<br/>                 |
    | ![captura de tela do ícone pequeno desabilitado/desconectado ](images/winenv-notification-image18.png)<br/> | Desabilitado/Desconectado<br/> |
    | ![captura de tela do pequeno ícone bloqueado/offline ](images/winenv-notification-image19.png)<br/>       | Bloqueado/Offline<br/>       |

    

     

    ![captura de tela da área de notificação e dois ícones ](images/winenv-notification-image20.png)

    Neste exemplo, os ícones sem fio e bateria mostram alterações em quantidades ou pontos fortes.

    ![captura de tela da área de notificação e duas sobreposições ](images/winenv-notification-image21.png)

    Neste exemplo, as sobreposições são usadas para mostrar estados de erro e aviso.

-   **Evite problemas de vermelho puro, amarelo e verde em seus ícones base.** Para evitar confusão, reserve essas cores para comunicar o status. Se sua [identidade visual usar](exper-branding.md) essas cores, considere o uso de tons mudos para seus ícones de área de notificação base.
-   Para [escalonamento progressivo,](mess-notif.md)use ícones com uma aparência **progressivamente mais enfática** à medida que a situação se torna mais urgente.

    ![captura de tela da área de notificação e cinco ícones ](images/winenv-notification-image22.png)

    Nesses exemplos, a aparência do ícone de bateria se torna mais enfática à medida que a urgência aumenta.

-   **Não altere o status com muita frequência.** Os ícones da área de notificação não devem parecer barulhentos, instável ou exigir atenção. O olho é sensível a alterações no campo periférico da visão, portanto, as alterações de status precisam ser sutis.
    -   **Não altere o ícone rapidamente.** Se o status subjacente estiver mudando rapidamente, o ícone refletirá o status de alto nível.

        **Incorreto:**

        ![captura de tela da área de notificação e ícone de modem ](images/winenv-notification-image23.png)

        Neste exemplo, o ícone de modem exibe luzes piscando (como faz um modem de hardware), mas essas alterações de estado não são significativas para os usuários.

    -   **Não use animações de execução longa para mostrar atividades contínuas.** Essas animações são uma distração. A presença de um ícone na área de notificação indica suficientemente a atividade contínua.
    -   **Animações sutis e breves são aceitáveis para mostrar o progresso durante alterações de status transitivas e temporárias importantes.**

        ![captura de tela da área de notificação e ícone sem fio ](images/winenv-notification-image24.png)

        Neste exemplo, o ícone Sem fio exibe um indicador de atividade para mostrar que o trabalho está em andamento.

    -   **Não flash do ícone.** Fazer isso é muito perigoso. Se um evento exigir atenção imediata, use uma caixa de diálogo. Se o evento precisar de atenção, use uma notificação.

-   **Não desabilite ícones de área de notificação.** Se o ícone não se aplicar no momento, remova-o. No entanto, você poderá mostrar um ícone habilitado com uma sobreposição de status desabilitada se os usuários puderem habilitar no ícone.

    ![captura de tela da área de notificação e do controle deslizante de volume ](images/winenv-notification-image25.png)

    Neste exemplo, os usuários podem habilitar a saída de som do ícone.

Para ver exemplos e diretrizes gerais de ícone, consulte [Ícones](vis-icons.md).

### <a name="interaction"></a>Interação

**Observação:** Os eventos de clique a seguir devem ocorrer no mouse para cima, não para baixo.

**Passar o mouse**

-   **Exibe uma dica de ferramenta ou infotip que indica o que o ícone representa.**

    ![captura de tela da área de notificação e dica de ferramenta ](images/winenv-notification-image26.png)

    Neste exemplo, uma dica de ferramenta é usada para descrever o ícone ao passar o mouse.

Para obter diretrizes de texto de infotip, consulte [a seção Texto](#context-menus) deste artigo.

**Clique com o botão direito do mouse esquerdo**

-   **Exibe os usuários que mais provavelmente querem ver**, que podem ser:

    -   Uma janela de flyout, caixa de diálogo ou janela do programa com as configurações mais úteis e tarefas normalmente executadas. Para diretrizes de apresentação, consulte [Flyouts da área de notificação.](#notification-area-flyouts)

        ![captura de tela da área de notificação e dos flyouts ](images/winenv-notification-image27.png)

        Nesses exemplos, clicar com o botão esquerdo do mouse exibe janelas pop-up com as configurações mais úteis.

    -   Um flyout de status.

        ![captura de tela da área de notificação e do flyout de status ](images/winenv-notification-image28.png)

        Neste exemplo, clicar com o botão esquerdo do mouse exibe o flyout de status.

        -   O item do painel de controle relacionado.
        -   O menu de contexto.

    Os usuários esperam que os cliques esquerdos para exibir algo, portanto, não exibir nada faz com que um ícone de área de notificação pareça sem resposta.

-   **Exibir um menu de contexto somente se as outras opções não se aplicarem**, com o comando padrão em negrito. Nesse caso, exibe o mesmo menu de contexto mostrado no clique com o botão direito do mouse para evitar confusão.
-   **Prefira usar uma janela pop-up em vez de uma caixa de diálogo** para uma sensação mais leve. Mostrar apenas as configurações mais comuns e fazer com que elas tenham efeito imediato para uma interação mais simples. Descarte a janela pop-up se o usuário clicar em qualquer lugar fora da janela.
-   **Exibir janelas pequenas perto do ícone associado.** No entanto, janelas grandes, como itens do painel de controle, podem ser exibidas no centro do monitor padrão.

**Clique duas vezes à esquerda**

-   **Execute o comando padrão no menu de contexto.** Normalmente, isso exibe a interface do usuário primária associada ao ícone, como o item do painel de controle associado, a folha de propriedades ou a janela do programa.
-   **Se não houver nenhum comando padrão, execute a mesma ação que um clique à esquerda.**

**Clique com o botão direito em**

-   **Exibe o menu de contexto**, com o comando padrão em negrito.

### <a name="context-menus"></a>Menus de contexto

-   **Exibe o menu de contexto próximo ao ícone associado,** mas fora da barra de tarefas.
-   **O menu de contexto pode incluir os seguintes itens**, conforme apropriado, na ordem listada (o texto exato está entre aspas):

Comandos primários

Abrir (padrão, listar primeiro, em negrito)

Executar

Comandos secundários

< separador>

Suspender/retomar o comando habilitar/desabilitar (marca de seleção)

"Minimizada para a área de notificação" (marca de seleção)

Aceitar notificações (marca de seleção)

"Exibir ícone na área de notificação" (marca de seleção)

Separador de <>

Opções

"Sair"

-   **Remova em vez de desabilitar quaisquer itens de menu de contexto que não se apliquem.**
-   Para comandos abrir, executar e suspender/retomar, **seja específico sobre o que está sendo aberto, executado, suspenso e retomado.**

![Captura de tela que mostra uma área de notificação e comandos.](images/winenv-notification-image29.png)

neste exemplo, Windows Defender tem comandos específicos de abrir e executar.

-   **Use suspender/retomar executando tarefas em segundo plano, habilitar/desabilitar para todo o resto.**
-   **Use marcas de seleção para indicar o estado.** Liste e habilite todos os Estados e coloque a marca de seleção ao lado do estado atual. Não desabilite opções ou altere os rótulos de opção para indicar o estado atual.

**Correto:**

![captura de tela de um comando com marca de seleção ](images/winenv-notification-image29.png)

**Incorreto:**

![captura de tela de um comando sem marca de seleção ](images/winenv-notification-image30.png)

no exemplo incorreto, Windows Defender deve usar uma marca de seleção para indicar o estado atual.

-   **Todas as tarefas em segundo plano devem ter um comando suspender/retomar.** A escolha do comando deve suspender temporariamente a tarefa. Os usuários talvez queiram suspender temporariamente as tarefas em segundo plano para aumentar o desempenho do sistema ou reduzir o consumo de energia. as tarefas em segundo plano suspensas são reiniciadas quando retomadas pelo usuário ou quando Windows é reiniciada.
-   **Permita que os usuários aceitem ou cancelem tipos de notificação diferentes** se o programa tiver notificações que alguns usuários talvez não queiram ver. O padrão de notificação do [FYI](mess-notif.md) exige que os usuários aceitem, portanto, essas notificações devem ser desabilitadas por padrão.

![captura de tela de área de notificação e comandos ](images/winenv-notification-image31.png)

neste exemplo, Outlook permite que os usuários escolham as notificações que recebem do ícone.

-   **Limpar a opção "ícone de exibição na área de notificação" Remove o ícone da área de notificação**, mas não afeta o programa, o recurso ou o processo subjacente. Os usuários podem exibir novamente o ícone na caixa de diálogo opções do programa. não reexiba automaticamente o ícone quando Windows for reiniciado.
-   **o comando Exit encerra o programa para a sessão de Windows atual e remove o ícone.** Não terá um comando de saída se o programa não puder ser desligado. o programa é reiniciado quando Windows é reiniciado. Os usuários podem encerrar permanentemente o programa na caixa de diálogo opções.
-   **Não tem um comando about.** Essas informações devem ser comunicadas pelo ícone, sua InfoTip e o menu de contexto. Se os usuários desejarem mais informações, eles poderão exibir a interface do usuário principal.
    -   **Exceção:** Você poderá fornecer um comando about se o ícone for para um programa que não tenha presença na área de trabalho.

Para obter diretrizes e exemplos do menu de contexto geral, consulte [menus](cmd-menus.md).

### <a name="rich-tooltips"></a>Dicas de ferramenta avançadas

-   **Use dicas de ferramenta avançadas apenas para facilitar a compreensão das informações.** Não use dicas de ferramenta avançadas apenas para decorar o recurso. Se você não puder usar a riqueza para facilitar a compreensão das informações, use uma dica de ferramenta simples.

    **Incorreto:**

    ![captura de tela da área de notificação e dica de ferramenta avançada ](images/winenv-notification-image32.png)

    **Correto:**

    ![captura de tela da área de notificação e dica de ferramenta simples ](images/winenv-notification-image33.png)

    No exemplo incorreto, o ícone de calendário não torna a data mais fácil de entender.

-   **Use uma apresentação concisa.** Use um texto conciso e um layout conciso com um ícone de 32 pixels. As dicas de ferramenta espaçosom o risco de se desviarem, especialmente quando exibidas sem intenção.
-   **Não coloque controles ou elementos que pareçam interativos em uma dica de ferramenta sofisticada.** Dicas de ferramentas não são interativas e, portanto, não devem aparecer interativas Não use texto azul ou sublinhado.

    **Correto:**

    ![captura de tela de dica de ferramenta avançada com texto em preto ](images/winenv-notification-image34.png)

    **Incorreto:**

    ![captura de tela de dica de ferramenta avançada com texto azul ](images/winenv-notification-image35.png)

    No exemplo incorreto, o plano de energia atual parece ser um link, mas é impossível clicar em.

### <a name="notification-area-flyouts"></a>Submenus da área de notificação

-   Quando apropriado, apresente os submenus da área de notificação com três seções:
    -   **Resumo.** Exiba as mesmas informações exibidas na dica de ferramenta ou InfoTip do ícone, possivelmente com mais detalhes. Para consistência, use o mesmo texto e ícones e, geralmente, o mesmo layout (se estiver usando uma dica de ferramenta sofisticada). Ao contrário do infotips, essas informações podem ser acessadas ao usar o toque.
    -   **Tarefas comuns.** Apresente as tarefas executadas com mais frequência diretamente no submenu.
    -   **Links relacionados.** Forneça no máximo um de cada tipo dos seguintes links opcionais:
        -   Um link para a tarefa executada com mais frequência no painel de controle. Forneça se houver uma tarefa executada com frequência que não possa ser apresentada na seção tarefas comuns.
        -   Um link para o item do painel de controle relacionado. Esse item do painel de controle deve permitir que os usuários executem tarefas que não podem ser executadas na seção tarefas comuns.
        -   Um link para um tópico de ajuda específico e relevante. Siga as [diretrizes de link de ajuda](winenv-help.md)padrão.

![captura de tela da área de notificação e do submenu ](images/winenv-notification-image36.png)

Este exemplo mostra um submenu da área de notificação usando a apresentação recomendada.

### <a name="options-dialog-box"></a>caixa de diálogo Opções

-   As opções não acessíveis diretamente do menu de contexto devem estar na caixa de diálogo opções. Essa caixa de diálogo pode ser o painel de controle do recurso.
-   **A caixa de diálogo opções pode incluir os seguintes itens** conforme apropriado (o texto exato está entre aspas):
    -   Habilitar o \[ nome \] do recurso (caixa de seleção)
        -   Limpar essa opção encerra permanentemente o programa. O programa pode ser reiniciado a partir de seu item do painel de controle. o comando Exit no menu de contexto encerra o programa somente para a sessão de Windows atual.
    -   "Exibir ícone na área de notificação" (caixa de seleção)
        -   A remoção do ícone da área de notificação não afeta o recurso subjacente.
        -   A seleção dessa opção permite que o usuário restaure o ícone, o que, naturalmente, não pode ser feito a partir do próprio ícone.
-   Desabilite os recursos que raramente são usados, ou potencialmente irritantes ou distração. Permitir que os usuários [aceitem](glossary.md) esses recursos.

Para obter as diretrizes gerais da caixa de diálogo opções e exemplos, consulte [Windows de propriedades](win-property-win.md).

### <a name="minimizing-programs-to-the-notification-area"></a>Minimizando programas para a área de notificação

**observação: minimizar as janelas de programas na área de notificação não é mais recomendado para o Windows 7.** Use os botões normais [da barra de tarefas](winenv-taskbar.md) . Seu programa pode dar suporte a ambos os mecanismos para compatibilidade com versões anteriores.

-   Para reduzir a aglomeração da barra de tarefas, considere a possibilidade de minimizar os programas para a área de notificação somente se todos os itens a seguir se aplicarem:
    -   O programa pode ter apenas uma única instância.
    -   O programa é executado por um longo período de tempo.
    -   O ícone mostra o status.
    -   O ícone pode ser uma fonte de notificação.
    -   Isso é opcional e os usuários devem [optar por](glossary.md).
-   Use o botão Minimizar na barra de título do aplicativo, não no botão Fechar.

## <a name="text"></a>Texto

### <a name="infotips"></a>Infotips

-   A infotip do ícone deve ter um dos seguintes formatos (em que o nome da empresa é opcional):
    -   (Nome da empresa) Recurso, programa ou nome do dispositivo
    -   ![captura de tela do infotip com o nome da empresa ](images/winenv-notification-image37.png)
    -   (Nome da empresa) Recurso, programa ou nome do dispositivo – Resumo do status
    -   ![captura de tela do infotip exibindo o resumo do status ](images/winenv-notification-image38.png)
    -   (Nome da empresa) Instrução de status de recurso, programa ou nome do dispositivo.
    -   ![captura de tela da instrução de status de exibição de infotip ](images/winenv-notification-image39.png)
    -   (Nome da empresa) Recurso, programa ou nome do dispositivo
    -   Lista de status com cada item em uma linha separada
    -   ![captura de tela da lista de status de exibição do infotip ](images/winenv-notification-image40.png)

Frase infotip:

-   Concentre-se nas informações mais úteis. Exibir outras informações no clique único esquerdo.
-   Seja conciso. Use fragmentos de frase ou instruções simples.
-   Não use pontuação final, a menos que a dica seja formulada como uma frase completa.
-   Omita palavras desnecessárias. Não inclua a versão do software ou outras informações falsas.

    **Incorreto:**

    ![captura de tela de infotip com informações desnecessárias ](images/winenv-notification-image41.png)

    Neste exemplo, a infotip tem informações falsas.

-   Não explique como interagir com o ícone.

    **Incorreto:**

    ![captura de tela do infotip com instruções de clique com o botão direito do mouse ](images/winenv-notification-image42.png)

    Neste exemplo, o ícone conexão de rede sem fio fornece instruções de clique com o botão direito do mouse.

## <a name="documentation"></a>Documentação

Ao fazer referência à área de notificação:

-   Consulte a área de notificação como a área de notificação, não a bandeja do sistema.

Ao se referir a um ícone de área de notificação:

-   Consulte o ícone usando o nome exato dado em sua infotip, incluindo sua capitalização, seguida pelo ícone .
-   Para a primeira referência, consulte também a área de notificação.
-   Quando possível, forja o texto do título usando negrito. Caso contrário, coloque o título entre aspas somente se necessário para evitar confusão.

**Exemplo:** Para verificar rapidamente o status da rede, clique no **ícone** Rede na área de notificação.

 

