---
title: Menus (noções básicas de Design)
description: Os menus são listas hierárquicas de comandos ou opções disponíveis para os usuários no contexto atual.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ba8c67716e6b30fcc32651c8932363310926e6bf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880377"
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
-   Use barras de menus, barras de ferramentas e menus de contexto com eficiência.
-   Use ícones com eficiência.
-   Use teclas de acesso e teclas de atalho com eficiência.

**Se você fizer apenas uma coisa...**

Escolha uma apresentação de comando que corresponda ao tipo de programa, aos tipos de janela, ao uso de comando e aos usuários de destino.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Todos os padrões de menu, exceto as barras de menu, precisam de uma seta suspensa para indicar a presença de um menu suspenso.** A presença de menus fica sem dizer em uma barra de menus, mas não em outros padrões.
-   **Não altere nomes de itens de menu dinamicamente.** Isso é confuso e inesperado. Por exemplo, não altere uma opção de modo retrato para modo paisagem na seleção. Para modos, use [marcadores e marcas](#bullets-and-checkmarks) de seleção em vez disso.
    -   **Exceção:** Você pode alterar nomes de itens de menu que são baseados em nomes de objetos dinamicamente. Por exemplo, as listas de arquivos usados recentemente ou nomes de janela podem ser dinâmicas.

### <a name="menu-bars"></a>Barras de menu

-   **Considere eliminar barras de menus com três ou menos categorias de menu.** Se houver apenas alguns comandos, prefira alternativas mais claras, como menus da barra de ferramentas, ou alternativas mais diretas, como botões de comando e links.
-   **Não há mais de 10 categorias de menu.** Muitas categorias de menu são enormes e tornam a barra de menus difícil de usar.
-   **Considere ocultar a barra de menus** se a barra de ferramentas ou os comandos diretos fornecerem quase todos os comandos necessários para a maioria dos usuários. Permitir que os usuários mostrem ou ocultem com uma opção de marca de seleção de barra de menus em um menu da barra de ferramentas.

![captura de tela da lista de opções com a barra de menus selecionada ](images/cmd-menus-image9.png)

neste exemplo, Windows o Internet Explorer fornece uma opção de barra de menus.

Para obter mais informações, consulte [ocultando barras de menu](#hiding-menu-bars).

### <a name="hiding-menu-bars"></a>Ocultando barras de menu

Em geral, as barras de ferramentas funcionam muito bem com barras de menus porque ambas permitem que cada uma se concentre em seus pontos fortes sem comprometimento.

-   Oculte a barra de menus por padrão se o design da barra de ferramentas tornar uma barra de menus redundante.
-   Oculte a barra de menus em vez de removê-la completamente, pois as barras de menus são mais acessíveis para usuários de teclado.
-   Para restaurar a barra de menus, forneça uma opção de marca de seleção de barra de menus na categoria de menu exibição (para barras de ferramentas primárias) ou ferramentas (para barras de ferramentas secundárias). Para obter mais informações, consulte [menu padrão e botões de divisão](cmd-toolbars.md).

### <a name="menu-categories"></a>Categorias de menu

-   **Escolha nomes de palavras únicas para categorias de menu.** O uso de várias palavras torna a separação entre categorias confusa.
-   **Para programas que criam ou exibem documentos, use as categorias de menu padrão** , como arquivo, editar, exibir, ferramentas e ajuda. Isso torna os itens de menu comuns previsíveis e fáceis de localizar.
-   **Para outros tipos de programas, considere organizar seus comandos e opções em categorias mais úteis e naturais** com base na finalidade do seu programa e na maneira como os usuários consideram suas tarefas e metas. Não se sinta obrigado a usar a organização de menu padrão se ela não for adequada para seu programa.
-   **Se você optar por usar categorias de menu não padrão, deverá escolher bons nomes de categoria.** Para obter mais informações, consulte a seção [Rótulos](#labels) .
-   **Prefira categorias de menu orientadas a tarefas em categorias genéricas.** As categorias orientadas a tarefas facilitam a localização de itens de menu.

![captura de tela da barra de menus com RIP, gravação e sincronização ](images/cmd-menus-image10.png)

neste exemplo, Windows Media Player usa categorias de menu orientado a tarefas.

-   **Evite categorias de menu com apenas um ou dois itens de menu.** Se for sensato, consolide com outras categorias de menu, talvez usando um submenu.
-   **Considere colocar o mesmo item de menu em várias categorias somente se:**
    -   O item de menu pertence logicamente a várias categorias de menu.
    -   Você tem dados mostrando que os usuários têm dificuldade para localizar o item em uma única categoria de menu.
    -   Você tem apenas um ou dois itens de menu de difícil localização em várias categorias.
-   **Não coloque itens de menu diferentes que usem o mesmo nome em várias categorias.** Por exemplo, não têm itens de menu de opções diferentes em várias categorias.
    -   **Exceção:** O padrão de menu da guia pode ter opções e itens de menu de ajuda diferentes em cada menu de guia.

![captura de tela de menus guia com itens de menu repetidos ](images/cmd-menus-image11.png)

neste exemplo, Windows Media Player tem opções e itens do menu ajuda em cada menu da guia.

### <a name="menu-item-organization-and-order"></a>Ordem e organização do item de menu

-   **Organize os itens de menu em grupos de sete ou menos itens fortemente relacionados.** Para isso, os submenus contam como um único item de menu no menu pai.
-   **Não coloque mais de 25 itens em um único nível de um menu** (não contando submenus).
-   **Coloque separadores entre os grupos dentro de um menu.** Um separador é uma única linha que abrange a largura do menu.
-   **Em um menu, coloque os grupos em sua ordem lógica.** Se não houver nenhuma ordem lógica, coloque os grupos usados com mais frequência primeiro.
-   **Dentro de um grupo, coloque os itens em sua ordem lógica.** Se não houver nenhuma ordem lógica, coloque os itens mais comumente usados primeiro. Coloque itens numéricos (como porcentagens de zoom) em ordem numérica.

### <a name="submenus"></a>Submenus

-   **Evite usar submenus desnecessariamente.** Os submenus exigem mais esforço físico para serem usados e geralmente tornam os itens de menu mais difíceis de localizar.
-   **Não coloque itens de menu usados com frequência em um submenu.** Isso tornaria o uso ineficiente desses comandos. No entanto, você pode colocar comandos usados com frequência em um submenu se eles normalmente são acessados mais diretamente, como com uma barra de ferramentas.
-   **Considere usar um submenu se:**
    -   Fazer isso simplifica o menu pai porque ele tem muitos itens (20 ou mais), ou o submenu faz parte de um grupo com mais de sete itens.
    -   Os itens no submenu são usados com menos frequência do que aqueles no menu pai.
    -   O submenu teria três ou mais itens.
    -   Há três ou mais comandos que começam com a mesma palavra. Nesse caso, use essa palavra como o rótulo do submenu.

![captura de tela do menu ' novo ' com quatro itens de submenu ](images/cmd-menus-image12.png)

Neste exemplo, o novo submenu substitui comandos separados para nova mensagem de email, nova mensagem de notícias, nova pasta e novo contato.

-   **Use no máximo três níveis de menus.** Ou seja, você pode ter um menu principal e, no máximo, dois níveis de submenus. Dois níveis de submenus devem ser raros.

### <a name="presentation"></a>Apresentação

-   **Desabilite os itens de menu que não se aplicam ao contexto atual,** em vez de removê-los. Isso torna o conteúdo da barra de menus estável e mais fácil de encontrar. **Exceções:**
    -   Para categorias de menu contextual, **remova em vez de Desabilitar itens de menu de contexto que não se aplicam ao contexto atual.** Uma categoria de menu é contextual quando é exibida somente para modos específicos, como quando um determinado tipo de objeto é selecionado. Para obter detalhes, consulte as diretrizes [remover versus desabilitar](#context-menus) para menus de contexto.
    -   Se a determinação de quando um item de menu deve ser desabilitado causar problemas de desempenho perceptíveis, deixe o item de menu ativo e, se necessário, terá sua seleção resultante de uma mensagem de erro.

### <a name="tab-menus"></a>Menus de guia

-   **Cada menu de guia pode ter opções específicas de contexto e itens de menu da ajuda.** Isso é diferente de todos os outros padrões de menu. Cada guia é usada para um conjunto dedicado de tarefas, portanto, qualquer redundância entre menus de guia não é confusa.

### <a name="context-menus"></a>Menus de contexto

-   **Use menus de contexto somente para comandos e opções contextuais.** Os itens de menu devem ser aplicados somente ao objeto ou região da janela selecionada (ou clicado), não o programa inteiro.
-   **Não torne os comandos disponíveis somente por meio de menus de contexto.** Como as teclas de atalho, os menus de contexto são meios alternativos de executar comandos e escolher opções. Por exemplo, um comando de propriedades também está disponível por meio da barra de menus ou da tecla de acesso Alt + Enter.
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
Imprimir  
&lt;separator&gt;  
</dl> </dd> <dd>Comandos secundários com suporte no objeto<dl> &lt;separator&gt;  
</dl> </dd> Comandos de transferência<dl> Recortar  
Copiar  
Colar  
&lt;separator&gt;  
</dl> </dd> <dd>Configurações de objeto<dl> &lt;separator&gt;  
</dl> </dd> Comandos de objeto<dl> Excluir  
Renomear  
&lt;separator&gt;  
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
    -   **Exceção:** Não exibir as atribuições de teclas de atalho nos menus de contexto. Os menus de contexto não exibem as atribuições de teclas de atalho porque elas são otimizadas para eficiência.
-   **Para atribuições de chave não padrão:**
    -   **Escolha as teclas de atalho que não têm atribuições padrão.** Nunca reatribua as teclas de atalho padrão.
    -   **Use atribuições de chave não padrão consistentemente em todo o programa.** Não atribua diferentes significados em janelas diferentes.
    -   **Se possível, escolha atribuições de chave mnemônico,** especialmente para comandos usados com frequência.
    -   **Use as teclas de função para comandos que têm um efeito de pequena escala,** como comandos que se aplicam ao objeto selecionado. Por exemplo, F2 renomeia o item selecionado.
    -   **Use combinações de teclas CTRL para comandos que têm um efeito de grande escala,** como comandos que se aplicam a um documento inteiro. Por exemplo, CTRL + S salva o documento atual.
    -   **Use combinações de teclas Shift para comandos que estendem ou complementem as ações da tecla de atalho padrão.** Por exemplo, a tecla de atalho Alt + Tab percorre as janelas primárias abertas, enquanto os ciclos Alt + Shift + Tab na ordem inversa. Da mesma forma, F1 exibe a ajuda, enquanto Shift + F1 exibe a ajuda contextual.
    -   **Não use os seguintes caracteres para as teclas de atalho:** @ $ {} \[ \] \\  ~  \| ^ '  < >. Esses caracteres exigem diferentes combinações de teclas em idiomas ou são específicos da localidade.
    -   **não use combinações Ctrl + Alt,** porque Windows interpreta essa combinação em algumas versões de idioma como uma chave AltGR, que gera caracteres alfanuméricos.
-   **Se o programa atribuir muitas teclas de atalho, forneça a capacidade de personalizar as atribuições.** Isso permite que os usuários reatribuam teclas de atalho conflitantes e migrem de outros produtos. A maioria dos programas não atribui teclas de atalho suficientes para que você precise desse recurso.

Para obter mais diretrizes e atribuições de teclas de atalho padrão, consulte [teclado](inter-keyboard.md).

### <a name="standard-menus"></a>Menus padrão

-   **Use a organização do menu padrão para programas que criam ou exibem documentos.** A organização do menu padrão torna os itens de menu comuns previsíveis e fáceis de localizar.
-   **Para outros tipos de programas, use a organização de menu padrão somente quando fizer sentido.** Considere organizar seus comandos e opções em categorias mais úteis e naturais com base na finalidade do seu programa e na maneira como os usuários consideram suas tarefas e metas.

**Barras de menus padrão**

A estrutura de barra de menus padrão é a seguinte. Esta lista mostra os rótulos de categoria e item de menu, sua ordem com separadores, suas teclas de acesso e de atalho e suas reticências.

<dl> Arquivo<dl> Novo Ctrl + N  
Abrir... CTRL + O  
Fechar  
&lt;separator&gt;  
Salvar Ctrl + S  
Salvar como...  
&lt;separator&gt;  
Enviar para  
&lt;separator&gt;  
Imprimir... CTRL + P  
Visualizar impressão  
Configuração de página  
&lt;separator&gt;  
1 <filename> 2 <filename> 3 <filename> ...  
&lt;separator&gt;  
Sair de Alt + F4 (atalho geralmente não fornecido)
</dl> </dd> Edit<dl> Desfazer CTRL + Z  
Refazer Ctrl + Y  
&lt;separator&gt;  
Recortar CTRL + X  
Copiar CTRL + C  
Colar Ctrl + V  
&lt;separator&gt;  
Selecionar tudo Ctrl + A  
&lt;separator&gt;  
Excluir del (o atalho normalmente não foi fornecido)  
&lt;separator&gt;  
Localizar... Ctrl + F  
Localizar próximo F3 (comando geralmente não fornecido)  
Substituir... CTRL + H  
Ir para... CTRL + G
</dl> </dd> View<dl> Barras de ferramentas  
Barra de Status  
&lt;separator&gt;
</dl> </dd> Zoom<dl> Ampliar CTRL + +  
Reduzir CTRL +-  
&lt;separator&gt;  
Tela inteira F11  
Atualizar F5
</dl> </dd> <dd>Ferramentas<dl> ...  
&lt;separator&gt;  
Opções
</dl> </dd> Ajuda<dl> <program name> ajuda F1  
&lt;separator&gt;  
Pensar <program name>  
</dl> </dd> </dl>

**Botões de menu da barra de ferramentas padrão**

Os botões de menu da barra de ferramentas padrão são os seguintes. Esta lista mostra os rótulos de categoria e item de menu, sua ordem com separadores, suas teclas de atalho e suas reticências.

<dl> Ferramentas<dl> ScreenF11 completo (reatribuir a chave de acesso se localizar também for usado.)  
Barras de ferramentas (Observe que o comando da barra de menus é inserido aqui.)  
&lt;separator&gt;  
Imprimir...  
Localizar...  
&lt;separator&gt;  
Zoom  
Tamanho do texto  
&lt;separator&gt;  
Opções  
</dl> </dd> Organize<dl> Novo folderCtrl + N  
&lt;separator&gt;  
CutCtrl + X  
CopyCtrl + C  
PasteCtrl + V  
&lt;separator&gt;  
Selecione allCtrl+A  
&lt;separator&gt;  
DeleteDel (o atalho geralmente não é dado)  
Renomear  
&lt;separator&gt;  
Opções  
</dl> </dd> Page<dl> Nova janelaCtrl+N  
&lt;separator&gt;  
Zoom  
Tamanho do texto  
</dl> </dd> </dl>

**Menus de contexto padrão**

O conteúdo do menu de contexto padrão é o seguinte. Esta lista mostra os rótulos do item de menu, seu pedido com separadores, suas chaves de acesso e suas reellipses. Os menus de contexto não mostram teclas de atalho.

<dl> Aberto  
Executar  
Reproduzir  
Editar  
Imprimir...  
&lt;separator&gt;  
Recortar  
Copiar  
Colar  
&lt;separator&gt;  
Excluir  
Renomear  
&lt;separator&gt;  
Bloquear <object name> o (marca de seleção)  
Propriedades
</dl>

### <a name="using-ellipses"></a>Usando reellipses

Embora os comandos de menu sejam usados para ações imediatas, mais informações podem ser necessárias para executar a ação. **Indique um comando que precisa de informações adicionais (incluindo uma confirmação) adicionando reellipses no final do rótulo.**

![captura de tela da caixa de diálogo Imprimir comando e impressão ](images/cmd-menus-image15.png)

Neste exemplo, a Imprime... O comando exibe uma caixa de diálogo Imprimir para coletar mais informações.

**O uso adequado de reellipses é importante para indicar que os usuários podem fazer outras escolhas antes de executar a ação ou até mesmo cancelar totalmente a ação.** A indicação visual oferecida por reellipses permite que os usuários explorem seu software sem medo.

**Isso não significa que você deve** usar reellipses sempre que uma ação exibir outra janela somente quando informações adicionais são necessárias para executar a ação. Por exemplo, os comandos About, Advanced, Help, Options, Properties e Configurações devem exibir outra janela quando clicados, mas não exigem informações adicionais do usuário. Portanto, eles não precisam de re elipses.

**No caso de ambiguidade (por exemplo, o rótulo de comando não tem um verbo), decida com base na ação do usuário mais provável.** Se simplesmente exibir a janela for uma ação comum, não use reellipses.

**Correto:**

Mais cores...

Informações da versão

No primeiro exemplo, é mais provável que os usuários escolham uma cor, portanto, o uso de reellipses está correto. No segundo exemplo, os usuários provavelmente verão as informações de versão, tornando as reellips desnecessárias.

> [!Note]  
> Ao determinar se um comando de menu precisa de reellipses, não use a necessidade de elevar [privilégios](winenv-uac.md) como um fator.

 

Elevação não são informações necessárias para executar um comando (em vez disso, é para permissão) e a necessidade de elevar é indicada com o shield de segurança.

## <a name="labels"></a>Rótulos

-   **Use a capitalização com estilo de frase.**
    -   **Exceção:** Para aplicativos herdado, você pode usar a capitalização de estilo de título, se necessário, para evitar a combinação de estilos de capitalização.

### <a name="menu-category-names"></a>Nomes de categoria de menu

-   **Use nomes de categoria de menu que são verbos ou substantivos de palavra única.** Um rótulo de várias palavras pode ser confundido para dois rótulos de uma palavra.
-   **Prefira nomes de menu baseados em verbo.** No entanto, omita o verbo se ele for Criar, Mostrar, Exibir ou Gerenciar. Por exemplo, as seguintes categorias de menu não têm verbos:
    -   Tabela
    -   Ferramentas
    -   Janela
-   Para nomes de categorias não padrão, use uma única palavra específica que descreva com clareza e precisão o **conteúdo do menu.** Embora os nomes não tenham que ser tão gerais que descrevam tudo no menu, eles devem ser previsíveis o suficiente para que os usuários não sejam surpresas com o que encontram no menu.

### <a name="menu-item-names"></a>Nomes de item de menu

-   **Use nomes de item de menu que começam com uma frase de verbo, substantivo ou substantivo.**
-   **Prefira nomes de menu baseados em verbo.** No entanto, omita o verbo se:
    -   **O verbo é Criar, Mostrar, Exibir ou Gerenciar.** Por exemplo, os seguintes comandos não têm verbos:
        -   Sobre
        -   Avançado
        -   Tela inteira
        -   Novo
        -   Opções
        -   Propriedades
    -   **O verbo é o mesmo que o nome da categoria de menu para evitar a repetição.** Por exemplo, na categoria de menu Inserir, use Texto, Tabela e Imagem em vez de Inserir texto, Inserir tabela e Inserir imagem.
-   **Use verbos específicos.** Evite verbos genéricos e sem ajuda, como Alterar e Gerenciar.
-   **Use substantivos singulares para comandos que se aplicam a um único objeto**; caso contrário, use substantivos plurais.
-   **Use modificadores conforme necessário para distinguir entre comandos semelhantes.** Exemplos: inserir linha acima, Inserir linha abaixo.
-   **Para pares de comandos complementares, escolha nomes claramente complementares.** Exemplos: Adicionar, Remover; Mostrar, Ocultar; Inserir, Excluir.
-   **Escolha nomes de item de menu com base nas metas e tarefas do usuário, não na tecnologia.**

**Correto:**

![captura de tela do menu suspenso com o item de menu de formato ](images/cmd-menus-image16.png)

**Incorreto:**

![captura de tela do menu suspenso com o item de menu codec ](images/cmd-menus-image17.png)

No exemplo incorreto, o item de menu baseia-se em sua tecnologia.

-   Use os seguintes nomes de item de menu para a finalidade afirmada:
    -   **Opções** Para exibir as opções do programa.
    -   **Personalizar** Para exibir as opções de programa relacionadas especificamente à configuração de interface do usuário mecânica.
    -   **Personalizar** Para exibir um resumo das configurações de [personalização comumente](glossary.md) usadas.
    -   **Preferências** Não use. Em vez disso, use Opções.
    -   **Propriedades** Para exibir a janela de propriedades de um objeto.
    -   **Configurações** Não use como um rótulo de menu. Em vez disso, use Opções.

### <a name="submenu-names"></a>Nomes de submenu

-   **Itens de menu que exibem submenus nunca têm reellipses em seu rótulo.** A seta de submenu indica que outra seleção é necessária.

**Incorreto:**

![captura de tela do novo item de menu com reellipses ](images/cmd-menus-image18.png)

Neste exemplo, o item de menu Novo tem incorretamente reellipses.

## <a name="documentation"></a>Documentação

Ao fazer referência a menus:

-   Em comandos que mostram ou ocultam menus, consulte barras de menu. Não se refira a eles como menus clássicos.
-   Consulte os menus por seus rótulos. Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua o sublinhado ou reellipse da chave de acesso.
-   Para se referir às categorias de menu, use "No <category name> menu". Se o local de um item de menu estiver claro no contexto, você não precisará mencionar a categoria de menu.
-   Para descrever a interação do usuário com itens de menu, use clique, sem o menu de palavras ou comando. Não use escolher, selecionar ou escolher. Não consulte um item de menu como um item de menu, exceto na documentação técnica.
-   Para descrever a remoção de uma marca de seleção de uma opção de menu, use clique para remover a marca de seleção. Não use clear.
-   Consulte menus de contexto como menus de contexto, não menus de atalho.
-   Não use em cascata, pull-down, menu suspenso ou pop-up para descrever menus, exceto na documentação de programação.
-   Consulte itens de menu indisponíveis como indisponíveis, não como esmaecidas, desabilitadas ou esmaecidas. Use desabilitado na documentação de programação.
-   Quando possível, forja os rótulos usando texto em negrito. Caso contrário, coloque os rótulos entre aspas somente se necessário para evitar confusão.

Exemplos:

-   No menu **Arquivo,** clique em **Imprimir** para imprimir o documento.
-   No menu **Exibir,** aponte para **Barras de Ferramentas** e clique em **Formatação**.

 

