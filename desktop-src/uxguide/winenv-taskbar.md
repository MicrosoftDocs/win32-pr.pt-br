---
title: Barra de tarefas
description: A barra de tarefas é o ponto de acesso para programas exibidos na área de trabalho. com os novos recursos da barra de tarefas do Windows 7, os usuários podem fornecer comandos, acessar recursos e exibir o status do programa diretamente na barra de tarefas.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 86b63e5f3b3dc1e8cecba78cbb1599c305d738250d92f76055596226c9028727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117854045"
---
# <a name="taskbar"></a>Barra de tarefas

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

A barra de tarefas é o ponto de acesso para programas exibidos na área de trabalho. com os novos recursos da barra de tarefas do Windows 7, os usuários podem fornecer comandos, acessar recursos e exibir o status do programa diretamente na barra de tarefas.

A barra de tarefas é o ponto de acesso para os programas exibidos na área de trabalho, mesmo que o programa seja minimizado. Esses programas são considerados com presença na área de trabalho. Com a barra de tarefas, os usuários podem exibir as janelas primárias abertas e determinadas janelas secundárias na área de trabalho e podem alternar rapidamente entre elas.

![captura de tela da barra de tarefas com recursos chamados ](images/winenv-taskbar-image1.png)

a barra de tarefas do Microsoft Windows.

Os controles na barra de tarefas são chamados de botões da barra de tarefas. quando um programa cria uma janela primária (ou uma janela secundária com determinadas características), Windows adiciona um botão da barra de tarefas para essa janela e o remove quando essa janela é fechada.

os programas projetados para o Windows 7 podem aproveitar esses novos recursos de botão da barra de tarefas:

-   as listas de atalhos fornecem acesso rápido a destinos usados com frequência (como arquivos, pastas e links) e comandos por meio de um menu de contexto acessível no botão da barra de tarefas do programa e menu Iniciar item, mesmo que o programa não esteja em execução no momento.
-   As barras de ferramentas de miniatura fornecem acesso rápido a comandos usados com frequência para uma janela específica. As barras de ferramentas de miniatura aparecem na miniatura do botão da barra de tarefas.
-   Ícones de sobreposição mostram a alteração do status no ícone do botão da barra de tarefas do programa.
-   As barras de progresso mostram o progresso das tarefas de execução longa no botão da barra de tarefas do programa.
-   Os botões da barra de tarefas da subjanela permitem que os usuários usem miniaturas de botão da barra de tarefas para alternar diretamente para guias de janela, janelas de projeto, janelas filhas MDI (interface de vários documentos) e janelas secundárias.
-   Botões de barra de tarefas fixados permitem que os usuários fixem botões de programa na barra de tarefas para fornecer acesso rápido a programas mesmo quando eles não estão em execução.

Tecnicamente, a barra de tarefas estende a barra inteira do botão Iniciar para a área de notificação; mais comumente, no entanto, a barra de tarefas refere-se apenas à área que contém os botões da barra de tarefas. Para várias configurações de monitor, apenas um monitor tem uma barra de tarefas e esse monitor é o monitor padrão.

**Observação:** As diretrizes relacionadas à [área de trabalho](winenv-desktop.md), área de [notificação](winenv-notification.md)e gerenciamento de [janelas](win-window-mgt.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

os programas criados para o Windows 7 podem aproveitar esses recursos do botão da barra de tarefas. Faça as seguintes perguntas importantes para determinar se elas devem ser usadas ou não:

**Listas de atalhos**

-   **Os usuários geralmente precisam iniciar novas tarefas usando seu programa?** Nesse caso, considere fornecer uma lista de atalhos. Embora as listas de atalhos possam ser usadas para outras finalidades, a maioria dos cenários envolve a inicialização de uma nova tarefa.
-   **Os usuários geralmente precisam acessar arquivos, pastas, links ou outros recursos usados recentemente ou frequentemente?** Nesse caso, considere fornecer uma lista de atalhos para acessar esses recursos úteis.

    ![captura de tela da barra de tarefas com a lista de atalhos do Internet Explorer ](images/winenv-taskbar-image2.png)

    neste exemplo, Windows o Internet Explorer usa uma lista de atalhos para apresentar páginas visitadas com frequência.

-   **Os usuários geralmente precisam de acesso rápido a um pequeno número de comandos do seu programa ao usar outros programas, mesmo que o programa não esteja em execução?** Nesse caso, considere fornecer uma lista de atalhos com esses comandos usados com frequência. Esses comandos devem funcionar mesmo se o programa não estiver em execução e devem ser aplicados a todo o programa, não a uma janela específica. Como alternativa, considere fornecer uma barra de ferramentas de miniatura para comandos que se aplicam a uma janela específica.

    ![captura de tela da barra de tarefas com a lista de atalhos de notas auto-adesivas ](images/winenv-taskbar-image3.png)

    neste exemplo, o acessório Notas Autoadesivas permite que os usuários criem uma nova anotação rapidamente ao usar outros programas.

-   **Você está promovendo recursos novos, de uso único ou difíceis de encontrar?** Nesse caso, não use listas de atalhos porque elas não se destinam a essa finalidade. Em vez disso, melhore a descoberta de tais comandos diretamente no programa.

**Barras de ferramentas de miniatura**

Todas as seguintes condições se aplicam?

-   **Os comandos se aplicam a uma janela específica?** As barras de ferramentas de miniatura são para comandos que se aplicam a tarefas existentes, enquanto comandos de lista de atalhos são para iniciar novas tarefas.
-   **Os usuários precisam interagir com uma tarefa em execução rapidamente ao usar outros programas?** Nesse caso, as barras de ferramentas de miniatura são uma boa opção. As barras de ferramentas de miniatura podem apresentar um máximo de sete comandos, mas um máximo de cinco comandos geralmente é preferencial.
-   **Os comandos são imediatos?** Ou seja, eles não exigem entrada adicional? As barras de ferramentas de miniatura precisam ter comandos imediatos para serem eficientes, enquanto as listas de atalhos funcionam melhor com comandos que exigem entrada adicional.

    **Incorreto:**

    ![captura de tela da barra de tarefas com janelas sobrepostas ](images/winenv-taskbar-image4.png)

    Comandos que exigem entrada adicional não funcionam bem em barras de ferramentas de miniatura.

-   **Os comandos são diretos?** Ou seja, os usuários podem interagir com eles usando um único clique? As barras de ferramentas precisam ter comandos diretos para serem eficientes.
-   **Os comandos são bem representados por ícones?** Os comandos da barra de ferramentas de miniatura são apresentados usando ícones que não são rótulos de texto, enquanto comandos de lista de atalhos são representados por rótulos de texto

    **Incorreto:**

    ![captura de tela do comando de miniatura com ícone ](images/winenv-taskbar-image5.png)

    Neste exemplo, o comando não é bem representado por ícones.

**Ícones de sobreposição**

-   **O programa tem "presença de área de trabalho"?** Caso contrário, use um ícone de área de notificação em vez disso. nesse caso, considere usar um ícone de sobreposição em vez de colocar o status no ícone da área de notificação para programas criados para o Windows 7. Isso garante que o ícone sempre estará visível (quando ícones grandes forem usados) e consolida o programa com seu status em um único lugar.
-   **O ícone de sobreposição é exibido temporariamente para mostrar uma alteração de status?** Nesse caso, um ícone de sobreposição pode ser apropriado, dependendo dos seguintes fatores:
    -   **O status é útil e relevante ao usar outros programas?** Caso contrário, exiba as informações nas [barras de status](ctrl-status-bars.md) do programa ou em outra área de status do programa.

        ![captura de tela da barra de status da janela do Internet Explorer ](images/winenv-taskbar-image7.png)

        Neste exemplo, a barra de status é usada porque o status não é útil ao usar outros programas.

    -   **O status mostra o andamento?** Em caso afirmativo, use uma barra de progresso de botão da barra de tarefas.
    -   **O status é crítico? A ação imediata é necessária?** Nesse caso, exiba as informações de uma maneira que exija atenção e não pode ser facilmente ignorada, como uma [caixa de diálogo](win-dialog-box.md).

**Barras de progresso**

-   **Os comentários sobre o progresso são úteis e relevantes ao usar outros programas?** Ou seja, os usuários provavelmente podem monitorar o progresso ao usar outros programas e alterar seu comportamento como resultado? Esse status útil e relevante geralmente é exibido usando uma caixa de diálogo de progresso sem janela restrita ou uma página de progresso dedicada, mas não com um ponteiro ocupado, um indicador de atividade ou uma barra de progresso em uma barra de status. Se o status não for útil ao usar outros programas, basta exibir os comentários de progresso diretamente no próprio programa.

    **Correto:**

    ![captura de tela da caixa de diálogo de cópia com barra de progresso ](images/winenv-taskbar-image8.png)

    **Incorreto:**

    ![captura de tela da barra de progresso no botão da barra de tarefas ](images/winenv-taskbar-image9.png)

    No exemplo incorreto, a barra de progresso do botão da barra de tarefas não é muito útil.

-   **A tarefa é contínua?** Se a tarefa nunca for concluída, não será necessário mostrar seu progresso. Exemplos de tarefas contínuas incluem verificações de antivírus que não são iniciadas pelos usuários e indexação de arquivos.

    **Incorreto:**

    ![captura de tela do ícone de progresso de uma tarefa contínua ](images/winenv-taskbar-image10.png)

    Neste exemplo, uma tarefa contínua não precisa mostrar o progresso.

**Barras de tarefas da subjanela**

-   **Seu programa contém guias, janelas de projeto, janelas filhas MDI ou janelas secundárias que os usuários geralmente desejariam mudar diretamente?** Se sim, dar a essas janelas suas próprias miniaturas de botão da barra de tarefas pode ser apropriado.

## <a name="design-concepts"></a>Conceitos de design

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Usando listas de salto e barras de ferramentas em miniatura com eficiência

Listas de salto e barras de ferramentas em miniatura ajudam os usuários a acessar recursos e executar comandos com mais eficiência. No entanto, ao projetar como seu programa dá suporte a esses recursos, não aproveite a eficiência aprimorada para concedido. Se os usuários não puderem prever com precisão qual recurso tem o comando de que precisam ou se precisam verificar vários locais, eventualmente os usuários se frustram e param de usar esses recursos.

As listas de salto e as barras de ferramentas em miniatura funcionam em conjunto com mais eficiência quando estão:

-   **Claramente diferenciado.** Os usuários sabem quando procurar um destino ou comando em um Lista de Atalhos e quando procurar em uma barra de ferramentas em miniatura. Há uma finalidade clara para cada um, portanto, os usuários raramente confundam o conteúdo dos dois. Geralmente, as Listas de Saltos são usadas para iniciar novas tarefas, enquanto as barras de ferramentas em miniatura são usadas para interagir com tarefas em execução ao usar outros programas.
-   **Útil.** Os destinos e comandos oferecidos são aqueles de que os usuários precisam. Se não for provável que os usuários precisem de algo, ele não será incluído. Não use o número máximo de itens se eles não são necessários.
-   **Previsível.** Os destinos e comandos oferecidos são aqueles que os usuários esperam encontrar. Os usuários raramente têm que procurar em mais de um lugar.
-   **Bem organizado.** Os usuários podem encontrar o que estão procurando rapidamente. Eles usam rótulos descritivos, mas concisos, e ícones adequados para auxiliar no reconhecimento.

Certifique-se de fazer a pesquisa do usuário para certificar-se de que você está certo. Se, em última análise, você achar que não é possível criar Listas de Saltos e barras de ferramentas em miniatura que atingem essas metas, considere fornecer apenas uma delas. É melhor ter uma maneira previsível de dar comandos do que dois confusos.

## <a name="guidelines"></a>Diretrizes

### <a name="taskbar-buttons"></a>Botões da barra de tarefas

-   **Faça com que os seguintes tipos de janela apareçam na barra de tarefas (para Windows 7, usando uma miniatura do botão da barra de tarefas):**
    -   Janelas primárias (que inclui caixas de diálogo sem proprietários)
    -   Folhas de propriedade
    -   Caixas de diálogo progresso sem modo
    -   Assistentes
-   **Por Windows 7, use miniaturas do botão de barra de tarefas para agrupar os tipos de janela a seguir com o botão da barra de tarefas da janela primária em que ele foi lançado.** Cada programa (especificamente, cada programa percebido como um programa separado) deve ter um único botão de barra de tarefas.

    -   Janelas secundárias
    -   Guias do workspace
    -   Project janelas
    -   Janelas filho MDI

    **Correto:**

    ![captura de tela do Windows Explorer e da barra de progresso ](images/winenv-taskbar-image11.png)

    Neste exemplo, uma janela secundária é agrupada com o botão da barra de tarefas da janela primária.

    **Incorreto:**

    ![captura de tela do Windows Explorer e do painel de controle ](images/winenv-taskbar-image12.png)

    Neste exemplo, o Painel de Controle está agrupado incorretamente com Windows Explorer. Os usuários as percebem como programas separados.

    **Incorreto:**

    ![captura de tela do programa, da barra de progresso e de uma barra de tarefas ](images/winenv-taskbar-image13.png)

    Neste exemplo, o Backup do Windows usa incorretamente dois botões de barra de tarefas para um único programa.

-   **A restauração de uma janela primária também deve** restaurar todas as janelas secundárias, mesmo que essas janelas secundárias tenham seus próprios botões de barra de tarefas. Ao restaurar, coloque janelas secundárias sobre a janela primária.
-   **Por Windows 7, programas que normalmente têm a presença da área de trabalho podem exibir temporariamente um botão de barra de tarefas para mostrar o status.** Faça isso somente se o programa normalmente for exibido na área de trabalho e os usuários interagirem com ele com frequência. Um programa que normalmente é executado sem a presença da área de trabalho deve usar seu ícone de área de notificação, mesmo que ele nem sempre seja visível.

    **Incorreto:**

    ![captura de tela do botão da barra de tarefas do Windows Sync Center ](images/winenv-taskbar-image14.png)

    Neste exemplo, o Windows Central de Sincronização usa incorretamente um botão de barra de tarefas temporário para exibir o status. Em vez disso, ele deve usar seu ícone de área de notificação.

### <a name="icons"></a>Ícones

-   **Projete o ícone do programa para ficar ótimo na barra de tarefas.** Verifique se ele é significativo e reflete sua função e sua marca. Torná-lo distinto, torná-lo especial e garantir que ele renderiza bem em todos os tamanhos de ícone. Gaste o tempo necessário para fazer isso certo. Siga as [diretrizes do ícone de estilo aero.](vis-icons.md)
-   **Se o programa usar ícones de sobreposição, projete o ícone base do programa para lidar bem com sobreposições.** Os ícones de sobreposição são exibidos no canto inferior direito, portanto, projete o ícone para que essa área possa ser obscurecida.

    ![captura de tela de ícones e com sobreposição inferior direita ](images/winenv-taskbar-image15.png)

    Neste exemplo, o ícone de botão da barra de tarefas do programa não tem informações importantes na área inferior direita.

-   **Não use sobreposições no ícone base** do programa, independentemente de seu programa usar ícones de sobreposição ou não. O uso de uma sobreposição no ícone base será confuso porque os usuários terão que descobrir que ele não está se comunicando com o status.

    **Incorreto:**

    ![captura de tela do ícone base com sobreposição ](images/winenv-taskbar-image16.png)

    Neste exemplo, o ícone base do programa parece estar mostrando o status.

Para ver exemplos e diretrizes gerais de ícone, consulte [Ícones](vis-icons.md).

### <a name="overlay-icons"></a>Ícones de sobreposição

-   **Use ícones de sobreposição para indicar apenas status útil e relevante.** Considere a exibição de um ícone de sobreposição como uma possível interrupção do trabalho do usuário, portanto, a alteração de status deve ser importante o suficiente para superar uma interrupção potencial.

    **Incorreto:**

    ![captura de tela de três ícones de sobreposição ](images/winenv-taskbar-image17.png)

    Nesses exemplos, o ícone de sobreposição não é importante o suficiente para superar uma possível interrupção.

-   **Use ícones de sobreposição para status temporário.** Os ícones de sobreposição perdem seu valor se exibidos constantemente, portanto, o status normal do programa não deve mostrar um ícone. Remova o ícone de sobreposição quando o ícone:

    -   **É para um problema:** Remova o ícone depois que o problema for resolvido.
    -   **Alertas de que algo é novo:** Remova o ícone depois que o usuário tiver ativado o programa.

    **Exceção:** Seu programa pode exibir constantemente um ícone de sobreposição se os usuários sempre precisam saber seu status.

    ![captura de tela do live messenger com ícone de sobreposição ](images/winenv-taskbar-image18.png)

    Neste exemplo, o Windows Live Messenger sempre exibe um ícone de sobreposição para que os usuários sempre possam verificar sua presença relatada.

-   **Não exibir um ícone para indicar que um problema foi resolvido.** Em vez disso, basta remover qualquer ícone anterior que indique um problema. Suponha que os usuários normalmente esperam que seu programa seja executado sem problemas.
-   **Exibe ícones de sobreposição ou ícones de área de notificação, mas nunca ambos.** Seu programa pode dar suporte a ambos os mecanismos para compatibilidade com compatibilidade com backward, mas se o programa exibir o status usando ícones de sobreposição, ele também não deverá usar ícones de área de notificação para status.

    **Incorreto:**

    ![captura de tela da barra de tarefas com o ícone exibido duas vezes ](images/winenv-taskbar-image19.png)

    Neste exemplo, o novo ícone de email é exibido com redundância.

-   **Não piscar o botão da barra de tarefas para chamar a atenção para uma alteração de status.** Fazer isso seria muito perigoso. Permitir que os usuários descubram ícones de sobreposição por conta própria.
-   **Prefira ícones de sobreposição padrão para indicar alterações de status ou status.** Use estes ícones de sobreposição padrão: 

    | Sobreposição | Status |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | ![captura de tela do ícone de aviso pequeno ](images/winenv-taskbar-image20.png)<br/>               | Aviso<br/>               |
    | ![captura de tela do ícone de erro pequeno ](images/winenv-taskbar-image21.png)<br/>                 | Erro<br/>                 |
    | ![captura de tela do ícone pequeno desabilitado/desconectado ](images/winenv-taskbar-image22.png)<br/> | Desabilitado/Desconectado<br/> |
    | ![captura de tela do pequeno ícone bloqueado/offline ](images/winenv-taskbar-image23.png)<br/>       | Bloqueado/Offline<br/>       |

    

     

-   **Para ícones de sobreposição personalizados, escolha um design facilmente reconhecível.** Use ícones de cor completos de 16 x 16 pixels de alta qualidade. Prefira ícones com contornos distintos em vez de ícones em forma de quadrado ou retangular. Aplique as outras [diretrizes de ícone de estilo Aero](vis-icons.md) também.
-   **Mantenha o design de ícones de sobreposição personalizados simples.** Não tente comunicar ideias complexas, desconhecidas ou abstratas. Se você não conseguir pensar em um ícone personalizado adequado, use um ícone padrão de erro ou ícone de aviso quando apropriado. Esses ícones podem ser usados com eficiência para comunicar muitos tipos de status.
-   **Não altere o status com muita frequência.** Os ícones de sobreposição não devem parecer barulhentos, instável ou exigir atenção. O olho é sensível a alterações no campo periférico da visão, portanto, as alterações de status precisam ser sutis.
    -   **Não altere o ícone rapidamente.** Se o status subjacente estiver mudando rapidamente, o ícone refletirá o status de alto nível.

        **Incorreto:**

        ![captura de tela do ícone de sobreposição em dois estados ](images/winenv-taskbar-image24.png)

        Neste exemplo, o ícone de sobreposição que muda rapidamente exige atenção.

    -   **Não use animações.** Fazer isso é muito perigoso.
    -   **Não flash do ícone.** Fazer isso é muito perigoso. Se um evento exigir atenção imediata, use uma caixa de diálogo. Se o evento precisar de atenção, use uma notificação.

### <a name="taskbar-button-flashing"></a>Botão da barra de tarefas piscando

-   **Use o botão da barra de tarefas piscando com moderação para exigir a atenção imediata do usuário para manter uma tarefa em execução.** É difícil para os usuários se concentrarem enquanto um botão da barra de tarefas está piscando, portanto, suponha que eles interrompam o que estão fazendo para fazê-lo parar. Ao piscar um botão de barra de tarefas é melhor do que roubar o foco de entrada, os botões da barra de tarefas intermitentes ainda são muito invasivos. Certifique-se de que a interrupção seja justificada, como para indicar que o usuário precisa salvar dados antes de fechar uma janela. Programas inativos raramente devem exigir ação imediata. Não ative o botão da barra de tarefas se a única coisa que o usuário precisa fazer é ativar o programa, ler uma mensagem ou ver uma alteração no status.
-   **Se a ação imediata não for necessária, considere estas alternativas:**
    -   Use uma [notificação de êxito de](mess-notif.md) ação para indicar que uma tarefa foi concluída.
    -   Não fazer nada. Basta aguardar que os usuários participem do problema na próxima vez que ativarem o programa. Geralmente, essa é a melhor opção.
-   **Se um programa inativo exigir atenção imediata, flash seu botão de barra de tarefas para chamar a atenção e deixá-lo realçada.** Não faça mais nada: não restaure nem ative a janela e não reproduza nenhum efeito de som. Em vez disso, respeitar a seleção de estado da janela do usuário e permitir que o usuário ative a janela quando estiver pronto.
-   **Para janelas secundárias que têm um botão de barra de tarefas, flash seu botão em vez do botão da barra de tarefas da janela primária.** Isso permite que os usuários participem diretamente da janela.
-   **Para janelas secundárias que não têm um botão de barra de tarefas, flash do botão da barra de tarefas da janela primária e colocar a janela secundária sobre todas as outras janelas para esse programa.** As janelas secundárias que exigem atenção devem ser mais alta para garantir que os usuários as vejam.
-   **Flash apenas um botão de barra de tarefas para uma janela por vez.** A exibição de mais de um botão é desnecessária e muito distração.
-   **Remova o realçador do botão da barra de tarefas depois que o programa ficar ativo.**
-   **Quando o programa ficar ativo, certifique-se de que haja algo óbvio a fazer.** Normalmente, esse objetivo é realizado exibindo uma caixa de diálogo que faz uma pergunta ou inicia uma ação.

### <a name="quick-launch-shortcuts"></a>Início Rápido atalhos

-   **Coloque atalhos de programa na área Início Rápido somente se os usuários optarem.** Como Início Rápido foi removido do Windows 7, os programas projetados para o Windows 7 não devem adicionar atalhos de programa à área Início Rápido ou fornecer opções para fazer isso.

### <a name="jump-lists"></a>Listas de saltos

**Projetar**

-   **Projete Listas de Saltos para atender às metas dos usuários para suas tarefas diárias.** Considere:
    -   **A finalidade do programa.** Pense no que os usuários têm mais probabilidade de fazer em seguida. Para programas de criação de documentos, os usuários provavelmente retornarão aos documentos usados recentemente. Para programas que mostram conteúdo existente, os usuários podem querer acesso aos recursos que usam com frequência. Para outros programas, os usuários podem provavelmente realizar tarefas que não realizaram antes, como ler novas mensagens, assistir a novos vídeos ou verificar sua próxima reunião.
    -   **O que os usuários mais se importam.** Pense em por que os usuários usariam o Lista de Atalhos em vez de outros meios. Por exemplo, os usuários têm maior probabilidade de se preocupar com destinos que identificaram explicitamente como importantes (como usuários de endereços Web colocados na barra de links ou em Favoritos ou digitados). Eles têm menos probabilidade de se preocupar com aqueles obtidos indiretamente ou com pouco esforço (como endereços Web visitados por meio de redirecionamento ou clicando em links).

        **Correto:**

        ![captura de tela da lista de saltos com um link para um destino ](images/winenv-taskbar-image25.png)

        **Incorreto:**

        ![captura de tela da lista de saltos com cinco links para o destino ](images/winenv-taskbar-image26.png)

        No exemplo incorreto, o Lista de Atalhos contém muitos destinos que os usuários provavelmente não se importam.

-   **Não torna os destinos muito granulares.** Tornar os destinos muito estreitos e específicos pode resultar em redundância, com várias maneiras de ir para o mesmo local. Por exemplo, em vez de listar páginas da Web individuais, liste home pages de nível superior; em vez de listar músicas, listar os álbums.

    **Correto:**

    ![captura de tela da lista de saltos organizada por grupos ](images/winenv-taskbar-image27.png)

    **Incorreto:**

    ![captura de tela da lista de saltos organizada por músicas ](images/winenv-taskbar-image28.png)

    No exemplo incorreto, listar músicas em um Lista de Atalhos o preencherá com um único álbum.

-   **Não preencha todos os slots Lista de Atalhos disponíveis se não for necessário.** Concentre Lista de Atalhos conteúdo nos itens mais úteis se o programa tiver apenas três itens úteis, forneça apenas três. Quanto mais itens em um Lista de Atalhos, mais esforço será necessário para encontrar qualquer item específico.

    ![captura de tela da lista de saltos com um comando ](images/winenv-taskbar-image29.png)

    Neste exemplo, o Notas Autoadesivas acessórios fornece um único Lista de Atalhos, porque isso é tudo o que é necessário.

-   **Forneça dicas de ferramenta somente quando necessário para ajudar os usuários a entender Lista de Atalhos itens.** Evite dicas de ferramenta redundantes porque elas são uma distração desnecessária. Para obter mais diretrizes de dica de ferramenta, consulte [Dicas de ferramenta e Infotips](ctrl-tooltips-and-infotips.md).

    **Incorreto:**

    ![captura de tela da lista de saltos com dica de ferramenta redundante ](images/winenv-taskbar-image30.png)

    Neste exemplo, a dica Lista de Atalhos ferramenta é redundante.

**Lista de Atalhos recursos vs. recursos do programa**

-   **Não disponibilizar destinos e comandos apenas por meio de Listas de Saltos.** Os mesmos destinos e comandos devem estar disponíveis diretamente do próprio programa.
-   **Use nomes consistentes para destinos e rótulos para comandos.** Lista de Atalhos itens devem ser rotulados da mesma forma que os itens equivalentes acessados diretamente do programa.
-   **Habilita seu programa para manipular destinos e comandos mesmo quando o programa não está em execução.** Isso é necessário para uma experiência consistente, confiável e conveniente.

**Agrupamento**

-   **Forneça pelo menos um e, no máximo, três grupos.** Lista de Atalhos itens são sempre agrupados para rotular sua finalidade. Ter mais de três grupos torna os itens mais difíceis de encontrar.
-   **Use nomes de grupo padrão quando apropriado.** Os nomes de grupo padrão são familiares e mais fáceis de entender para os usuários.

    Os comandos receberão o nome do grupo Tarefas, que é atribuído por Windows e, portanto, não pode ser alterado.

    **Correto:**

    ![captura de tela da lista de saltos com o nome do grupo recente ](images/winenv-taskbar-image31.png)

    **Incorreto:**

    ![captura de tela da lista de saltos com o nome do grupo de histórico ](images/winenv-taskbar-image32.png)

    Recente é o melhor nome de grupo porque é familiar e a distinção sutil entre histórico e recente não vale a pena fazer.

**Comandos**

-   **Forneça um conjunto fixo de comandos, independentemente do estado de execução do programa, do documento atual ou do usuário atual.** Os comandos devem ser aplicados a todo o programa, não a uma janela ou documento específico. Isso é necessário para uma experiência consistente, confiável e conveniente. Os comandos não devem ser removidos ou desabilitados.

    **Exceções:** Você pode substituir ou remover comandos quando:

    -   Um conjunto de comandos mutuamente exclusivos compartilha um único slot de comando, desde que um comando sempre se aplique.
    -   Os comandos não se aplicam até que recursos específicos tenham sido usados, desde que os comandos sempre se apliquem.

    **Incorreto:**

    ![captura de tela da lista de saltos com tarefa de impressão ](images/winenv-taskbar-image33.png)

    Neste exemplo, Imprimir não é um bom comando Lista de Atalhos porque depende do documento atual.

    **Correto:**

    ![captura de tela da lista de saltos com a saída e a saída ](images/winenv-taskbar-image34.png)

    Neste exemplo, Entrar e Sair são comandos mutuamente exclusivos. Além disso, separadores são usados para agrupar comandos relacionados.

-   **Use os seguintes rótulos de comando padrão quando apropriado.** Os rótulos de comando padrão são mais fáceis de entender para os usuários.
-   **Apresente os comandos em uma ordem lógica.** Os pedidos comuns incluem por frequência de uso ou ordem de uso. Coloque comandos altamente relacionados ao lado uns dos outros. Dentro do grupo Tarefas, coloque separadores entre grupos de comandos relacionados, conforme necessário.
-   **Não forneça comandos para abrir ou fechar o programa.** Esses comandos são integrados a todas as Listas de Saltos.

**Ícones de comando**

-   **No grupo Tarefas,** forneça um ícone de comando somente quando ajudar os usuários a entender, reconhecer ou diferenciar comandos, especialmente quando houver um ícone estabelecido para o comando usado no programa.

    -   **Exceção:** Se o programa usar ambos os destinos (que sempre têm ícones) e comandos, considere fornecer ícones para todos os comandos, caso não o tenha feito, pareceria estranho.

    **Incorreto:**

    ![captura de tela do uso inconsistente da lista de saltos de ícones ](images/winenv-taskbar-image35.png)

    Neste exemplo, o Internet Explorer deve fornecer ícones para todos os comandos para evitar uma aparência complicada.

**Destinos**

-   **Forneça um conjunto dinâmico de destinos específicos para o usuário atual, mas independentemente do programa que executa o estado ou o documento atual.** Conforme mencionado anteriormente, certifique-se de que eles se ajustam à finalidade do programa, são o que os usuários mais se importam e têm o nível certo de especificidade.
-   **Quando adequado, use uma lista de destino "automática".** Destinos automáticos são gerenciados por Windows, mas seu programa controla os destinos específicos que são passados.
    -   Considere usar Recente para programas de criação de documentos em que os usuários provavelmente retornarão aos destinos usados recentemente.

        ![captura de tela da lista de saltos com o nome do grupo 'recente' ](images/winenv-taskbar-image36.png)

        Neste exemplo, o Windows Bloco de notas usa Destinos recentes.

    -   Considere usar Frequente para programas que mostram conteúdo existente, em que os usuários provavelmente retornarão aos itens que eles usam com frequência. Destinos frequentes são classificar em ordem de frequência, sendo os mais frequentes primeiro.

        ![captura de tela da lista de saltos com o nome do grupo frequente ](images/winenv-taskbar-image37.png)

        Neste exemplo, o Windows Explorer usa destinos frequentes.

    -   Use Frequente se Recente resultar em muitos destinos inúteis. As listas frequentes são mais estáveis e a melhor opção quando os usuários vão para muitos destinos diferentes, mas provavelmente não retornarão aos raramente usados.

        **Incorreto:**

        ![captura de tela da lista de saltos com vários itens recentes ](images/winenv-taskbar-image38.png)

        Usar Recente no Windows Internet Explorer resultaria em muitos destinos inúteis.

    -   Se Recentes ou Frequentes são opções igualmente adequadas, use Recente porque essa abordagem é mais fácil para os usuários entenderem e é mais previsível.
    -   Se estiver usando Recente e o programa tiver um equivalente no menu Arquivo, faça com que as listas tenham o mesmo conteúdo na mesma ordem. Para os usuários, elas devem parecer ser as mesmas listas.

-   **Quando necessário, use uma lista de destino personalizada.** Seu programa tem controle total sobre o conteúdo e a ordem de classificação de uma lista de destino personalizada e, portanto, pode basear a lista em qualquer fator.
    -   Crie versões personalizadas de Recentes ou Frequentes se elas são adequadas, mas o gerenciamento automático não funciona bem para seu programa. Por exemplo, seu programa pode precisar acompanhar uma variedade de fatores além dos comandos de arquivo abertos. Nesse caso, use o mesmo nome (Recente ou Frequente) e a ordem de classificação porque os usuários não estarão cientes da diferença.
    -   Caso contrário, use um tipo diferente de destino para atender melhor às metas do usuário. Geralmente, essas listas ajudam os usuários a executar tarefas que ainda não realizaram, como ler novas mensagens, assistir a novos vídeos ou verificar sua próxima reunião.

        ![captura de tela da lista de saltos com o nome do grupo 'new' ](images/winenv-taskbar-image39.png)

        Neste exemplo, Windows Media Center lista os registros recentes mostram que o usuário ainda não viu.

    -   Escolha uma ordem de classificação que corresponda ao modelo mental do usuário da lista. Por exemplo, uma lista de estilos de coisas a fazer teria a próxima coisa a fazer listada primeiro. Se não houver nenhum modelo mental claro, classificar a lista de destino em ordem alfabética.

-   **Não use várias listas de destino que dão exibições diferentes dos mesmos dados.** Em vez disso, várias listas de destino devem ter principalmente dados diferentes para dar suporte a cenários de diferença. Por exemplo, você pode fornecer uma lista Recente ou uma lista Frequente, mas não ambos. Fazer isso é desperdício se itens sobrepostos estão presentes, mas confuso se itens sobrepostos são removidos.

    **Incorreto:**

    ![captura de tela da lista de saltos com itens de grupo repetidos ](images/winenv-taskbar-image40.png)

    Neste exemplo, é desperdício fornecer diferentes exibições dos mesmos destinos.

    **Correto:**

    ![captura de tela da lista de saltos com tarefas bem organizadas ](images/winenv-taskbar-image41.png)

    Neste exemplo, as listas de destino têm dados diferentes para tarefas diferentes.

-   **Se o programa tiver um comando para limpar os dados para privacidade, limpe também as listas Destinos.** As listas de destino podem conter dados confidenciais.

### <a name="thumbnail-toolbars"></a>Barras de ferramentas em miniatura

**Interação**

-   **Forneça até sete dos comandos mais importantes e usados com frequência que se aplicam à janela mostrada na miniatura.** Não se sinta obrigado a fornecer o máximo de comandos possível se o programa tiver apenas três comandos importantes e usados com frequência, forneça apenas três.

    **Incorreto:**

    ![captura de tela da barra de ferramentas com muitos comandos ](images/winenv-taskbar-image42.png)

    Neste exemplo, a barra de ferramentas em miniatura tem comandos que não são importantes.

-   **Use comandos diretos e imediatos.** Esses comandos devem ter um efeito imediato ao clicar no comando não devem exibir um menu suspenso ou uma caixa de diálogo para obter mais entrada.

    **Incorreto:**

    ![captura de tela da miniatura com o menu suspenso ](images/winenv-taskbar-image43.png)

    Os comandos da barra de ferramentas em miniatura devem ter um efeito imediato.

-   **Desabilitar comandos que não se aplicam ao contexto atual ou que resultariam diretamente em um erro.** Não o oculta porque fazer isso torna a apresentação da barra de ferramentas instável.
-   **Não descarte a miniatura quando os usuários clicarem em um comando se eles provavelmente revisarem os resultados ou clicarem imediatamente em outro comando.** Remova a miniatura para comandos que indicam que o usuário foi concluído por enquanto, como com comandos que exibem outras janelas.

    ![captura de tela da miniatura do player de mídia com o comando ](images/winenv-taskbar-image44.png)

    Neste exemplo, clicar em Próximo no Windows Media Player continua a exibir a miniatura porque os usuários talvez queiram dar outros comandos.

    ![captura de tela da miniatura com o ícone de chat ](images/winenv-taskbar-image45.png)

    Neste exemplo, clicar em Chat Windows Live Messenger a miniatura porque os usuários têm maior probabilidade de enviar uma mensagem.

**Apresentação**

-   **Certifique-se de que os ícones da barra de ferramentas em miniatura estão em conformidade com as diretrizes do ícone de estilo aero.** Para cada comando, forneça ícones de cor completo de alta qualidade 16x16, 20x20 e 24x24 pixels. As versões maiores são usadas em modos de exibição de alto dpi.
-   **Certifique-se de que os ícones estão claramente visíveis em relação à cor da tela de fundo da barra de ferramentas nos estados normal e de foco.** Sempre avalie ícones no contexto e nos modos de alto contraste.
-   **Escolha designs de ícone de comando que comuniquem claramente seu efeito.** Ícones de comando bem projetados são autoexplicativos para ajudar os usuários a encontrar e entender comandos com eficiência.
-   **Escolha ícones reconhecíveis e diferenciáveis.** Certifique-se de que os ícones tenham cores e formas distintas. Isso ajuda os usuários a encontrar os comandos rapidamente, mesmo que eles não se lembre do símbolo de ícone. Após o uso inicial, os usuários não devem depender de dicas de ferramenta para distinguir entre os comandos.
-   **Forneça uma dica de ferramenta para rotular cada comando.** Uma dica de ferramenta boa rotula o controle sem rótulo que está sendo apontado. Para obter diretrizes e exemplos, consulte [Dicas de ferramenta e Infotips](ctrl-tooltips-and-infotips.md).

### <a name="progress-bars"></a>Barras de progresso

-   **Siga as diretrizes da barra de** progresso geral, incluindo não reiniciar ou fazer o back-up do progresso e usar uma barra de progresso vermelha para indicar um problema.
-   **Evite usar barras de progresso indeterminadas.** Barras de progresso indeterminadas mostram a atividade, não o progresso. Reserve barras de progresso indeterminadas para essas situações raras em que os usuários não levam atividades como concedidas.

Para obter mais diretrizes, consulte [Barras de progresso.](progress-bars.md)

## <a name="text"></a>Texto

### <a name="window-titles"></a>Títulos da janela

Ao escolher títulos de janela, considere a aparência do título na barra de tarefas:

-   Otimize os títulos para exibição na barra de tarefas colocando concisamente as informações de distinção primeiro.
-   Para caixas de diálogo de progresso sem modo, primeiro resumir o progresso. Exemplo: "66% concluído".
-   Evite títulos de janela que tenham truncamentos complicados.

    **Incorreto:**

    ![captura de tela do título que corta o nome do programa ](images/winenv-taskbar-image48.png)

    Neste exemplo, o título da janela truncada tem resultados desafortunados.

### <a name="jump-list-commands"></a>Lista de Atalhos comandos

-   **Iniciar comandos com um verbo.**
-   **Use a capitalização com estilo de frase.**

Para obter mais diretrizes de rótulo de comando, consulte [Menus](cmd-menus.md).

## <a name="documentation"></a>Documentação

Ao fazer referência à barra de tarefas:

-   Consulte a barra inteira como a barra de tarefas (uma única palavra composta em minúsculas).
-   Consulte itens na barra de tarefas especificamente por seu rótulo ou geralmente como botões da barra de tarefas.
-   Quando possível, forja os rótulos da barra de tarefas usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.
-   Consulte ícones de sobreposição como ícones de botão da barra de tarefas. Não as veja como notificações, mesmo que sua finalidade seja notificar os usuários. No entanto, você pode dizer que esses ícones notificam os usuários sobre eventos específicos.

Exemplo: o ícone de botão da barra de tarefas Novo Email notifica que uma nova mensagem de email chegou.

 

