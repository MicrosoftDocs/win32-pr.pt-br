---
title: Caixas de diálogo (noções básicas de design)
description: Uma caixa de diálogo é uma janela secundária que permite aos usuários executar um comando, faz uma pergunta aos usuários ou fornece aos usuários informações ou comentários de progresso.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0e0deb28a706436e4d33ece35a40c26bd7499e0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444847"
---
# <a name="dialog-boxes-design-basics"></a>Caixas de diálogo (noções básicas de design)

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma caixa de diálogo é uma janela secundária que permite aos usuários executar um comando, faz uma pergunta aos usuários ou fornece aos usuários informações ou comentários de progresso.

![captura de tela identificando elementos da caixa de diálogo ](images/win-dialog-box-image1.png)

Uma caixa de diálogo típica.

As caixas de diálogo consistem em uma barra de título (para identificar o comando, o recurso ou o programa de onde veio uma caixa de diálogo), uma instrução principal opcional (para explicar o objetivo do usuário com a caixa de diálogo), vários controles na área de conteúdo (para apresentar opções) e botões de confirmação (para indicar como o usuário deseja se comprometer com a tarefa).

As caixas de diálogo têm dois tipos fundamentais:

-   **As caixas de diálogo modais** exigem que os usuários concluam e fechem antes de continuar com a janela do proprietário. Essas caixas de diálogo são mais bem usadas para tarefas críticas ou pouco frequentes que exigem conclusão antes de continuar.
-   **As caixas de diálogo sem modo** permitem que os usuários alternem entre a caixa de diálogo e a janela do proprietário conforme desejado. Essas caixas de diálogo são mais bem usadas para tarefas frequentes, repetitivas e em movimento.

**Uma caixa de diálogo de tarefa é uma caixa de diálogo implementada usando a API (interface de programação de aplicativo) da caixa de diálogo de tarefa.** Elas consistem nas seguintes partes, que podem ser montadas em uma variedade de combinações:

-   Uma **barra de título** para identificar o recurso do aplicativo ou do sistema de onde veio a caixa de diálogo.
-   Uma **instrução principal**, com um ícone opcional, para identificar o objetivo do usuário com a caixa de diálogo.
-   Uma **área de conteúdo** para controles e informações descritivas.
-   Uma **área de comando** para botões de commit, incluindo um botão Cancelar e opções mais opcionais e Não mostrar isso <item> controles novamente.
-   Uma **área de nota de rodapé** para explicações adicionais opcionais e ajuda, normalmente direcionada a usuários menos experientes.

![captura de tela de uma caixa de diálogo de tarefa típica ](images/win-dialog-box-image2.png)

Uma caixa de diálogo de tarefa típica.

**As caixas de diálogo de tarefa são recomendadas sempre que apropriados porque são fáceis de criar e atingem uma aparência consistente.** As caixas de diálogo de tarefa exigem o Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Microsoft Windows.

Um painel de tarefas é como uma caixa de diálogo, exceto que ele é apresentado dentro de um painel de janela em vez de uma janela separada. Como resultado, os painéis de tarefas têm uma sensação mais direta e contextual do que as caixas de diálogo. Embora tecnicamente eles não sejam os mesmos, os painéis de tarefas são tão semelhantes às caixas de diálogo que suas diretrizes são **apresentadas neste artigo.**

![captura de tela de um painel de tarefas típico ](images/win-dialog-box-image3.png)

Um painel de tarefas típico.

[As janelas](win-property-win.md) de propriedades são um tipo especializado de caixa de diálogo usada para exibir e alterar propriedades de um objeto, coleção de objetos ou um programa. Além disso, as janelas de propriedades normalmente suportam várias tarefas, enquanto as caixas de diálogo normalmente suportam uma única tarefa ou etapa em uma tarefa. Como seu uso é especializado, **as janelas de propriedades são abordadas em um conjunto diferente de diretrizes**.

As caixas de diálogo [podem ter guias](ctrl-tabs.md)e, se for o caso, são chamadas caixas de diálogo com guias. As janelas de propriedades são determinadas pela apresentação das propriedades, não pelo uso de guias.

**Observação:** As diretrizes relacionadas ao [layout,](vis-layout.md)gerenciamento de [janelas,](win-window-mgt.md)caixas de diálogo [comuns,](win-property-win.md)janelas de propriedades, [assistentes,](win-wizards.md)confirmações, [](mess-error.md)mensagens de erro e mensagens [de](mess-warn.md) aviso são [apresentadas](mess-confirm.md)em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **A finalidade é fornecer informações aos usuários, fazer uma pergunta aos usuários ou permitir que os usuários selecionem opções para executar um comando ou tarefa?** Caso não, use outra interface do usuário.
-   **A finalidade é exibir e alterar as propriedades de um objeto, coleção de objetos ou um programa?** Em caso afirmado, use uma [janela de propriedades](win-property-win.md) ou uma barra de [ferramentas.](cmd-toolbars.md)
-   **A finalidade é apresentar uma coleção de comandos ou ferramentas?** Em caso afirmado, use uma barra de ferramentas [ou uma janela de paleta](glossary.md).
-   **A finalidade é verificar se o usuário deseja continuar com uma ação?** Há um motivo claro para não continuar e uma chance razoável de que, às vezes, os usuários não continuarão? Em caso afirmado, use uma [confirmação](mess-confirm.md).
-   **A finalidade é dar uma mensagem de erro ou de aviso?** Em caso afirmado, use uma [mensagem de erro](mess-error.md) ou uma mensagem de [aviso](mess-warn.md).
-   É a finalidade de:
    -   Abrir arquivos
    -   Salvar arquivos
    -   Abrir pastas
    -   Encontrar ou substituir texto
    -   Imprimir um documento
    -   Selecionar atributos de uma página impressa
    -   Selecionar uma fonte
    -   Escolher uma cor
    -   Procurar um arquivo, pasta, computador ou impressora
    -   Pesquisar usuários, computadores ou grupos no Microsoft Active Directory
    -   Solicitar um nome de usuário e senha?

Em caso afirmaível, use a caixa [de diálogo comum](win-common-dlg.md) apropriada. Muitos desses diálogos comuns são extensíveis.

-   **A finalidade é executar uma tarefa de várias etapas que requer mais de uma única janela?** Em caso afirmado, use um [fluxo de tarefas](glossary.md) ou um [assistente.](win-wizards.md)
-   **A finalidade é informar os usuários sobre um evento de sistema ou programa que não está relacionado à atividade do usuário atual, que não exige ação imediata do usuário e os usuários podem ignorar livremente?** Em caso afirmado, use uma [notificação.](mess-notif.md)
-   **A finalidade é mostrar o status do programa?** Em caso afirmado, use uma [barra de status.](ctrl-status-bars.md)
-   **Seria preferível usar a interface do usuário in-locar?** As caixas de diálogo podem quebrar o fluxo do usuário exigindo atenção. Às vezes, essa quebra no fluxo é justificada, como quando o usuário deve executar uma ação que está fora do contexto atual. Em outros casos, uma abordagem melhor é apresentar a interface do usuário no contexto, seja diretamente com a interface do usuário in-loque (como um painel de tarefas) ou sob demanda usando a divulgação [progressiva.](ctrl-progressive-disclosure-controls.md)
-   **A finalidade é exibir um problema de entrada de usuário não crítico ou uma condição especial?** Em caso afirmado, use um [balão.](ctrl-balloons.md)
-   **Para fluxos de tarefas, seria preferível usar outra página?** Geralmente, você deseja que uma tarefa flua de página para página em uma única janela. Use caixas de diálogo para confirmar comandos in-locar, para obter entrada para comandos in-locar e executar tarefas secundárias e autônomas que são melhor feitas de forma independente e fora do fluxo de tarefas principal.
-   **Para selecionar opções, os usuários têm probabilidade de alterar as opções?** Caso não, considere alternativas, como:
    -   Usar as opções padrão sem perguntar, mas permitir que os usuários façam alterações posteriormente.
    -   Fornecendo uma versão com opções (por exemplo, **Imprimir...** em um menu), bem como uma versão sem opções (por exemplo, **Imprimir** na barra de ferramentas). Em geral, os comandos da barra de ferramentas devem ser imediatos e evitar exibir caixas de diálogo.
-   **Para selecionar opções, há uma maneira mais simples e direta de apresentar as opções?** Nesse caso, considere alternativas, como:
    -   Usando um [botão de divisão](ctrl-command-buttons.md) para selecionar variações de um comando.
    -   Usando um submenu para comandos, caixas de seleção, botões de rádio e listas simples.

![Captura de tela que mostra um menu e um sub menu.](images/win-dialog-box-image4.png)

![captura de tela de um menu e submenu ](images/win-dialog-box-image5.png)

Nesses exemplos, os submenus são usados em vez de caixas de diálogo para seleções simples.

## <a name="design-concepts"></a>Conceitos de design

Quando usadas corretamente, as caixas de diálogo são uma ótima maneira de dar potência e flexibilidade ao programa. Quando usadas indevidamente, as caixas de diálogo são uma maneira fácil de atrapalhar os usuários, interromper seu fluxo e fazer com que o programa se sinta indireto e entediante de usar. **As caixas de diálogo modais exigem a atenção dos usuários.** As caixas de diálogo geralmente são mais fáceis de implementar do que as UIs alternativas, portanto, elas tendem a ser superutilizadas.

**Uma caixa de diálogo é mais eficaz quando suas características de design corresponderem ao seu uso.** O design de uma caixa de diálogo é determinado em grande parte por sua finalidade (oferecer opções, fazer perguntas, fornecer informações ou comentários), tipo (modal ou sem modo) e interação do usuário (obrigatório, resposta opcional ou confirmação), enquanto seu uso é determinado em grande parte por seu contexto (iniciado pelo usuário ou programa), probabilidade de ação do usuário e frequência de exibição.

Para criar caixas de diálogo efetivas, use os seguintes elementos com eficiência:

-   Texto da caixa de diálogo
-   Instruções principais
-   Não mostre isso <item> opção again

**Se você fizer apenas uma coisa...**

Certifique-se de que o design da caixa de diálogo (determinado por sua finalidade, tipo e interação do usuário) corresponde ao uso (determinado pelo contexto, probabilidade de ação do usuário e frequência de exibição).

## <a name="usage-patterns"></a>Padrões de uso

As caixas de diálogo têm vários padrões de uso:

-   As caixas de diálogo de pergunta (usando botões) fazem aos usuários uma única pergunta ou para confirmar um comando e usam respostas simples em botões de comando organizados horizontalmente.
-   As caixas de diálogo de pergunta (usando links de comando) fazem aos usuários uma única pergunta ou selecionam uma tarefa para executar e usam respostas detalhadas em links de comando organizados verticalmente.
-   As caixas de diálogo de escolha apresentam aos usuários um conjunto de opções, geralmente para especificar um comando mais completamente. Ao contrário das caixas de diálogo de pergunta, as caixas de diálogo de escolha podem fazer várias perguntas.
-   As caixas de diálogo de progresso apresentam aos usuários comentários de progresso durante uma operação demorada (mais de cinco segundos), juntamente com um comando para cancelar ou parar a operação.
-   As caixas de diálogo informativas exibem informações solicitadas pelo usuário.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não use caixas de diálogo roláveis.** Não use caixas de diálogo que exigem que o uso de uma barra de rolagem seja exibido completamente durante o uso normal. Em vez disso, reprojete a caixa de diálogo. Considere o uso [de divulgação](ctrl-progressive-disclosure-controls.md) progressiva [ou guias](ctrl-tabs.md).
-   **Não tem uma barra de menus ou barra de status.** Em vez disso, forneça acesso a comandos e status diretamente na própria caixa de diálogo ou usando menus de contexto nos controles relevantes.

    -   **Exceção:** As barras de menu são aceitáveis quando uma caixa de diálogo é usada para implementar uma janela primária (como um utilitário).

    **Incorreto:**

    ![captura de tela de uma caixa de diálogo com uma barra de menus ](images/win-dialog-box-image6.png)

    Neste exemplo, Encontrar Certificados é uma caixa de diálogo sem modo com uma barra de menus.

-   Se uma caixa de diálogo exigir atenção imediata e o programa não estiver ativo, flash seu botão de barra de tarefas três vezes para chamar a atenção e **deixe-o realçado.** Não faça mais nada: não restaure nem ative a janela e não reproduza nenhum efeito de som. Em vez disso, respeitar a seleção de estado da janela do usuário e permitir que o usuário ative a janela quando estiver pronto.
-   Para obter mais diretrizes e exemplos, consulte [Barra de tarefas](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Caixas de diálogo modais

-   **Use para tarefas críticas ou pouco frequentes que exigem conclusão antes de continuar.**
-   Use um [modelo de commit atrasado para](glossary.md) que as alterações não entre em vigor até que seja explicitamente comprometida.
-   **Implemente o uso de uma caixa de diálogo de tarefa sempre que apropriado para obter uma aparência consistente.** As caixas de diálogo de tarefa exigem o Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Windows.

### <a name="modeless-dialog-boxes"></a>Caixas de diálogo sem modo

-   **Use para tarefas frequentes, repetitivas e em movimento.**
-   Use um [modelo de commit imediato para](glossary.md) que as alterações entre em vigor imediatamente.
-   Para caixas de diálogo sem modo, use um botão de comando Fechar explícito na caixa de diálogo para fechar a janela. Para ambos, use um botão Fechar na barra de título para fechar a janela.
-   **Considere tornar as caixas de diálogo sem modo encaixadas.** Diálogos sem modo encaixado permitem um posicionamento mais flexível.

![captura de tela de uma caixa de diálogo encaixada sem modo ](images/win-dialog-box-image7.png)

Algumas caixas de diálogo sem modo usadas Microsoft Office são encaixadas.

### <a name="multiple-dialog-boxes"></a>Várias caixas de diálogo

-   **Não exibir mais de uma caixa de diálogo de propriedade por vez de uma caixa de diálogo de escolha do proprietário.** Exibir mais de um dificulta o entendimento do significado dos botões de confirmação para os usuários. Você pode exibir outros tipos de caixas de diálogo (como diálogos de pergunta) conforme necessário.
-   **Para uma sequência de diálogos relacionados, considere usar uma caixa de diálogo de várias páginas, se possível.** Use diálogos individuais se eles não estão claramente relacionados.

### <a name="multi-page-dialog-boxes"></a>Caixas de diálogo de várias páginas

-   Use uma caixa de diálogo de várias páginas em vez de caixas de diálogo individuais quando você tiver a seguinte sequência de páginas relacionadas:
    -   Uma única página de entrada (opcional)
    -   Uma página de progresso
    -   Uma única página de resultados

A página de entrada é opcional porque a tarefa pode ter sido iniciada em outro lugar. **Isso proporciona à experiência resultante uma sensação estável, simples e leve.**

![captura de tela de uma barra de progresso ](images/win-dialog-box-image8.png)

![captura de tela da mensagem 'sem problemas encontrados' ](images/win-dialog-box-image9.png)

Neste exemplo, o Diagnóstico de Rede do Windows consiste em páginas de progresso e resultados.

-   **Não use uma caixa de diálogo de várias páginas se a página de entrada for um diálogo padrão.** Nesse caso, a consistência de usar uma caixa de diálogo padrão é mais importante.
-   **Não use os botões Próximo ou Voltar e não tenha mais de três páginas.** As caixas de diálogo de várias páginas são para tarefas de etapa única com comentários. Eles não são [assistentes](win-wizards.md), que são usados para tarefas de várias etapas. Os assistentes têm uma sensação pesada e indireta em comparação com caixas de diálogo de várias páginas.
-   **Na página de entrada, use botões de comando específicos ou links de comando para iniciar a tarefa.**
-   **Use um botão Cancelar nas páginas de entrada e progresso e um botão Fechar na página de resultados.**

**Desenvolvedores:** Você pode criar caixas de diálogo de tarefa de várias páginas usando a [mensagem TDM \_ NAVIGATE \_ PAGE.](../controls/tdm-navigate-page.md)

### <a name="presentation"></a>Apresentação

Para tornar as caixas de diálogo fáceis de encontrar e acessar, associe claramente a caixa de diálogo à sua origem e funcione bem com vários monitores:

-   **Inicialmente, exibe diálogos "centralizados" na parte superior da janela do proprietário.** Para exibição subsequente, considere exibi-lo em seu último local (em relação à janela do proprietário) se isso for provavelmente mais conveniente.

![diagrama da caixa de diálogo centralizada na janela atrás dela ](images/win-dialog-box-image10.png)

Inicialmente, centralmente as caixas de diálogo na parte superior da janela do proprietário.

-   **Se uma caixa de diálogo for contextual, exibe-a perto do objeto do qual ele foi lançado.** No entanto, coloque-o fora do caminho (preferencialmente deslocamento para baixo e para a direita) para que o objeto não seja coberto pela caixa de diálogo.

![diagrama de deslocamento da caixa de diálogo para baixo e para a direita ](images/win-dialog-box-image11.png)

As propriedades de um objeto são exibidas perto do objeto .

-   **Para caixas de diálogo sem modo, é exibida inicialmente na parte superior da janela do proprietário para facilitar a encontrá-la.** Se o usuário ativar a janela do proprietário, isso poderá obscurecer a caixa de diálogo sem modo.
-   **Se necessário, ajuste o local inicial para que toda a caixa de diálogo seja visível no monitor de destino.** Se uma janela resizável for maior que o monitor de destino, reduza-a para se ajustar.
-   **Quando uma caixa de diálogo for replayada, considere exibi-la no mesmo estado do último acesso.** Ao fechar, salve o monitor usado, o tamanho da janela, o local e o estado (maximizada versus restauração). Na reprodução, restaure o tamanho, o local e o estado da caixa de diálogo salvos usando o monitor apropriado. Além disso, considere fazer com que esses atributos persistam entre instâncias do programa por usuário.
-   **Para janelas reizáveis, de definir um tamanho mínimo de janela se houver um tamanho abaixo do qual o conteúdo não é mais acessível.** Considere alterar a apresentação para tornar o conteúdo acessível em tamanhos menores.

![captura de tela dos botões centralizados do player de mídia ](images/win-dialog-box-image12.png)

Neste exemplo, o Windows Media Player altera seu formato quando a janela se torna muito pequena para o formato padrão.

-   **Não use o atributo Always On Top.**
    -   **Exceção:** Use somente quando uma caixa de diálogo implementa uma operação essencialmente modal, mas ela precisa ser suspensa brevemente para acessar a janela do proprietário. Por exemplo, ao verificar orticamente um documento, os usuários podem, ocasionalmente, sair da caixa de diálogo de seleção ortagem e acessar o documento para corrigir erros.

Para obter mais informações e exemplos, consulte [Gerenciamento de janelas](win-window-mgt.md).

### <a name="title-bars"></a>Barras de título

-   **As caixas de diálogo não têm ícones de barra de título.** Os ícones da barra de título são usados como uma distinção visual entre [janelas primárias](glossary.md) [e secundárias.](glossary.md)
    -   **Exceção:** Se uma caixa de diálogo for usada para implementar uma janela primária (como um utilitário) e, portanto, aparecer na barra de tarefas, ela terá um ícone de barra de título. Nesse caso, otimize o título para exibição na barra de tarefas colocando as informações de distinção primeiro.
-   **As caixas de diálogo sempre têm um botão Fechar.** Caixas de diálogo sem modo também podem ter um botão Minimizar. Caixas de diálogo reizáveis podem ter um botão Maximizar.
-   **Não desabilite o botão Fechar.** Ter um botão Fechar ajuda os usuários a permanecerem no controle, permitindo que eles fechem as janelas que não querem.
    -   **Exceção:** Para as caixas de diálogo de progresso, você poderá desabilitar o botão Fechar se a tarefa tiver que ser concluída para atingir um estado válido ou evitar a perda de dados.
-   **O botão Fechar na barra de título deve ter o mesmo** efeito que o botão Cancelar ou Fechar dentro da caixa de diálogo. Nunca dê a ele o mesmo efeito que OK.
-   Se a legenda e o ícone da barra de título já estão exibidos de maneira proeminente perto da parte superior da janela, você pode ocultar a legenda e o ícone da barra de título para evitar a redundância. No entanto, você ainda precisa definir um título adequado internamente para uso pelo Windows.

### <a name="interaction"></a>Interação

-   **Quando exibidas, as caixas de diálogo iniciadas pelo usuário sempre devem ter o foco de entrada.** As caixas de diálogo iniciadas pelo programa não devem ter o foco de entrada porque o usuário pode estar interagindo com outra janela. Essa interação mal direcionada na caixa de diálogo pode ter consequências não intencionais.
-   **Atribua o foco de entrada inicial** ao controle com o qual os usuários têm maior probabilidade de interagir primeiro, que geralmente é (mas nem sempre) o primeiro controle interativo. Evite atribuir o foco de entrada inicial a um link da Ajuda.
-   **Para navegação por teclado, a ordem de tabulação deve fluir em uma ordem lógica, geralmente da esquerda para a direita, de cima para baixo.** Geralmente, a ordem de tabulação segue a ordem de leitura, mas considere fazer essas exceções:

    -   Coloque os controles mais usados anteriormente na ordem de tabulação.
    -   Coloque os links da Ajuda na parte inferior de uma caixa de diálogo, após os botões de confirmação na ordem de tabulação.

    Ao atribuir o pedido, suponha que os usuários exibem caixas de diálogo para sua finalidade pretendido; portanto, por exemplo, os usuários exibem diálogos de escolha para fazer escolhas, não para revisar e clicar em Cancelar.

-   **Pressionar a tecla Esc sempre fecha uma caixa de diálogo ativa.** Isso é verdadeiro para caixas de diálogo com Cancelar ou Fechar e, mesmo que Cancel tenha sido renomeado para Fechar porque os resultados não podem mais ser desfeitos.

**Chaves de acesso**

-   **Sempre que possível, atribua chaves de acesso exclusivas a todos os controles interativos ou seus rótulos.** [As caixas de texto somente](ctrl-text-boxes.md) leitura são controles interativos (porque os usuários podem rolar e copiar texto) para que se beneficiem das chaves de acesso. **Não atribua chaves de acesso a:**
    -   **Botões OK, Cancelar e Fechar.** Enter e Esc são usados para suas chaves de acesso. No entanto, sempre atribua uma chave de acesso a um controle que significa OK ou Cancelar, mas tem um rótulo diferente.

        ![captura de tela da caixa de diálogo Excluir arquivo ](images/win-dialog-box-image13.png)

        Neste exemplo, o botão de confirmação positiva tem uma chave de acesso atribuída.

    -   **Rótulos de grupo.** Normalmente, os controles individuais em um grupo são atribuídos a chaves de acesso, portanto, o rótulo do grupo não precisa de uma. No entanto, se houver uma falta de chaves de acesso, atribua uma chave de acesso ao rótulo do grupo e não aos controles individuais.
    -   **Botões de Ajuda Genérica,** que são acessados com F1.
    -   **Rótulos de link.** Geralmente, há muitos links para atribuir chaves de acesso exclusivas e os sublinhados geralmente usados para significar links ocultam os sublinhados da chave de acesso. Em vez disso, acesse links com a tecla Tab.
    -   **Nomes de tabulação.** As guias são ciclodas usando Ctrl+Tab e Ctrl+Shift+Tab.
    -   **Procure os botões rotulados como "...".** Esses botões Procurar não podem ser atribuídos exclusivamente às chaves de acesso.
    -   **Controles sem rótulo, como controles** de rotação, botões de comando gráfico e controles de divulgação progressiva sem rótulo.
    -   **Texto estático sem rótulo ou rótulos para controles que não são interativos,** como barras de progresso.

-   **Sempre que possível, atribua chaves de acesso para comandos comumente** usados de acordo com as Atribuições de Chave de Acesso Padrão . Embora as atribuições de chave de acesso consistentes nem sempre sejam possíveis, elas certamente são preferenciais especialmente para caixas de diálogo usadas com frequência.
-   **Atribua primeiro as chaves de acesso do botão de confirmação para garantir que elas tenham as atribuições de chave padrão.** Se não houver uma atribuição de chave padrão, use a primeira letra da primeira palavra. Por exemplo, a chave de acesso para os botões Sim e Não de confirmação sempre deve ser "Y" e "N", independentemente dos outros controles na caixa de diálogo.
-   Para tornar as chaves de acesso fáceis de encontrar, atribua as chaves de acesso a um caractere que aparece no início do **rótulo,** idealmente o primeiro caractere, mesmo que haja uma palavra-chave que apareça posteriormente no rótulo.
-   **Prefira caracteres com larguras largas,** como w, m e letras maiúsculas.
-   **Prefira uma consoante distinta ou uma voga,** como "x" em Exit.
-   Evite usar caracteres que dificultam a viagem do **sublinhado,** como (da mais problemática para a menos problemática):
    -   Letras que têm apenas um pixel de largura, como i e l.
    -   Letras com descendentes, como g, j, p, q e y.
    -   Letras ao lado de uma letra com um descendente.

Para obter mais diretrizes e exemplos, consulte [Teclado](inter-keyboard.md).

### <a name="progress-dialogs"></a>Diálogos de progresso

Para tarefas de execução longa, **suponha que os usuários vão fazer outra coisa enquanto a tarefa está concluindo**. Projete a tarefa para ser executado de forma autônoma.

-   **Apresente aos usuários a caixa de diálogo comentários** de progresso se uma operação levar mais de cinco segundos para ser concluída, juntamente com um comando para cancelar ou parar a operação.
    -   **Exceção:** Para assistentes e fluxos de tarefas, use uma caixa de diálogo modal para progresso somente se a tarefa permanecer na mesma página (em vez de avançar para outra página) e os usuários não puderem fazer nada enquanto aguardam. Caso contrário, use uma página de progresso ou o progresso in-locar.
-   Se a operação for uma tarefa de execução longa (mais de 30 segundos) e puder ser executada em segundo plano, use uma caixa de diálogo de progresso sem modo para que os usuários possam continuar a usar seu programa enquanto aguardam.
-   Caixas de diálogo de progresso sem modo:
    -   Tenha um botão Minimizar na barra de título.
    -   São exibidos na barra de tarefas.
-   Implemente diálogos de progresso sem modo para que eles continuem a ser executados mesmo que a janela do proprietário seja fechada.

![captura de tela da caixa de diálogo copiar com a barra de progresso ](images/win-dialog-box-image14.png)

Neste exemplo, a cópia do arquivo continuará mesmo se a janela do proprietário estiver fechada.

-   **Forneça um botão de comando para interromper a operação se levar mais de alguns segundos para ser concluída ou tiver o potencial de nunca ser concluído.** Rotule o botão Cancelar se cancelar retornar o ambiente ao estado anterior (sem efeitos colaterais); caso contrário, rotule o botão Parar para indicar que ele deixa a operação parcialmente concluída intacta. Você pode alterar o rótulo do botão de Cancelar para Parar no meio da operação, se, em algum momento, não for possível retornar o ambiente para seu estado anterior.

![captura de tela da caixa de diálogo com o botão Cancelar ](images/win-dialog-box-image15.png)

Neste exemplo, interromper o diagnóstico do problema não tem nenhum efeito colateral.

-   **Forneça um botão de comando para pausar a operação se levar mais de vários minutos para ser concluída e isso prejudicará a capacidade dos usuários de realizar o trabalho.** Isso não força o usuário a escolher entre concluir a tarefa e realizar seu trabalho.
-   **Reúna o máximo de informações possível antes de iniciar a tarefa.**
-   **Se problemas recuperáveis são detectados, os usuários lidam com todos os problemas encontrados no final da tarefa.** Se isso não for prático, os usuários lidarão com problemas conforme eles ocorrem.
-   **Não abandone tarefas como resultado de erros recuperáveis.**

![captura de tela da caixa de diálogo com o botão Tentar novamente ](images/win-dialog-box-image16.png)

Neste exemplo, Windows Explorer permite que os usuários continuem com a tarefa após um erro recuperável.

-   **Indique problemas, transformando a barra de progresso em vermelho.**

![captura de tela da barra de progresso e tente novamente botão ](images/win-dialog-box-image17.png)

Neste exemplo, um disco removível foi removido durante uma cópia de arquivo.

-   **Se os resultados são claramente aparentes para os usuários, feche a caixa de diálogo de progresso automaticamente após a conclusão bem-sucedida.** Caso contrário, use comentários somente para relatar problemas:
    -   Para exibir comentários simples, exibe os comentários na caixa de diálogo de progresso e altere o botão Cancelar para Fechar.
    -   Para exibir comentários detalhados, feche a caixa de diálogo progresso e exibir uma caixa de diálogo informacional.

**Não use uma notificação para comentários de conclusão.** Use uma caixa de diálogo de progresso ou uma [notificação de êxito de ação,](mess-notif.md)mas não ambas.

**Tempo restante**

-   **Use os formatos de hora a seguir.** Comece com o primeiro dos formatos a seguir em que a maior unidade de tempo não é zero e, em seguida, altere para o próximo formato quando a maior unidade de tempo se tornar zero.

**Para barras de progresso:**

**Se as informações relacionadas são mostradas em um formato de dois-pontos:**

Tempo restante: h horas, m minutos

Tempo restante: m minutos, s segundos

Tempo restante: s segundos

**Se o espaço na tela estiver em um premium:**

h horas, m min restante

m min, s segundos restantes

s segundos restantes

**,**

h horas, m minutos restantes

m minutos, s segundos restantes

s segundos restantes

**Para barras de título:**

hh: mm restantes

mm: SS restantes

0: SS restantes

Esse formato compacto mostra as informações mais importantes primeiro, para que não sejam truncadas na barra de tarefas.

-   **Tornar as estimativas precisas, mas não dar precisão falsa.** Se a unidade maior for horas, dê minutos (se for significativo), mas não segundos.

**Incorreto:**

HH horas, mm minutos, ss segundos

-   **Mantenha a estimativa atualizada.** Tempo de atualização que as estimativas restantes têm pelo menos a cada 5 segundos.
-   **Concentre-se no tempo restante** porque essas são as informações que os usuários se preocupam mais. Dê tempo total decorrido somente quando houver cenários em que o tempo decorrido é útil (por exemplo, quando a tarefa provavelmente será repetida). Se a estimativa de tempo restante estiver associada a uma barra de progresso, não terá o texto de porcentagem concluída, pois essas informações são transmitidas pela própria barra de progresso.
-   **Tenha uma gramática correta.** Use unidades singulares quando o número for um.

**Incorreto:**

1 minutos, 1 segundo

-   **Use a capitalização com estilo de frase.**

Para obter mais informações e exemplos, consulte [barras de progresso](progress-bars.md).

### <a name="icons-and-graphics"></a>Ícones e gráficos

**Elementos gráficos**

-   **Não use gráficos grandes que não atendam a nenhuma finalidade além de preencher espaço com colírio para os olhos.** Em vez disso, mantenha a aparência simples.

**Incorreto:**

![captura de tela da caixa de diálogo com um gráfico grande ](images/win-dialog-box-image18.png)

Neste exemplo, o elemento gráfico grande não tem nenhuma finalidade.

**Ícones da barra de título**

-   **As caixas de diálogo não têm ícones de barra de título.**
    -   **Exceção:** Se uma caixa de diálogo for usada para implementar uma janela primária (como um utilitário) e, portanto, aparecer na barra de tarefas, ela terá um ícone de barra de título.

**Ícones do corpo**

-   **Escolha o ícone de corpo com base no padrão de design:**



| Padrão | Ícone de corpo |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Caixas de diálogo de pergunta**<br/>      | Programa, recurso, objeto, ícone de aviso (se possível perda de dados ou acesso ao sistema), aviso de segurança ou nenhum.<br/> |
| **Caixas de diálogo de escolha**<br/>        | Nenhum.<br/>                                                                                                           |
| **Caixas de diálogo de progresso**<br/>      | Nenhum (mas pode ter uma animação).<br/>                                                                               |
| **Caixas de diálogo informativas**<br/> | Nenhum.<br/>                                                                                                           |



 

-   **Incorreto:**

![captura de tela da caixa de diálogo com ícone de aviso ](images/win-dialog-box-image19.png)

Neste exemplo, um ícone de aviso é usado incorretamente para uma pergunta que não envolve perda potencial de dados ou acesso ao sistema.

- **Considere o uso de ícones para ajudar os usuários a reconhecer visualmente os recursos do seu programa.** Essa técnica é mais eficaz quando os ícones são facilmente reconhecíveis e usados em vários locais dentro de seu programa.

![captura de tela da caixa de diálogo favoritos com o ícone de estrela ](images/win-dialog-box-image20.png)

Neste exemplo, o ícone de estrela amarela representa os favoritos. O ícone é facilmente reconhecível e é usado consistentemente em todo o Windows para representar os favoritos.

-   **Use ícones para ajudar os usuários a reconhecer o objeto em questão.**

![captura de tela da caixa de diálogo com o ícone do PowerPoint ](images/win-dialog-box-image21.png)

Neste exemplo, o ícone do objeto ajuda os usuários a reconhecer o tipo de arquivo que está sendo aberto ou salvo.

-   **Considere o uso de ícones para ajudar a tornar os recursos auto-explicativos.**

![imagens de setas mostrando como posicionar o monitor ](images/win-dialog-box-image22.png)

Neste exemplo, esses ícones ajudam os usuários a visualizar o efeito de seus recursos.

-   **Use um ícone em caixas de diálogo de caixa para a identidade visual do aplicativo.**

![captura de tela da caixa de diálogo sobre com o logotipo do Windows ](images/win-dialog-box-image23.png)

Neste exemplo, um bitmap é usado na caixa sobre para identificar e marcar o aplicativo.

**Ícones da nota de rodapé**

-   **Se você tiver uma nota de rodapé, considere usar um ícone de nota de rodapé para resumir o assunto da nota de rodapé.**

![captura de tela da caixa de diálogo com ícone de nota de rodapé ](images/win-dialog-box-image24.png)

Neste exemplo, o ícone de nota de rodapé indica que a pergunta tem implicações de segurança.

-   **Não use um ícone de nota de rodapé que repete o ícone de corpo.**
-   **Não use os ícones de erro ou informações padrão.** As condições de erro devem ser transmitidas por meio do ícone de corpo e as notas de rodapé são sempre para informações, tornando o ícone de informações redundante. No entanto, você pode usar o ícone de aviso padrão e a blindagem de segurança amarela para alertar os usuários sobre consequências arriscadas.

Para obter mais informações e exemplos, consulte [ícones](vis-icons.md).

### <a name="commit-buttons"></a>Botões de confirmação

**Observações:**

-   Essas diretrizes não se aplicam a caixas de diálogo de perguntas usando links de comando, pois esse padrão usa links de comando em vez de botões.
-   \[Faça isso \] e \[ não faça isso \] é afirmativo e respostas negativas, respectivamente, para a instrução principal.

**Geral**

-   **Escolha os botões de confirmação com base no padrão de design:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Padrão</strong><br/></td>
    <td><strong>Botões de confirmação</strong><br/></td>
    </tr>
    <tr class="even">
    <td><strong>Caixas de diálogo de pergunta (usando botões)</strong><br/></td>
    <td>Um dos seguintes conjuntos de comandos conciso: Sim/Não, sim/não/cancelar, [faça isso]/Cancel, [faça isso]/[não faça isso], [faça]/[não faça isso]/Cancel.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Caixas de diálogo de pergunta (usando links)</strong><br/></td>
    <td>Cancelar.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Caixas de diálogo de escolha</strong><br/></td>
    <td><ul>
    <li>Caixas de diálogo modais: OK/cancelar ou [fazer]/Cancel</li>
    <li>Caixas de diálogo sem janela restrita: botão fechar na caixa de diálogo e barra de título</li>
    <li>Painel de tarefas: botão fechar na barra de título</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Caixas de diálogo de progresso</strong><br/></td>
    <td>Usar cancelar se retorna o ambiente para seu estado anterior (não deixando nenhum efeito colateral); caso contrário, use stop.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Caixas de diálogo informativas</strong><br/></td>
    <td>Fechar.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Todos os botões de confirmação, exceto aplicar resultado, fechando a janela da caixa de diálogo.**
-   **Não confirme os botões de confirmação.** Fazer isso desnecessariamente pode ser muito irritante. **Exceções:**

    -   A ação é potencialmente catastrófica.
    -   A ação é claramente inconsistente com outras ações.
    -   Se estiver incorreta, a ação poderá resultar em uma perda significativa de dados, tempo ou esforço em nome do usuário.

    Para obter mais diretrizes e exemplos, consulte [Confirmações](mess-confirm.md).

-   **Não desabilite os botões de commit. Exceções:**
    -   **Se os usuários precisam elevar para fazer uma alteração, desabilite os botões de confirmação positivos até que o usuário faça uma alteração.** Isso impede que os usuários elevem apenas para fechar uma janela, forçando-os a clicar em Cancelar.
    -   Para obter mais exceções, consulte Desabilitando ou [removendo controles versus dando mensagens de erro](#disabling-or-removing-controls-vs-giving-error-messages).
-   **Alinhe com** o botão direito os botões de confirmação em uma única linha na parte inferior da caixa de diálogo, mas acima da área de nota de rodapé. Faça isso mesmo se houver um único botão de commit (como OK).

    **Incorreto:**

    ![captura de tela da mensagem com o botão ok centralizado ](images/win-dialog-box-image25.png)

    Neste exemplo, o botão OK é centralizado incorretamente.

-   **Apresente os botões de confirmação na seguinte ordem:**
    1.  OK/ \[ Faça isso \] /Sim
    2.  \[Não faça isso \] /Não
    3.  Cancelar
    4.  Aplicar (se presente)
    5.  Ajuda (se presente)
-   **Se você tiver muitos botões de commit relacionados, consolide-os usando botões de divisão**.
-   **Ter uma separação clara dos botões de confirmação (que fecham a janela) e de todos os outros botões de comando (como Avançado).**

**Respondendo às instruções principais**

-   **Use botões de confirmação positiva que são respostas específicas para a instrução principal, em vez de rótulos genéricos, como OK ou Sim/Não.** Os usuários devem ser capazes de entender as opções lendo o texto do botão sozinho. **Exceções:**
    -   Use Fechar para caixas de diálogo que não têm configurações, como caixas de diálogo informativas. Nunca use Fechar para caixas de diálogo que têm configurações.
    -   Use OK quando as respostas "específicas" ainda são genéricas, como Salvar, Selecionar ou Escolher. Use OK ao alterar uma configuração específica ou uma coleção de configurações.
    -   **Para caixas de diálogo herdadas sem uma instrução principal, você pode usar rótulos genéricos, como OK.** Geralmente, essas caixas de diálogo não são projetadas para executar uma tarefa específica, impedindo respostas mais específicas.
    -   Determinadas tarefas exigem mais atenção e leitura cuidadosa para os usuários tomarem decisões informadas. Normalmente, esse é o caso com [confirmações](mess-confirm.md). **Nesses casos, você pode usar propositalmente rótulos de botão de confirmação genéricos para forçar os usuários a lerem as instruções principais e evitar decisões hasty.**

        **Correto:**

        ![captura de tela da mensagem com botões sim e sem](images/win-dialog-box-image26.png)

        Neste exemplo, usar botões de confirmação Sim/Não força os usuários a lerem pelo menos a instrução principal.

-   Como alternativa, você pode adicionar a palavra **"mesmo assim"** ao rótulo do botão de confirmação positiva para indicar que a caixa de diálogo apresenta um motivo para não continuar e que os usuários devem ler a caixa de diálogo com cuidado antes de continuar.

    **Correto:**

    ![captura de tela da mensagem e do botão desinstalar mesmo assim ](images/win-dialog-box-image27.png)

    Neste exemplo, "de qualquer forma" é adicionado ao rótulo do botão de confirmação para indicar que os usuários devem continuar com cuidado.

-   **Use Cancelar ou Fechar para botões de confirmação negativos em vez de respostas específicas à instrução principal.** Muitas vezes, os usuários percebe que não querem executar uma tarefa quando veem uma caixa de diálogo. Se Cancelar ou Fechar fosse rotulado para respostas específicas, os usuários teriam que ler cuidadosamente todos os botões de confirmação para determinar como cancelar. **Rotular Cancelar e Fechar de forma consistente os torna fáceis de encontrar. Exceções:**
    -   **Não use Sim/Cancelar.** Sempre use Sim/Não como um par.
    -   **Use uma resposta específica quando Cancelar for ambíguo.**
-   **Não mapeie rótulos genéricos para seu significado específico com texto na área de conteúdo.** Em vez disso, use rótulos de botão de confirmação específicos ou uma caixa de diálogo de pergunta usando links se os rótulos são longos.

    **Incorreto:**

    ![captura de tela da mensagem com uso não claro de botões ](images/win-dialog-box-image28.png)

    Neste exemplo, OK é mapeado para Continuar, Cancelar é mapeado para Permanecer na Página.

**Botões Sim e Não**

-   **Prefira respostas específicas aos botões Sim e Não.** Embora não haja nada de errado com o uso de Sim e Não, respostas específicas podem ser compreendidas mais rapidamente, resultando em uma tomada de decisão eficiente. No entanto, [as confirmações](mess-confirm.md) geralmente têm os botões Sim e Não para fazer com que os usuários façam a confirmação [pensar um pouco antes](mess-confirm.md) de responder.
-   **Use os botões Sim e Não apenas para responder a perguntas sim ou não.** A instrução principal deve ser expressa naturalmente como uma pergunta sim ou não. Nunca use OK e Cancelar para perguntas sim ou não.

    **Incorreto:**

    ![Captura de tela que mostra uma mensagem com um "OK" para uma pergunta sim-não.](images/win-dialog-box-image29.png)

    **Correto:**

    ![captura de tela da mensagem com sim para a mesma pergunta ](images/win-dialog-box-image30.png)

    **Melhor:**

    ![captura de tela da mensagem com executar para a mesma pergunta ](images/win-dialog-box-image31.png)

    Nesses exemplos, Sim e Não são boas respostas para sim e nenhuma pergunta, mas respostas específicas são ainda melhores.

-   **Considere a frase da instrução principal como uma pergunta sim ou não se os botões de confirmação com frases específicas são longos ou complicados.** Como alternativa, você pode usar links de comando para respostas mais longas (cinco palavras ou mais) para a instrução principal.

    **Incorreto:**

    ![captura de tela da mensagem com rótulos de botão wordy ](images/win-dialog-box-image32.png)

    **Correto:**

    ![captura de tela da mensagem com rótulos de botão sim/não ](images/win-dialog-box-image33.png)

    A frase específica no exemplo incorreto é muito longa, portanto, o exemplo correto usa Sim e Não.

-   **Não use os botões Sim e Não se o significado da resposta Não estiver claro.** Se sim, use respostas específicas em vez disso.

**Botões OK**

-   **Em caixas de diálogo modais, clicar em OK significa aplicar os valores, executar a tarefa e fechar a janela.**
-   **Não use botões OK para responder a perguntas.**
-   **Não atribua chaves de acesso a OK, pois Enter é a chave de acesso para o botão padrão.** Isso facilita a atribuição das outras chaves de acesso.
-   **Rotule os botões OK corretamente.** O botão OK deve ser rotulado OK, não OK ou Ok.
-   **Não use botões OK para erros ou avisos.** Os problemas nunca estão ok. Em vez disso, use Fechar.

    **Incorreto:**

    ![captura de tela da mensagem com o botão OK ](images/win-dialog-box-image34.png)

    Neste exemplo, Close deve ser usado em vez de OK.

-   **Não use botões OK em caixas de diálogo sem modo.** Em vez disso, as caixas de diálogo sem modo devem usar botões de commit específicos da tarefa (por exemplo, Find). No entanto, algumas caixas de diálogo sem modo exigem apenas um botão Fechar.

**Botões Cancelar**

-   **Clicar em Cancelar significa abandonar todas as alterações, cancelar a tarefa, fechar a janela e retornar o ambiente para seu estado anterior, sem nenhum efeito colateral.** Para caixas de diálogo de escolha aninhadas, clicar em Cancelar na caixa de diálogo de escolha do proprietário significa que todas as alterações feitas pelos diálogos de escolha de propriedade também serão abandonadas.
-   **Forneça um botão Cancelar para permitir que os usuários abandonem explicitamente as alterações.** As caixas de diálogo precisam de um ponto de saída claro. Não dependa dos usuários localizarem o botão Fechar na barra de título.

    -   **Exceção:** Não forneça um botão Cancelar para caixas de diálogo sem configurações. Os botões OK e Close têm o mesmo efeito que Cancelar nesse caso.

    **Incorreto:**

    ![captura de tela da mensagem apenas com o botão OK ](images/win-dialog-box-image35.png)

    Neste exemplo, ter apenas um botão Fechar na barra de título faz com que pareça que os usuários não têm uma opção.

-   **Não use os botões Cancelar para responder a perguntas.**

    **Incorreto:**

    ![captura de tela da mensagem com ok para pergunta sim-não ](images/win-dialog-box-image36.png)

    Neste exemplo, OK e Cancelar são usados incorretamente para responder a uma pergunta Sim ou Não.

-   **Não atribua chaves de acesso a Cancelar, pois Esc é a chave de acesso.** Isso facilita a atribuição das outras chaves de acesso.
-   **Não use os botões Cancelar em caixas de diálogo sem modo.** Em vez disso, use Fechar.
-   **Não desabilite o botão Cancelar.** Os usuários sempre devem ser capazes de cancelar caixas de diálogo.
    -   **Exceção:** Você poderá desabilitar o botão Cancelar em uma caixa de diálogo de progresso se houver um período durante o qual a operação não possa ser cancelada. No entanto, uma solução melhor é projetar essas operações para que sempre sejam canceláveis.

**Fechar botões**

-   **Use botões Fechar para caixas de diálogo sem modo, bem como caixas de diálogo modais que não podem ser canceladas.**
-   **Clicar em Fechar significa fechar a janela da caixa de diálogo, deixando quaisquer efeitos colaterais existentes.** Não use Done, porque não é uma construção imperativa. Para caixas de diálogo de escolha aninhadas, clicar em Fechar na caixa de diálogo de escolha do proprietário significa que todas as alterações feitas por caixas de diálogo de escolha de propriedade serão preservadas.
-   **Coloque um botão Fechar explícito no corpo da caixa de diálogo.** As caixas de diálogo precisam de um ponto de saída claro. Não dependa dos usuários localizarem o botão Fechar na barra de título.
-   **Certifique-se de que o botão Fechar na barra de título tenha o mesmo efeito que Cancelar ou Fechar.**
-   **Não atribua chaves de acesso para Fechar, pois Esc é a chave de acesso.** Isso facilita a atribuição das outras chaves de acesso.

**Aplicar botões**

-   **Não use os botões Aplicar em caixas de diálogo que não são folhas de propriedades ou painéis de controle.** O botão Aplicar significa aplicar as alterações pendentes, mas deixe a janela aberta. Isso permite que os usuários avaliem as alterações antes de fechar a janela. No entanto, somente a folha de propriedades e os painéis de controle têm essa necessidade.

    **Incorreto:**

    ![captura de tela da caixa de diálogo com o botão Aplicar ](images/win-dialog-box-image37.png)

    Neste exemplo, uma caixa de diálogo de escolha sem necessidade tem um botão Aplicar.

**Botões de commit para caixas de diálogo indiretas**

**Observação:** As caixas de diálogo indiretas são exibidas fora do contexto, como um resultado indireto de uma tarefa ou o resultado de um problema com um sistema ou processo em segundo plano. Para diálogos indiretos, o botão Cancelar é ambíguo porque pode significar cancelar a caixa de diálogo ou cancelar toda a tarefa.

-   **Se os usuários precisam cancelar a caixa de diálogo e a tarefa, dê botões de confirmação para fazer ambos.** Rotule o botão que cancela a caixa de diálogo com uma resposta negativa à instrução principal. Rotule o botão que cancela toda a tarefa com Cancelar. Usar Cancelar permite que a caixa de diálogo seja usada em muitos contextos.

    **Correto:**

    ![captura de tela da caixa de diálogo com salvar/não salvar ](images/win-dialog-box-image38.png)

    Neste exemplo, essa caixa de diálogo é exibida pelo Windows Paint como resultado de um comando New ou Exit quando o gráfico não foi salvo. Não Salvar fecha a caixa de diálogo sem salvar, enquanto Cancelar cancela o comando Novo ou Sair.

    **Incorreto:**

    ![captura de tela da caixa de diálogo com botões sim/não ](images/win-dialog-box-image39.png)

    Neste exemplo, não há como cancelar a tarefa (fechando a Barra de Atalhos do Office) que levou à exibição dessa caixa de diálogo. Essa caixa de diálogo precisa de um botão Cancelar.

-   Se os usuários apenas precisam cancelar a caixa de diálogo, mas não **a tarefa, use** um botão com uma resposta negativa específica à instrução principal e não tenha um botão Cancelar.

    ![captura de tela da caixa de diálogo com executar/não executar ](images/win-dialog-box-image24.png)

    Neste exemplo, essa caixa de diálogo é exibida indiretamente como resultado da navegação para uma página da Web que instala um controle ActiveX. Usar Cancelar seria ambíguo aqui, portanto, Não executar é usado em vez disso.

Para obter mais informações e exemplos, consulte [Botões de comando](ctrl-command-buttons.md).

### <a name="command-links"></a>Links de comando

-   **Apresente um conjunto de comandos longos usando links de comando, em vez de botões de comando ou uma combinação de botões de opção e um botão OK.** Isso permite que os usuários respondam com um único clique. No entanto, essa abordagem funciona apenas para uma única pergunta.
-   **Apresente os links de comando mais usados primeiro.** A ordem resultante deve seguir aproximadamente a probabilidade de uso, mas também ter um fluxo lógico.
    -   **Exceção:** Os links de comando que resultam em fazer tudo devem ser colocados primeiro.
-   Se um link de comando exigir mais explicações, **forneça uma explicação complementar.** Explicações complementares descrevem por que os usuários podem querer escolher o comando ou o que acontece se o comando for escolhido.
-   **Não use explicações complementares que são restatementações wordy do link de comando.** Use uma explicação complementar somente quando não for possível tornar um link de comando autoexplicativo. Fornecer uma explicação complementar para um link de comando não significa que você precisa forenciá-los para todos os comandos.

![captura de tela da caixa de diálogo com opções de notação de texto ](images/win-dialog-box-image40.png)

Neste exemplo, a explicação complementar descreve as implicações de uma das opções.

-   **Use frases que começam com um verbo, sem terminar a pontuação.**
-   **Se um comando for altamente recomendado, considere adicionar "(recomendado)" ao rótulo.** Certifique-se de adicionar ao rótulo do link, não à explicação complementar.
-   **Se um comando for destinado somente a usuários avançados, considere adicionar "(advanced)" ao rótulo.** Certifique-se de adicionar ao rótulo do link, não à explicação complementar.
-   **Sempre forneça um botão Cancelar explícito**. Não use um link de comando para essa finalidade.

**Incorreto:**

![captura de tela da caixa de diálogo com o link não sair ](images/win-dialog-box-image41.png)

Neste exemplo, a caixa de diálogo usa um link de comando em vez de um botão Cancelar.

Para obter mais informações e exemplos, consulte [Links de comando.](ctrl-command-links.md)

### <a name="dont-show-this-item-again"></a>Não mostre isso <item> Novamente

-   **Considere usar uma opção Não mostrar novamente para permitir que os usuários suprimem uma caixa de diálogo recorrente, somente se não <item> houver uma alternativa melhor.** É melhor sempre mostrar a caixa de diálogo se os usuários realmente precisam dela ou simplesmente eliminá-la caso não precisem.
-   **Use essa frase específica para substituir <item> pelo item específico.** Por exemplo, Não mostrar este lembrete novamente. Ao fazer referência a uma caixa de diálogo em geral, use Não mostrar esta mensagem novamente.
-   **Indique claramente quando a entrada do usuário será** usada para valores padrão futuros adicionando a seguinte frase na opção: Suas seleções serão usadas por padrão no futuro.
-   **Não selecione a opção por padrão. Se a caixa de diálogo realmente precisar ser exibida apenas uma vez, faça isso sem perguntar.** Não use essa opção como um contraspeso para que os usuários se certifiquem de que o comportamento padrão não seja entediante.

**Incorreto:**

![captura de tela da mensagem fazendo uma pergunta desnecessária ](images/win-dialog-box-image42.png)

Neste exemplo, a mensagem deve ser exibida apenas uma vez. Não é necessário perguntar.

-   **Faça com que a configuração persista por usuário.**
-   **Se os usuários selecionarem a opção e clicarem em Cancelar, essa opção entre em vigor.** Essa configuração é uma meta-opção, portanto, ela não segue o comportamento padrão Cancelar de não deixar nenhum efeito colateral. Observe que, se os usuários não quiserem ver a caixa de diálogo no futuro, provavelmente eles também querem cancelá-la.
-   Se os usuários talvez precisem restaurar essas caixas de diálogo, forneça **um comando Restaurar** mensagens na caixa de diálogo Opções do programa.

### <a name="ask-me-later"></a>Perguntar depois

-   Forneça esta opção para descartar uma caixa de diálogo somente quando:
    -   **A caixa de diálogo é indireta,** portanto, os usuários provavelmente se concentram em outra tarefa.
    -   **Os usuários devem responder, mas não imediatamente**, para que possam continuar com seu trabalho.
    -   **A pergunta requer pensamento ou esforço suficiente** , de forma que os usuários possam tomar decisões melhores se receberem mais tempo.
    -   **A caixa de diálogo ou a opção será apresentada automaticamente mais tarde** (para que os usuários realmente sejam solicitados posteriormente).
-   **Incorreto:**
-   ![captura de tela da mensagem com a opção perguntar mais tarde ](images/win-dialog-box-image43.png)
-   Neste exemplo, a pergunta é simples o suficiente para adicionar uma opção perguntar mais tarde apenas complica-a.
-   Caso contrário, espere que os usuários respondam agora, mas permita que eles fechem a caixa de diálogo normalmente com cancelamento ou fechamento. Quando usado corretamente, essa opção deve ser rara.

### <a name="morefewer"></a>Mais/menos

-   **Use mais/menos botões de divulgação progressiva para mostrar ou Ocultar opções avançadas ou raramente usadas, comandos ou detalhes que os usuários de destino normalmente não precisam.** Fazer isso simplifica a caixa de diálogo para uso típico. Não oculte opções, comandos ou informações comumente usadas porque os usuários podem não encontrá-las.

![captura de tela da caixa de diálogo com o botão mais opções ](images/win-dialog-box-image24.png)

Neste exemplo, as opções raramente usadas ficam ocultas por padrão.

-   **Não use mais ou menos controles, a menos que realmente haja mais detalhes a serem mostrados.** Não apenas redeclare as mesmas informações em um formato diferente.
-   **Não use mais ou menos controles para mostrar a ajuda.** Em vez disso, use links de ajuda ou notas de rodapé.
-   **Com as caixas de diálogo de tarefas, evite combinar mais ou menos controles, mas não mostre isso <item> novamente.** Essa combinação tem uma aparência estranha.
-   Para obter diretrizes de rotulamento, consulte [divulgação progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="footnotes"></a>Notas de rodapé

-   **Use notas de rodapé para obter informações que não são essenciais para a finalidade de uma caixa de diálogo, mas que os usuários podem achar úteis para tomar decisões.** A maioria dos usuários deve ser capaz de ignorar notas de rodapé e ainda tomar decisões informadas em sua resposta à caixa de diálogo.

![captura de tela da caixa de diálogo com nota de rodapé de esclarecimento ](images/win-dialog-box-image44.png)

Neste exemplo, as informações de nota de rodapé são suplementares, não essenciais.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Desabilitando ou removendo controles vs. fornecendo mensagens de erro

-   Quando um controle não se aplica no contexto atual, considere as seguintes opções:
    -   **Remova o controle quando não há nenhuma maneira para os usuários habilitá-lo, ou os usuários não esperam que ele seja aplicado e seu estado não é alterado com frequência.** Fazer isso simplifica a caixa de diálogo e os usuários não perdem isso. Ter um controle exibido e desaparecer frequentemente é irritante.
    -   **Desabilite o controle quando os usuários esperam que eles sejam aplicados ou suas alterações de estado com frequência, e os usuários podem facilmente deduzir por que o controle está desabilitado.** Um exemplo de dedução fácil é desabilitar um botão de confirmação quando há uma caixa de texto única e vazia que requer qualquer entrada. Você pode usar [balões](ctrl-balloons.md) para exibir problemas de entrada de usuário não críticos com caixas de texto e listas suspensas editáveis. No entanto, se o problema não puder ser explicado com um balão ou envolver vários controles, a dedução não será mais fácil.
    -   **Caso contrário, deixe o controle habilitado, mas forneça uma mensagem de erro quando ele for usado incorretamente.** Desabilitar, nesse caso, dificultaria para os usuários entenderem por que o controle está desabilitado. Os usuários seriam forçados a determinar o problema por meio de experimentação e lógica deduzida. É melhor apenas fornecer uma mensagem de erro útil para explicar o problema explicitamente.
-   **Dica:** Se você não tiver certeza se deve desabilitar um controle ou dar uma mensagem de erro, comece compondo a mensagem de erro que você pode dar. Se a mensagem de erro contiver informações úteis que os usuários de destino não têm probabilidade de deduzir rapidamente, deixe o controle habilitado e dê o erro. Caso contrário, desabilite o controle.
-   **Se você desabilitar um controle, também desabilitará todos os controles associados**, como seu rótulo, explicações complementares ou botões de comando. No entanto, não desabilite suas [caixas de grupo](ctrl-group-boxes.md), rótulo de grupo ou explicação de grupo, se houver.

![captura de tela da caixa de diálogo com controles esmaecidos ](images/win-dialog-box-image45.png)

Neste exemplo, os rótulos da caixa de texto desabilitados também são desabilitados, mas a explicação do rótulo e do grupo do grupo não é.

### <a name="required-input"></a>Entrada Requerida

-   Para indicar que os usuários devem fornecer informações em um controle, considere as seguintes opções:
    -   **Não indique nada, mas trate da entrada necessária ausente com mensagens de erro.** Essa abordagem reduz a desordem e funciona bem se a maioria das entradas é opcional ou os usuários não têm probabilidade de ignorar controles, mantendo o número de mensagens de erro baixas.
    -   **Indique a entrada necessária usando um asterisco no início do rótulo.** Explique o asterisco usando:

        -   Uma nota de rodapé na parte inferior da área de conteúdo que informa a \* entrada necessária.
        -   Uma dica de ferramenta no asterisco que informa a entrada necessária.

        Essa abordagem funciona bem se não houver muitos controles necessários, mas ruim se a maioria dos controles for necessária.

        ![captura de tela dos rótulos da caixa de texto com asteriscos ](images/win-dialog-box-image46.png)

        Neste exemplo, os asteriscos são usados para indicar a entrada necessária.

    -   **Se todos os controles exigirem entrada, declare "todas as entradas necessárias" em um local apropriado na parte superior da área de conteúdo.** Essa abordagem reduz a desordem nesse caso específico.
    -   **Indique entradas opcionais com "(opcional)" após o rótulo.** Essa abordagem funciona bem se a maioria das entradas é necessária, mas de outra forma mal.

-   **Para consistência, tente usar o mesmo método para indicar a entrada necessária em todo o seu programa.** Especificamente, indique a entrada necessária ou opcional, conforme necessário, mas evite usar ambos dentro do mesmo programa.

### <a name="error-handling"></a>Tratamento de erros

-   Evitar erros usando controles que são restritos a uma entrada de usuário válida. Você também pode ajudar a reduzir o número de erros fornecendo valores padrão razoáveis.
-   Valide a entrada do usuário assim que possível e mostre erros o mais próximo possível do ponto de entrada.
-   **Use o tratamento de erros sem janela restrita (erros in-loco ou balões) para problemas de entrada do usuário.**
    -   **Use balões para problemas de entrada do usuário de ponto único não crítico detectados em uma caixa de texto ou imediatamente depois que uma caixa de texto perde o foco.** Os balões não exigem o espaço de tela disponível ou o layout dinâmico necessário para exibir mensagens in-loco. Exibir apenas um único balão de cada vez. Como o problema não é crítico, nenhum ícone de erro é necessário. Os balões desaparecem quando clicados, quando o problema é resolvido ou após um tempo limite.

        ![captura de tela da mensagem ' caractere incorreto ' ](images/win-dialog-box-image47.png)

        Neste exemplo, um balão indica um problema de entrada enquanto ainda está no controle.

-   **Use erros in-loco para detecção de erro atrasada**, geralmente erros encontrados ao clicar em um botão de confirmação. (Não use erros in-loco para as configurações que são confirmadas imediatamente.) Pode haver vários erros in-loco por vez. Use um texto normal e um ícone de erro de 16x16 pixels, colocando-os diretamente ao lado do problema sempre que possível. Os erros in-loco não desaparecem a menos que o usuário confirme e nenhum outro erro seja encontrado.

    ![captura de tela da caixa de diálogo com duas mensagens de erro ](images/win-dialog-box-image48.png)

    Neste exemplo, um erro in-loco é usado para um erro encontrado clicando no botão confirmar.

-   **Use o tratamento de erro modal (caixas de diálogo de tarefas ou de mensagens) para todos os outros problemas,** incluindo erros que envolvem vários controles ou que são erros não-contextuais ou não de entrada encontrados ao clicar em um botão de confirmação.
-   **Quando um problema de entrada for encontrado e relatado, defina o foco de entrada para o primeiro controle com os dados incorretos.** Role o controle para a exibição, se necessário.

Para obter mais informações e exemplos, consulte [mensagens de erro](mess-error.md) e [balões](ctrl-balloons.md).

### <a name="help"></a>Ajuda

-   Ao fornecer assistência ao usuário, considere as seguintes opções (listadas na ordem de preferência):
    -   Forneça rótulos autoexplicativos aos controles interativos. Os usuários têm mais probabilidade de ler os rótulos em controles interativos do que qualquer outro texto.
    -   Forneça explicações no contexto usando [Rótulos de texto estáticos](text-ui.md).
    -   Forneça um link de ajuda específico para um tópico de ajuda relevante.
-   **Localize os links de ajuda na parte inferior da área de conteúdo da caixa de diálogo.** Se a caixa de diálogo tiver uma nota de rodapé e o link de ajuda estiver relacionado a ela, coloque o link de ajuda dentro da nota de rodapé.

    ![captura de tela da caixa de diálogo com o link de ajuda ](images/win-dialog-box-image40.png)

    Neste exemplo, o link de ajuda se aplica a toda a caixa de diálogo.

    -   **Exceção:** Se uma caixa de diálogo tiver vários grupos distintos de configurações que têm tópicos de ajuda separados (talvez dentro das caixas de grupo), localize os links de ajuda na parte inferior dos grupos.

-   **Não use links de tópicos de ajuda gerais ou vagas ou botões de ajuda genéricos.** Os usuários geralmente ignoram a ajuda genérica.

Para obter mais informações e exemplos, consulte [a ajuda](winenv-help.md).

### <a name="default-values"></a>Valores padrão

-   Incluir um botão de confirmação padrão em cada caixa de diálogo.
-   Para caixas de diálogo de pergunta:
    -   **Selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema), a resposta mais segura para o padrão.** Se não houver fatores de segurança e segurança, selecione a resposta mais provável ou conveniente.
        -   **Exceção:** Não faça uma resposta destrutiva do padrão, a menos que haja uma maneira simples e óbvia de desfazer o comando.
-   Para diálogos de escolha:
    -   Para os valores padrão iniciais, **Selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema) e os valores mais seguros para cada controle.** Se não houver fatores de segurança e segurança, selecione as opções mais prováveis ou convenientes.
    -   Para os valores padrão subsequentes, **selecione novamente as opções selecionadas anteriormente se esses valores provavelmente forem repetidos, e se isso for seguro e seguro.** Caso contrário, selecione os valores padrão iniciais.

![captura de tela da caixa de diálogo Imprimir ](images/win-dialog-box-image49.png)

Neste exemplo, é mais provável que os usuários escolham as mesmas configurações de impressão que faziam na última vez. No entanto, é provável que o número de cópias desejadas seja alterado, portanto, essa configuração não é selecionada novamente.

## <a name="recommended-sizing-and-spacing&quot;></a>Dimensionamento e espaçamento recomendados

-   **Suporte à resolução mínima de tela do Windows Vista de 800 x 600 pixels.** Os layouts podem ser otimizados para janelas redimensionáveis usando uma resolução de tela de 1024 x 768 pixels.
-   **Use janelas redimensionáveis sempre que for prático para evitar barras de rolagem e dados truncados.** O Windows com conteúdo dinâmico e lista se beneficia mais das janelas redimensionáveis.
-   **O Windows de tamanho fixo deve ser totalmente visível e dimensionado para se ajustar na área de trabalho.**
-   **Janelas redimensionáveis podem ser otimizadas para resoluções mais altas, mas são dimensionadas conforme necessário no momento da exibição para a resolução de tela real.**
-   **Escolha um tamanho de janela padrão apropriado para seu conteúdo.** Não tenha medo de usar tamanhos de janela iniciais maiores se você puder usar o espaço com eficiência.

## <a name=&quot;text&quot;></a>Text

### <a name=&quot;general&quot;></a>Geral

-   **Remova o texto redundante.** Procure texto redundante em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de confirmação. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância dos outros locais.
-   **Use frases positivas.** Frases positivas são mais fáceis para os usuários entenderem.

**Correto:**

Deseja habilitar o compartilhamento de arquivos e impressoras?

**Incorreto:**

Deseja desabilitar o compartilhamento de arquivos e impressoras?

No entanto, a formulação deve corresponder ao comando associado, mesmo que o comando seja desenhado negativamente; Portanto, por exemplo, use Disable para confirmar um comando Disable.

-   **Se necessário, use a palavra &quot;janela&quot; para fazer referência à própria caixa de diálogo.**
-   **Use a segunda pessoa (&quot;você/seu") para informar aos usuários o que fazer** na principal instrução e na área de conteúdo. Geralmente, a segunda pessoa está implícita.

**Exemplos:**

Escolha as imagens que você deseja imprimir

Escolha uma conta

-   **Use a primeira pessoa ("I/me/My") para permitir que os usuários informem ao programa o que fazer** nos controles na área de conteúdo que respondem à instrução principal.

**Exemplo:** Imprima as fotos na minha câmera.

### <a name="dialog-box-titles"></a>Títulos da caixa de diálogo

-   **Use o título para identificar o comando, o recurso ou o programa do qual uma caixa de diálogo veio.**
    -   Se a caixa de diálogo for iniciada pelo usuário, identifique-a usando o comando ou o nome do recurso. **Exceções:**
        -   Se uma caixa de diálogo for exibida por vários comandos diferentes, considere usar o nome do programa em vez disso.
        -   Se esse título fosse redundante com a instrução principal, use o nome do programa em vez disso.
    -   Se for um programa ou sistema iniciado (e, portanto, fora do contexto), identifique-o usando o nome do programa ou do recurso para dar contexto.
    -   Não use o título para explicar o que fazer na caixa de diálogo que é a finalidade da instrução principal.
-   Use o nome de comando exato para nomes baseados em comando, mas não inclua as reticências se houver uma. Você pode incluir o título do menu do comando, se necessário, para compor um bom título. Exemplo: para um objeto... em um menu Inserir, use o título Inserir objeto.
-   **Se uma caixa de diálogo sem janela restrita aparecer na barra de tarefas, otimize o título para exibição na barra de tarefas** colocando concisamente as informações de distinção primeiro. Exemplos: "66% concluído" e "3 lembretes".
-   **Não inclua as palavras "Dialog" ou "Progress" no título.** Isso é implícito e deixá-lo desativado torna mais fácil para os usuários verificar.
-   Use [maiúsculas e minúsculas no estilo de título](glossary.md), sem pontuação final.

### <a name="main-instructions"></a>Instruções principais

-   **Use a instrução principal para explicar de forma concisa o que fazer na caixa de diálogo.** A instrução deve ser uma instrução específica, uma direção imperativa ou uma pergunta. Boas instruções comunicam o objetivo do usuário com a caixa de diálogo em vez de se concentrar puramente na mecânica de manipulação.
-   **Omita a instrução principal quando a única coisa que você pode dizer é óbvia.** Nesses casos, o conteúdo da caixa de diálogo é auto-explicativo. Por exemplo, as caixas de diálogo arquivo abrir e salvar arquivo não precisam de uma instrução principal porque seu contexto e design tornam sua finalidade óbvia.
-   **Omita os rótulos de controle que redefinem a instrução principal.** Nesse caso, a instrução Main usa a chave de acesso.

**Aceitável:**

![captura de tela da caixa de texto com rótulo redundante ](images/win-dialog-box-image50.png)

Neste exemplo, o rótulo da caixa de texto é apenas uma recondição da instrução principal.

**Melhor:**

![captura de tela da mesma caixa de texto com um rótulo ](images/win-dialog-box-image51.png)

Neste exemplo, o rótulo redundante é removido, portanto, a instrução Main usa a chave de acesso.

-   **Seja conciso Use apenas uma única frase completa.** Parênteses da instrução principal até as informações essenciais. Se você precisar explicar algo mais, use a instrução complementar.
-   **Use verbos específicos sempre que possível.** Os verbos específicos (exemplos: conectar, salvar, instalar) são mais significativos para os usuários do que os genéricos (exemplos: configurar, gerenciar, definir).
-   Use [a capitalização no estilo de frase](glossary.md).
-   **Não inclua os períodos finais se a instrução for uma instrução.** Se a instrução for uma pergunta, inclua um ponto de interrogação final.
-   **Para caixas de diálogo de progresso, use uma frase gerund explicando brevemente a operação em andamento,** terminando com uma elipse. Exemplo: imprimindo suas imagens...
-   **Dica:** Você pode avaliar uma instrução principal ao imaginar o que você diria a um amigo. Se responder com a instrução principal não for natural, não ajuda ou estranha, retrabalhe com a instrução.

### <a name="supplemental-instructions"></a>Instruções complementares

-   **Quando necessário, use uma instrução complementar opcional para apresentar informações adicionais úteis para entender ou usar a página.** Você pode fornecer informações mais detalhadas e definir a terminologia.
-   **Se a aparência da caixa de diálogo for programa ou sistema iniciado (e, portanto, fora do contexto), use a instrução complementar para explicar por que a caixa de diálogo apareceu.** Para essas caixas de diálogo, o contexto geralmente não é óbvio.
-   **Não repita a instrução principal com uma palavra ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver mais a adicionar.
-   Use frases completas, maiúsculas e minúsculas no estilo da frase e pontuação final.

### <a name="command-links"></a>Links de comando

-   **Escolha um texto de link conciso que se comunique claramente e diferencie o que o link de comando faz.** Ele deve ser auto-explicativo e corresponder à instrução principal. Os usuários não devem ter que descobrir o que o link significa realmente ou como ele difere de outros links.
-   **Sempre inicie links de comando com um verbo.**
-   Use a capitalização com estilo de frase.
-   Não use pontuação final.
-   **Se necessário, forneça qualquer explicação adicional usando frases completas e pontuação final.** No entanto, adicione essas explicações somente quando necessário não adicione explicações a todos os links de comando apenas porque um link de comando precisa de um.

Para obter mais informações e exemplos, consulte Diretrizes de [link de comando](ctrl-command-links.md) .

### <a name="commit-buttons"></a>Botões de confirmação

-   **Use rótulos de botão de confirmação específicos que fazem sentido por conta própria e são uma resposta para a instrução principal.** Idealmente, os usuários não precisam ler mais nada para entender o rótulo. Os usuários têm muito mais probabilidade de ler rótulos de botão de comando do que texto estático.
-   **Inicie os rótulos do botão confirmar com um verbo. As exceções são OK, sim e não.**
-   Use a capitalização com estilo de frase.
-   Não use pontuação final.
-   Atribua uma [chave de acesso](glossary.md)exclusiva.
    -   **Exceção:** Não atribua chaves de acesso a botões OK e cancelar porque Enter e ESC são suas chaves de acesso. Isso torna as outras chaves de acesso mais fáceis de atribuir.

## <a name="documentation"></a>Documentação

Ao fazer referência a caixas de diálogo:

-   Em programação e outras documentações técnicas, consulte caixas de diálogo como caixas de diálogo. Em qualquer outro lugar, consulte as caixas de diálogo por seu título. Se a barra de título estiver oculta, consulte a caixa de diálogo usando a instrução principal.
-   Se você precisar fazer referência a uma caixa de diálogo em geral, use a janela na documentação do usuário. Você pode consultar uma caixa de diálogo de pergunta simples ou uma confirmação como uma mensagem.
-   Use o título exato ou o texto de instrução principal, incluindo sua capitalização.
-   Quando possível, formate o título usando texto em negrito. Caso contrário, coloque o título entre aspas somente se necessário para evitar confusão.

Exemplo: em **segurança do Windows**, clique em **mais opções**.

