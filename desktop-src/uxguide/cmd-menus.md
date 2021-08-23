---
title: Menus (noções básicas de Design)
description: Os menus são listas hierárquicas de comandos ou opções disponíveis para os usuários no contexto atual.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9b2c3559163ff77e8e3f08354b017c1b7cb53c95fd51802ae2565efdf71abcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350084"
---
# <a name="menus-design-basics"></a>Menus (noções básicas de Design)

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Os menus são listas hierárquicas de comandos ou opções disponíveis para os usuários no contexto atual.

Menus suspensos são menus exibidos sob demanda no clique do mouse ou em foco. Eles normalmente são ocultados da exibição e, portanto, são um meio eficiente de economizar espaço na tela. Um submenu ou menu em cascata é um menu secundário exibido sob demanda de dentro de um menu. Elas são indicadas por uma seta no final do rótulo do submenu. Um item de menu é um comando individual ou uma opção dentro de um menu.

Os menus são geralmente exibidos de uma barra de menus, que é uma lista de categorias de menu rotuladas normalmente localizadas próximo à parte superior de uma janela. Por outro lado, um menu de contexto cai quando os usuários clicam com o botão direito do mouse em uma região de objeto ou janela que dá suporte a um menu de contexto.

![captura de tela da barra de menus com menu e submenu ](images/cmd-menus-image1.png)

Uma barra de menus típica que exibe um menu suspenso e um submenu.

> [!Note]  
> As diretrizes relacionadas a [botões de comando](ctrl-command-buttons.md), barras de [ferramentas](cmd-toolbars.md)e [teclado](inter-keyboard.md) são apresentadas em artigos separados.

 

## <a name="usage-patterns"></a>Padrões de uso

Os menus têm vários padrões de uso:



| Uso                                                                                                                                                |    Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de menu**<br/> uma barra de menus exibe comandos e opções nos menus suspensos. <br/>                                               | as barras de menu são muito comuns e fáceis de encontrar, bem como um uso eficiente de espaço. <br/> ![captura de tela da barra de menus com o menu suspenso ](images/cmd-menus-image2.png)<br/> uma barra de menus do Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Menus da barra de ferramentas**<br/> uma barra de menus implementada como uma barra de ferramentas. <br/>                                                                   | os menus da barra de ferramentas são barras de ferramentas que consistem principalmente em comandos em [botões de menu](ctrl-command-buttons.md) e botões de divisão, com apenas alguns comandos diretos, se houver. <br/> ![captura de tela do menu da barra de ferramentas com o menu suspenso ](images/cmd-menus-image3.png)<br/> um menu de barra de ferramentas na galeria de fotos Windows.<br/> Para obter diretrizes sobre esse padrão, consulte [barras de ferramentas](cmd-toolbars.md).<br/>                                                                                                                                                                                                             |
| **Menus de guia**<br/> botões dentro de guias que exibem um pequeno conjunto de comandos e opções relacionadas a uma guia em um menu suspenso. <br/> | guias com menus são semelhantes a guias comuns, exceto que sua parte inferior tem um botão com a seta suspensa. clicar no botão exibe um menu suspenso em vez de selecionar a guia. <br/> ![captura de tela do menu guia com o menu suspenso ](images/cmd-menus-image4.png)<br/> Os menus de guia são usados no Windows Media Player.<br/>                                                                                                                                                                                                                                                                                           |
| **Botões de menu**<br/> botões de comando que exibem um pequeno conjunto de comandos relacionados em um menu suspenso. <br/>                       | os [botões de menu](ctrl-command-buttons.md) parecem botões de comando comuns, exceto por terem uma seta suspensa dentro deles. clicar no botão exibe um menu suspenso em vez de executar um comando.<br/> os [botões de divisão](ctrl-command-buttons.md) são semelhantes aos botões de menu, exceto que eles são variações de um comando, e clicar na parte esquerda do botão executa a ação diretamente no rótulo.<br/> ![captura de tela do botão de menu com comandos suspensos ](images/cmd-menus-image5.png)<br/> Um botão de menu com um pequeno conjunto de comandos relacionados.<br/> |
| **Menus de contexto**<br/> menus suspensos que exibem um pequeno conjunto de comandos e opções relacionadas ao contexto atual. <br/>       | menu suspenso de menus de contexto quando os usuários clicam com o botão direito do mouse em uma região de objeto ou de janela que oferece suporte a menus de contexto. <br/> ![captura de tela do menu de contexto exibindo comandos ](images/cmd-menus-image6.png)<br/> um menu de contexto do Windows Explorer.<br/> Se os menus de contexto forem a melhor opção de menu, mas você precisar de uma solução adequada para todos os usuários, você poderá usar um botão de seta suspensa menu. <br/> ![captura de tela de foto com o botão de menu suspenso ](images/cmd-menus-image7.png)<br/> Um menu de contexto ficou visível com um botão suspenso de menu.<br/>                                                   |
| **Menus do painel de tarefas**<br/> um pequeno conjunto de comandos relacionados ao modo de programa ou objeto selecionado. <br/>                              | ao contrário dos menus de contexto, eles são exibidos automaticamente dentro de um painel de janela, em vez de sob demanda. <br/> ![captura de tela de foto com o menu do painel de tarefas à direita ](images/cmd-menus-image8.png)<br/> um menu do painel de tarefas no visualizador da galeria de fotos Windows.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

### <a name="menu-bars"></a>Barras de menu

As seguintes condições se aplicam:

-   A janela é uma janela principal?
-   Há muitos itens de menu?
-   Há muitas categorias de menu?
-   A maioria dos itens de menu se aplica a todo o programa e à janela principal?
-   O menu precisa funcionar para todos os usuários?

Nesse caso, considere usar uma barra de menus.

### <a name="toolbar-menus"></a>Menus da barra de ferramentas

As seguintes condições se aplicam:

-   A janela é uma janela principal?
-   A janela tem uma barra de ferramentas?
-   Há apenas algumas categorias de menu?
-   O menu precisa funcionar para todos os usuários?

Nesse caso, considere usar um menu da barra de ferramentas em vez de ou além de uma barra de menus.

### <a name="tab-menus"></a>Menus de guia

As seguintes condições se aplicam:

-   A janela é uma janela principal?
-   A janela tem guias, onde cada guia é usada para um conjunto dedicado de tarefas (em oposição ao uso de guias para mostrar diferentes modos de exibição)?
-   Há uma categoria de menu que se aplica a cada guia?
-   Há muitos comandos e opções, mas apenas um pequeno conjunto para cada guia?

Nesse caso, considere usar um menu de guia em vez de uma barra de menus.

### <a name="context-menu"></a>Menu de contexto

As seguintes condições se aplicam:

-   Há um pequeno conjunto de comandos e opções contextuais que se aplicam ao objeto ou à região da janela selecionada?
-   Esses itens de menu são redundantes?
-   Os usuários de destino estão familiarizados com os menus de contexto?

Nesse caso, considere fornecer menus de contexto para os objetos e regiões de janela que precisam deles.

Para programas baseados em navegador, os menus do painel de tarefas são uma solução mais comum para comandos contextuais. Atualmente, os usuários esperam que os menus de contexto em programas baseados em navegador sejam genéricos e não tenham ajuda.

### <a name="task-pane-menu"></a>Menu do painel de tarefas

As seguintes condições se aplicam:

-   A janela é uma janela principal?
-   Há um pequeno conjunto de comandos contextuais e opções que se aplicam ao modo de programa ou objeto selecionado?
-   Há algumas categorias de menu?
-   O menu precisa funcionar para todos os usuários?

Nesse caso, considere usar um menu de painel de tarefas em vez de um menu de contexto.

## <a name="design-concepts"></a>Conceitos de design

Menus eficientes que promovem uma boa experiência do usuário:

-   Use uma apresentação de comando que corresponda ao tipo de programa, tipos de janela, uso de comando e usuários de destino.
-   São bem organizados, usando a organização de menu padrão quando apropriado.
-   Use barras de menu, barras de ferramentas e menus de contexto com eficiência.
-   Use ícones com eficiência.
-   Use chaves de acesso e teclas de atalho com eficiência.

**Se você fizer apenas uma coisa...**

Escolha uma apresentação de comando que corresponde ao tipo de programa, tipos de janela, uso de comando e usuários de destino.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Todos os padrões de menu, exceto barras de menu, precisam de uma seta para baixo para indicar a presença de um menu suspenso.** A presença de menus fica sem dizer em uma barra de menus, mas não nos outros padrões.
-   **Não altere nomes de item de menu dinamicamente.** Fazer isso é confuso e inesperado. Por exemplo, não altere uma opção de modo Retrato para Modo paisagem após a seleção. Para modos, use [marcadores e marcas de seleção.](#bullets-and-checkmarks)
    -   **Exceção:** Você pode alterar nomes de item de menu baseados em nomes de objeto dinamicamente. Por exemplo, listas de arquivos usados recentemente ou nomes de janela podem ser dinâmicas.

### <a name="menu-bars"></a>Barras de menu

-   **Considere eliminar barras de menu com três ou menos categorias de menu.** Se houver apenas alguns comandos, prefira alternativas mais leves, como menus da barra de ferramentas ou alternativas mais diretas, como botões de comando e links.
-   **Não tem mais de 10 categorias de menu.** Muitas categorias de menu são difíceis de usar e dificultam o uso da barra de menus.
-   **Considere ocultar a barra de menus** se a barra de ferramentas ou comandos diretos fornecerem quase todos os comandos necessários para a maioria dos usuários. Permitir que os usuários mostrem ou o hide com uma opção de marca de seleção da barra de menus em um menu da barra de ferramentas.

![captura de tela da lista de opções com a barra de menus selecionada ](images/cmd-menus-image9.png)

Neste exemplo, o Windows Internet Explorer fornece uma opção de barra de menus.

Para obter mais informações, consulte [ocultando barras de menu](#hiding-menu-bars).

### <a name="hiding-menu-bars"></a>Ocultando barras de menu

Em geral, as barras de ferramentas funcionam muito bem junto com barras de menu, pois ter ambos permite que cada um se concentre em seus pontos fortes sem comprometimento.

-   Ocultar a barra de menus por padrão se o design da barra de ferramentas torna a redundância de uma barra de menus.
-   Ocultar a barra de menus em vez de removê-la completamente, pois as barras de menu são mais acessíveis para usuários de teclado.
-   Para restaurar a barra de menus, forneça uma opção de marca de seleção barra de menus na categoria de menu Exibir (para barras de ferramentas primárias) ou Ferramentas (para barras de ferramentas secundárias). Para obter mais informações, consulte [Menu padrão e botões de divisão](cmd-toolbars.md).

### <a name="menu-categories"></a>Categorias de menu

-   **Escolha nomes de palavra única para categorias de menu.** Usar várias palavras torna a separação entre categorias confusa.
-   **Para programas que criam ou visualizam documentos, use** as categorias de menu padrão, como Arquivo, Editar, Exibir, Ferramentas e Ajuda. Isso torna os itens de menu comuns previsíveis e mais fáceis de encontrar.
-   **Para outros tipos de programas,** considere organizar seus comandos e opções em categorias naturais mais úteis com base na finalidade do programa e na maneira como os usuários pensam sobre suas tarefas e metas. Não se sinta obrigado a usar a organização do menu padrão se ela não for adequada para seu programa.
-   **Se você optar por usar categorias de menu não padrão, deverá escolher bons nomes de categoria.** Para obter mais informações, consulte a [seção Rótulos.](#labels)
-   **Prefira categorias de menu orientadas a tarefas em vez de categorias genéricas.** As categorias orientadas a tarefas facilitam a encontrar itens de menu.

![captura de tela da barra de menus com ondulação, gravar e sincronizar ](images/cmd-menus-image10.png)

Neste exemplo, o Windows Media Player usa categorias de menu orientadas a tarefas.

-   **Evite categorias de menu com apenas um ou dois itens de menu.** Se for razoável, consolide com outras categorias de menu, talvez usando um submenu.
-   **Considere colocar o mesmo item de menu em várias categorias somente se:**
    -   O item de menu pertence logicamente a várias categorias de menu.
    -   Você tem dados mostrando que os usuários têm problemas para localizar o item em uma única categoria de menu.
    -   Você tem apenas um ou dois itens de menu difíceis de encontrar em várias categorias.
-   **Não coloque itens de menu diferentes que usam o mesmo nome em várias categorias.** Por exemplo, não há itens de menu Opções diferentes em várias categorias.
    -   **Exceção:** O padrão de menu guia pode ter diferentes itens de menu Opções e Ajuda em cada menu de guia.

![captura de tela de menus de tabulação com itens de menu repetidos ](images/cmd-menus-image11.png)

Neste exemplo, o Windows Media Player tem itens de menu Opções e Ajuda em cada menu de guia.

### <a name="menu-item-organization-and-order"></a>Organização e ordem do item de menu

-   **Organize os itens de menu em grupos de sete ou menos itens fortemente relacionados.** Para isso, os submenus contam como um único item de menu no menu pai.
-   **Não coloque mais de 25 itens** em um único nível de um menu (sem contar submenus).
-   **Coloque separadores entre os grupos dentro de um menu.** Um separador é uma única linha que abrange a largura do menu.
-   **Em um menu, coloque os grupos em sua ordem lógica.** Se não houver nenhuma ordem lógica, coloque os grupos mais usados primeiro.
-   **Em um grupo, coloque os itens em sua ordem lógica.** Se não houver nenhuma ordem lógica, coloque os itens mais usados primeiro. Coloque itens numéricos (como percentuais de zoom) em ordem numérica.

### <a name="submenus"></a>Submenus

-   **Evite usar submenus desnecessariamente.** Os submenus exigem mais esforço físico para usar e geralmente dificultam a localização dos itens de menu.
-   **Não coloque itens de menu usados com frequência em um submenu.** Isso faria com que o uso desses comandos fosse ineficiente. No entanto, você pode colocar comandos usados com frequência em um submenu se eles normalmente são acessados mais diretamente, como com uma barra de ferramentas.
-   **Considere usar um submenu se:**
    -   Isso simplifica o menu pai porque ele tem muitos itens (20 ou mais) ou o submenu faz parte de um grupo de mais de sete itens.
    -   Os itens no submenu são usados com menos frequência do que aqueles no menu pai.
    -   O submenu teria três ou mais itens.
    -   Há três ou mais comandos que começam com a mesma palavra. Nesse caso, use essa palavra como o rótulo de submenu.

![captura de tela do menu "novo" com quatro itens de submenu ](images/cmd-menus-image12.png)

Neste exemplo, o submenu Novo substitui comandos separados para Nova mensagem de email, Nova mensagem de notícias, Nova pasta e Novo contato.

-   **Use no máximo três níveis de menus.** Ou seja, você pode ter um menu primário e, no máximo, dois níveis de submenus. Dois níveis de submenus devem ser raros.

### <a name="presentation"></a>Apresentação

-   **Desabilite itens de menu que não se aplicam ao contexto atual, em** vez de removê-los. Isso torna o conteúdo da barra de menus estável e mais fácil de encontrar. **Exceções:**
    -   Para categorias de menu contextual, remova em vez de desabilitar itens de menu de contexto **que não se aplicam ao contexto atual.** Uma categoria de menu é contextual quando é exibida somente para modos específicos, como quando um determinado tipo de objeto é selecionado. Para obter detalhes, consulte [remover versus desabilitar diretrizes](#context-menus) para menus de contexto.
    -   Se determinar quando um item de menu deve ser desabilitado causar problemas de desempenho perceptíveis, deixe o item de menu ativo e, se necessário, sua seleção resultará em uma mensagem de erro.

### <a name="tab-menus"></a>Menus de tabulação

-   **Cada menu de guia pode ter itens de menu Opções e Ajuda específicos do contexto.** Isso é diferente de todos os outros padrões de menu. Cada guia é usada para um conjunto dedicado de tarefas, portanto, qualquer redundância entre menus de tabulação não é confusa.

### <a name="context-menus"></a>Menus de contexto

-   **Use menus de contexto somente para comandos contextuais e opções.** Os itens de menu devem ser aplicados somente ao objeto selecionado (ou clicado) ou à região da janela, não ao programa inteiro.
-   **Não disponibiliza comandos somente por meio de menus de contexto.** Assim como as teclas de atalho, os menus de contexto são meios alternativos de executar comandos e escolher opções. Por exemplo, um comando de propriedades também está disponível por meio da barra de menus ou da tecla de acesso Alt + Enter.
-   **Forneça menus de contexto para todos os objetos e regiões de janela** que se beneficiam de um pequeno conjunto de comandos e opções contextuais. Muitos usuários clicam com o botão direito do mouse regularmente e esperam encontrar menus de contexto em qualquer lugar.
-   **Considere usar um botão de seta suspensa menu para menus de contexto direcionados a todos os usuários.** Normalmente, os menus de contexto são adequados para comandos e opções direcionadas a usuários avançados. No entanto, você pode usar um botão suspenso de menu nos casos em que os menus de contexto são a melhor opção de menu e você precisa direcionar todos os usuários.

![captura de tela de foto com o botão de menu suspenso ](images/cmd-menus-image7.png)

Neste exemplo, um botão suspenso de menu é usado para tornar visível um menu de contexto.

**Ordem e organização do item de menu**

-   **Organize os itens de menu em grupos de sete ou menos itens fortemente relacionados.**
-   **Evite usar submenus** para manter os menus de contexto simples, diretos e eficientes.
-   **Não coloque mais de 15 itens em um menu de contexto.**
-   **Coloque separadores entre os grupos dentro de um menu.** Um separador é uma única linha que abrange a largura do menu.
-   **Apresente os itens de menu usando a seguinte ordem:**

<dl> Comandos primários (usados com mais frequência)<dl> Aberto  
Executar  
Reproduzir  
Imprimir <separator>  
</dl> </dd> <dd>Comandos secundários com suporte no objeto<dl> <separator>  
</dl> </dd> Comandos de transferência<dl> Recortar  
Copiar  
Olar <separator>  
</dl> </dd> <dd>Configurações de objeto<dl> <separator>  
</dl> </dd> Comandos de objeto<dl> Excluir  
Nome <separator>  
Propriedades
</dl> </dd> </dl>

**Apresentação**

-   **Exiba o comando padrão usando negrito.** Quando for prático, também o tornará o primeiro item de menu. O comando padrão é invocado quando os usuários clicam duas vezes ou selecionam um objeto e pressionam Enter.
-   **Remova em vez de Desabilitar itens de menu de contexto que não se aplicam ao contexto atual.** Isso torna os menus de contexto contextuais e eficientes.
    -   **Exceção:** Desabilite os itens de menu que não se aplicam se houver uma expectativa razoável para que eles estejam disponíveis:
        -   Sempre tenha os comandos de menu de contexto padrão relevantes, como recortar, copiar, colar, excluir e renomear.
        -   Sempre tenha os comandos que concluem os conjuntos relacionados. Por exemplo, se houver um back, também deverá haver um encaminhamento. Se houver um recorte, sempre terá uma copiar e colar.

### <a name="bullets-and-checkmarks"></a>Marcadores e marcas de seleção

-   **Itens de menu que são opções podem usar marcadores e marcas de seleção.** Os comandos podem não.
-   **Use um marcador para escolher uma opção de um pequeno conjunto de opções mutuamente exclusivas.** Sempre deve haver pelo menos dois marcadores em um grupo. Para obter mais informações, consulte [botões de opção](ctrl-radio-buttons.md).
-   **Use uma marca de seleção para ativar ou desativar uma configuração independente.** Se os Estados selecionado e limpo não forem opostos claros e não ambíguos, use um conjunto de marcadores. Para obter mais informações, consulte [caixas de seleção](ctrl-check-boxes.md).
-   **Para um estado de marca de seleção mista, exiba um item de menu sem uma marca de seleção.** O estado misto é usado para seleção múltipla para indicar que a opção está definida para alguns objetos, mas não todos, para que cada objeto individual tenha o estado selecionado ou limpo. O estado misto não é usado como um terceiro estado para um item individual.
-   **Coloque separadores entre os conjuntos relacionados de marcas de seleção ou marcadores.** Um separador é uma única linha que abrange a largura do menu.

### <a name="icons"></a>Ícones

-   **Considere fornecer ícones de item de menu para:**
    -   Os itens de menu usados com mais frequência.
    -   Itens de menu cujo ícone é Standard e bem conhecido.
    -   Os itens de menu cujo ícone ilustra bem o que faz o comando.
-   **Se você usar ícones, não se sinta obrigado a fornecê-los para todos os itens de menu.** Os ícones criptografados não são úteis, criam poluição visual e impedem que os usuários se concentrem nos itens de menu importantes.

![captura de tela de itens de menu com e sem ícones ](images/cmd-menus-image13.png)

Neste exemplo, o menu organizar tem ícones apenas para os itens de menu mais usados.

-   **Certifique-se de que os ícones de menu estão de acordo com as diretrizes de ícone do estilo Aero.**

Para obter mais informações e exemplos, consulte [ícones](vis-icons.md).

### <a name="access-keys"></a>Chaves de acesso

-   **Atribuir chaves de acesso a todos os itens de menu.** Sem exceções.
-   **Sempre que possível, atribua chaves de acesso para comandos comumente usados de acordo com as atribuições de chave de acesso padrão.** Embora as atribuições de chave de acesso consistente nem sempre sejam possíveis, elas são certamente preferenciais – especialmente para comandos usados com frequência.
-   **Para itens de menu dinâmico (como arquivos usados recentemente), atribua chaves de acesso numericamente.**

![captura de tela de itens de menu com chaves de acesso numéricos ](images/cmd-menus-image14.png)

neste exemplo, o programa Paint no Windows atribui chaves de acesso numérico a arquivos usados recentemente.

-   **Atribua chaves de acesso exclusivas dentro de um nível de menu.** Você pode reutilizar as chaves de acesso em diferentes níveis de menu.
-   **Torne as chaves de acesso fáceis de localizar:**
    -   Para os itens de menu usados com mais frequência, escolha caracteres no início da primeira ou segunda palavra do rótulo, preferivelmente o primeiro caractere.
    -   Para itens de menu usados com menos frequência, escolha letras que sejam uma consoante distinta ou uma vogal no rótulo.
-   **Prefira caracteres com larguras largas,** como w, m e letras maiúsculas.
-   **Prefira uma consoante distinta ou uma vogal,** como "x" em "Exit".
-   **Evite usar caracteres que tornem o sublinhado difícil de ver,** como (do mais problemático ao menos problemático):
    -   Letras que têm apenas um pixel de largura, como i e l.
    -   Letras com descendentes, como g, j, p, q e y.
    -   As letras ao lado de uma letra com um descendente.

Para obter mais diretrizes e exemplos, consulte [teclado](inter-keyboard.md).

### <a name="shortcut-keys"></a>Teclas de atalho

-   **Atribua teclas de atalho para os itens de menu usados com mais frequência.** Itens de menu usados raramente não precisam de teclas de atalho porque os usuários podem usar chaves de acesso em vez disso.
-   **Não crie uma tecla de atalho a única maneira de executar uma tarefa.** Os usuários também devem ser capazes de usar o mouse ou o teclado com teclas de tabulação, seta e acesso.
-   **Para as teclas de atalho conhecidas, use as atribuições padrão.**
-   **Não atribua diferentes significados a teclas de atalho bem conhecidas.** Como eles são memorizados, os significados inconsistentes para atalhos bem conhecidos são frustrantes e sujeitos a erros. consulte Windows teclas de atalho de teclado para as teclas de atalho conhecidas usadas por Windows programas.
-   **Não tente atribuir teclas de atalho do programa em todo o sistema.** As teclas de atalho do programa terão efeito somente quando o seu programa tiver o foco de entrada.
-   **Documente todas as teclas de atalho.** Isso ajuda os usuários a aprender as atribuições de teclas de atalho.
    -   **Exceção:** Não exibir as atribuições de teclas de atalho nos menus de contexto. Os menus de contexto não exibem as atribuições de tecla de atalho porque são otimizadas para eficiência.
-   **Para atribuições de chave não padrão:**
    -   **Escolha teclas de atalho que não têm atribuições padrão.** Nunca reatribuir teclas de atalho padrão.
    -   **Use atribuições de chave não padrão consistentemente em todo o programa.** Não atribua significados diferentes em janelas diferentes.
    -   **Se possível, escolha atribuições de chave mnemônica,** especialmente para comandos usados com frequência.
    -   **Use chaves de função para comandos que têm um efeito** de pequena escala, como comandos que se aplicam ao objeto selecionado. Por exemplo, F2 renomeia o item selecionado.
    -   **Use combinações de teclas Ctrl para comandos** que têm um efeito em grande escala, como comandos que se aplicam a um documento inteiro. Por exemplo, Ctrl+S salva o documento atual.
    -   **Use combinações de teclas Shift para comandos que estendem ou complementam as ações da tecla de atalho padrão.** Por exemplo, a tecla de atalho Alt+Tab passa pelas janelas primárias abertas, enquanto Alt+Shift+Tab é um ciclo na ordem inversa. Da mesma forma, F1 exibe a Ajuda, enquanto Shift+F1 exibe a Ajuda contextitivo.
    -   **Não use os seguintes caracteres para teclas de atalho:** @ $ {} \[ \] \\  ~  \| ^ ' < >. Esses caracteres exigem combinações de teclas diferentes entre idiomas ou são específicos da localidade.
    -   Não use combinações **Ctrl+Alt,** pois Windows essa combinação em algumas versões de linguagem como uma chave AltGR, que gera caracteres alfanuméricos.
-   **Se o programa atribuir muitas teclas de atalho, forneça a capacidade de personalizar as atribuições.** Isso permite que os usuários reatribuam chaves de atalho conflitantes e migre de outros produtos. A maioria dos programas não atribui teclas de atalho suficientes para precisar desse recurso.

Para obter mais diretrizes e atribuições de teclas de atalho padrão, consulte [Teclado](inter-keyboard.md).

### <a name="standard-menus"></a>Menus padrão

-   **Use a organização de menu padrão para programas que criam ou visualizam documentos.** A organização do menu padrão torna os itens de menu comuns previsíveis e fáceis de encontrar.
-   **Para outros tipos de programas, use a organização de menu padrão somente quando fizer sentido.** Considere organizar seus comandos e opções em categorias mais úteis e naturais com base na finalidade do programa e na maneira como os usuários pensam sobre suas tarefas e metas.

**Barras de menu padrão**

A estrutura da barra de menus padrão é a seguinte. Esta lista mostra a categoria de menu e rótulos de item, sua ordem com separadores, suas teclas de acesso e atalho e suas reellipses.

<dl> Arquivo<dl> Novo Ctrl+N  
Aberto... Ctrl+O  
Feche o <separator>  
Salvar Ctrl+S  
Salvar como... <separator>  
Enviar para <separator>  
Imprimir... Ctrl+P  
Visualização de impressão  
Configuração de página <separator>  
1 <filename> 2 <filename> 3 <filename> ... <separator>  
Sair de Alt+F4 (o atalho geralmente não é dado)
</dl> </dd> Edit<dl> Desfazer Ctrl+Z  
Refazer Ctrl+Y <separator>  
Recortar Ctrl+X  
Copiar Ctrl+C  
Colar Ctrl+V <separator>  
Select all Ctrl+A <separator>  
Excluir Del (o atalho geralmente não é dado) <separator>  
Encontrar... Ctrl+F  
Encontre o próximo F3 (o comando geralmente não é dado)  
Substituir... Ctrl+H  
Ir para... Ctrl+G
</dl> </dd> View<dl> Barras de ferramentas  
Barra de status <separator>  
</dl> </dd> Zoom<dl> Ampliar Ctrl++  
Reduzir Ctrl+- <separator>  
Tela inteira F11  
Atualizar F5
</dl> </dd> <dd>Ferramentas<dl> ... <separator>  
Opções
</dl> </dd> Ajuda<dl> <program name> ajuda F1 <separator>  
Sobre <program name>  
</dl> </dd> </dl>

**Botões de menu da barra de ferramentas padrão**

Os botões de menu da barra de ferramentas padrão são os a seguir. Esta lista mostra a categoria de menu e rótulos de item, sua ordem com separadores, suas teclas de atalho e suas reellipses.

<dl> Ferramentas<dl> Tela inteiraF11(Reatribuir chave de acesso se Find também for usado.)  
Barras de ferramentas (Observe que o comando da barra de menus é aqui.) <separator>  
Imprimir...  
Encontrar... <separator>  
Zoom  
Tamanho do texto <separator>  
Opções
</dl> </dd> Organize<dl> Nova pastaCtrl+N <separator>  
CutCtrl+X  
CopyCtrl+C  
ColarCtrl+V <separator>  
Selecione allCtrl+A <separator>  
DeleteDel (o atalho geralmente não é dado)  
Renomear <separator>  
Opções
</dl> </dd> Page<dl> Nova janelaCtrl+N <separator>  
Zoom  
Tamanho do texto
</dl> </dd> </dl>

**Menus de contexto padrão**

O conteúdo do menu de contexto padrão é o seguinte. Esta lista mostra os rótulos do item de menu, seu pedido com separadores, suas chaves de acesso e suas reellipses. Os menus de contexto não mostram teclas de atalho.

<dl> Aberto  
Executar  
Reproduzir  
Editar  
Imprimir... <separator>  
Recortar  
Copiar  
Colar <separator>  
Excluir  
Renomear <separator>  
Bloquear <object name> o (marca de seleção)  
Propriedades
</dl>

### <a name="using-ellipses"></a>Usando reticências

Enquanto os comandos de menu são usados para ações imediatas, mais informações podem ser necessárias para executar a ação. **Indique um comando que precise de informações adicionais (incluindo uma confirmação) adicionando reticências ao final do rótulo.**

![captura de tela do comando Imprimir e caixa de diálogo Imprimir ](images/cmd-menus-image15.png)

Neste exemplo, a impressão... comando exibe uma caixa de diálogo de impressão para coletar mais informações.

**O uso adequado de reticências é importante para indicar que os usuários podem fazer mais escolhas antes de executar a ação ou até mesmo cancelar a ação inteiramente.** A indicação visual oferecida por uma elipse permite que os usuários explorem seu software sem medo.

**Isso não significa que você deve usar uma elipse sempre que uma ação exibir outra janela** somente quando forem necessárias informações adicionais para executar a ação. por exemplo, os comandos sobre, avançado, ajuda, opções, propriedades e Configurações devem exibir outra janela quando clicados, mas não exigem informações adicionais do usuário. Portanto, eles não precisam de reticências.

**No caso de ambiguidade (por exemplo, o rótulo de comando não tem um verbo), decida com base na ação do usuário mais provável.** Se a simples exibição da janela for uma ação comum, não use reticências.

**Correto:**

Mais cores...

Informações da versão

No primeiro exemplo, os usuários provavelmente vão escolher uma cor, portanto, usar reticências está correto. No segundo exemplo, os usuários provavelmente irão exibir as informações de versão, tornando as reticências desnecessárias.

> [!Note]  
> Ao determinar se um comando de menu precisa de uma elipse, não use a necessidade de [elevar privilégios](winenv-uac.md) como um fator.

 

A elevação não é uma informação necessária para executar um comando (em vez disso, é para permissão) e a necessidade de elevação é indicada com a blindagem de segurança.

## <a name="labels"></a>Rótulos

-   **Use a capitalização com estilo de frase.**
    -   **Exceção:** Para aplicativos herdados, você pode usar a capitalização no estilo de título, se necessário, para evitar a mistura de estilos de capitalização.

### <a name="menu-category-names"></a>Nomes de categoria de menu

-   **Use nomes de categoria de menu que sejam verbos ou substantivos de palavra única.** Um rótulo de várias palavras pode ser confundido com rótulos de palavras de 2 1.
-   **Prefira nomes de menu baseados em verbo.** No entanto, omita o verbo se ele for criar, mostrar, exibir ou gerenciar. Por exemplo, as seguintes categorias de menu não têm verbos:
    -   Tabela
    -   Ferramentas
    -   Janela
-   Para nomes de categoria não padrão, **use uma palavra única e específica que descreva claramente e precisamente o conteúdo do menu.** Embora os nomes não precisem ser tão gerais que descrevam tudo no menu, eles devem ser previsíveis o suficiente para que os usuários não fiquem surpresos com o que eles consideram no menu.

### <a name="menu-item-names"></a>Nomes de item de menu

-   **Use nomes de itens de menu que começam com uma frase Verb, substantivo ou substantivo.**
-   **Prefira nomes de menu baseados em verbo.** No entanto, omita o verbo se:
    -   **O verbo é criar, mostrar, exibir ou gerenciar.** Por exemplo, os seguintes comandos não têm verbos:
        -   Sobre
        -   Avançado
        -   Tela inteira
        -   Novo
        -   Opções
        -   Propriedades
    -   **O verbo é o mesmo que o nome da categoria de menu para evitar repetição.** Por exemplo, na categoria de menu Inserir, use texto, tabela e imagem em vez de inserir texto, inserir tabela e inserir imagem.
-   **Use verbos específicos.** Evite verbos genéricos, não auxiliares, como alterar e gerenciar.
-   **Use substantivos singulares para comandos que se aplicam a um único objeto**; caso contrário, use os substantivos do plural.
-   **Use modificadores conforme necessário para distinguir entre comandos semelhantes.** Exemplos: Inserir linha acima, Inserir linha abaixo.
-   **Para pares de comandos complementares, escolha nomes claramente complementares.** Exemplos: Adicionar, remover; Mostrar, ocultar; Inserir, excluir.
-   **Escolha nomes de itens de menu com base em metas e tarefas do usuário, não em tecnologia.**

**Correto:**

![captura de tela do menu Copiar com o item de menu Formatar ](images/cmd-menus-image16.png)

**Incorreto:**

![captura de tela do menu Copiar com o item de menu codec ](images/cmd-menus-image17.png)

No exemplo incorreto, o item de menu se baseia em sua tecnologia.

-   Use os seguintes nomes de item de menu para a finalidade indicada:
    -   **Opções** do Para exibir as opções do programa.
    -   **Personalizar** Para exibir as opções de programa especificamente relacionadas à configuração de interface do usuário mecânica.
    -   **Personalizar** Para exibir um resumo das configurações de [personalização](glossary.md) comumente usadas.
    -   **Preferências** do Não use. Use as opções em vez disso.
    -   **Propriedades** do Para exibir a janela de propriedades de um objeto.
    -   **Configurações** Não use como um rótulo de menu. Use as opções em vez disso.

### <a name="submenu-names"></a>Nomes de submenu

-   **Os itens de menu que exibem submenus nunca têm reticências em seu rótulo.** A seta do submenu indica que outra seleção é necessária.

**Incorreto:**

![captura de tela do novo item de menu com reticências ](images/cmd-menus-image18.png)

Neste exemplo, o novo item de menu apresenta incorretamente uma elipse.

## <a name="documentation"></a>Documentação

Ao fazer referência a menus:

-   Em comandos que mostram ou ocultam menus, consulte barras de menu. Não faça referência a eles como menus clássicos.
-   Consulte os menus por seus rótulos. Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou reticências.
-   Para se referir a categorias de menu, use "no <category name> menu". Se o local de um item de menu estiver claro no contexto, você não precisará mencionar a categoria do menu.
-   Para descrever a interação do usuário de itens de menu, use Click, sem o menu ou comando do Word. Não use escolher, selecionar ou escolher. Não faça referência a um item de menu como um item de menu, exceto na documentação técnica.
-   Para descrever a remoção de uma marca de seleção de uma opção de menu, use clique para remover a marca de seleção. Não use claro.
-   Consulte menus de contexto como menus de contexto, não menus de atalho.
-   Não use cascata, suspenso, suspenso ou pop-up para descrever os menus, exceto na documentação de programação.
-   Consulte itens de menu indisponíveis como não disponíveis, não como esmaecido, desabilitado ou acinzentado. Use Disabled na documentação de programação.
-   Quando possível, formate os rótulos usando texto em negrito. Caso contrário, coloque os rótulos entre aspas somente se necessário para evitar confusão.

Exemplos:

-   No menu **arquivo** , clique em **Imprimir** para imprimir o documento.
-   No menu **Exibir** , aponte para **barras de ferramentas** e clique em **formatação**.

 

