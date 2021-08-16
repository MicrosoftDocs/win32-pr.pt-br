---
title: Exibições de árvore
description: Com um modo de exibição de árvore, os usuários podem exibir e interagir com uma coleção hierarquicamente organizada de objetos, usando uma única seleção ou seleção múltipla.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0b5a456673338fec7240bb3b3a11047327239f70675786f26add1bbecdb7211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118217571"
---
# <a name="tree-views"></a>Exibições de árvore

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um modo de exibição de árvore, os usuários podem exibir e interagir com uma coleção hierarquicamente organizada de objetos, usando uma única seleção ou seleção múltipla.

Em uma árvore, os objetos que contêm dados são chamados nós de folha e objetos que contêm outros objetos são chamados de nós de contêiner. Um único nó de contêiner mais alto é chamado de nó raiz. Os usuários podem expandir e recolher nós de contêiner clicando nos botões mais e menos expansor.

![captura de tela do modo de exibição de árvore do Windows Explorer ](images/ctrl-tree-views-image1.png)

Um modo de exibição de árvore típico.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md) e aos [menus](cmd-menus.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

**Ter dados hierárquicos não significa que você deve usar um modo de exibição de árvore.** Muitas vezes, uma [exibição de lista](ctrl-list-views.md) é uma opção mais simples, mas mais poderosa. Exibições de lista:

-   Suporte a várias exibições diferentes.
-   Suporte à classificação de dados por qualquer uma das colunas na exibição de detalhes.
-   Suporte à organização de dados em grupos, formando uma hierarquia de dois níveis.

**Para usar um modo de exibição de lista, você pode mesclar informações hierárquicas usando as seguintes técnicas:**

-   Remova o nó raiz, se estiver presente, porque ele geralmente não é necessário.
-   Use grupos de exibição de lista, guias, [listas suspensas](/windows/desktop/uxguide/ctrl-drop)ou [títulos expansíveis](glossary.md) para substituir os contêineres de nível superior.

    ![captura de tela de grupos de exibição de lista contendo listas ](images/ctrl-tree-views-image2.png)

    Neste exemplo, os grupos de exibição de lista são usados para os contêineres de nível superior.

    ![captura de tela de guias usadas para contêineres de nível superior ](images/ctrl-tree-views-image3.png)

    Neste exemplo, as guias são usadas para os contêineres de nível superior

    ![captura de tela da lista suspensa usada como um contêiner ](images/ctrl-tree-views-image4.png)

    Neste exemplo, uma lista suspensa é usada para os contêineres de nível superior.

-   Se um controle associado exibir o conteúdo do contêiner selecionado, esse controle poderá exibir níveis inferiores da hierarquia.

    ![captura de tela do painel Sumário ](images/ctrl-tree-views-image5.png)

    Neste exemplo, os contêineres de nível baixo são exibidos na janela do documento.

**Você deve usar um modo de exibição de árvore se precisar exibir uma hierarquia de mais de dois níveis (não incluindo o nó raiz).**

Para decidir se um modo de exibição de árvore é o controle certo, considere estas perguntas:

-   **Os dados são hierárquicos?** Se não, use outro controle.
-   **A hierarquia tem pelo menos três níveis (não incluindo a raiz)?** Caso contrário, considere alternativas como grupos de exibição de lista, guias, listas suspensas ou títulos expansíveis.
-   **Os itens têm dados auxiliares?** Nesse caso, considere usar um modo de exibição de lista no modo de exibição de detalhes para aproveitar ao máximo os dados auxiliares.
-   **Os dados de nível inferior estão relacionados a subtarefas independentes?** Nesse caso, considere exibir as informações em um controle associado ou em uma janela separada (exibida usando [botões de comando](ctrl-command-buttons.md) ou [links](ctrl-command-links.md)).
-   **Os usuários de destino são avançados?** Os usuários avançados são mais proficientes no uso de árvores. Se seu aplicativo for destinado a usuários iniciantes, evite usar exibições de árvore.
-   **Os itens têm uma categorização única, natural e hierárquica familiar para a maioria dos usuários?** Nesse caso, os dados são ideais para um modo de exibição de árvore. Se houver uma necessidade de várias exibições ou classificação, use uma exibição de lista em vez disso.
-   **Os usuários precisam ver os dados de nível inferior em alguns, mas não em todos os cenários, ou alguns, mas não o tempo todo?** Nesse caso, os dados são ideais para um modo de exibição de árvore.

> [!Note]  
> Às vezes, um controle parecido com um modo de exibição de árvore é implementado usando uma exibição de lista. Nesses casos, aplique as diretrizes com base no uso, não na implementação.

 

## <a name="design-concepts"></a>Conceitos de design

As árvores são destinadas a organizar dados e facilitar a localização, ainda que seja difícil tornar os dados dentro de uma árvore facilmente detectáveis. Tenha em mente os princípios a seguir ao decidir sobre exibições de árvore e sua organização.

### <a name="predictability-and-discoverability"></a>Previsibilidade e descoberta

**Um modo de exibição de árvore é baseado nas relações entre objetos.** As árvores funcionam melhor quando os objetos formam uma relação clara, bem conhecida, mutuamente exclusiva, na qual cada objeto é mapeado para um contêiner único e fácil de determinar.

**Um problema significativo é que um objeto pode aparecer em nós diferentes.** Por exemplo, onde os usuários esperam encontrar um dispositivo de hardware que reproduza música, tem um disco rígido grande e usa uma porta USB? talvez em qualquer um dos vários nós de contêiner diferentes, como multimídia, Armazenamento, USB e possivelmente em recursos de Hardware. Uma solução é colocar cada objeto sob o contêiner único mais apropriado, independentemente das circunstâncias; outra abordagem é inserir cada objeto em todos os contêineres que se aplicam. A primeira promove uma hierarquia simples e limpa, e a segunda promove a descoberta, cada uma tem vantagens e problemas potenciais.

**Os usuários podem não entender completamente o layout da árvore, mas eles formarão um modelo mental das relações depois de interagir com a árvore por um tempo.** Se esse modelo mental estiver incorreto, isso resultará em confusão. por exemplo, suponha que um player de música possa ser encontrado nos contêineres multimídia, Armazenamento e USB. Essa disposição melhora a capacidade de descoberta. Se um usuário encontrar o dispositivo pela primeira vez em multimídia, o usuário poderá concluir que todos os dispositivos, como players de música, apareçam no contêiner multimídia. O usuário esperará que dispositivos semelhantes, como câmeras digitais, apareçam no contêiner de multimídia e se tornarão confusos se não for o caso.

**O desafio ao criar uma árvore é equilibrar a capacidade de descoberta com um modelo de usuário previsível que minimiza a confusão.**

### <a name="breadth-vs-depth"></a>Amplitude versus profundidade

Estudos de usabilidade mostraram que **os usuários são mais bem-sucedidos na localização de objetos em uma árvore que é ampla do que em uma árvore que é profunda**, portanto, ao criar uma árvore, você deve preferir a amplitude em profundidade. O ideal é que uma árvore não tenha mais de quatro níveis (não contando o nó raiz) e os objetos acessados com mais frequência apareçam nos dois primeiros níveis.

### <a name="other-principles"></a>Outros princípios

-   Quando os usuários encontram o que estão procurando, eles param de procurar. Eles não parecem ver onde mais um objeto pode ser encontrado, pois eles não precisam. Esses usuários podem pressupor que o primeiro caminho encontrado é o único caminho.
-   Os usuários têm dificuldade para localizar objetos em árvores grandes e complexas. Os usuários não executarão uma pesquisa manual e completa para localizar objetos em tais árvores; Eles param de quando acham que gastaram um esforço razoável. Consequentemente, árvores grandes e complexas precisam ser complementadas com outros métodos de acesso, como o Word Search, um índice ou uma filtragem.
-   Alguns programas permitem que os usuários criem suas próprias árvores. Embora essas árvores autoprojetadas possam ser alinhadas com o modelo mental de um usuário, elas são criadas com frequência e são mantidas de forma insatisfatória. Por exemplo, embora um sistema de arquivos, programa de email e lista de favoritos normalmente armazenem tipos semelhantes de informações, os usuários raramente se preocupam em organizá-los da mesma maneira.

**Se você fizer apenas uma coisa...**

Avalie atentamente os benefícios e as desvantagens do uso de exibições de árvore. Ter dados hierarquicamente organizados não significa que você precisa usar uma exibição de árvore.

## <a name="usage-patterns"></a>Padrões de uso

Os modos de exibição de árvore têm vários padrões de uso:



| Uso                           |    Exemplo                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Exibições de árvore com apenas nós de contêiner**<br/> os usuários podem exibir e interagir com um contêiner por vez. <br/>                        | Normalmente, essas exibições de árvore têm um controle associado que exibe o conteúdo do contêiner selecionado, para que os usuários possam interagir com apenas um contêiner por vez. <br/> ![captura de tela do painel de contêineres e painel de conteúdo ](images/ctrl-tree-views-image6.png)<br/> Neste exemplo, o modo de exibição de árvore tem apenas nós de contêiner. O conteúdo do nó selecionado é exibido no controle de exibição de lista associado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Exibições de árvore com nós de contêiner e folha**<br/> os usuários podem exibir e interagir com contêineres e folhas.<br/>                       | Normalmente, essas exibições de árvore têm um controle associado que exibe o conteúdo do contêiner ou folha selecionado. permitir que os usuários interajam com as folhas geralmente torna necessário dar suporte a várias seleções. <br/> ![captura de tela do painel de exibição de árvore e do painel de conteúdo ](images/ctrl-tree-views-image7.png)<br/> neste exemplo, o exibição de árvore tem nós de contêiner e folha. como há suporte para várias seleções, o conteúdo dos itens abertos é exibido usando [guias](ctrl-tabs.md) no controle associado.<br/> como alternativa, o exibição de árvore pode ter uma lista organizada, em que os contêineres são títulos e as folhas são opções. <br/> ![captura de tela do tree-view com títulos e opções ](images/ctrl-tree-views-image8.png)<br/> Neste exemplo, as folhas de árvore são opções e os contêineres são categorias de opção.<br/> |
| **Exibições de árvore de caixa de seleção**<br/> os usuários podem selecionar qualquer número de itens, incluindo nenhum.<br/>                                             | As caixas de seleção indicam claramente que várias seleções são possíveis. use esse padrão de árvore quando várias seleções são essenciais ou comumente usadas. <br/> ![captura de tela do exibição de árvore com caixas de seleção ](images/ctrl-tree-views-image9.png)<br/> Neste exemplo, um exibição de árvore de caixa de seleção permite que a seleção de recursos seja ativas ou desligadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Construtores de exibição de árvore**<br/> os usuários podem criar uma árvore adicionando um contêiner ou folha por vez e, opcionalmente, definindo o pedido.<br/> | Muitas árvores podem ser criadas ou modificadas pelos usuários. algumas árvores são criadas no local usando menus de contexto e do tipo "arrastar e soltar" (como as pastas no Windows Explorer), enquanto outras árvores são criadas usando uma caixa de diálogo especializada (como a lista de favoritos no Windows Internet Explorer). <br/> ![captura de tela da caixa de diálogo favoritos ](images/ctrl-tree-views-image10.png)<br/> Neste exemplo de Internet Explorer, os usuários podem criar sua própria lista de favoritos usando uma caixa de diálogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Exibições de árvore com métodos de acesso alternativos**<br/> os usuários podem encontrar objetos de maneiras diferentes de usar uma árvore hierárquica.<br/>        | Conforme mencionado anteriormente, os usuários têm problemas para localizar objetos em árvores grandes e complexas, portanto, essas árvores devem ser complementadas com outros métodos de acesso, como uma pesquisa de palavras, um índice ou filtragem. <br/> ![captura de tela das guias conteúdo, índice e favoritos ](images/ctrl-tree-views-image11.png)<br/> neste exemplo, os usuários também podem acessar informações usando um tabela de conteúdo, um índice e favoritos. para alguns usuários, as guias de índice e pesquisa podem ser mais úteis do que a guia conteúdo.<br/> ![captura de tela do menu Iniciar do Windows e caixa de pesquisa ](images/ctrl-tree-views-image12.png)<br/> Neste exemplo, o Windows menu Iniciar também permite que os usuários acessem programas, arquivos e páginas da Web digitando parte do nome na caixa De pesquisa.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Em um contêiner, classificar os itens em uma ordem lógica.** Classificar nomes em ordem alfabética, números em ordem numérica e datas em ordem cronológica.
-   **Use o atributo Sempre Mostrar** Seleção para que os usuários possam determinar prontamente o item selecionado, mesmo quando o controle não tiver o foco de entrada.
-   **Se a árvore estiver atuando como um tabela de conteúdo, use o atributo Expansão Única para simplificar o gerenciamento da árvore.** Dessa forma, somente a parte relevante da árvore é expandida.
-   **Evite apresentar árvores vazias.** Se um usuário criar uma árvore, inicialize a árvore com instruções ou itens de exemplo que os usuários possam precisar.

    ![captura de tela da lista de favoritos do Internet Explorer ](images/ctrl-tree-views-image13.png)

    Neste exemplo, a lista é inicialmente apresentada com exemplos.

-   **Não tornar os nós de contêiner reutíveis se os usuários não têm motivo para reacioná-los.** Isso adiciona complexidade desnecessária.
-   **Se o desempenho da carga for um problema, exibe apenas os contêineres de primeiro e segundo níveis da árvore por padrão.** Em seguida, você pode carregar dados adicionais sob demanda quando um usuário expande branches na árvore.
-   Se os usuários expandirem ou fecharem um **contêiner,** faça com que esse estado persista para que ele entre em vigor na próxima vez que o modo de exibição de árvore for exibido, a menos que os usuários prefiram começar no estado padrão. A persistência deve ser em uma exibição por árvore, por usuário.
-   **Se os contêineres de alto nível têm conteúdo semelhante, considere usar pistas visuais para diferenciá-los.**

    **Incorreto:**

    ![captura de tela de itens do Outlook com ícones diferentes ](images/ctrl-tree-views-image14.png)

    Neste exemplo, as Pastas de Caixa de Correio e Arquivo Morto têm conteúdo semelhante. Depois que as árvores são expandidas ainda mais, é muito difícil para os usuários saberem onde estão na árvore, levando a confusão. Usar ícones ligeiramente diferentes nas diferentes seções resolveria esse problema.

-   **Reverso linhas de conexão.** Embora essas linhas mostrem claramente as relações entre os nós de contêiner e folha, elas adicionam confusão visual sem ajudar significativamente a compreensão. Especificamente, eles não ajudam quando os nós estão próximos, nem ajudam quando os nós estão tão distantes que a rolagem é necessária.

    **Correto:**

    ![captura de tela do exibição de árvore com linhas de conexão ](images/ctrl-tree-views-image15.png)

    **Melhor:**

    ![captura de tela do exibição de árvore sem conectar linhas ](images/ctrl-tree-views-image16.png)

    As linhas de conexão fazem pouco para ajudar na compreensão.

### <a name="interaction"></a>Interação

-   **Considere fornecer o comportamento de clique duplo.** Clicar duas vezes deve ter o mesmo efeito que selecionar um item e executar seu comando padrão.
-   **Tornar o comportamento de clique duplo redundante.** Sempre deve haver um botão de comando ou um comando de menu de contexto que tenha o mesmo efeito.
-   Se um item exigir mais explicações, **forneça a explicação em uma infotip**.

    ![captura de tela de favoritos com infotip para um item ](images/ctrl-tree-views-image17.png)

    Neste exemplo, uma infotip fornece mais informações.

-   **Forneça menus de contexto de comandos relevantes.** Esses comandos incluem Recortar, Copiar, Colar, Remover ou Excluir, Renomear e Propriedades.
-   **Ao desabilitar um modo de exibição de árvore, desabilite também todos os rótulos e botões de comando associados.**

### <a name="tree-organization"></a>Organização de árvore

-   **Use uma estrutura hierárquica natural que seja familiar para a maioria dos usuários.**
-   **Se você não puder usar essa estrutura, tente equilibrar a descoberta com um modelo de usuário previsível que minimize a confusão.**
-   **Para melhorar a descoberta com segurança, coloque um item em vários contêineres quando:**
    -   O item não está relacionado a nenhum outro item semelhante (para que os usuários não se confundam por associações incorretas).
    -   Há apenas alguns desses itens localizados com redundância (para que a árvore não se torne sobrecarrada).
-   **Use a estrutura hierárquica mais simples que funcione bem.** Para fazer isso:
    -   Coloque os objetos acessados mais comumente nos dois primeiros níveis da árvore (sem contar o nó raiz) e coloque os objetos acessados com menos acesso mais adiante na hierarquia.
    -   Elimine contêineres de nível intermediário redundantes ou desnecessários.
-   **Prefira amplitude em vez de profundidade.** O ideal é que uma árvore não tenha mais de quatro níveis e os objetos acessados mais comumente apareçam nos dois primeiros níveis.
-   **Determine se você realmente precisa de um nó raiz.** Forneça um nó raiz se os usuários precisam da capacidade de executar comandos em toda a árvore (possivelmente usando um menu de contexto no nó raiz). Caso contrário, a árvore será mais simples e fácil de usar sem ela.
-   **Se a árvore tiver métodos de acesso alternativos, como uma pesquisa de palavras ou um índice, otimize a árvore para navegação concentrando-se no conteúdo mais útil.** Com métodos de acesso alternativos, o conteúdo da árvore não precisa ser abrangente. Simplificar a árvore torna mais fácil para os usuários encontrar o conteúdo mais útil.

### <a name="check-box-tree-views"></a>Exibições de árvore de caixa de seleção

-   **Exibe o número de itens selecionados abaixo da lista**, especialmente se os usuários provavelmente selecionarem vários itens. Esse comentário ajuda os usuários a confirmar que sua seleção está correta.

    ![captura de tela do número de itens selecionados ](images/ctrl-tree-views-image18.png)

    Neste exemplo, o número de itens selecionados é exibido abaixo da árvore. Está claro que dois itens não estão selecionados.

-   Se houver potencialmente muitos itens e a seleção ou a limpeza de todos eles for provável, adicione Select all e desmarcar todos os botões de comando.
-   **Use caixas de seleção de estado misto para indicar a seleção parcial dos itens em um contêiner.**

    **Correto:**

    ![captura de tela da janela com caixas de seleção de estado misto ](images/ctrl-tree-views-image19.png)

    Neste exemplo, as caixas de seleção de estado misto são usadas para indicar a seleção parcial.

## <a name="recommended-sizing-and-spacing"></a>Espaçamento e o espaçamento recomendados

![captura de tela do tamanho e do espaçamento de exibição de árvore ](images/ctrl-tree-views-image20.png)

O espaçamento e o espaçamento recomendados para controles de exibição de árvore.

-   **Escolha uma largura de exibição de árvore que evite a** necessidade de rolagem horizontal para a maioria dos itens quando a árvore estiver totalmente expandida.
-   **Inclua 30% adicionais para acomodar a localização.**
-   **Escolha uma altura de exibição de árvore que elimina a rolagem vertical desnecessária.** Considere tornar um modo de exibição de árvore um pouco mais longo (ou ainda mais, se houver espaço disponível) se isso reduzir a necessidade de uma barra de rolagem vertical.

    **Incorreto:**

    ![captura de tela do controle de exibição de árvore curto e estreito ](images/ctrl-tree-views-image21.png)

    Neste exemplo, tornar o modo de exibição de árvore ligeiramente mais largo e eliminaria as barras de rolagem na maioria dos casos. Nessa árvore específica, apenas um contêiner pode ser aberto por vez.

-   **Se os usuários se beneficiarem de tornar o modo de exibição de árvore maior, torne a exibição de árvore e sua janela pai redimensionável.** Isso permite que os usuários ajustem o tamanho da exibição de árvore conforme necessário.

## <a name="labels"></a>Rótulos

### <a name="control-labels"></a>Rótulos de controle

-   Todas as exibições de árvore precisam de rótulos. Grave o rótulo como uma palavra ou frase, não como uma frase, terminando com dois-pontos e usando [texto estático](glossary.md).
-   Atribua uma chave de acesso exclusiva. Para obter diretrizes de atribuição, consulte [teclado](inter-keyboard.md).
-   Use a capitalização com estilo de frase.
-   Posicione o rótulo acima do controle e alinhe o rótulo com a borda esquerda do controle.
-   Para exibições de árvore de seleção múltipla, escreva o rótulo para que fique claro que a seleção múltipla é possível. Os rótulos da exibição de árvore da caixa de seleção podem ser menos explícitos.

    **Incorreto:**

    ![captura de tela do modo de exibição de árvore com rótulo de componentes ](images/ctrl-tree-views-image22.png)

    Neste exemplo, o rótulo não fornece nenhuma informação sobre a seleção múltipla.

    **Melhor:**

    ![captura de tela da exibição de árvore com o rótulo ' um ou mais ' ](images/ctrl-tree-views-image23.png)

    Neste exemplo, o rótulo indica claramente que é possível selecionar várias seleções.

    **Recomendá**

    ![captura de tela do modo de exibição de árvore com caixas de seleção ](images/ctrl-tree-views-image24.png)

    Neste exemplo, as caixas de seleção indicam claramente que a seleção múltipla é possível, portanto, o rótulo não precisa ser explícito.

### <a name="data-text"></a>Texto de dados

-   Use a capitalização com estilo de frase.

### <a name="instructional-text"></a>Texto de instrução

-   Se você precisar adicionar texto de instruções sobre um modo de exibição de árvore, adicione-o acima do rótulo. Use frases completas com pontuação final.
-   Use a capitalização com estilo de frase.
-   Explicações complementares que são úteis, mas não necessárias, devem ser mantidas curtas. Coloque essas informações entre parênteses entre o rótulo e os dois-pontos, após a instrução principal, se usado em vez de um rótulo ou abaixo do controle.

    ![captura de tela de explicação abaixo do modo de exibição de árvore ](images/ctrl-tree-views-image8.png)

    Neste exemplo, a explicação suplementar está abaixo do controle.

## <a name="documentation"></a>Documentação

Ao fazer referência a exibições de árvore:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou dois-pontos. Inclua a lista de palavras ou a lista hierárquica se o contexto exigir uma distinção de listas regulares.
-   Para itens de árvore, use o texto exato do item, incluindo sua capitalização.
-   Consulte exibições de árvore como exibições de árvore somente em programação e outras documentações técnicas. Em qualquer outra parte, use lista ou lista hierárquica porque a árvore de termos é confusa para a maioria dos usuários.
-   Para descrever a interação do usuário, use selecionar para os dados e expanda e recolha para os botões de adição e subtração.
-   Quando possível, formate o rótulo e os itens de árvore usando texto em negrito. Caso contrário, coloque o rótulo e os itens entre aspas somente se necessário para evitar confusão.

Exemplo: na lista **conteúdo** , selecione **design da interface do usuário**.

Ao se referir a caixas de seleção em um modo de exibição de árvore:

-   Use o texto exato do rótulo, incluindo sua capitalização, e inclua a caixa de seleção palavras. Não inclua o sublinhado da chave de acesso.
-   Para descrever a interação do usuário, use selecionar e limpar.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: na lista **itens para fazer backup** , marque a caixa de seleção **meus documentos** .

