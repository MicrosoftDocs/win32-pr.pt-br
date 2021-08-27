---
title: Caixas de diálogo (noções básicas de Design)
description: Uma caixa de diálogo é uma janela secundária que permite aos usuários executar um comando, pergunta aos usuários uma pergunta ou fornece aos usuários informações ou comentários sobre o progresso.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dbcf7887a90c7407224bbfbb0c9b316ccb426f76
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880017"
---
# <a name="dialog-boxes-design-basics"></a>Caixas de diálogo (noções básicas de Design)

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma caixa de diálogo é uma janela secundária que permite aos usuários executar um comando, pergunta aos usuários uma pergunta ou fornece aos usuários informações ou comentários sobre o progresso.

![elementos da caixa de diálogo identificação da captura de tela ](images/win-dialog-box-image1.png)

Uma caixa de diálogo típica.

As caixas de diálogo consistem em uma barra de título (para identificar o comando, o recurso ou o programa do qual uma caixa de diálogo veio), uma instrução principal opcional (para explicar o objetivo do usuário com a caixa de diálogo), vários controles na área de conteúdo (para apresentar opções) e botões de confirmação (para indicar como o usuário deseja confirmar a tarefa).

As caixas de diálogo têm dois tipos fundamentais:

-   As **caixas de diálogo modais** exigem que os usuários concluam e fechem antes de continuar com a janela do proprietário. Essas caixas de diálogo são mais bem usadas para tarefas críticas ou pouco frequentes que exigem conclusão antes de continuar.
-   As **caixas de diálogo sem janela restrita** permitem que os usuários alternem entre a caixa de diálogo e a janela do proprietário conforme desejado. Essas caixas de diálogo são mais bem usadas para tarefas contínuas, repetitivas e frequentes.

**Uma caixa de diálogo de tarefas é implementada usando a API (interface de programação de aplicativo) de diálogo de tarefa.** Eles consistem nas seguintes partes, que podem ser montadas em uma variedade de combinações:

-   Uma **barra de título** para identificar o recurso do aplicativo ou do sistema no qual a caixa de diálogo veio.
-   Uma **instrução principal**, com um ícone opcional, para identificar o objetivo do usuário com a caixa de diálogo.
-   Uma **área de conteúdo** para informações e controles descritivos.
-   Uma **área de comando** para botões de confirmação, incluindo um botão de cancelamento e mais opções opcionais e não mostrar este &lt; item &gt; novamente controles.
-   Uma **área de nota de rodapé** para obter explicações e ajuda adicionais opcionais, normalmente direcionadas a usuários menos experientes.

![captura de tela de uma caixa de diálogo de tarefa típica ](images/win-dialog-box-image2.png)

Uma caixa de diálogo de tarefa típica.

**As caixas de diálogo de tarefas são recomendadas sempre que forem apropriadas, pois são fáceis de criar e elas obtêm uma aparência consistente.** as caixas de diálogo de tarefas exigem o Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Microsoft Windows.

Um painel de tarefas é como uma caixa de diálogo, exceto que é apresentada dentro de um painel de janela em vez de uma janela separada. Como resultado, os painéis de tarefas têm uma ideia mais direta e contextual do que as caixas de diálogo. Embora tecnicamente eles não sejam os mesmos, os **painéis de tarefas são tão semelhantes às caixas de diálogo que suas diretrizes são apresentadas neste artigo**.

![captura de tela de um painel de tarefas típico ](images/win-dialog-box-image3.png)

Um painel de tarefas típico.

As [janelas de propriedades](win-property-win.md) são um tipo especializado de caixa de diálogo usado para exibir e alterar propriedades de um objeto, coleção de objetos ou um programa. Além disso, as janelas de propriedades normalmente dão suporte a várias tarefas, enquanto as caixas de diálogo normalmente dão suporte a uma única tarefa ou etapa em uma tarefa. Como seu uso é especializado, as **janelas de propriedades são cobertas em um conjunto diferente de diretrizes**.

As caixas de diálogo podem ter [guias](ctrl-tabs.md)e, se forem chamadas de caixas de diálogo com guias. As janelas de propriedades são determinadas pela apresentação das propriedades, não pelo uso de guias.

**Observação:** As diretrizes relacionadas ao [layout](vis-layout.md), ao [Gerenciamento de janelas](win-window-mgt.md), às caixas de diálogo comuns, janelas de [Propriedades](win-property-win.md), [assistentes](win-wizards.md), [confirmações](mess-confirm.md), [mensagens de erro](mess-error.md)e mensagens de [aviso](mess-warn.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **É a finalidade de fornecer aos usuários informações, pedir aos usuários uma pergunta ou permitir que os usuários selecionem opções para executar um comando ou uma tarefa?** Caso contrário, use outra interface do usuário (IU).
-   **É a finalidade de exibir e alterar as propriedades de um objeto, coleção de objetos ou um programa?** Em caso afirmativo, use uma [janela de propriedades](win-property-win.md) ou uma [barra de ferramentas](cmd-toolbars.md) .
-   **É a finalidade de apresentar uma coleção de comandos ou ferramentas?** Nesse caso, use uma barra de ferramentas ou uma [janela de paleta](glossary.md).
-   **É a finalidade de verificar se o usuário deseja continuar com uma ação?** Há um motivo claro para não continuar e uma chance razoável que às vezes os usuários não? Nesse caso, use uma [confirmação](mess-confirm.md).
-   **É a finalidade de fornecer uma mensagem de erro ou de aviso?** Nesse caso, use uma mensagem de [erro](mess-error.md) ou [mensagem de aviso](mess-warn.md).
-   É a finalidade:
    -   Arquivos abertos
    -   Salvar arquivos
    -   Abrir pastas
    -   Localizar ou substituir texto
    -   Imprimir um documento
    -   Selecionar atributos de uma página impressa
    -   Selecionar uma fonte
    -   Escolher uma cor
    -   Procurar um arquivo, uma pasta, um computador ou uma impressora
    -   Pesquisar usuários, computadores ou grupos no Microsoft Active Directory
    -   Solicitar um nome de usuário e uma senha?

Em caso afirmativo, use a [caixa de diálogo comum](win-common-dlg.md) apropriada. Muitas dessas caixas de diálogo comuns são extensíveis.

-   **É a finalidade de executar uma tarefa de várias etapas que requer mais de uma única janela?** Em caso afirmativo, use um [fluxo de tarefas](glossary.md) ou um [Assistente](win-wizards.md) .
-   **É a finalidade de informar os usuários de um evento do sistema ou do programa que não está relacionado à atividade do usuário atual, que não exige ação imediata do usuário e que os usuários podem ignorar livremente?** Nesse caso, use uma [notificação](mess-notif.md) .
-   **É a finalidade de mostrar o status do programa?** Nesse caso, use uma [barra de status](ctrl-status-bars.md) .
-   **Seria preferível usar a interface do usuário in-loco?** As caixas de diálogo podem interromper o fluxo do usuário exigindo atenção. Às vezes, esse intervalo de interrupção é justificado, por exemplo, quando o usuário deve executar uma ação que está fora do contexto atual. Em outros casos, uma abordagem melhor é apresentar a interface do usuário no contexto, seja diretamente com a interface do usuário in-loco (como um painel de tarefas) ou sob demanda usando a [divulgação progressiva](ctrl-progressive-disclosure-controls.md).
-   **É a finalidade de exibir um problema de entrada de usuário não crítico ou uma condição especial?** Nesse caso, use um [balão](ctrl-balloons.md) .
-   **Para fluxos de tarefas, seria preferível usar outra página?** Em geral, você deseja que uma tarefa flua de uma página para uma página em uma única janela. Use caixas de diálogo para confirmar comandos in-loco, para obter entrada para comandos in-loco e para executar tarefas secundárias e autônomas que são mais bem executadas de forma independente e fora do fluxo de tarefas principal.
-   **Para selecionar opções, é provável que os usuários alterem as opções?** Caso contrário, considere alternativas, como:
    -   Usar as opções padrão sem perguntar, mas permitir que os usuários façam alterações posteriormente.
    -   Fornecendo uma versão com opções (por exemplo, **Imprimir...** em um menu), bem como uma versão sem opções (por exemplo, **Imprimir** na barra de ferramentas). Geralmente, os comandos da barra de ferramentas devem ser imediatos e evitar a exibição das caixas de diálogo.
-   **Para selecionar opções, há uma maneira mais simples e direta de apresentar as opções?** Nesse caso, considere alternativas, como:
    -   Usando um [botão de divisão](ctrl-command-buttons.md) para selecionar variações de um comando.
    -   Usando um submenu para comandos, caixas de seleção, botões de opção e listas simples.

![Captura de tela que mostra um menu e um submenu.](images/win-dialog-box-image4.png)

![captura de tela de um menu e submenu ](images/win-dialog-box-image5.png)

Nesses exemplos, os submenus são usados em vez de caixas de diálogo para seleções simples.

## <a name="design-concepts"></a>Conceitos de design

Quando usadas corretamente, as caixas de diálogo são uma ótima maneira de fornecer energia e flexibilidade ao seu programa. Quando inutilizados, as caixas de diálogo são uma maneira fácil de incomodar os usuários, interromper seu fluxo e fazer com que o programa se sinta indireto e entediante para uso. **As caixas de diálogo modais exigem a atenção dos usuários.** As caixas de diálogo geralmente são mais fáceis de implementar do que as UIs alternativas, para que elas tendem a ser utilizadas.

**Uma caixa de diálogo é mais eficaz quando suas características de design correspondem a seu uso.** O design de uma caixa de diálogo é determinado principalmente por sua finalidade (para oferecer opções, fazer perguntas, fornecer informações ou comentários), digitar (modal ou sem janela restrita) e interação do usuário (obrigatória, resposta opcional ou confirmação), enquanto seu uso é basicamente determinado por seu contexto (iniciado pelo usuário ou programa), a probabilidade de ação do usuário e a frequência de exibição.

Para criar caixas de diálogo em vigor, use os seguintes elementos com eficiência:

-   Texto da caixa de diálogo
-   Instruções principais
-   Não mostrar este &lt; item novamente &gt; opção

**Se você fizer apenas uma coisa...**

Certifique-se de que o design da caixa de diálogo (determinado pela finalidade, tipo e interação do usuário) corresponde ao uso (determinado pelo contexto, probabilidade de ação do usuário e frequência de exibição).

## <a name="usage-patterns"></a>Padrões de uso

As caixas de diálogo têm vários padrões de uso:

-   As caixas de diálogo de pergunta (usando botões) fazem aos usuários uma única pergunta ou para confirmar um comando e usam respostas simples em botões de comando organizados horizontalmente.
-   As caixas de diálogo de pergunta (usando links de comando) fazem aos usuários uma única pergunta ou para selecionar uma tarefa a executar e usar respostas detalhadas em links de comando organizados verticalmente.
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
-   **Implemente o uso de uma caixa de diálogo de tarefa sempre que apropriado para obter uma aparência consistente.** As caixas de diálogo de tarefa exigem Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Windows.

### <a name="modeless-dialog-boxes"></a>Caixas de diálogo sem modo

-   **Use para tarefas frequentes, repetitivas e em movimento.**
-   Use um [modelo de commit imediato para](glossary.md) que as alterações entre em vigor imediatamente.
-   Para caixas de diálogo sem modo, use um botão de comando Fechar explícito na caixa de diálogo para fechar a janela. Para ambos, use um botão Fechar na barra de título para fechar a janela.
-   **Considere tornar as caixas de diálogo sem modo encaixadas.** Diálogos sem modo encaixado permitem um posicionamento mais flexível.

![captura de tela de uma caixa de diálogo encaixada e sem modo ](images/win-dialog-box-image7.png)

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

Neste exemplo, Windows diagnóstico de rede consiste em páginas de progresso e resultados.

-   **Não use uma caixa de diálogo de várias páginas se a página de entrada for um diálogo padrão.** Nesse caso, a consistência de usar uma caixa de diálogo padrão é mais importante.
-   **Não use os botões Próximo ou Voltar e não tenha mais de três páginas.** As caixas de diálogo de várias páginas são para tarefas de etapa única com comentários. Eles não são [assistentes](win-wizards.md), que são usados para tarefas de várias etapas. Os assistentes têm uma sensação pesada e indireta em comparação com caixas de diálogo de várias páginas.
-   **Na página de entrada, use botões de comando específicos ou links de comando para iniciar a tarefa.**
-   **Use um botão Cancelar nas páginas de entrada e progresso e um botão Fechar na página de resultados.**

**Desenvolvedores:** Você pode criar diálogos de tarefa de várias páginas usando a [mensagem TDM \_ NAVIGATE \_ PAGE.](../controls/tdm-navigate-page.md)

### <a name="presentation"></a>Apresentação

Para tornar as caixas de diálogo fáceis de encontrar e acessar, associe claramente a caixa de diálogo à sua origem e funcione bem com vários monitores:

-   **Inicialmente, exibe diálogos "centralizados" na parte superior da janela do proprietário.** Para exibição subsequente, considere exibi-lo em seu último local (em relação à janela do proprietário) se for provável que isso seja mais conveniente.

![diagrama da caixa de diálogo centralizada na janela atrás dela ](images/win-dialog-box-image10.png)

Inicialmente, centralmente as caixas de diálogo na parte superior da janela do proprietário.

-   **Se uma caixa de diálogo for contextual, exibe-a perto do objeto do qual ela foi lançada.** No entanto, coloque-o fora do caminho (preferencialmente deslocamento para baixo e para a direita) para que o objeto não seja coberto pela caixa de diálogo.

![diagrama de deslocamento da caixa de diálogo para baixo e para a direita ](images/win-dialog-box-image11.png)

As propriedades de um objeto são exibidas perto do objeto .

-   **Para caixas de diálogo sem modo, é exibida inicialmente na parte superior da janela do proprietário para facilitar a encontrá-la.** Se o usuário ativar a janela do proprietário, isso poderá obscurecer a caixa de diálogo sem modo.
-   **Se necessário, ajuste o local inicial para que toda a caixa de diálogo seja visível no monitor de destino.** Se uma janela resizável for maior que o monitor de destino, reduza-a para se ajustar.
-   **Quando uma caixa de diálogo for replayada, considere exibi-la no mesmo estado que o último acesso.** Ao fechar, salve o monitor usado, o tamanho da janela, o local e o estado (maximizada versus restauração). Na reprodução, restaure o tamanho, o local e o estado da caixa de diálogo salvos usando o monitor apropriado. Além disso, considere fazer com que esses atributos persistam entre instâncias do programa por usuário.
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
-   Se a legenda e o ícone da barra de título já estão exibidos de maneira proeminente próximo à parte superior da janela, você pode ocultar a legenda e o ícone da barra de título para evitar redundância. No entanto, você ainda precisa definir um título adequado internamente para uso pelo Windows.

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
-   **Atribua primeiro as chaves de acesso do botão de confirmação para garantir que elas tenham as atribuições de chave padrão.** Se não houver uma atribuição de chave padrão, use a primeira letra da primeira palavra. Por exemplo, a chave de acesso para botões Sim e Não de confirmação sempre deve ser "Y" e "N", independentemente dos outros controles na caixa de diálogo.
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

-   **Forneça um botão de comando para interromper a operação se levar mais de alguns segundos para ser concluída ou tiver o potencial de nunca ser concluído.** Rotule o botão Cancelar se o cancelamento retornar o ambiente para seu estado anterior (sem efeitos colaterais); caso contrário, rotule o botão Parar para indicar que ele deixa a operação parcialmente concluída intacta. Você pode alterar o rótulo do botão de Cancelar para Parar no meio da operação, se, em algum momento, não for possível retornar o ambiente para seu estado anterior.

![captura de tela da caixa de diálogo com o botão Cancelar ](images/win-dialog-box-image15.png)

Neste exemplo, interromper o diagnóstico do problema não tem nenhum efeito colateral.

-   **Forneça um botão de comando para pausar a operação se levar mais de vários minutos para ser concluída e isso prejudicará a capacidade dos usuários de realizar o trabalho.** Isso não força o usuário a escolher entre concluir a tarefa e realizar seu trabalho.
-   **Reúna o máximo de informações possível antes de iniciar a tarefa.**
-   **Se problemas recuperáveis são detectados, os usuários lidam com todos os problemas encontrados no final da tarefa.** Se isso não for prático, os usuários lidarão com problemas conforme eles ocorrem.
-   **Não abandone tarefas como resultado de erros recuperáveis.**

![captura de tela da caixa de diálogo com o botão Tentar novamente ](images/win-dialog-box-image16.png)

Neste exemplo, o Windows Explorer permite que os usuários continuem com a tarefa após um erro recuperável.

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

h hrs, m mins remaining

m mins, s s segundos restantes

s segundos restantes

**Caso contrário:**

h horas, m minutos restantes

m minutos, s segundos restantes

s segundos restantes

**Para barras de título:**

hh:mm restante

mm:ss restante

0:ss restantes

Esse formato compacto mostra as informações mais importantes primeiro para que ele não seja truncado na barra de tarefas.

-   **Faça estimativas precisas, mas não dê precisão falsa.** Se a maior unidade for de horas, dê minutos (se significativo), mas não segundos.

**Incorreto:**

hh hours, mm minutes, ss seconds

-   **Mantenha a estimativa atualizada.** Tempo de atualização restante estima pelo menos a cada 5 segundos.
-   **Concentre-se no tempo restante** porque essas são as informações que os usuários mais se importam. Dê tempo total decorrido somente quando houver cenários em que o tempo decorrido seja útil (por exemplo, quando a tarefa provavelmente será repetida). Se a estimativa de tempo restante estiver associada a uma barra de progresso, não tenha o texto completo percentual porque essas informações são transmitidas pela própria barra de progresso.
-   **Seja gramaticalmente correto.** Use unidades singulares quando o número for um.

**Incorreto:**

1 minuto, 1 segundo

-   **Use a capitalização com estilo de frase.**

Para obter mais informações e exemplos, consulte Barras [de progresso](progress-bars.md).

### <a name="icons-and-graphics"></a>Ícones e elementos gráficos

**Elementos gráficos**

-   **Não use gráficos grandes que não servem para nenhuma finalidade além de preencher o espaço com óculos.** Em vez disso, mantenha a aparência simples.

**Incorreto:**

![captura de tela da caixa de diálogo com um gráfico grande ](images/win-dialog-box-image18.png)

Neste exemplo, o gráfico grande não serve para nenhuma finalidade.

**Ícones da barra de título**

-   **As caixas de diálogo não têm ícones de barra de título.**
    -   **Exceção:** Se uma caixa de diálogo for usada para implementar uma janela primária (como um utilitário) e, portanto, aparecer na barra de tarefas, ela terá um ícone de barra de título.

**Ícones de corpo**

-   **Escolha o ícone de corpo com base no padrão de design:**



| Padrão | Ícone de corpo |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Diálogos de pergunta**<br/>      | Programa, recurso, objeto, ícone de aviso (se possível perda de dados ou acesso ao sistema), aviso de segurança ou nenhum.<br/> |
| **Caixas de diálogo de escolha**<br/>        | Nenhum.<br/>                                                                                                           |
| **Diálogos de progresso**<br/>      | Nenhum (mas pode ter uma animação).<br/>                                                                               |
| **Caixas de diálogo informativas**<br/> | Nenhum.<br/>                                                                                                           |



 

-   **Incorreto:**

![captura de tela da caixa de diálogo com o ícone de aviso ](images/win-dialog-box-image19.png)

Neste exemplo, um ícone de aviso é usado incorretamente para uma pergunta que não envolve perda potencial de dados ou acesso ao sistema.

- **Considere usar ícones para ajudar os usuários a reconhecer visualmente os recursos do programa.** Essa técnica é mais eficaz quando os ícones são facilmente reconhecíveis e usados em vários locais em seu programa.

![captura de tela da caixa de diálogo favoritos com ícone de estrela ](images/win-dialog-box-image20.png)

Neste exemplo, o ícone de estrela amarela representa Favoritos. O ícone é facilmente reconhecível e é usado consistentemente em Windows para representar favoritos.

-   **Use ícones para ajudar os usuários a reconhecer o objeto em questão.**

![captura de tela da caixa de diálogo com o ícone do powerpoint ](images/win-dialog-box-image21.png)

Neste exemplo, o ícone do objeto ajuda os usuários a reconhecer o tipo de arquivo que está sendo aberto ou salvo.

-   **Considere usar ícones para ajudar a tornar os recursos autoexplicativos.**

![imagens de setas mostrando como posicionar o monitor ](images/win-dialog-box-image22.png)

Neste exemplo, esses ícones ajudam os usuários a visualizar o efeito de seus recursos.

-   **Use um ícone nas caixas de diálogo Sobre Caixa para identidade visual do aplicativo.**

![captura de tela da caixa de diálogo sobre com o logotipo do Windows ](images/win-dialog-box-image23.png)

Neste exemplo, um bitmap é usado no About Box para identificar e identificar o aplicativo.

**Ícones de nota de rodapé**

-   **Se você tiver uma nota de rodapé, considere usar um ícone de nota de rodapé para resumir o assunto da nota de rodapé.**

![captura de tela da caixa de diálogo com o ícone de nota de rodapé ](images/win-dialog-box-image24.png)

Neste exemplo, o ícone de nota de rodapé indica que a pergunta tem implicações de segurança.

-   **Não use um ícone de nota de rodapé que repita o ícone de corpo.**
-   **Não use os ícones padrão de erro ou informações.** As condições de erro devem ser transmitidas por meio do ícone de corpo e as notas de rodapé são sempre para obter informações, tornando o ícone de informações redundante. No entanto, você pode usar o ícone de aviso padrão e o blindagem de segurança amarelo para alertar os usuários sobre consequências arriscadas.

Para obter mais informações e exemplos, consulte [Ícones](vis-icons.md).

### <a name="commit-buttons"></a>Botões de commit

**Observações:**

-   Essas diretrizes não se aplicam a diálogos de pergunta usando links de comando, porque esse padrão usa links de comando em vez de botões.
-   \[Faça isso \] e Não faça isso são respostas \[ \] afirmativas e negativas, respectivamente, à instrução principal.

**Geral**

-   **Escolha os botões de confirmação com base no padrão de design:**

    
| | | <strong>Padrão</strong><br /> | <strong>Botões de commit</strong><br /> | | <strong>Diálogos de pergunta (usando botões)</strong><br /> | Um dos seguintes conjuntos de comandos concisos: Sim/Não, Sim/Não/Cancelar, [Do it]/Cancel, [Do it]/[Don't do it], [Do it]/[Don't do it]/Cancel.<br /> | | <strong>Diálogos de pergunta (usando links)</strong><br /> | Cancelar.<br /> | | <strong>Caixas de diálogo de escolha</strong><br /> | <ul><li>Caixas de diálogo modais: OK/Cancelar ou [Fazer]/Cancelar</li><li>Caixas de diálogo sem modo: botão Fechar na caixa de diálogo e na barra de título</li><li>Painel de tarefas: botão Fechar na barra de título</li></ul> | | <strong>Diálogos de progresso</strong><br /> | Use Cancelar se retornar o ambiente para seu estado anterior (sem nenhum efeito colateral); caso contrário, use Parar.<br /> | | <strong>Caixas de diálogo informativas</strong><br /> | Perto.<br /> | 


    

     

-   **Todos os botões de confirmação, exceto Aplicar, resultam no fechamento da janela da caixa de diálogo.**
-   **Não confirme os botões de confirmação.** Fazer isso desnecessariamente pode ser muito entediante. **Exceções:**

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

-   **Não use os botões Sim e Não se o significado da resposta Não estiver claro.** Em caso afirmado, use respostas específicas.

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

**Observação:** Caixas de diálogo indiretas são exibidas fora do contexto, como um resultado indireto de uma tarefa ou o resultado de um problema com um sistema ou processo em segundo plano. Para diálogos indiretos, o botão Cancelar é ambíguo porque pode significar cancelar a caixa de diálogo ou cancelar toda a tarefa.

-   **Se os usuários precisam cancelar a caixa de diálogo e a tarefa, dê botões de confirmação para fazer ambos.** Rotule o botão que cancela a caixa de diálogo com uma resposta negativa à instrução principal. Rotule o botão que cancela toda a tarefa com Cancelar. Usar Cancelar permite que a caixa de diálogo seja usada em muitos contextos.

    **Correto:**

    ![captura de tela da caixa de diálogo com salvar/não salvar ](images/win-dialog-box-image38.png)

    Neste exemplo, essa caixa de diálogo é exibida por Windows Paint como resultado de um comando New ou Exit quando o gráfico não foi salvo. Não Salvar fecha a caixa de diálogo sem salvar, enquanto Cancelar cancela o comando Novo ou Sair.

    **Incorreto:**

    ![captura de tela da caixa de diálogo com botões sim/não ](images/win-dialog-box-image39.png)

    Neste exemplo, não há como cancelar a tarefa (fechar Office Barra de Atalho) que levou à exibição dessa caixa de diálogo. Essa caixa de diálogo precisa de um botão Cancelar.

-   Se os usuários apenas precisam cancelar a caixa de diálogo, mas não **a tarefa, use** um botão com uma resposta negativa específica à instrução principal e não tenha um botão Cancelar.

    ![captura de tela da caixa de diálogo com executar/não executar ](images/win-dialog-box-image24.png)

    Neste exemplo, essa caixa de diálogo é exibida indiretamente como resultado da navegação para uma página da Web que instala um controle ActiveX dados. Usar Cancelar seria ambíguo aqui, portanto, Não executar é usado em vez disso.

Para obter mais informações e exemplos, consulte [Botões de comando](ctrl-command-buttons.md).

### <a name="command-links"></a>Links de comando

-   **Apresente um conjunto de comandos longos usando links de comando, em vez de botões de comando ou uma combinação de botões de opção e um botão OK.** Isso permite que os usuários respondam com um único clique. No entanto, essa abordagem funciona apenas para uma única pergunta.
-   **Apresente os links de comando mais usados primeiro.** A ordem resultante deve seguir aproximadamente a probabilidade de uso, mas também ter um fluxo lógico.
    -   **Exceção:** Os links de comando que resultam em fazer tudo devem ser colocados primeiro.
-   Se um link de comando exigir mais explicações, **forneça uma explicação complementar.** Explicações complementares descrevem por que os usuários podem querer escolher o comando ou o que acontece se o comando for escolhido.
-   **Não use explicações complementares que sejam restatementações wordy do link de comando.** Use uma explicação complementar somente quando não for possível tornar um link de comando autoexplicativo. Fornecer uma explicação complementar para um link de comando não significa que você precisa forenciá-los para todos os comandos.

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

### <a name="dont-show-this-ltitemgt-again"></a>Não mostrar este &lt; item &gt; novamente

-   **Considere usar uma opção Não mostrar este item novamente para permitir que os usuários suprimem uma caixa de diálogo recorrente, somente se não &lt; &gt; houver uma alternativa melhor.** É melhor sempre mostrar a caixa de diálogo se os usuários realmente precisam dela ou simplesmente eliminá-la caso não precisem.
-   **Use essa frase específica para substituir &lt; o item pelo item &gt; específico.** Por exemplo, Não mostrar este lembrete novamente. Ao fazer referência a uma caixa de diálogo em geral, use Não mostrar esta mensagem novamente.
-   **Indique claramente quando a entrada do usuário será** usada para valores padrão futuros adicionando a seguinte frase na opção: Suas seleções serão usadas por padrão no futuro.
-   **Não selecione a opção por padrão. Se a caixa de diálogo realmente precisar ser exibida apenas uma vez, faça isso sem perguntar.** Não use essa opção como um contrassalente para que os usuários se certifiquem de que o comportamento padrão não seja entediante.

**Incorreto:**

![captura de tela da mensagem fazendo uma pergunta desnecessária ](images/win-dialog-box-image42.png)

Neste exemplo, a mensagem deve ser exibida apenas uma vez. Não é necessário perguntar.

-   **Faça com que a configuração persista por usuário.**
-   **Se os usuários selecionarem a opção e clicarem em Cancelar, essa opção entre em vigor.** Essa configuração é uma meta-opção, portanto, ela não segue o comportamento padrão Cancelar de não deixar nenhum efeito colateral. Observe que, se os usuários não quiserem ver a caixa de diálogo no futuro, provavelmente eles também querem cancelá-la.
-   Se os usuários talvez precisem restaurar essas caixas de diálogo, forneça **um comando Restaurar** mensagens na caixa de diálogo Opções do programa.

### <a name="ask-me-later"></a>Perguntar depois

-   Forneça esta opção para descartar uma caixa de diálogo somente quando:
    -   **A caixa de diálogo é indireta,** portanto, os usuários provavelmente se concentram em outra tarefa.
    -   **Os usuários devem responder, mas não imediatamente,** para que possam continuar com seu trabalho.
    -   **A pergunta requer um esforço ou um esforço** suficiente para que os usuários possam tomar decisões melhores se receberem mais tempo.
    -   **A caixa de diálogo ou a opção será apresentada automaticamente posteriormente** (para que os usuários realmente sejam solicitados posteriormente).
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
-   **Com as caixas de diálogo de tarefas, evite combinar mais ou menos controles com não mostrar este &lt; item &gt; novamente.** Essa combinação tem uma aparência estranha.
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
    -   **Selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema), a resposta mais segura para o padrão.** Se segurança e segurança não são fatores, selecione a resposta mais provável ou conveniente.
        -   **Exceção:** Não faça uma resposta destrutiva o padrão, a menos que haja uma maneira fácil e óbvia de desfazer o comando.
-   Para caixas de diálogo de escolha:
    -   Para os valores padrão iniciais, selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema) e os valores mais **seguros para cada controle.** Se segurança e segurança não são fatores, selecione as opções mais prováveis ou convenientes.
    -   Para os valores padrão **subsequentes, reselecione** as opções selecionadas anteriormente se esses valores provavelmente forem repetidos, e fazer isso é seguro e seguro. Caso contrário, selecione os valores padrão iniciais.

![captura de tela da caixa de diálogo imprimir ](images/win-dialog-box-image49.png)

Neste exemplo, é mais provável que os usuários escolham as mesmas configurações de impressão da última vez. No entanto, é provável que o número de cópias desejadas mude, portanto, essa configuração não é reeleita.

## <a name="recommended-sizing-and-spacing&quot;></a>Espaçamento e o espaçamento recomendados

-   **Suporte à resolução mínima Windows vista de 800 x 600 pixels.** Os layouts podem ser otimizados para janelas reizáveis usando uma resolução de tela de 1024 x 768 pixels.
-   **Use janelas reizáveis sempre que for prático para evitar barras de rolagem e dados truncados.** Windows com conteúdo dinâmico e listas se beneficiam mais de janelas reizáveis.
-   **As janelas de tamanho fixo devem ser totalmente visíveis e dimensionada para se ajustarem à área de trabalho.**
-   **As janelas reizáveis podem ser otimizadas para resoluções mais altas, mas dimensionados conforme necessário no tempo de exibição para a resolução real da tela.**
-   **Escolha um tamanho de janela padrão apropriado para seu conteúdo.** Não tenha medo de usar tamanhos de janela iniciais maiores se você puder usar o espaço com eficiência.

## <a name=&quot;text&quot;></a>Texto

### <a name=&quot;general&quot;></a>Geral

-   **Remova texto redundante.** Procure texto redundante em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de commit. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância de outros locais.
-   **Use frases positivas.** Frase positiva é mais fácil para os usuários entenderem.

**Correto:**

Você deseja habilitar o compartilhamento de arquivos e impressoras?

**Incorreto:**

Você deseja desabilitar o compartilhamento de arquivos e impressoras?

No entanto, a frase deve corresponder ao comando associado, mesmo que o comando seja frasedo negativamente; portanto, por exemplo, use disable para confirmar um comando Disable.

-   **Se necessário, use a palavra &quot;janela&quot; para se referir à própria caixa de diálogo.**
-   **Use a segunda pessoa (&quot;você/seu") para** dizer aos usuários o que fazer na área principal de instrução e conteúdo. Geralmente, a segunda pessoa está implícita.

**Exemplos:**

Escolha as imagens que você deseja imprimir

Escolha uma conta

-   **Use a primeira pessoa ("I/me/my")** para permitir que os usuários diga ao programa o que fazer em controles na área de conteúdo que respondem à instrução principal.

**Exemplo:** Imprima as fotos na minha câmera.

### <a name="dialog-box-titles"></a>Títulos da caixa de diálogo

-   **Use o título para identificar o comando, o recurso ou o programa de onde uma caixa de diálogo veio.**
    -   Se a caixa de diálogo for iniciada pelo usuário, identifique-a usando o comando ou o nome do recurso. **Exceções:**
        -   Se uma caixa de diálogo for exibida por muitos comandos diferentes, considere usar o nome do programa.
        -   Se esse título for redundante com a instrução principal, use o nome do programa.
    -   Se ele for iniciado pelo programa ou pelo sistema (e, portanto, fora do contexto), identifique-o usando o programa ou o nome do recurso para dar contexto.
    -   Não use o título para explicar o que fazer na caixa de diálogo que é a finalidade da instrução principal.
-   Use o nome exato do comando para nomes baseados em comando, mas não inclua as reellipses se houver um. Você pode incluir o título do menu do comando, se necessário, para compor um bom título. Exemplo: para um Objeto... em um menu Inserir, use o título Inserir Objeto.
-   **Se uma caixa de diálogo** sem modo for exibida na barra de tarefas, otimize o título para exibição na barra de tarefas colocando concisamente as informações de distinção primeiro. Exemplos: "66% Concluído" e "3 Lembretes".
-   **Não inclua as palavras "dialog" ou "progress" no título.** Isso é implícito e deixá-lo desligado facilita a verificação dos usuários.
-   Use [a capitalização de estilo de título](glossary.md), sem terminar a pontuação.

### <a name="main-instructions"></a>Instruções principais

-   **Use a instrução principal para explicar concisamente o que fazer na caixa de diálogo.** A instrução deve ser uma instrução específica, uma direção imperativa ou uma pergunta. Boas instruções comunicam o objetivo do usuário com a caixa de diálogo em vez de se concentrar puramente na mecânica de manipulação.
-   **Omita a instrução principal quando a única coisa que você pode dizer for óbvia.** Nesses casos, o conteúdo da caixa de diálogo é autoexplicativo. Por exemplo, as caixas de diálogo comuns Abrir Arquivo e Salvar Arquivo não precisam de uma instrução principal porque seu contexto e design torna sua finalidade óbvia.
-   **Omita rótulos de controle que restate a instrução principal.** Nesse caso, a instrução principal recebe a chave de acesso.

**Aceitável:**

![captura de tela da caixa de texto com rótulo redundante ](images/win-dialog-box-image50.png)

Neste exemplo, o rótulo da caixa de texto é apenas uma reformulação da instrução principal.

**Melhor:**

![captura de tela da mesma caixa de texto com um rótulo ](images/win-dialog-box-image51.png)

Neste exemplo, o rótulo redundante é removido, portanto, a instrução principal assume a chave de acesso.

-   **Seja conciso, use apenas uma única frase completa.** Pare a instrução principal até as informações essenciais. Se você precisa explicar mais alguma coisa, use instruções complementares.
-   **Use verbos específicos sempre que possível.** Verbos específicos (exemplos: conectar, salvar, instalar) são mais significativos para os usuários do que os genéricos (exemplos: configurar, gerenciar, definir).
-   Use [a capitalização de estilo de frase](glossary.md).
-   **Não inclua períodos finais se a instrução for uma instrução.** Se a instrução for uma pergunta, inclua um ponto de interrogação final.
-   **Para diálogos de progresso, use uma frase gerund** explicando brevemente a operação em andamento, terminando com reellipse. Exemplo: imprimindo suas imagens...
-   **Dica:** Você pode avaliar uma instrução principal com o que você poderia dizer a um amigo. Se responder com a instrução principal for anormal, insínteante ou inconveniente, retrabalho a instrução.

### <a name="supplemental-instructions"></a>Instruções complementares

-   **Quando necessário, use uma instrução complementar opcional para apresentar informações adicionais úteis para entender ou usar a página.** Você pode fornecer informações mais detalhadas e definir a terminologia.
-   **Se a aparência da caixa de diálogo for iniciada pelo programa ou pelo sistema (e, portanto, fora do contexto), use a instrução complementar para explicar por que a caixa de diálogo apareceu.** Para esses diálogos, o contexto geralmente não é óbvio.
-   **Não repita a instrução principal com um texto ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver mais a adicionar.
-   Use frases completas, capitalização de estilo de frase e pontuação final.

### <a name="command-links"></a>Links de comando

-   **Escolha texto de link conciso que se comunique claramente e diferencie o que o link de comando faz.** Ele deve ser autoexplicativo e corresponder à instrução principal. Os usuários não devem ter que descobrir o que o link realmente significa ou como ele difere de outros links.
-   **Sempre inicie links de comando com um verbo.**
-   Use a capitalização com estilo de frase.
-   Não use pontuação final.
-   **Se necessário, forneça qualquer explicação posterior usando frases completas e pontuação final.** No entanto, adicione essas explicações somente quando necessário não adicione explicações a todos os links de comando apenas porque um link de comando precisa de um.

Para obter mais informações e exemplos, consulte [Diretrizes de Link](ctrl-command-links.md) de Comando.

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

exemplo: em **Segurança do Windows**, clique em **mais opções**.

