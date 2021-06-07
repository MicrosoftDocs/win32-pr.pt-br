---
title: Exibições de árvore
description: Com um exibição de árvore, os usuários podem exibir e interagir com uma coleção hierárquica de objetos, usando seleção única ou seleção múltipla.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ade51b421350dc90bf72e2ff1a683bf1d352f7c1
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524490"
---
# <a name="tree-views"></a>Exibições de árvore

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com um exibição de árvore, os usuários podem exibir e interagir com uma coleção hierárquica de objetos, usando seleção única ou seleção múltipla.

Em uma árvore, os objetos que contêm dados são chamados de nós folha e objetos que contêm outros objetos são chamados de nós de contêiner. Um único nó de contêiner superior é chamado de nó raiz. Os usuários podem expandir e retraí-los clicando nos botões do expansador de mais e menos.

![captura de tela do exibição de árvore do Windows Explorer ](images/ctrl-tree-views-image1.png)

Uma exibição de árvore típica.

> [!Note]  
> As diretrizes relacionadas [ao layout](vis-layout.md) [e aos menus](cmd-menus.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

**Ter dados hierárquicos não significa que você deve usar uma exibição de árvore.** Muitas vezes, uma [exibição de](ctrl-list-views.md) lista é uma opção mais simples, mas mais poderosa. Listar exibições:

-   Suporte a várias exibições diferentes.
-   Suporte à classificação de dados por qualquer uma das colunas na exibição Detalhes.
-   Suporte à organização de dados em grupos, formar uma hierarquia de dois níveis.

**Para usar uma exibição de lista, você pode nivelar informações hierárquicas usando as seguintes técnicas:**

-   Remova o nó raiz se estiver presente, porque geralmente não é necessário.
-   Use grupos de exibição de lista, guias, [listas](/windows/desktop/uxguide/ctrl-drop)listadas ou [títulos expansíveis](glossary.md) para substituir os contêineres de nível superior.

    ![captura de tela de grupos de exibição de lista que contêm listas ](images/ctrl-tree-views-image2.png)

    Neste exemplo, os grupos de exibição de lista são usados para os contêineres de nível superior.

    ![captura de tela de guias usadas para contêineres de nível superior ](images/ctrl-tree-views-image3.png)

    Neste exemplo, as guias são usadas para os contêineres de nível superior

    ![captura de tela da lista lista listada usada como um contêiner ](images/ctrl-tree-views-image4.png)

    Neste exemplo, uma listada é usada para os contêineres de nível superior.

-   Se um controle associado exibir o conteúdo do contêiner selecionado, esse controle poderá exibir níveis inferiores da hierarquia.

    ![captura de tela do painel de tabela de conteúdo ](images/ctrl-tree-views-image5.png)

    Neste exemplo, contêineres de baixo nível são exibidos na janela do documento.

**Você deverá usar um exibição de árvore se precisar exibir uma hierarquia de mais de dois níveis (não incluindo o nó raiz).**

Para decidir se uma exibição de árvore é o controle certo, considere estas perguntas:

-   **Os dados são hierárquicos?** Se não, use outro controle.
-   **A hierarquia tem pelo menos três níveis (não incluindo a raiz)?** Caso não, considere alternativas como grupos de exibição de lista, guias, listas listadas ou títulos expansíveis.
-   **Os itens têm dados auxiliares?** Nesse caso, considere usar uma exibição de lista no modo de exibição Detalhes para aproveitar ao máximo os dados auxiliares.
-   **Os dados de nível inferior estão relacionados a subtarefas independentes?** Nesse caso, considere exibir as informações em um controle associado ou em uma janela separada (exibida usando botões [de comando](ctrl-command-buttons.md) ou [links](ctrl-command-links.md)).
-   **Os usuários de destino são avançados?** Os usuários avançados são mais proficientes ao usar árvores. Se seu aplicativo for destinado a usuários iniciantes, evite usar exibições de árvore.
-   **Os itens têm uma categorização única, natural e hierárquica que seja familiar para a maioria dos usuários?** Se sim, os dados são ideais para um modo de exibição de árvore. Se houver necessidade de várias exibições ou classificação, use uma exibição de lista.
-   **Os usuários precisam ver os dados de nível inferior em alguns, mas não em todos os cenários ou em alguns, mas não o tempo todo?** Se sim, os dados são ideais para um modo de exibição de árvore.

> [!Note]  
> Às vezes, um controle que se parece com um exibição de árvore é implementado usando uma exibição de lista. Nesses casos, aplique as diretrizes com base no uso, não na implementação.

 

## <a name="design-concepts"></a>Conceitos de design

As árvores destinam-se a organizar dados e facilitar a descoberta, mas é difícil tornar os dados em uma árvore facilmente descobriveis. Tenha os princípios a seguir em mente ao decidir sobre exibições de árvore e sua organização.

### <a name="predictability-and-discoverability"></a>Previsibilidade e descoberta

**Uma exibição de árvore baseia-se nas relações entre objetos.** As árvores funcionam melhor quando os objetos formam uma relação clara, bem conhecida e mutuamente exclusiva na qual cada objeto é mapeado para um único contêiner fácil de determinar.

**Um problema significativo é que um objeto pode aparecer em nós diferentes.** Por exemplo, onde os usuários esperam encontrar um dispositivo de hardware que reproduz música, tem um disco rígido grande e usa uma porta USB? Talvez em qualquer um dos vários nós de contêiner diferentes, como Multimídia, Armazenamento, USB e, possivelmente, em Recursos de Hardware. Uma solução é colocar cada objeto no único contêiner mais apropriado, independentemente das circunstâncias; outra abordagem é colocar cada objeto em todos os contêineres que se aplicam. O primeiro promove uma hierarquia simples e limpa e a segunda promove a descoberta, cada uma tem vantagens e possíveis problemas.

**Os usuários podem não entender completamente o layout da árvore, mas formarão um modelo mental das relações depois de interagir com a árvore por um tempo.** Se esse modelo mental estiver incorreto, isso causará confusão. Por exemplo, suponha que um player de música possa ser encontrado nos contêineres Multimídia, Armazenamento e USB. Essa disposição melhora a capacidade de descoberta. Se um usuário encontrar primeiro o dispositivo em Multimídia, o usuário poderá concluir que todos os dispositivos como players de música aparecem no contêiner Multimídia. Em seguida, o usuário esperará que dispositivos semelhantes, como câmeras digitais, apareçam no contêiner Multimídia e se confundirão se esse não for o caso.

**O desafio ao projetar uma árvore é equilibrar a descoberta com um modelo de usuário previsível que minimiza a confusão.**

### <a name="breadth-vs-depth"></a>Amplitude versus profundidade

Os estudos de usabilidade mostraram que os usuários são mais bem-sucedidos em localizar objetos em uma árvore ampla do que em uma árvore que é **profunda,** portanto, ao projetar uma árvore, você deve preferir amplitude em vez de profundidade. O ideal é que uma árvore não tenha mais de quatro níveis (sem contar o nó raiz) e os objetos mais acessados devem aparecer nos dois primeiros níveis.

### <a name="other-principles"></a>Outros princípios

-   Quando os usuários encontram o que estão procurando, eles param de procurar. Eles não parecem ver onde mais um objeto pode ser encontrado porque não é necessário. Esses usuários podem assumir que o primeiro caminho que eles encontram é o único caminho.
-   Os usuários têm problemas para localizar objetos em árvores grandes e complexas. Os usuários não executarão uma pesquisa manual e exaustiva para encontrar objetos em tais árvores; eles param quando pensam que gastaram um esforço razoável. Consequentemente, árvores grandes e complexas precisam ser complementadas com outros métodos de acesso, como pesquisa de palavras, índice ou filtragem.
-   Alguns programas permitem que os usuários criem suas próprias árvores. Embora essas árvores autoprofissadas possam ser alinhadas com o modelo mental de um usuário, elas geralmente são criadas hafafamente e mal mantidas. Por exemplo, embora um sistema de arquivos, um programa de email e uma lista de Favoritos normalmente armazenem tipos semelhantes de informações, os usuários raramente se preocupam em organizá-las da mesma maneira.

**Se você fizer apenas uma coisa...**

Avalie cuidadosamente os benefícios e desvantagens do uso de exibições de árvore. Ter dados organizados hierarquicamente não significa que você precisa usar uma exibição de árvore.

## <a name="usage-patterns"></a>Padrões de uso

As exibições de árvore têm vários padrões de uso:



| Uso                           |    Exemplo                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Exibições de árvore com apenas nós de contêiner**<br/> os usuários podem exibir e interagir com um contêiner por vez. <br/>                        | Normalmente, essas exibições de árvore têm um controle associado que exibe o conteúdo do contêiner selecionado, para que os usuários possam interagir com apenas um contêiner por vez. <br/> ![captura de tela do painel de contêiner e do painel de conteúdo ](images/ctrl-tree-views-image6.png)<br/> Neste exemplo, o exibição de árvore tem apenas nós de contêiner. O conteúdo do nó selecionado é exibido no controle de exibição de lista associado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Exibições de árvore com nós de contêiner e folha**<br/> os usuários podem exibir e interagir com contêineres e folhas.<br/>                       | Normalmente, essas exibições de árvore têm um controle associado que exibe o conteúdo do contêiner ou folha selecionado. permitir que os usuários interajam com folhas geralmente torna necessário dar suporte a várias seleções. <br/> ![captura de tela do painel de exibição de árvore e do painel de conteúdo ](images/ctrl-tree-views-image7.png)<br/> Neste exemplo, o modo de exibição de árvore tem nós de contêiner e folha. como há suporte para várias seleções, o conteúdo dos itens abertos é exibido usando [guias](ctrl-tabs.md) no controle associado.<br/> Como alternativa, o modo de exibição de árvore pode ter uma lista organizada, onde os contêineres são os cabeçalhos e as folhas são opções. <br/> ![captura de tela de exibição em árvore com títulos e opções ](images/ctrl-tree-views-image8.png)<br/> Neste exemplo, a árvore deixa as opções e os contêineres são categorias de opção.<br/> |
| **Exibições de árvore da caixa de seleção**<br/> os usuários podem selecionar qualquer número de itens, incluindo nenhum.<br/>                                             | As caixas de seleção indicam claramente que a seleção múltipla é possível. Use esse padrão de árvore quando várias seleções forem essenciais ou usadas com frequência. <br/> ![captura de tela de exibição de árvore com caixas de seleção ](images/ctrl-tree-views-image9.png)<br/> Neste exemplo, uma exibição de árvore da caixa de seleção permite que a seleção de recursos seja ativada ou desativada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Construtores de exibição de árvore**<br/> os usuários podem criar uma árvore adicionando um contêiner ou folha por vez e, opcionalmente, definindo a ordem.<br/> | Muitas árvores podem ser criadas ou modificadas pelos usuários. algumas árvores são criadas no local usando menus de contexto e arrastar e soltar (como as pastas no Windows Explorer), enquanto outras árvores são criadas usando uma caixa de diálogo especializada (como a lista de favoritos no Windows Internet Explorer). <br/> ![captura de tela da caixa de diálogo favoritos ](images/ctrl-tree-views-image10.png)<br/> Neste exemplo do Internet Explorer, os usuários podem criar sua própria lista de favoritos usando uma caixa de diálogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Exibições de árvore com métodos de acesso alternativos**<br/> os usuários podem encontrar objetos de outras maneiras além de usar uma árvore hierárquica.<br/>        | Conforme mencionado anteriormente, os usuários têm dificuldade em encontrar objetos em árvores grandes e complexas, portanto, essas árvores devem ser complementadas com outros métodos de acesso, como uma pesquisa de palavras, um índice ou uma filtragem. <br/> ![captura de tela de conteúdo, guias de índice e favoritos ](images/ctrl-tree-views-image11.png)<br/> Neste exemplo, os usuários também podem acessar informações usando um sumário, um índice e favoritos. para alguns usuários, as guias de índice e pesquisa podem ser mais úteis do que a guia conteúdo.<br/> ![captura de tela do menu Iniciar do Windows e caixa de pesquisa ](images/ctrl-tree-views-image12.png)<br/> Neste exemplo, o menu Iniciar do Windows também permite que os usuários acessem programas, arquivos e páginas da Web digitando parte do nome na caixa de pesquisa.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Dentro de um contêiner, classifique os itens em uma ordem lógica.** Classifique os nomes em ordem alfabética, números em ordem numérica e datas em ordem cronológica.
-   **Use o atributo de seleção sempre mostrar** para que os usuários possam imediatamente determinar o item selecionado, mesmo quando o controle não tiver o foco de entrada.
-   **Se a árvore estiver agindo como um sumário, use o único atributo de expansão para simplificar o gerenciamento da árvore.** Dessa forma, apenas a parte relevante da árvore é expandida.
-   **Evite apresentar árvores vazias.** Se um usuário criar uma árvore, inicialize a árvore com instruções ou itens de exemplo que os usuários podem precisar.

    ![captura de tela da lista de favoritos do Internet Explorer ](images/ctrl-tree-views-image13.png)

    Neste exemplo, a lista é apresentada inicialmente com exemplos.

-   **Não torne os nós de contêiner recolhíveis se os usuários não tiverem motivo para recolhê-los.** Isso adiciona complexidade desnecessária.
-   **Se o desempenho da carga for um problema, exiba somente os contêineres do primeiro e do segundo nível da árvore por padrão.** Em seguida, você pode carregar dados adicionais sob demanda quando um usuário expande branches na árvore.
-   **Se os usuários expandirem ou recolherem um contêiner, fazer esse estado persistir para que ele entre em vigor na próxima vez que o modo de exibição de árvore for exibido**, a menos que os usuários provavelmente prefiram iniciar no estado padrão. A persistência deve estar em uma exibição por árvore, por usuário.
-   **Se contêineres de alto nível tiverem conteúdo semelhante, considere o uso de pistas visuais para diferenciá-los.**

    **Incorreto:**

    ![captura de tela de itens do Outlook com ícones diferentes ](images/ctrl-tree-views-image14.png)

    Neste exemplo, as pastas de caixa de correio e de arquivo têm conteúdo semelhante. Depois que as árvores são expandidas ainda mais, é muito difícil para os usuários saber onde estão na árvore, levando a confusão. Usar ícones ligeiramente diferentes nas seções diferentes resolveria esse problema.

-   **Reconsidere as linhas de conexão.** Embora essas linhas mostrem claramente as relações entre os nós de contêiner e folha, elas adicionam confusão visuais sem a compreensão de auxiliar significativamente. Especificamente, eles não ajudam quando os nós estão próximos, nem ajudam quando os nós estão tão distantes que a rolagem é necessária.

    **Correto:**

    ![captura de tela do modo de exibição de árvore com linhas de conexão ](images/ctrl-tree-views-image15.png)

    **Melhor:**

    ![captura de tela do modo de exibição de árvore sem linhas de conexão ](images/ctrl-tree-views-image16.png)

    As linhas de conexão fazem pouco para ajudar na compreensão.

### <a name="interaction"></a>Interação

-   **Considere fornecer um comportamento de clique duplo.** Clicar duas vezes deve ter o mesmo efeito que selecionar um item e executar o comando padrão.
-   **Faça com que o comportamento de clique duplo seja redundante.** Sempre deve haver um botão de comando ou comando de menu de contexto que tenha o mesmo efeito.
-   Se um item exigir mais explicações, **forneça a explicação em um InfoTip**.

    ![captura de tela de favoritos com InfoTip para um item ](images/ctrl-tree-views-image17.png)

    Neste exemplo, um InfoTip fornece mais informações.

-   **Fornecer menus de contexto de comandos relevantes.** Esses comandos incluem recortar, copiar, colar, remover ou excluir, renomear e propriedades.
-   **Ao desabilitar um modo de exibição de árvore, desabilite também todos os rótulos e botões de comando associados.**

### <a name="tree-organization"></a>Organização em árvore

-   **Use uma estrutura hierárquica natural familiar para a maioria dos usuários.**
-   **Se você não puder usar essa estrutura, tente balancear a capacidade de descoberta com um modelo de usuário previsível que minimize a confusão.**
-   **Para melhorar a descoberta com segurança, coloque um item em vários contêineres quando:**
    -   O item não está relacionado a nenhum outro item semelhante (para que os usuários não fiquem confusos com associações incorretas).
    -   Há apenas alguns desses itens localizados de forma redundante (para que a árvore não fique inflada).
-   **Use a estrutura hierárquica mais simples que funciona bem.** Para fazer isso:
    -   Coloque os objetos acessados com mais frequência nos dois primeiros níveis da árvore (não contando o nó raiz) e coloque objetos menos acessados mais distantes da hierarquia.
    -   Eliminar contêineres de nível intermediário redundantes ou combinados desnecessários.
-   **Prefira amplitude sobre profundidade.** O ideal é que uma árvore não tenha mais de quatro níveis e os objetos acessados com mais frequência apareçam nos dois primeiros níveis.
-   **Determine se você realmente precisa de um nó raiz.** Forneça um nó raiz se os usuários precisarem da capacidade de executar comandos em toda a árvore (possivelmente usando um menu de contexto no nó raiz). Caso contrário, a árvore é mais simples e fácil de usar sem ela.
-   **Se a árvore tiver métodos de acesso alternativos, como uma pesquisa de palavra ou um índice, otimize a árvore para navegação concentrando-se no conteúdo mais útil.** Com métodos de acesso alternativos, o conteúdo da árvore não precisa ser abrangente. Simplificar a árvore torna mais fácil para os usuários encontrarem o conteúdo mais útil.

### <a name="check-box-tree-views"></a>Exibições de árvore da caixa de seleção

-   **Exiba o número de itens selecionados abaixo da lista**, especialmente se for provável que os usuários selecionem vários itens. Esse comentário ajuda os usuários a confirmar que sua seleção está correta.

    ![captura de tela do número de itens selecionados ](images/ctrl-tree-views-image18.png)

    Neste exemplo, o número de itens selecionados é exibido abaixo da árvore. Está claro que dois itens não estão selecionados.

-   Se houver potencialmente muitos itens e a seleção ou limpeza de todos eles for provável, adicione selecionar todos e limpar todos os botões de comando.
-   **Use caixas de seleção de estado misto para indicar a seleção parcial dos itens em um contêiner.**

    **Correto:**

    ![captura de tela da janela com caixas de seleção de estado misto ](images/ctrl-tree-views-image19.png)

    Neste exemplo, as caixas de seleção de estado misto são usadas para indicar a seleção parcial.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![captura de tela de dimensionamento e espaçamento da exibição em árvore ](images/ctrl-tree-views-image20.png)

Dimensionamento e espaçamento recomendados para controles de exibição em árvore.

-   **Escolha uma largura de exibição de árvore que evite a necessidade de rolagem horizontal** para a maioria dos itens quando a árvore estiver totalmente expandida.
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

