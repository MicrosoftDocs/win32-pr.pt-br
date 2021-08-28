---
title: Listar exibições
description: Com um modo de exibição de lista, os usuários podem exibir e interagir com uma coleção de objetos de dados, usando uma única seleção ou seleção múltipla.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8b8a1ce068b03ddf2a7aba40a0044f79914102d3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983059"
---
# <a name="list-views"></a>Listar exibições

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um modo de exibição de lista, os usuários podem exibir e interagir com uma coleção de objetos de dados, usando uma única seleção ou seleção múltipla.

![captura de tela da exibição de lista com cabeçalhos de coluna ](images/ctrl-list-views-image1.png)

Uma exibição de lista típica.

As exibições de lista têm mais flexibilidade e funcionalidade do que as caixas de listagem. Ao contrário das caixas de listagem, elas dão suporte à alteração de exibições, agrupamento, várias colunas com títulos, classificação por colunas, alteração de larguras de coluna e ordem, sendo uma origem de arrastar, um destino de soltar e a cópia de dados de e para a área de transferência.

> [!Note]  
> As diretrizes relacionadas às caixas de [layout](vis-layout.md) e de [lista](ctrl-list-boxes.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Uma exibição de lista é mais do que apenas uma caixa de listagem mais flexível e funcional: sua funcionalidade extra resulta em uso diferente. A tabela a seguir mostra a comparação.



|   Uso                          | Caixas de listagem                 | Modos de exibição de lista               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Data type**<br/>    | Opções de dados e programas.<br/> | Somente dados.<br/>                                                                                                                         |
| **Contents**<br/>     | Somente rótulos.<br/>                   | Rótulos e dados auxiliares, possivelmente em várias colunas.<br/>                                                                           |
| **Interação**<br/>  | Usado para fazer seleções.<br/>    | Pode ser usado para fazer seleções, mas geralmente é usado para exibir e interagir com dados. Pode ser uma origem de arrastar ou um destino de soltar.<br/> |
| **Apresentação**<br/> | Fixado.<br/>                         | Os usuários podem alterar modos de exibição, agrupar, classificar por colunas e alterar larguras de coluna e ordem.<br/>                                                |



 

Para decidir se esse é o controle certo, considere estas perguntas:

-   **A lista apresenta dados, em vez de opções de programa?** Caso contrário, considere usar uma caixa de listagem em vez disso.
-   **Os usuários precisam alterar as exibições, agrupar, classificar por colunas ou alterar as larguras e a ordem das colunas?** Caso contrário, use uma caixa de listagem em vez disso.
-   **O controle precisa ser uma origem de arrastar ou um destino de soltura?** Nesse caso, use um modo de exibição de lista.
-   **Os itens da lista precisam ser copiados ou colados da área de transferência?** Nesse caso, use um modo de exibição de lista.

### <a name="check-box-list-views"></a>Exibições da lista de caixas de seleção

-   **O controle é usado para escolher zero ou mais itens de uma lista de dados?** Para escolher um item, use uma única seleção em vez disso.
-   **A seleção é essencial para a tarefa ou é normalmente usada?** Nesse caso, use uma exibição de lista da caixa de seleção para tornar a seleção mais óbvia, especialmente se os usuários de destino não forem avançados. Caso contrário, use uma exibição de lista de seleção múltipla padrão se as caixas de seleção desenharem muita atenção para a seleção múltipla ou resultarem em muita confusão na tela.
-   **A estabilidade da seleção múltipla é importante?** Nesse caso, use uma lista de [caixas de seleção](ctrl-list-boxes.md), o construtor de listas ou a lista de adicionar/remover porque clicar em altera apenas um único item por vez. Com uma lista de seleção múltipla padrão, é muito fácil limpar todas as seleções mesmo por acidente.

> [!Note]  
> Às vezes, um controle parecido com um modo de exibição de lista é implementado usando uma caixa de listagem e vice-versa. Nesses casos, aplique as diretrizes com base no uso, não na implementação.

 

## <a name="usage-patterns"></a>Padrões de uso

Todas as exibições dão suporte à seleção única, em que os usuários podem selecionar apenas um item por vez e várias seleções, nas quais os usuários podem selecionar qualquer número de itens, incluindo nenhum. As exibições de lista dão suporte ao [modo de seleção estendida](glossary.md), em que a seleção pode ser estendida arrastando ou com SHIFT + clique ou CTRL + clique para selecionar grupos de valores contíguos ou não adjacentes, respectivamente. Ao contrário das caixas de listagem, elas não dão suporte ao [modo de seleção múltipla](glossary.md), no qual clicar em qualquer item alterna seu estado de seleção, independentemente das teclas Shift e Ctrl.

### <a name="standard-list-view"></a>Exibição de lista padrão

O controle de exibição de lista dá suporte a cinco exibições padrão:



|    Uso    |   Exemplo        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tile**<br/> cada item aparece como um ícone médio, com um rótulo e detalhes opcionais à direita. <br/>                                                                                                                         | ![captura de tela de miniaturas com títulos e detalhes ](images/ctrl-list-views-image2.png)<br/> Exibição de bloco mostra ícones médios com rótulos e detalhes opcionais à direita.<br/>                                                                                                                                                                |
| **Ícone grande**<br/> cada item aparece como um ícone extra grande, grande ou médio com um rótulo abaixo dele.<br/>                                                                                                                      | ![captura de tela da exibição de lista de miniatura grande ](images/ctrl-list-views-image3.png)<br/> Exibição de ícones grandes mostra cada item como um ícone grande com um rótulo abaixo dele.<br/>                                                                                                                                                                              |
| **Ícone pequeno**<br/> cada item é exibido como um ícone pequeno com um rótulo à direita.<br/>                                                                                                                                           | ![captura de tela da exibição de lista de miniatura pequena ](images/ctrl-list-views-image4.png)<br/> A exibição de ícones pequenos mostra cada item como um ícone pequeno com seu rótulo à direita.<br/>                                                                                                                                                                        |
| **Lista**<br/> cada item é exibido como um ícone pequeno com um rótulo à direita.<br/>                                                                                                                                                 | no modo de lista, essa exibição ordena itens em colunas e usa uma barra de rolagem horizontal. por outro lado, os modos de exibição de ícone ordenam itens em linhas e usam uma barra de rolagem vertical. <br/> ![captura de tela do modo de exibição de lista no modo de lista ](images/ctrl-list-views-image5.png)<br/> O modo de lista mostra cada item como um ícone pequeno com seu rótulo à direita.<br/> |
| **Detalhes**<br/> cada item aparece como uma linha em um formato tabular. a coluna mais à esquerda contém o ícone e o rótulo opcionais do item, e as colunas subsequentes contêm informações adicionais, como propriedades do item.<br/> | Além disso, as colunas podem ser adicionadas ou removidas, reordenadas e redimensionadas. as linhas podem ser agrupadas, classificadas por coluna. <br/> ![captura de tela da exibição de lista no modo de detalhes ](images/ctrl-list-views-image6.png)<br/> Exibição de detalhes mostra cada item como uma linha em um formato de tabela.<br/>                                                              |



 

### <a name="list-view-variations"></a>Variações de exibição de lista




| Rótulo | Valor |
|--------|-------|
| <strong>Seletor de coluna</strong><br /> As exibições de lista às vezes têm tantas colunas que não é prático mostrar todas elas. Nesse caso, a melhor abordagem é exibir as colunas mais úteis por padrão e permitir que os usuários adicionem ou removam colunas conforme necessário. <br /> | <img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br /> Clicar com o botão direito do mouse no título da coluna exibe um menu de contexto que permite aos usuários adicionar ou remover colunas.<br /><img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br /> Clicar em mais no menu de contexto de cabeçalho de coluna exibe a caixa de diálogo escolher colunas, que permite aos usuários adicionar ou remover colunas, bem como reordená-las.<br /> | 
| <strong>Exibir lista de caixas de seleção</strong><br /> Permitir que os usuários selecionem vários itens.<br /> | As exibições de lista de seleção múltipla têm exatamente a mesma aparência que as exibições de lista de seleção única, portanto, não há nenhuma pista visual de que ofereça suporte a seleção múltipla. Uma exibição de lista da caixa de seleção pode ser usada para indicar claramente que a seleção múltipla é possível. Consequentemente, esse padrão deve ser usado para tarefas em que a seleção múltipla é essencial ou comumente usada.<br /><img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br /> Neste exemplo, um modo de exibição de ícone pequeno usa caixas de seleção porque várias seleções são essenciais para a tarefa.<br /> | 
| <strong>Listar exibições com grupos</strong><br /> Organize os dados em grupos.<br /> | Embora as exibições de detalhes com frequência ofereçam suporte à classificação dos dados por qualquer uma das colunas, as exibições de lista permitem que os usuários organizem os itens em grupos. Alguns benefícios do agrupamento são:<br /><ul><li>Os grupos funcionam em todas as exibições (exceto lista); portanto, por exemplo, os usuários podem agrupar um grande modo de exibição de ícones grandes de álbuns por artista.</li><li>Os grupos podem ser coleções de alto nível, que geralmente são mais significativas do que o agrupamento diretamente dos dados. por exemplo, Windows Explorer agrupa datas em hoje, ontem, semana passada, no início deste ano e há muito tempo.</li></ul><img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br /> neste exemplo, o centro de boas-vindas Windows mostra itens agrupados em uma exibição de lista.<br /> | 




 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Classificar itens de lista em uma ordem lógica.** Classifique os nomes em ordem alfabética, números em ordem numérica e datas em ordem cronológica.
-   **Se apropriado, permita que os usuários alterem a ordem de classificação.** A classificação do usuário será importante se a lista tiver muitos itens ou se houver cenários em que os itens sejam encontrados com mais eficiência usando uma ordem de classificação diferente da padrão.
-   **Use o atributo de seleção sempre mostrar** para que os usuários possam imediatamente determinar o item selecionado, mesmo quando o controle não tiver foco.
-   **Evite apresentar exibições de lista vazia.** Se os usuários criarem uma lista, inicialize a lista com instruções ou itens de exemplo que os usuários possam precisar.

    ![captura de tela da caixa de diálogo Pesquisar com instruções ](images/ctrl-list-views-image11.png)

    Neste exemplo, a exibição de lista de pesquisa inicialmente apresenta instruções.

-   **Se os usuários puderem alterar as exibições, agrupar, classificar por colunas ou alterar colunas e suas larguras e ordenar, faça essas configurações persistirem para que entrem em vigor na próxima vez que a exibição de lista for exibida.** Faça com que eles persistam em uma exibição por lista, por usuário.

### <a name="interaction"></a>Interação

-   **Usar um clique para selecionar o item de lista ao qual o usuário está apontando. Exceção:** para o padrão de lista de links de comando, o clique único seleciona o item e fecha a janela ou navega para a próxima página.
-   **Considere fornecer um comportamento de clique duplo.** Clicar duas vezes deve ter o mesmo efeito que selecionar um item e executar o comando padrão.
-   **Faça com que o comportamento de clique duplo seja redundante.** Sempre deve haver um botão de comando ou comando de menu de contexto que tenha o mesmo efeito.
-   Se um item de lista exigir mais explicações, **forneça a explicação em um** [InfoTip](ctrl-tooltips-and-infotips.md). Use frases completas e pontuação final.

    ![captura de tela da exibição de lista com o teclado InfoTip ](images/ctrl-list-views-image12.png)

    Neste exemplo, um InfoTip é usado para fornecer mais informações.

-   **Fornecer menus de contexto de comandos relevantes.** Esses comandos incluem recortar, copiar, colar, remover ou excluir, renomear e propriedades.
-   **Se os usuários puderem alterar a ordem de classificação e o agrupamento, forneça os menus de contexto classificar por e agrupar por.** O primeiro clique em um nome de coluna classifica ou agrupa a lista na ordem crescente para essa coluna, o segundo clique classifica ou agrupa em ordem decrescente. Use a ordem anterior (de outra coluna) como a chave secundária.

    ![captura de tela da exibição de lista com o menu "classificar por" ](images/ctrl-list-views-image13.png)

    Neste exemplo, o menu classificar por contexto altera a ordem de classificação. Clicar em nome uma vez classifica por nome em ordem crescente. Clicar em nome novamente classifica por nome em ordem decrescente.

-   **Torne o cabeçalho da coluna de exibição de lista acessível usando o teclado.**
    -   **Desenvolvedores:** Você pode fazer isso definindo o foco no controle de cabeçalho de coluna. essa funcionalidade é nova no Windows Vista.
-   **Ao desabilitar um modo de exibição de lista, desabilite também todos os rótulos e botões de comando associados.**
-   **Evite a rolagem horizontal.** O modo de lista usa a rolagem horizontal. Esse modo é geralmente o mais compacto, mas a rolagem horizontal geralmente é mais difícil de usar do que a rolagem vertical. Considere usar a exibição de ícone pequeno em vez disso, se a compactação não for importante. No entanto, o modo de lista é uma boa opção quando há muitos itens classificados alfabeticamente e espaço em tela suficiente para um controle amplo.

    **Aceitável:**

    ![captura de tela de um controle de modo de lista grande ](images/ctrl-list-views-image14.png)

    Neste exemplo, o modo de lista é usado porque há muitos itens e muito espaço de tela disponível para um controle amplo.

### <a name="multiple-selection-lists"></a>Listas de seleção múltipla

-   **Considere a exibição do número de itens selecionados abaixo da lista**, especialmente se for provável que os usuários selecionem vários itens. Essas informações não apenas fornecem comentários úteis, mas também indica claramente que a exibição de lista dá suporte à seleção múltipla.

    ![captura de tela da lista de cinco miniaturas selecionadas ](images/ctrl-list-views-image15.png)

    Neste exemplo, o número de itens selecionados é exibido abaixo da lista.

-   Como alternativa, em vez do número de itens selecionados, você pode fornecer outras métricas de seleção que podem ser mais significativas, como os recursos necessários para as seleções.

    ![captura de tela da caixa de diálogo mostrando espaço em disco ](images/ctrl-list-views-image16.png)

    Neste exemplo, o espaço em disco necessário para instalar os componentes é mais significativo do que o número de componentes selecionados.

-   Para exibições de lista de caixas de seleção, se houver potencialmente muitos itens e a seleção ou limpeza de todos eles for provável, adicione selecionar tudo e desmarcar todos os botões de comando.
-   **Use caixas de seleção de estado misto para indicar a seleção parcial dos itens em um contêiner.** O estado misto não é usado como um terceiro estado para um item individual.

### <a name="changing-views"></a>Alterando exibições

Se os usuários puderem alterar as exibições:

-   **Escolha a exibição mais conveniente por padrão.** As alterações feitas pelos usuários devem se tornar persistentes em uma exibição por lista, por usuário.
-   **Altere a exibição usando um botão de divisão, botão de menu ou lista suspensa.** Sempre que for prático, use um [botão de divisão](ctrl-command-buttons.md) na barra de ferramentas e altere o rótulo do botão para refletir o modo de exibição atual.

    ![captura de tela da lista com o botão ' exibições ' dividido ](images/ctrl-list-views-image17.png)

    Neste exemplo, um botão de divisão na barra de ferramentas é usado para alterar as exibições.

-   **Forneça um menu de contexto de exibição.**

    ![captura de tela da lista com o menu de contexto ' Exibir ' ](images/ctrl-list-views-image18.png)

Neste exemplo, um menu de contexto de exibição é usado para alterar as exibições.

### <a name="details-views"></a>Exibições de detalhes

-   **Considere usar a exibição de blocos para melhorar a legibilidade.**

    **Aceitável:**

    ![captura de tela da lista de detalhes com colunas estreitas ](images/ctrl-list-views-image19.png)

    Neste exemplo, há muitos dados e a janela, lista e colunas são muito pequenas, tornando os itens de lista difíceis de ler.

    **Melhor:**

    ![captura de tela da lista de detalhes com dados em grupos ](images/ctrl-list-views-image20.png)

    Neste exemplo, a exibição de bloco exibe os dados sem truncamento.

-   **Escolha as larguras de coluna padrão apropriadas para os dados mais longos.** As exibições de lista truncam automaticamente dados longos com reticências, portanto, as larguras das colunas são apropriadas se algumas elipses são exibidas por padrão. Embora os usuários possam redimensionar colunas, prefira outras soluções:

    -   Dimensione a largura de cada coluna para ajustar seus dados.
    -   Dimensione a largura do controle para se ajustar a suas colunas, além de barras de rolagem prováveis.
    -   Se necessário, use a rolagem horizontal.
    -   Ter dados truncados somente para itens de tamanho ímpar ou como último recurso.

    Se os dados de tamanho normal devem ser truncados por padrão, torne a janela e a exibição de lista redimensionável. Inclua mais 30% (até 200 por cento para texto mais curto) para qualquer texto (mas não números) que serão localizados.

    **Incorreto:**

    ![captura de tela de colunas de lista com dados truncados ](images/ctrl-list-views-image21.png)

    Neste exemplo, a maioria dos dados é truncada. As várias reticências indicam claramente que as larguras de controle e coluna são muito pequenas para os dados.

    **Incorreto:**

    ![captura de tela de lista de uma coluna com dados truncados ](images/ctrl-list-views-image22.png)

    Neste exemplo, os dados são truncados sem motivo.

-   **Escolha uma ordem de coluna padrão apropriada.** Em geral, ordene as colunas da seguinte maneira:

    -   Primeiro, o nome do item ou os dados de identificação.
    -   Em seguida, outros dados são úteis para diferenciar os itens da lista.
    -   Em seguida, os dados mais úteis (preferencialmente curto ou fixo).
    -   Em seguida, dados menos úteis (preferíveis de comprimento curto ou fixo).
    -   Dados por último, longos e de comprimento variável.

    Dados longos e de comprimento variável são colocados nas últimas colunas para reduzir a necessidade de rolagem horizontal. Dentro dessas categorias, coloque as informações relacionadas juntas em uma sequência lógica.

-   **Quando apropriado, permita que os usuários adicionem e removam colunas, bem como alterem o pedido.** Exibe as colunas mais úteis por padrão. Isso é feito com o atributo Header Drag Drop.
-   Escolha um alinhamento apropriado para os dados. Use as seguintes regras:
    -   Alinhar à direita números, moedas e horas.
    -   Texto alinhado à esquerda, IDs (mesmo se numérico) e datas.
-   Para títulos de colunas sortíveis, o primeiro clique em um título classifica a lista em ordem crescente para a coluna, o segundo clique classifica em **ordem decrescente.** Use a ordem de classificação anterior (de outra coluna) como a chave de classificação secundária.

    ![captura de tela da lista de detalhes com dados classificação ](images/ctrl-list-views-image23.png)

    Neste exemplo, a coluna Nome foi clicada primeiro e, em seguida, a coluna Tipo. Como resultado, Tipo em ordem crescente é a chave de classificação primária e Nome em ordem crescente é o secundário.

-   **Use o atributo Selecionar Linha Completa** para que os usuários possam determinar prontamente os itens selecionados em todas as colunas.
-   **Não use um header de coluna sortível, a menos que os dados possam ser classificação.**
-   **Não use um header de coluna se houver apenas uma coluna e não for necessário reverter a classificação.** Em vez disso, use um rótulo para identificar os dados.

    **Incorreto:**

    ![captura de tela da lista com rótulo no header de coluna ](images/ctrl-list-views-image24.png)

    **Correto:**

    ![captura de tela da lista com o rótulo acima do controle ](images/ctrl-list-views-image25.png)

    No exemplo correto, um rótulo é usado em vez de um header de coluna.

## <a name="recommended-sizing-and-spacing"></a>Espaçamento e o espaçamento recomendados

![captura de tela de tamanho e espaçamento de lista ](images/ctrl-list-views-image26.png)

O espaçamento e o espaçamento recomendados para exibições de lista.

-   **Escolha uma altura de exibição de lista que exibe um número integral de itens.** Evite truncar itens verticalmente.
-   **Escolha um tamanho de exibição de lista que elimine a rolagem vertical e horizontal desnecessária em todas as exibições com suporte.** Exibições de lista devem ser exibidas entre 3 e 20 itens. Considere tornar uma exibição de lista um pouco maior se isso eliminar uma barra de rolagem. Listas com potencialmente muitos itens devem exibir pelo menos cinco itens para facilitar a rolagem mostrando mais itens por vez e facilitando a posição da barra de rolagem.
-   **Se os usuários se beneficiarem de tornar a exibição de lista maior, faça com que a exibição de lista e sua janela pai resizáveis.** Isso permite que os usuários ajustem o tamanho da exibição de lista conforme necessário. No entanto, exibições de lista reizáveis não devem exibir menos de três itens.

## <a name="labels"></a>Rótulos

### <a name="control-labels"></a>Rótulos de controle

-   Todas as exibições de lista precisam de rótulos. Escreva o rótulo como uma palavra ou frase, não como uma frase, terminando com dois-pontos usando texto estático.
-   Atribua uma chave [de acesso exclusiva](glossary.md) para cada rótulo. Para diretrizes, consulte [Teclado](inter-keyboard.md).
-   Use [a capitalização de estilo de frase](glossary.md).
-   Posiciona o rótulo acima do controle e alinhe o rótulo com a borda esquerda do controle.
-   Para exibições de lista de seleção múltipla, escreva o rótulo que indica claramente que várias seleções são possíveis. Rótulos de exibição de lista de caixas de seleção podem ser menos explícitos.

    **Correto:**

    ![captura de tela do rótulo: selecione um ou mais complementos ](images/ctrl-list-views-image27.png)

    Neste exemplo, o rótulo indica claramente que várias seleções são possíveis.

    **Incorreto:**

    ![captura de tela do rótulo: complementos ](images/ctrl-list-views-image28.png)

    Neste exemplo, o rótulo não fornece informações sobre várias seleções.

    **Aceitável:**

    ![captura de tela do rótulo da lista de caixas de seleção: complementos ](images/ctrl-list-views-image29.png)

    Neste exemplo, as caixas de seleção indicam claramente que várias seleções são possíveis, portanto, o rótulo não precisa ser explícito.

-   Você pode especificar unidades (segundos, conexões e assim por diante) entre parênteses após o rótulo.

### <a name="heading-labels"></a>Rótulos de título

-   Mantenha os rótulos de título breves (três palavras ou menos).
-   Use uma única frase de substantivo ou substantivo sem pontuação final.
-   Use [a capitalização de estilo de frase](glossary.md).
-   Alinhe o título da mesma maneira que os dados.

### <a name="group-labels"></a>Rótulos de grupo

-   Use os seguintes rótulos de grupo para coleções de alto nível:
    -   Nomes: use a primeira letra de intervalos de nome ou letra.
    -   Tamanhos: não especificado, 0 KB, 0-10 KB, 10-100 KB, 100 KB - 1 MB, 1-16 MB, 16-128 MB
    -   Datas: Hoje, Ontem, Última semana, Início deste ano e Há muito tempo.
-   Caso contrário, os rótulos de grupo usam o texto exato dos dados que estão sendo agrupados, incluindo maiúsculas e pontuação.

### <a name="data-text"></a>Texto de dados

-   Use [a capitalização de estilo de frase](glossary.md).

### <a name="instructional-text"></a>Texto de instrução

-   Se você precisar adicionar texto de instrução sobre uma exibição de lista, adicione-o acima do rótulo. Use frases completas com pontuação final.
-   Use [a capitalização de estilo de frase](glossary.md).
-   Informações adicionais úteis, mas não necessárias, devem ser mantidas curtas. Coloque essas informações entre parênteses entre o rótulo e dois-pontos ou sem parênteses abaixo do controle .

## <a name="documentation"></a>Documentação

Ao fazer referência a exibições de lista:

-   Use o texto de rótulo exato, incluindo sua capitalização, mas não inclua o sublinhado ou dois-pontos da chave de acesso e inclua a lista de palavras. Não consulte uma caixa de listagem como uma caixa de listagem, exibição de lista ou campo.
-   Para dados de lista, use o texto de dados exato, incluindo sua capitalização.
-   Consulte exibições de lista como exibições de lista somente em programação e outras documentações técnicas. Em qualquer outro lugar, use a lista.
-   Para descrever a interação do usuário, use selecionar para os dados e clique nos títulos.
-   Quando possível, forja as opções de rótulo e lista usando texto em negrito. Caso contrário, coloque o rótulo e as opções entre aspas somente se necessário para evitar confusão.

Exemplo: na lista **Programas e serviços,** selecione **Compartilhamento de arquivos e impressoras.**

Ao fazer referência às caixas de seleção em uma exibição de lista:

-   Use o texto exato do rótulo, incluindo sua capitalização, e inclua a caixa de seleção palavra. Não inclua o sublinhado da chave de acesso.
-   Para descrever a interação do usuário, use selecionar e limpar.
-   Quando possível, forja o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: marque a **caixa de seleção Sublinhado.**

 

