---
title: Teclado
description: O teclado é o dispositivo de entrada primário usado para entrada de texto no Microsoft Windows. Para acessibilidade e eficiência, a maioria das ações também pode ser executada usando o teclado.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c1554ca1a9769b562f154498cd0871bc1b813067
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524290"
---
# <a name="keyboard"></a>Teclado

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

O teclado é o dispositivo de entrada primário usado para entrada de texto no Microsoft Windows. Para acessibilidade e eficiência, a maioria das ações também pode ser executada usando o teclado.

Os teclados também podem se referir a teclados virtuais, na tela e de escrita de pads usados por computadores sem um mouse físico, como computadores baseados em Tablet.

![captura de tela do teclado virtual ](images/inter-keyboard-image1.png)

O teclado virtual Windows Tablet and Touch Technology.

![captura de tela do painel de escrita do Tablet Windows ](images/inter-keyboard-image2.png)

O painel de escrita da tecnologia Windows Tablet e Touch.

Há seis tipos básicos de chaves:

-   Uma chave de caractere envia um caractere literal para a janela com o foco de entrada.
-   Uma tecla modificadora combinada com outra chave altera o significado de sua chave associada, como CTRL, ALT, Shift e a tecla de logotipo do Windows.
-   As teclas de navegação são as setas direcionais, além de Home, end, Page up e Page Down.
-   As chaves de edição são inserir, backspace e Delete.
-   As teclas de função são F1 por meio de F12.
-   As chaves do sistema colocam o sistema em um modo ou executam uma tarefa do sistema, como tela de impressão, Caps Lock e num lock.

Chaves de acesso são chaves ou combinações de teclas usadas para acessibilidade para interagir com todos os controles ou itens de menu usando o teclado. As teclas de atalho são chaves ou combinações de teclas usadas por usuários avançados para executar comandos usados com frequência para eficiência. O Windows indica as chaves de acesso ao sublinhar a atribuição de chave de acesso.

![captura de tela de teclas de acesso e teclas de atalho ](images/inter-keyboard-image3.png)

Este exemplo mostra as teclas de acesso e as teclas de atalho.

Para eliminar a desordem Visual, o Windows oculta os sublinhados de chave de acesso por padrão e os exibe somente quando a tecla Alt é pressionada. Para manter a consistência com o Windows, as imagens no guia de UX também são mostradas com os sublinhados de chave de acesso ocultos, a menos que a diretriz envolva chaves de acesso.

Para melhorar a conscientização das atribuições de chave de acesso em seu programa durante todo o processo de desenvolvimento, você pode exibi-las em todos os momentos. No painel de controle, acesse a central de facilidade de acesso e clique em **facilitar o uso do teclado**; em seguida, marque a caixa de seleção **sublinhar atalhos de teclado e chaves de acesso** .

**Observação:** As diretrizes relacionadas à [acessibilidade](inter-accessibility.md) são apresentadas em um artigo separado.

## <a name="design-concepts"></a>Conceitos de design

### <a name="elements-of-keyboard-navigation"></a>Elementos da navegação do teclado

Os usuários interagem com uma janela usando o teclado navegando para controles, fazendo seleções e executando comandos. Os elementos a seguir funcionam em conjunto para fazer com que isso aconteça.

![captura de tela da caixa de diálogo Editar cores ](images/inter-keyboard-image4.png)

Para ilustrar os elementos da navegação por teclado na lista a seguir, vamos nos referir a essa caixa de diálogo.

-   **Foco de entrada.** O controle com foco de entrada recebe a maioria das entradas de teclado. O foco de entrada é indicado com um retângulo pontilhado chamado de retângulo de foco. Algumas entradas de teclado são enviadas para controles que não têm o foco de entrada, conforme explicado posteriormente.

    ![captura de tela da primeira linha na caixa de diálogo Editar cores ](images/inter-keyboard-image5.png)

    O primeiro controle Basic Colors tem o foco de entrada, conforme indicado com um retângulo pontilhado.

-   **Tecla Tab e paradas de tabulação.** A tecla Tab é o mecanismo principal para navegar em uma janela. A tecla Tab visita apenas esses controles com uma parada de tabulação. Todos os controles interativos devem ter paradas de tabulação (a menos que estejam em um grupo), enquanto os controles não interativos, como rótulos, não devem.
-   **Ordem de tabulação.** Todos os controles com tabulações são visitados na ordem de tabulação. Pressionar TAB move o foco de entrada para o próximo controle na ordem de tabulação, enquanto pressionar SHIFT + TAB move o foco de entrada para o controle anterior.
-   **Grupos de controle.** Um conjunto de controles relacionados pode ser feito em um grupo e receber uma única parada de tabulação. Grupos de controle são usados para conjuntos de controles que se comportam como um único controle, como botões de opção. Eles também podem ser usados quando há muitos controles para navegar de forma eficiente somente com a tecla Tab.

    ![captura de tela de grupos de cores básica e personalizada ](images/inter-keyboard-image6.png)

    Cores básicas e cores personalizadas são grupos de controle, dando a essa caixa de diálogo cinco paradas de tabulação. Há muitos controles que a navegação seria ineficiente sem usar grupos de controle.

-   **Teclas de direção.** As teclas de seta movem o foco de entrada entre os controles dentro de um grupo. Pressionar a tecla de seta para a direita move o foco de entrada para o próximo controle na ordem de tabulação, enquanto pressionar a seta para a esquerda move o foco de entrada para o controle anterior. Início, fim, para cima e para baixo também têm o comportamento esperado dentro de um grupo. Os usuários não podem navegar fora de um grupo de controle usando as teclas de direção.
-   **Botões padrão.** O Windows com botões de comando e links de comando têm um único botão padrão indicado por uma borda realçada, que é o botão que é clicado quando a tecla Enter é pressionada. Há um único botão de comando padrão ou link de comando atribuído por padrão. No entanto, o botão padrão é movido quando o usuário faz a tabulação para outro botão de comando ou link de comando. Consequentemente, qualquer botão de comando ou link de comando com foco de entrada também é sempre o botão padrão.

    ![captura de tela dos botões OK e cancelar ](images/inter-keyboard-image7.png)

    O botão OK normalmente é o botão padrão, conforme indicado por sua borda realçada. No entanto, se o usuário fosse tabular para o botão Cancelar, ele se tornaria o botão padrão e será ativado com a tecla Enter.

-   **Barra de espaços, Enter e teclas ESC.** A barra de espaços ativa o controle com o foco de entrada, enquanto a tecla ENTER ativa o botão padrão. Pressionar a tecla ESC cancela ou fecha a janela.
-   **Chaves de acesso.** As chaves de acesso são usadas para interagir com controles diretamente, em vez de navegar com Tab. Eles são combinados com a tecla Alt e são indicados com uma letra sublinhada em seu rótulo.
-   **Acessar rótulos de chave.** Embora alguns controles contenham seus próprios rótulos, como botões de comando, caixas de seleção e botões de opção, outros controles têm rótulos externos, como caixas de listagem e exibições de árvore. Para rótulos externos, a chave de acesso é atribuída ao rótulo e, se invocada, navega para o próximo controle na ordem de tabulação. Os botões rotulados OK, cancelar e fechar não são chaves de acesso atribuídas porque são invocados com Enter e ESC.

    ![captura de tela de rótulos com ' b ' e ' d' sublinhados ](images/inter-keyboard-image8.png)

    Pressionar ALT + B navega para a cor básica selecionada, pressionar ALT + D clica no botão definir cores personalizadas, Enter invoca o botão OK e ESC invoca cancelar.

-   **Comportamento da chave de acesso.** Quando uma chave de acesso é invocada e é atribuída exclusivamente, o controle associado é clicado. Se a atribuição não for exclusiva, o controle associado receberá o foco de entrada. Se o usuário digitar a mesma chave de acesso novamente, o próximo controle na ordem de tabulação com a mesma atribuição receberá o foco de entrada.

Embora esse mecanismo seja razoavelmente complicado, ele também é bastante intuitivo. Os usuários pegam a maioria desses detalhes imediatamente, embora poucos possam explicar exatamente como eles funcionam.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Suporte de teclado para acessibilidade e usuários avançados

**No Windows, a criação para o teclado se resume a fornecer navegação de teclado bem projetada, chaves de acesso para acessibilidade e teclas de atalho para usuários avançados.**

Para garantir que a funcionalidade do programa esteja facilmente disponível para a maior variedade de usuários, incluindo aqueles que têm deficiências e deficiências, todos os elementos interativos da interface do usuário devem ser acessíveis pelo teclado. Em geral, isso significa que os elementos da interface do usuário usados com mais frequência são acessíveis usando uma única combinação de tecla de acesso ou chave, enquanto elementos usados com menos frequência podem exigir navegação de tecla de seta ou guia adicional. Para esses usuários, a capacidade de abrangência é mais importante do que consistência.

Para garantir que a funcionalidade do programa seja eficiente para usuários experientes, os elementos de interface do usuário comumente usados também devem ter teclas de atalho para acesso direto ao teclado. Os usuários experientes muitas vezes têm uma forte preferência por usar o teclado, pois os comandos de teclado podem ser inseridos mais rapidamente e não exigem remover as mãos do teclado. Para esses usuários, eficiência e consistência são cruciais; a abrangência é importante apenas para os comandos mais usados.

Há distinções sutis ao criar o acesso ao teclado para esses dois grupos, motivo pelo qual o Windows fornece dois mecanismos independentes de acesso de teclado direto. Ao usar o acesso e as teclas de atalho com eficiência, você pode dar a seus programas um acesso de teclado eficiente, consistente e abrangente que beneficia todos.

### <a name="access-keys"></a>Chaves de acesso

As teclas de acesso possuem as seguintes características:

-   Elas usam a tecla Alt, mais uma tecla alfanumérica.
-   Elas são principalmente para acessibilidade.
-   Elas são atribuídas a todos os menus e a maioria dos controles de caixa de diálogo.
-   Elas não devem ser memorizadas, portanto, estão documentadas diretamente na interface do usuário, com o caractere de rótulo de controle correspondente sublinhado.
-   Elas afetam apenas a janela atual, navegando ao menu de itens ou controle correspondente.
-   Elas não são atribuídas consistentemente porque nem sempre podem. No entanto, as teclas de acesso devem ser atribuídas consistentemente a comandos usados comumente, em especial os botões de confirmação.
-   Elas são localizadas.

Como as chaves de acesso não devem ser **memorizadas,** elas são atribuídas a um caractere que está no início do rótulo para torná-las fáceis de encontrar, mesmo se houver uma palavra-chave que aparece posteriormente no rótulo.

**Correto:**

![captura de tela do primeiro caractere no rótulo sublinhado ](images/inter-keyboard-image9.png)

**Incorreto:**

![captura de tela do 21º caractere sublinhado ](images/inter-keyboard-image10.png)

No exemplo correto, a chave de acesso é atribuída a um caractere que está no início do rótulo.

### <a name="shortcut-keys"></a>Teclas de atalho

Por outro lado, as teclas de atalho têm as seguintes características:

-   Elas usam principalmente as sequências de teclas Ctrl e Função (as teclas de atalho do sistema Windows também usam Alt+teclas não alfanuméricas e o logotipo do Windows).
-   Elas são principalmente para eficiência de usuários avançados.
-   Elas são atribuídas apenas a comandos usados mais comumente.
-   Elas devem ser memorizadas e estão documentadas apenas em menus, dicas de ferramentas e na Ajuda.
-   Elas têm efeito em todo o programa, mas não têm nenhum efeito caso não se apliquem.
-   Elas devem ser atribuídas consistentemente, uma vez que são memorizadas e não diretamente documentadas.
-   Elas não são localizadas.

Como as teclas de atalho devem ser **memorizadas,** as teclas de atalho usadas com mais frequência usam letras dos primeiros ou mais memorizáveis caracteres dentro das palavras-chave do comando, como Ctrl+C para Cópia e Ctrl+Q para Solicitação.

Significados inconsistentes para teclas de atalho conhecidas são frustrantes e causam erros.

**Incorreto:**

![captura de tela do botão de avanço com "w" sublinhado ](images/inter-keyboard-image11.png)

Neste exemplo, Ctrl+F é o atalho padrão para Find, portanto, atribuí-lo a Encaminhar é frustrante e propenso a erros. Ctrl+W seria uma opção melhor e fácil de lembrar.

Por fim, como elas devem ser memorizadas, as teclas de atalho específicas do aplicativo fazem sentido apenas para programas e recursos que são executados com frequência suficiente para os usuários incentivados a **memorizar.** Programas e recursos usados raramente não precisam de teclas de atalho. Por exemplo, os programas de instalação e a maioria dos assistentes não precisam de nenhuma atribuição especial de tecla de atalho, nem de comandos usados raramente em um aplicativo de produtividade.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Atribuindo chaves de acesso nas caixas de diálogo

Sempre que possível, atribua chaves de acesso exclusivas a todos os controles interativos, exceto aqueles que normalmente não são chaves de acesso atribuídas. No entanto, em inglês há apenas 26 caracteres. Alguns caracteres podem não aparecer em nenhum dos rótulos e pode não haver caracteres distintos em todos os rótulos, reduzindo ainda mais esse número. Além disso, você deve planejar ter alguns caracteres não atribuídos para facilitar a localização. Consequentemente, você pode atribuir apenas cerca de 20 chaves de acesso exclusivas em uma única caixa de diálogo.

Se você tiver uma caixa de diálogo com mais de 20 controles interativos, não atribua chaves de acesso a alguns controles ou, em situações raras, atribua chaves de acesso duplicadas.

![captura de tela da caixa de diálogo de fonte ](images/inter-keyboard-image12.png)

Quando há muitos controles interativos, nem todos eles precisam de uma chave de acesso atribuída.

Use o procedimento geral a seguir para atribuir chaves de acesso:

-   Primeiro, atribua chaves de acesso aos [botões de confirmação](glossary.md) e links de comando. Use a tabela de atribuições de chave de acesso padrão quando ela se aplicar; caso contrário, use a primeira letra da primeira palavra.
-   Ignore os controles que não são atribuídos a chaves de acesso.
-   Atribua chaves de acesso exclusivas aos controles restantes (começando com os mais usados):
    -   Se possível, atribua a chave de acesso de acordo com a tabela de atribuições de chave de acesso padrão.
    -   Caso contrário:
        -   Prefira caracteres que aparecem no início do rótulo, idealmente o primeiro caractere da primeira ou segunda palavra.
        -   Prefira uma consoante distinta ou uma voga, como "x" em "Exit".
        -   Prefira caracteres com larguras largas, como w, m e letras maiúsculas.
        -   Evite usar caracteres que dificultam a imagem do sublinhado, como letras com um pixel de largura, letras com descendentes e letras ao lado de uma letra com um descendente.
-   Se nem todos os controles puderem ter chaves de acesso exclusivas (comece com o menos usado):
    -   Se houver grupos de controles relacionados, como:
        -   Um único conjunto de botões de rádio
        -   Um conjunto de caixas de seleção relacionadas
        -   Um conjunto de controles relacionados dentro de uma caixa de grupo

Atribua chaves de acesso a rótulos de grupo em vez dos controles individuais. Normalmente, você faria o oposto. (Ao fazer isso, certifique-se de que haja um grupo de controle definido para esses controles.)

-   Se ainda não todos os controles puderem ter chaves de acesso exclusivas:
    -   Você poderá atribuir chaves de acesso não exclusivas se:
        -   De outra forma, os controles seriam muito difíceis de navegar.
        -   As chaves de acesso não exclusivas não estão em conflito com as chaves de acesso dos controles comumente usados.
    -   Caso contrário, os controles restantes podem ser acessados usando a navegação de tecla tab e seta.

![captura de tela de grupos com chaves de acesso diferentes ](images/inter-keyboard-image13.png)

Neste exemplo, há controles repetitivos para que as chaves de acesso sejam atribuídas aos grupos de botões de rádio.

### <a name="preventing-accidental-commands"></a>Impedindo comandos acidentais

Se uma janela exibida fora do contexto (não iniciada pelo usuário) roubar o foco de entrada, há uma boa chance de que essa janela receba a entrada destinada a outra janela. Além disso, as chaves de acesso entrarão em vigor quando pressionadas sem pressionar a tecla Alt se a caixa de diálogo não tiver controles que levam entrada de texto (como caixas de texto e listas). Portanto, no exemplo a seguir, pressionar "r" ativa o botão Reiniciar agora.

Claramente, essa entrada pode ter consequências não intencionais significativas.

**Incorreto:**

![captura de tela do botão reiniciar agora, "r" sublinhado ](images/inter-keyboard-image14.png)

Neste exemplo, digitar texto com espaço, "r" ou Enter reinicia acidentalmente o Windows.

É claro que a melhor solução para esse problema é não roubar o foco de entrada. Em vez disso, ative o botão da barra de tarefas do [programa](winenv-taskbar.md) ou exibe uma notificação para chamar a atenção do usuário.

No entanto, se você precisa exibir essa janela, a melhor abordagem é não atribuir um botão padrão ou chaves de acesso e dar foco de entrada inicial a um controle diferente de um botão de confirmação.

**Correto:**

![captura de tela do botão reiniciar, 'r' não sublinhado ](images/inter-keyboard-image15.png)

Neste exemplo, reiniciar acidentalmente o Windows é muito mais difícil de fazer.

**Se você fizer apenas seis coisas...**

1.  Projete uma boa navegação por teclado, com uma ordem de tabulação adequada e grupos de controle apropriados, foco de entrada inicial e botões padrão.
2.  Atribua chaves de acesso a todos os menus e à maioria dos controles.
3.  Atribua as chaves de acesso a um caractere que aparece no início do rótulo para torná-las fáceis de encontrar.
4.  Atribua teclas de atalho aos comandos mais usados.
5.  Tente atribuir as teclas de atalho aos primeiros ou mais importantes caracteres dentro de palavras-chave.
6.  Dê às teclas de atalho conhecidas um significado consistente.

## <a name="guidelines"></a>Diretrizes

### <a name="interaction"></a>Interação

-   **Não use a tecla Shift para modificar comandos em menus ou caixas de diálogo.** Fazer isso é indiscoverable e inesperado.

    **Incorreto:**

    ![captura de tela da caixa de diálogo confirmar substituição de pasta ](images/inter-keyboard-image16.png)

    Neste exemplo do Windows XP, manter a tecla Shift substitui Sim para Todos por Não para Todos.

-   **Não desabilite um controle com foco de entrada. Isso pode impedir que a janela receba a entrada do teclado.** Em vez disso, antes de desabilitar um controle com foco de entrada, mova o foco de entrada para outro controle.
-   **Se uma janela for exibida fora do contexto, potencialmente surpreendente para os usuários, talvez seja necessário evitar consequências não intencionais significativas:**
    -   Não atribua um botão padrão.
    -   Não atribua chaves de acesso.
    -   Dê foco de entrada inicial a um controle diferente de um botão de commit.

### <a name="keyboard-navigation"></a>Navegação por teclado

-   **Sempre mostre o indicador de foco de entrada. Exceção:** você poderá suprimir temporariamente o indicador de foco de entrada se:
    -   O indicador de foco de entrada é visualmente distração (como com uma exibição de lista grande que não está na exibição Detalhes).
    -   O uso da tecla Enter provavelmente é precedido por outras entradas de teclado, como Alt ou teclas de seta.
    -   O indicador de foco de entrada é exibido em qualquer entrada de teclado.
-   **Atribua o foco de entrada inicial ao controle com o** qual os usuários têm maior probabilidade de interagir primeiro, que geralmente é o primeiro controle interativo. Se o primeiro controle interativo não for uma boa opção, considere alterar o layout da janela.
-   **Atribua paradas de guias a todos os controles interativos, incluindo caixas de edição somente leitura. Exceções:**
    -   Agrupa conjuntos de controles relacionados que se comportam como um único controle, como botões de rádio. Esses grupos têm uma única parada de tabulação.
    -   Contêm grupos corretamente para que as teclas de direção andem para frente e para trás dentro do grupo e permaneçam dentro do grupo.
-   **A ordem de tabulação deve seguir a ordem de leitura, que geralmente flui da esquerda para a direita, de cima para baixo.** Considere fazer exceções para controles comumente usados colocando-os anteriormente na ordem de tabulação. A guia deve passar por todas as paradas da guia em ambas as direções sem parar.
-   **Em uma parada de tabulação, a ordem** de tecla de direção deve fluir da esquerda para a direita, de cima para baixo, sem exceções. As teclas de direção devem passar por todos os itens em ambas as direções sem parar.
-   **Apresente os botões de confirmação na seguinte ordem:**
    -   OK/ \[ Faça isso \] /Sim
    -   \[Não faça isso \] /Não
    -   Cancelar
    -   Aplicar (se presente)

em \[ que Fazer isso e Não fazer isso são respostas \] \[ \] específicas para a instrução principal.

-   **Selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema) e o botão de comando ou o link de comando mais seguro para ser o padrão.** Se segurança e segurança não são fatores, selecione a resposta mais provável ou conveniente.
-   **A navegação por teclado não deve alterar os valores de controle nem resultar em uma mensagem de erro.** Nunca exigir que os usuários alterem o valor inicial de um controle durante a navegação. Em vez disso, inicialize os controles que validam na saída com valores válidos e validem o valor de um controle somente quando ele for alterado.

### <a name="access-keys"></a>Chaves de acesso

-   **Sempre que possível, atribua chaves de acesso para comandos comumente usados de acordo com a tabela a seguir.** Embora as atribuições de chave de acesso consistentes nem sempre sejam possíveis, elas certamente são preferenciais especialmente para comandos usados com frequência.

    |  Chave de acesso         | Comando                             |
    |---------------------------|-------------------------------------------|
    | Um<br/>              | Sobre<br/>                          |
    | Um<br/>              | Sempre na parte superior<br/>                  |
    | Um<br/>              | Aplicar<br/>                          |
    | B<br/>              | Voltar<br/>                           |
    | B<br/>              | Bold<br/>                           |
    | B ou r<br/>         | Procurar<br/>                         |
    | C<br/>              | Feche<br/>                          |
    | C<br/>              | Copiar<br/>                           |
    | C<br/>              | Copie aqui<br/>                      |
    | s<br/>              | Criar atalho<br/>                |
    | s<br/>              | Criar atalho aqui<br/>           |
    | t<br/>              | Recortar<br/>                            |
    | D<br/>              | Excluir<br/>                         |
    | D<br/>              | Não mostrar este \[ item \] novamente<br/> |
    | E<br/>              | Editar<br/>                           |
    | x<br/>              | Fechar<br/>                           |
    | E<br/>              | Explorar<br/>                        |
    | F<br/>              | Menos<br/>                          |
    | F<br/>              | Arquivo<br/>                           |
    | F<br/>              | Localizar<br/>                           |
    | n<br/>              | Localizar próximo<br/>                      |
    | F<br/>              | Fonte<br/>                           |
    | F<br/>              | Encaminhar<br/>                        |
    | H<br/>              | Ajuda<br/>                           |
    | t<br/>              | Tópicos da Ajuda<br/>                    |
    | H<br/>              | Ocultar<br/>                           |
    | I<br/>              | Inserir<br/>                         |
    | o<br/>              | Objeto Insert<br/>                  |
    | I<br/>              | Itálico<br/>                         |
    | L<br/>              | Link aqui<br/>                      |
    | x<br/>              | Maximizar<br/>                       |
    | n<br/>              | Minimizar<br/>                       |
    | M<br/>              | Mais<br/>                           |
    | M<br/>              | Mover<br/>                           |
    | M<br/>              | Mover aqui<br/>                      |
    | N<br/>              | Novo<br/>                            |
    | N<br/>              | Avançar<br/>                           |
    | N<br/>              | Não<br/>                             |
    | O<br/>              | Aberto<br/>                           |
    | w<br/>              | Abrir com<br/>                      |
    | O<br/>              | Opções<br/>                        |
    | u<br/>              | Configuração de página<br/>                     |
    | P<br/>              | Colar<br/>                          |
    | l<br/>              | Colar link<br/>                     |
    | s<br/>              | Colar atalho<br/>                 |
    | s<br/>              | Colar especial<br/>                  |
    | P<br/>              | Pausar<br/>                          |
    | P<br/>              | Reproduzir<br/>                           |
    | P<br/>              | Impressão<br/>                          |
    | P<br/>              | Imprimir aqui<br/>                     |
    | r<br/>              | Propriedades<br/>                     |
    | R<br/>              | Refazer<br/>                           |
    | R<br/>              | Repetir<br/>                         |
    | R<br/>              | Restaurar<br/>                        |
    | R<br/>              | Retomar<br/>                         |
    | R<br/>              | Tentar novamente<br/>                          |
    | R<br/>              | Executar<br/>                            |
    | S<br/>              | Salvar<br/>                           |
    | um<br/>              | Salvar como<br/>                        |
    | um<br/>              | Selecionar tudo<br/>                     |
    | n<br/>              | Enviar para<br/>                        |
    | S<br/>              | Mostrar<br/>                           |
    | S<br/>              | Tamanho<br/>                           |
    | p<br/>              | Divisão<br/>                          |
    | S<br/>              | Stop<br/>                           |
    | T<br/>              | Ferramentas<br/>                          |
    | U<br/>              | Underline<br/>                      |
    | U<br/>              | Desfazer<br/>                           |
    | V<br/>              | Visualizar<br/>                           |
    | W<br/>              | Janela<br/>                         |
    | Y<br/>              | Sim<br/>                            |

    

     

-   **Prefira caracteres com larguras largas,** como w, m e letras maiúsculas.
-   **Prefira uma consoante distinta ou uma vogal,** como "x" em "Exit".
-   **Evite usar caracteres que tornem o sublinhado difícil de ver,** como (do mais problemático ao menos problemático):
    -   Caracteres que são apenas um pixel de largura, como i e l.
    -   Caracteres com descendentes, como g, j, p, q e y.
    -   Caracteres ao lado de uma letra com um descendente.
-   Ao atribuir chaves de acesso nas páginas do assistente, lembre-se de reservar "B" para voltar e "N" para o próximo.
-   Ao atribuir chaves de acesso em páginas de propriedades, lembre-se de reservar "A" para aplicar, se usado.

### <a name="menu-access-keys"></a>Teclas de acesso do menu

-   **Atribuir chaves de acesso a todos os itens de menu.** Sem exceções.
-   **Para itens de menu dinâmico (como arquivos usados recentemente), atribua chaves de acesso numericamente.**

    ![captura de tela de itens de menu com chaves de acesso numéricos ](images/inter-keyboard-image17.png)

    Neste exemplo, o programa de pintura no Windows atribui chaves de acesso numérico a arquivos usados recentemente.

-   **Atribua chaves de acesso exclusivas dentro de um nível de menu.** Você pode reutilizar as chaves de acesso em diferentes níveis de menu.
-   **Torne as chaves de acesso fáceis de localizar:**
    -   Para os itens de menu usados com mais frequência, escolha caracteres no início da primeira ou segunda palavra do rótulo, preferivelmente o primeiro caractere.
    -   Para itens de menu usados com menos frequência, escolha letras que sejam uma consoante distinta ou uma vogal no rótulo.

### <a name="dialog-box-access-keys"></a>Chaves de acesso da caixa de diálogo

-   **Sempre que possível, atribua chaves de acesso exclusivas a todos os controles interativos ou seus rótulos.** [Caixas de texto somente leitura](ctrl-text-boxes.md) são controles interativos (porque os usuários podem rolar e copiar texto), para que se beneficiem das chaves de acesso. **Não atribua chaves de acesso para:**
    -   **Botões OK, cancelar e fechar.** Enter e ESC são usados para suas chaves de acesso. No entanto, sempre atribua uma chave de acesso a um controle que significa OK ou cancelar, mas tem um rótulo diferente.

        ![captura de tela da caixa de diálogo com botões Sim e não ](images/inter-keyboard-image18.png)

        Neste exemplo, o botão de confirmação positivo tem uma chave de acesso atribuída.

    -   **Rótulos de grupo.** Normalmente, os controles individuais dentro de um grupo recebem chaves de acesso e, portanto, o rótulo do grupo não precisa de um. No entanto, atribua uma chave de acesso ao rótulo do grupo e não aos controles individuais se houver uma falta de chaves de acesso.
    -   **Botões de ajuda genéricos,** que são acessados com F1.
    -   **Rótulos de link.** Geralmente, há muitos links para atribuir chaves de acesso exclusivas e os sublinhados de link ocultam os sublinhados da chave de acesso. Faça com que os usuários acessem links com a chave de guia em vez disso.
    -   **Nomes de guias.** As guias são alternadas usando Ctrl + Tab e Ctrl + Shift + Tab.
    -   **Procurar botões rotulados como "...".** Essas chaves de acesso não podem ser atribuídas exclusivamente.
    -   **Controles sem rótulo,** como controles de rotação, botões de comando gráficos e controles de divulgação progressivos sem rótulo.
    -   **Texto estático não rotulado ou rótulos para controles que não são interativos,** como barras de progresso.

-   **Atribua as chaves de acesso do botão confirmar primeiro para garantir que elas tenham as atribuições de chave padrão.** Se não houver uma atribuição de chave padrão, use a primeira letra da primeira palavra. Por exemplo, a tecla de acesso para botões Sim e não confirmar sempre deve ser "Y" e "N", independentemente dos outros controles na caixa de diálogo.
-   **Para botões de confirmação negativos (diferente de cancelar) com frase como "não", atribua a chave de acesso ao "n" em "não".** Se não for fraseada como "não", use a atribuição de chave de acesso padrão ou atribua a primeira letra da primeira palavra. Ao fazer isso, tudo não é e não tem uma chave de acesso consistente.
-   **Para facilitar a localização das chaves de acesso, atribua as chaves de acesso a um caractere que aparece no início do rótulo,** idealmente o primeiro caractere, mesmo se houver uma palavra-chave que aparece posteriormente no rótulo.
-   **Atribua no máximo 20 chaves de acesso,** para que você tenha alguns caracteres não atribuídos para facilitar a localização.
-   **Se houver muitos controles interativos para atribuir chaves de acesso exclusivas, você poderá atribuir chaves de acesso não exclusivas** se:
    -   De outra forma, os controles seriam muito difíceis de navegar.
    -   As chaves de acesso não exclusivas não entram em conflito com as chaves de acesso dos controles comumente usados.
-   **Não use barras de menu em caixas de diálogo.** É difícil atribuir chaves de acesso exclusivas nesse caso, pois os itens de menu e controles da caixa de diálogo compartilham os mesmos caracteres.

### <a name="shortcut-keys"></a>Teclas de atalho

-   **Atribua teclas de atalho para os comandos usados com mais frequência.** Os programas e recursos usados raramente não precisam de teclas de atalho porque os usuários podem usar chaves de acesso em vez disso.
-   **Não crie uma tecla de atalho a única maneira de executar uma tarefa.** Os usuários também devem ser capazes de usar o mouse ou o teclado com teclas de tabulação, seta e acesso.
-   **Não atribua diferentes significados a teclas de atalho bem conhecidas.** Como eles são memorizados, os significados inconsistentes para atalhos bem conhecidos são frustrantes e sujeitos a erros.
-   **Não tente atribuir teclas de atalho do programa em todo o sistema.** As teclas de atalho do programa terão efeito somente quando o seu programa tiver o foco de entrada.
-   **Documente todas as teclas de atalho.** Documentar atalhos em itens da barra de menus, dicas de ferramenta da barra de ferramentas e um único artigo de ajuda que documenta todas as teclas de atalho usadas. Isso ajuda os usuários a aprender as atribuições de teclas de atalho que não devem ser um segredo.

    -   **Exceção:** Não exibir as atribuições de teclas de atalho nos menus de contexto. Os menus de contexto não exibem as atribuições de teclas de atalho porque esses menus são otimizados quanto à eficiência.

    ![captura de tela de dica de ferramenta para tecla de atalho em negrito ](images/inter-keyboard-image19.png)

    A tecla de atalho está documentada na dica de ferramenta.

-   **Se o programa atribuir muitas teclas de atalho, forneça a capacidade de personalizar as atribuições.** Isso permite que os usuários reatribuam teclas de atalho conflitantes e migrem de outros produtos. A maioria dos programas não atribui teclas de atalho suficientes para que você precise desse recurso.

### <a name="choosing-shortcut-keys"></a>Escolhendo teclas de atalho

-   **Para as teclas de atalho conhecidas, use as atribuições padrão.**
-   **Para atribuições de chave não padrão, use as seguintes teclas de atalho recomendadas para comandos usados com mais frequência.** Essas teclas de atalho são recomendadas porque não entram em conflito com os atalhos bem conhecidos e são fáceis de pressionar.
    -   CTRL + G, J, K, L M, Q, R ou T
    -   CTRL + qualquer número
    -   F7, F8, F9 ou F12
    -   Shift + F2, F3, F4, F5, F7, F8, F9, F11 ou F12
    -   Alt + qualquer tecla de função, exceto F4
-   **Use as seguintes teclas de atalho recomendadas para comandos usados com menos frequência.** Essas teclas de atalho não têm conflitos, mas são mais difíceis de pressionar muitas vezes exigindo duas mãos.
    -   CTRL + qualquer tecla de função, exceto F4 e F6
    -   Ctrl + Shift + qualquer letra ou número
-   **Facilitar a memorização das teclas de atalho usadas com frequência:**
    -   Use letras em vez de números ou teclas de função.
    -   Tente usar uma letra que esteja na primeira palavra ou na maioria dos caracteres de memorização dentro das palavras-chave do comando.
-   **Use as teclas de função para comandos que têm um efeito de pequena escala,** como comandos que se aplicam ao objeto selecionado. Por exemplo, F2 renomeia o item selecionado.
-   **Use combinações de teclas CTRL para comandos que têm um efeito de grande escala,** como comandos que se aplicam a um documento inteiro. Por exemplo, CTRL + S salva o documento atual.
-   **Use combinações de teclas Shift para comandos que estendem ou complementem as ações da tecla de atalho padrão.** Por exemplo, a tecla de atalho Alt + Tab percorre as janelas primárias abertas, enquanto os ciclos Alt + Shift + Tab na ordem inversa. Da mesma forma, F1 exibe a ajuda, enquanto Shift + F1 exibe a ajuda contextual.
-   **Ao usar as teclas de seta para mover ou redimensionar um item, use Ctrl + Seta teclas para um controle mais granular.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Escolhendo teclas de atalho (o que não fazer)

-   **Não faça distinção entre locais de chave.** Por exemplo, o Windows pode distinguir entre SHIFT esquerda e direita, ALT, CTRL, [logotipo do Windows](glossary.md)e chaves de [aplicativo](glossary.md), bem como chaves no teclado numérico. A atribuição de comportamento a apenas um local de chave é confusa e inesperada.
-   **Não use a tecla modificador do logotipo do Windows para as teclas de atalho do programa.** A chave do logotipo do Windows é reservada para uso do Windows. Mesmo que uma combinação de teclas de logotipo do Windows não esteja sendo usada pelo Windows agora, ela pode estar no futuro.
-   **Não use a chave do aplicativo como um modificador de tecla de atalho.** Em vez disso, use Ctrl, ALT e Shift.
-   **Não use as teclas de atalho usadas pelo Windows para as teclas de atalho do programa.** Isso entrará em conflito com as teclas de atalho do sistema Windows quando o seu programa tiver o foco de entrada.
-   **Não use combinações de teclas Alt + alfanuméricas para teclas de atalho.** Essas teclas de atalho podem entrar em conflito com as chaves de acesso.
-   **Não use os seguintes caracteres para as teclas de atalho:** @ $ {} \[ \] \\  ~  \| ^ '  < >. Esses caracteres exigem diferentes combinações de teclas em idiomas ou são específicos da localidade.
-   **Evite combinações de chaves complexas,** como três ou mais chaves juntas (exemplo: CTRL + ALT + barra de espaços) ou chaves que estão muito separadas no teclado (exemplo: CTRL + F5). Use teclas de atalho simples para comandos usados com frequência.
-   **Não use combinações CTRL + ALT,** porque o Windows interpreta essa combinação em algumas versões de idioma como uma chave AltGr, que gera caracteres alfanuméricos.

### <a name="keyboard-and-mouse-combinations"></a>Combinações de teclado e mouse

-   Para links, use Shift + clique para navegar usando uma nova janela e Ctrl + clique para navegar usando uma nova guia. Essa abordagem é consistente com o Windows Internet Explorer.

## <a name="documentation"></a>Documentação

Ao fazer referência ao teclado:

-   Use o teclado na tela para se referir a uma representação de teclado na tela que o usuário toca em caracteres de entrada.
-   Forneça combinações de teclado começando com a tecla modificadora. Apresente as chaves modificadoras na seguinte ordem: logotipo do Windows, aplicativo, CTRL, ALT, Shift. Se o modificador do teclado numérico for usado, coloque-o pouco antes da chave que ele modifica.
-   Não use todas as letras maiúsculas para as teclas do teclado. Em vez disso, siga as letras maiúsculas usadas por teclados padrão ou em minúsculas se a chave não estiver rotulada como um painel.
    -   Para combinações de chave alfabética, use uma letra maiúscula.
    -   Soletrar página para cima, página abaixo, tela de impressão e bloqueio de rolagem.
    -   Soletrar sinal de adição, sinal de subtração, hífen, ponto e vírgula.
    -   Para teclas de direção, use seta para a esquerda, seta para a direita, seta para cima e seta para baixo. Não use rótulos gráficos para as teclas de direção.
    -   Use a chave de logotipo do Windows e a Chave do aplicativo para se referir às chaves rotuladas com ícones. Não use rótulos gráficos para essas chaves.

**Correto:**

barra de espaços, Guia, Inserir, Página Para Cima, Ctrl+Alt+Del, Alt+W, Ctrl+sinal de adição

**Incorreto:**

SPACEBAR, TAB, ENTER, PG UP, Ctrl+Alt+DEL, Alt+w, Ctrl++

-   Indique combinações de teclas com um sinal de a mais, sem espaços.

**Correto:**

Ctrl+A, Shift+F5

**Incorreto:**

Ctrl-A, Shift + F5

-   Para mostrar uma combinação de chaves que inclui pontuação que requer o uso da tecla Shift, como o ponto de interrogação, adicione Shift à combinação e dê o nome ou símbolo da chave deslocada. O uso do nome da chave não trocada, como 4 em vez de $, pode ser confuso para os usuários ou até mesmo errado; por exemplo, o ? e/caracteres nem sempre são teclas deslocadas em cada teclado.

**Correto:**

Ctrl+Shift+?, Ctrl+Shift+, \* Ctrl+Shift+vírgula

**Incorreto:**

Ctrl+Shift+/, Ctrl+?, Ctrl+Shift+8, Ctrl+\*

-   Na primeira menção, use a chave e com o nome da chave, se necessário, para maior clareza, por exemplo, a tecla F1. Em todas as referências subsequentes, consulte a chave apenas pelo nome, por exemplo, pressione F1.
-   Consulte especificamente as teclas de acesso e as teclas de atalho na programação e em outras documentações técnicas. Não use acelerador, mnemônico ou teclas de acesso. Em qualquer outro lugar, use o atalho de teclado, especialmente na documentação do usuário.

Ao se referir à interação:

-   Use pressione, não pressione, pressione, pressione ou digite ao pressionar e liberar imediatamente uma chave inicia uma ação dentro do programa ou navega dentro de um documento ou interface do usuário.
-   Use o tipo, não enter, para direcionar os usuários para o tipo de texto.
-   Use o uso em situações em que pressionar pode ser confuso, como ao fazer referência a um tipo de chave, como teclas de direção ou teclas de função. Nesses casos, pressionar pode fazer os usuários pensarem que precisam pressionar todas as chaves simultaneamente.
-   Use hold ao pressionar e manter uma tecla pressionada, como uma tecla modificadora.
-   Não use pressionar como sinônimo para clicar.

Exemplos:

-   Digite seu nome e pressione Enter.
-   Pressione Ctrl+F e digite o texto que você deseja pesquisar.
-   Para salvar o arquivo, pressione Y.
-   Para mover o ponto de inserção, use as teclas de direção.

 

