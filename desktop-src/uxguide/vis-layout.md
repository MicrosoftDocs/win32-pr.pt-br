---
title: Layout
description: Layout é o dimensionamento, o espaçamento e o posicionamento do conteúdo dentro de uma janela ou página.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f6b33375cbb679cc7c7efdeb12e5cd30be6280c5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172433"
---
# <a name="layout"></a>Layout

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Layout é o dimensionamento, o espaçamento e o posicionamento do conteúdo dentro de uma janela ou página. O layout eficaz é crucial para ajudar os usuários a encontrar o que estão procurando rapidamente, além de tornar a aparência visualmente atraente. O layout efetivo pode fazer a diferença entre os designs que os usuários entendem imediatamente e aqueles que deixam os usuários se sentirem um quebra-cabeça e sobrecarregados.

**Observação:** As diretrizes relacionadas ao [Gerenciamento de janelas](win-window-mgt.md) são apresentadas em um artigo separado. O dimensionamento e o espaçamento de controle específico recomendados são apresentados em seus respectivos artigos de diretriz.

## <a name="design-concepts"></a>Conceitos de design

### <a name="visual-hierarchy"></a>Hierarquia visual

Uma janela ou página tem uma hierarquia visual clara quando sua aparência indica a relação e a prioridade de seus elementos. Sem uma hierarquia visual, os usuários teriam que descobrir essas relações e prioridades.

A hierarquia visual é obtida por skillfully combinando os seguintes atributos:

-   **Foca.** O layout indica onde os usuários precisam procurar primeiro.
-   **Fluxo.** O olho flui suavemente e naturalmente por um caminho claro por meio da superfície, Localizando elementos da interface do usuário na ordem apropriada para seu uso.
-   **Agrupamento.** Elementos de interface do usuário relacionados logicamente têm uma relação visual clara. Itens relacionados são agrupados; itens não relacionados são separados.
-   **Ênfase.** Elementos de interface do usuário são enfatizados com base em sua importância relativa.
-   **Sintonia.** Os elementos da interface do usuário têm posicionamento coordenado e, portanto, são fáceis de verificar e aparecem ordenalmente.

Além disso, o layout efetivo tem estes atributos:

-   **Independência de dispositivo.** O layout aparece como pretendido, independentemente do tipo de fonte ou tamanho, pontos por polegada (DPI), exibição ou adaptador gráfico.
-   **Fácil de examinar.** Os usuários podem encontrar o conteúdo que estão procurando em um relance.
-   **Redução.** Elementos de interface do usuário que são grandes que precisam ser grandes, e os elementos que são muito pequenos funcionam.
-   **Capacidade.** Se for útil, uma janela será redimensionável e seu layout de conteúdo ficará efetivo, independentemente de quão grande ou pequena for a superfície.
-   **Lance.** O conteúdo aparece uniformemente distribuído pela superfície.
-   **Simplicidade Visual.** A percepção de que um layout não é mais complicado do que precisa ser. Os usuários não se sentem sobrecarregados com a aparência do layout.
-   **Verificação.** Janelas semelhantes ou páginas usam um layout semelhante, para que os usuários sempre se sintam orientados.

Embora o dimensionamento, o espaçamento e o posicionamento sejam conceitos simples, o desafio com layout é atingir a combinação certa desses atributos.

No Windows, o layout é comunicado usando métricas independentes de dispositivo, como DLUs (unidades de caixa de diálogo) e pixels relativos.

### <a name="a-design-model-for-reading"></a>Um modelo de design para leitura

**Os usuários escolhem o que eles lêem pela aparência e organização do conteúdo.** Para criar um layout eficaz, você precisará entender o que os usuários tendem a ler e por quê.

Você pode tomar decisões de layout usando este modelo de design para leitura:

-   As pessoas lidam em uma ordem da esquerda para a direita, de cima para baixo (em culturas ocidentais).
-   Há dois modos de leitura: leitura e verificação de imersão. A meta da leitura de imersão é a compreensão.

    ![figura da seta vermelha no padrão de leitura ziguezague ](images/vis-layout-image1.png)

    Este diagrama modela leitura imersiva.

    Por outro lado, o objetivo da verificação é localizar coisas. O caminho de verificação geral tem esta aparência:

    ![figura da seta vermelha no padrão de leitura diagonal ](images/vis-layout-image2.png)

    Este diagrama analisa os modelos.

    ![figura da seta vermelha em um padrão inferior e de arco ](images/vis-layout-image3.png)

    Se houver texto em execução ao longo da borda esquerda de uma página, os usuários verificarão a borda esquerda primeiro.

-   Ao usar o software, os usuários não estão imersos na própria interface do usuário, mas em seu trabalho. Consequentemente, os usuários geralmente não lêem o texto da interface do usuário que o examinam. Em seguida, eles lêem o texto de forma abrangente apenas quando eles acreditam que precisam.
-   Os usuários tendem a ignorar os painéis de navegação no lado esquerdo ou direito de uma página. Os usuários reconhecem que estão lá, mas examinam os painéis de navegação somente quando desejam navegar.
-   Os usuários tendem a ignorar grandes blocos de texto não formatado sem lê-los.

    ![figura do texto com setas mostrando texto de verificação ](images/vis-layout-image4.png)

    Os usuários tendem a ignorar grandes blocos de texto e painéis de navegação quando digitalizam.

-   Todas as coisas sendo iguais, os usuários primeiro examinam no canto superior esquerdo de uma janela, verificam na página e encerram sua verificação no canto inferior direito. Eles tendem a ignorar o canto inferior esquerdo.

    ![Figura de página e esquerda superior para seta inferior direita ](images/vis-layout-image5.png)

    Todas as coisas sendo iguais, os usuários lerá esses números na seguinte ordem: 1, 2, 4 e 3.

-   Mas, na interface do usuário interativa, nem todas as coisas são iguais, de forma que elementos de interface do usuário diferentes recebam diferentes níveis de atenção. Os usuários tendem a examinar controles interativos especialmente controles no canto superior esquerdo e no centro da janela e texto proeminente primeiro.

![Figura de tela com texto nítido e borrado ](images/vis-layout-image6.png)

Os usuários se concentram nos principais controles interativos e na principal instrução proeminente e examinam outras coisas apenas quando precisam.

-   Os usuários tendem a ler rótulos de controle interativos, especialmente aqueles que parecem relevantes para concluir a tarefa em questão. Por outro lado, os usuários tendem a ler texto estático apenas quando acham que precisam.
-   Itens que parecem uma atenção de atraição diferente. O texto em negrito e o texto grande se destacam do texto normal. Itens da interface do usuário com cor ou em um plano de fundo colorido. Itens com ícones se destacam de itens sem ícones.
-   Os usuários não rolam, a menos que tenham um motivo para. Se o conteúdo [acima da dobra](glossary.md) não fornecer um motivo para rolar, eles não vão.
-   Depois que os usuários decidirem o que fazer, eles imediatamente interromperão a verificação e o farão.
-   Como os usuários param de verificar quando acham que são concluídos, eles tendem a ignorar qualquer coisa além do que parece ser o ponto de conclusão.

![captura de tela das opções de teclado ](images/vis-layout-image7.png)

Os usuários param de verificar quando acham que estão prontos.

É claro que haverá exceções para esse modelo geral. Dispositivos de acompanhamento ocular indicam que o comportamento real dos usuários é bastante irregular. O objetivo desse modelo é ajudá-lo a tomar boas decisões e compensações, não para modelar o comportamento do usuário com precisão. Mas, como você leu esta lista, espero que também tenha reconhecido muitos dos seus próprios padrões de leitura.

### <a name="designing-for-scanning"></a>Criando para verificação

**Os usuários não lêem, eles verificam se você deve criar superfícies de interface do usuário para verificação.** Não presuma que os usuários lerám o texto como escrito em ordem da esquerda para a direita e de cima para baixo, mas sim que examinam os elementos da interface do usuário que atraiem sua atenção.

Para criar para verificação:

-   Suponha que os usuários comecem verificando rapidamente toda a janela e, em seguida, lendo os elementos da interface do usuário em aproximadamente a seguinte ordem:
    -   Controles interativos no centro
    -   Os botões de confirmação
    -   Controles interativos encontrados em outro lugar
    -   Instrução principal
    -   Explicações suplementares
    -   Texto apresentado com um ícone de aviso
    -   Título da janela
    -   Outro texto estático no corpo principal
    -   Notas de rodapé
-   Coloque os elementos da interface do usuário que iniciam uma tarefa no canto superior esquerdo ou no centro superior.
-   Coloque os elementos da interface do usuário que concluem uma tarefa no canto inferior direito.
-   Sempre que possível, coloque texto crucial em controles interativos em vez de texto estático.
-   Evite colocar informações cruciais no canto inferior esquerdo ou na parte inferior de um controle ou página rolável longo.
-   Não apresente grandes blocos de texto. Elimine o texto desnecessário. Use o estilo de apresentação da [pirâmide invertida](text-ui.md) .
-   Se você fizer algo para atrair a atenção dos usuários, certifique-se de que a atenção seja garantida.

Sempre que possível, trabalhe com esse modelo em vez de combater; Mas haverá ocasiões em que você precisa enfatizar ou realçar elementos específicos da interface do usuário.

Para enfatizar os principais elementos da interface do usuário:

-   Coloque os elementos principais da interface do usuário no [caminho de verificação](glossary.md).
-   Coloque qualquer interface do usuário para iniciar uma tarefa no canto superior esquerdo ou no centro superior.
-   Coloque os botões de confirmação no canto inferior direito.
-   Coloque a interface do usuário principal restante no centro.
-   Use controles que atraiam atenção, como botões de comando, links de comando e ícones.
-   Use texto em destaque, incluindo texto grande e texto em negrito.
-   Colocar texto os usuários devem ler em controles interativos ou com ícones ou em [faixas](vis-graphic.md).
-   Use texto escuro em um plano de fundo claro.
-   Coloque os elementos com espaço generosa.
-   Não exija nenhuma interação, como apontar ou focalizar, para ver o elemento que você está enfatizando.

    ![captura de tela das opções de ativação do Windows ](images/vis-layout-image8.png)

    Este exemplo mostra muitas maneiras de enfatizar os principais elementos da interface do usuário.

Para realçar elementos da interface do usuário secundária:

-   Coloque os elementos da interface do usuário secundária fora do caminho de verificação.
-   Coloque qualquer coisa que os usuários normalmente não precisem ver no canto inferior esquerdo ou inferior da janela.
-   Use controles que não atraiam atenção, como links de tarefas em vez de botões de comando.
-   Use texto normal ou cinza.
-   Use texto claro em um plano de fundo escuro. O texto branco em um plano de fundo cinza escuro ou azul funciona bem.
-   Coloque os elementos com espaço mínimo.
-   Considere usar a [divulgação progressiva](ctrl-progressive-disclosure-controls.md) para ocultar elementos de interface do usuário secundários.

    ![captura de tela de elementos de interface grandes e pequenos ](images/vis-layout-image9.png)

    Este exemplo mostra muitas maneiras de realçar elementos de interface do usuário secundários.

### <a name="using-screen-space-effectively"></a>Usando o espaço da tela com eficiência

O uso eficiente de espaço na tela exige que você equilibre vários fatores: Use um número excessivo de espaço e uma janela seja pesada e inútil, e até mesmo difícil de usar com base na [lei de Fitts](inter-mouse.md).

**Incorreto:**

![captura de tela mostrando muito espaço em branco ](images/vis-layout-image10.png)

Neste exemplo, a janela é muito grande para seu conteúdo.

Por outro lado, use um pouco de espaço e uma janela se sentirá cramped, desconfortável e intimidante, e difícil de usar se exigir rolagem e outras manipulações a serem usadas.

**Incorreto:**

![captura de tela com muitos controles ](images/vis-layout-image11.png)

Neste exemplo, a janela é muito pequena para seu conteúdo.

Embora a interface do usuário crítica deva se ajustar à [resolução efetiva](glossary.md)mínima com suporte, não assuma que o uso do espaço da tela com eficiência significa que o Windows deve ser tão pequeno quanto possível. **O layout efetivo tem relação com o espaço aberto e não tenta cram tudo no menor espaço possível.** Os monitores modernos têm um espaço de tela significativo e faz sentido usar esse espaço com eficiência quando possível. Consequentemente, Err no lado de usar muito espaço na tela em vez de muito pouco. Fazer isso faz com que suas janelas se sintam mais claras e mais abordáveis.

Você sabe que um layout está usando espaço na tela com eficiência quando:

-   Janelas, painéis de janelas e controles não precisam ser redimensionados para serem utilizáveis. Se a primeira coisa que os usuários fazem é redimensionar uma janela, painel ou controle, seu tamanho está errado.
-   Os dados não estão truncados. A maioria dos dados nas exibições de lista e em árvore não tem reticências e os dados em outros controles não são recortados, a menos que o comprimento dos dados seja incomum demais. Os dados que devem ser lidos para executar uma tarefa não devem ser truncados.
-   As janelas e os controles são dimensionados adequadamente para eliminar a rolagem desnecessária. Há poucas barras de rolagem horizontais e nenhuma barra de rolagem vertical desnecessária.
-   Os controles usam principalmente seus tamanhos padrão. Busque para reduzir o número de tamanhos de controle, por exemplo, usando apenas uma ou duas larguras de botão de comando em uma superfície.
-   A superfície da interface do usuário é equilibrada. Não há áreas de tela grandes não utilizadas.

Escolha tamanhos de janela que sejam muito grandes o suficiente para atender bem às suas finalidades. (E se a janela for redimensionável, essa meta se aplicará ao seu tamanho padrão.) **Uma combinação de dados truncados ou barras de rolagem e muito espaço na tela disponível é um sinal claro de layout ineficaz.**

### <a name="control-sizing"></a>Dimensionamento de controle

Normalmente, a primeira etapa para usar o espaço da tela com eficiência é determinar o tamanho certo para os vários elementos da interface do usuário. Consulte a [tabela de dimensionamento de controles](#recommended-sizing-and-spacing) , bem como o dimensionamento recomendado nos artigos específicos de diretrizes de controle.

A lei Fitts diz que o menor destino é, quanto mais tempo leva para adquiri-lo com o mouse. Além disso, para computadores que usam a tecnologia Tablet e Touch do Windows, o "mouse" pode, na verdade, ser uma caneta ou o dedo do usuário, portanto, você deve considerar dispositivos de entrada alternativos ao determinar tamanhos para pequenos controles. **Um tamanho de controle de 16 pixels relativos é um bom tamanho mínimo para qualquer dispositivo de entrada.** Por outro lado, os botões de controle de giro de pixel 15x9 padrão são muito pequenos para serem usados com eficiência pelas canetas.

### <a name="spacing"></a>Espaçamento

Fornecer espaço generosa (mas não excessivo) faz com que o layout fique mais confortável e mais fácil de analisar. O espaço efetivo não é um espaço não utilizado, ele desempenha um papel importante no aprimoramento da capacidade de verificação dos usuários e também do acréscimo à aparência visual do design. Para obter diretrizes, consulte a [tabela de espaçamento](#recommended-sizing-and-spacing).

Para computadores que usam a tecnologia Tablet e Touch do Windows, o "mouse", na verdade, pode ser uma caneta ou o dedo do usuário. O direcionamento é mais difícil ao usar uma caneta ou um dedo como o dispositivo apontador, fazendo com que os usuários toquem fora do destino pretendido. Quando os controles interativos são colocados muito próximos, mas não estão realmente em contato, os usuários podem clicar no espaço inativo entre os controles. Como clicar em espaço inativo não tem nenhum resultado ou comentário visual, geralmente os usuários não têm certeza do que deu errado. Se pequenos controles tiverem um espaço muito grande, o usuário precisará tocar com precisão para evitar tocar no objeto errado. **Para resolver esses problemas, as regiões de destino dos controles interativos devem ser tocadas ou ter pelo menos 3 DLUs (5 pixels relativos) de espaço entre eles.**

Você sabe que um layout tem um bom espaçamento quando:

-   Em geral, a superfície da interface do usuário se sente confortável e não se sente cramped.
-   O espaço aparece uniforme e equilibrado.
-   Os elementos relacionados estão próximos e os elementos não relacionados são relativamente distantes.
-   Não há nenhum espaço inativo entre os controles que devem estar juntos, como botões da barra de ferramentas.

### <a name="resizable-windows"></a>Janelas redimensionáveis

Janelas redimensionáveis também são um fator no uso eficiente do espaço da tela. Algumas janelas consistem em conteúdo fixo e não se beneficiam de serem redimensionáveis, mas o Windows com conteúdo redimensionável deve ser redimensionável. É claro que o motivo pelo qual os usuários redimensionam uma janela é tomar uma medida avançada do espaço adicional da tela, de modo que o conteúdo deve ser expandido de acordo com o fornecimento de mais espaço aos elementos da interface do usuário que precisam dela. O Windows com conteúdo dinâmico, documentos, imagens, listas e árvores beneficiam-se mais do que as janelas redimensionáveis.

![captura de tela de controle redimensionado ao obter a barra de rolagem ](images/vis-layout-image12.png)

Neste exemplo, redimensionar a janela redimensiona o controle de exibição de lista.

Dito isso, o Windows pode ser ampliado demais. Por exemplo, muitas páginas do painel de controle se tornam difíceis quando o conteúdo é mais largo do que 600 pixels relativos. Nesse caso, é melhor não redimensionar a área de conteúdo além dessa largura máxima ou alterar a origem do conteúdo à medida que a janela é mais redimensionada. Em vez disso, mantenha uma largura máxima e uma origem da parte superior esquerda fixa.

O texto se torna difícil de ler à medida que o comprimento da linha aumenta. Para documentos de texto, considere um comprimento máximo de linha de 80 caracteres para facilitar a leitura do texto. (Os caracteres incluem letras, pontuação e espaços.)

**Incorreto:**

![captura de tela da caixa de mensagem larga com texto longo ](images/vis-layout-image13.png)

Neste exemplo, o comprimento de texto longo torna a leitura difícil.

Por fim, as janelas redimensionáveis também precisam usar o espaço de tela com eficiência quando tornam-se menores, tornando o conteúdo redimensionável menor e removendo o espaço dos elementos da interface do usuário que podem funcionar com eficiência sem ele. Em algum momento, a janela ou seus elementos da interface do usuário se tornam muito pequenos para serem utilizáveis e, portanto, devem receber um tamanho mínimo ou alguns elementos devem ser removidos completamente.

![captura de tela de janela com faixa de uma de altura e invasiva ](images/vis-layout-image14.png)

![captura de tela da janela sem faixa de uma ](images/vis-layout-image15.png)

Neste exemplo, o painel tem um tamanho mínimo.

Alguns programas se beneficiam do uso de uma apresentação completamente diferente para tornar o conteúdo utilizável em tamanhos menores.

![captura de tela dos botões do Media Player centralizado ](images/vis-layout-image16.png)

Neste exemplo, o Windows Media Player altera seu formato quando a janela se torna muito pequena para o formato padrão.

### <a name="focus"></a>Foco

Um layout tem o foco quando há um local óbvio a ser examinado primeiro. O foco é importante para mostrar aos usuários onde começar a verificar sua janela ou página. Sem o foco claro, o olho do usuário fará o aimlessly. O ponto focal deve ser algo importante que os usuários precisam encontrar e entender rapidamente e devem ter a maior ênfase Visual. O canto superior esquerdo é o ponto focal natural para a maioria das janelas.

Deve haver apenas um ponto focal. Assim como na vida real, os olhos podem se concentrar apenas em uma coisa de cada vez, os usuários não podem se concentrar em vários locais simultaneamente.

Para tornar um elemento de interface do usuário o ponto focal, você pode dar ênfase visual a ele:

-   Colocando-o na parte superior esquerda ou no centro superior da superfície.
-   Usando controles interativos que são importantes e prontamente abrangentes.
-   Usando texto proeminente, como uma instrução principal.
-   Dando à seleção padrão de controles e ao foco de entrada inicial.
-   Colocando os controles em um plano de fundo colorido diferente.

Considere o Windows Search. O ponto focal do Windows Search deve ser a caixa de pesquisa porque é o ponto de partida para a tarefa. No entanto, ele está localizado no canto superior direito para ser consistente com o posicionamento da caixa de pesquisa padrão. A caixa de pesquisa tem o foco de entrada, mas, considerando seu local no caminho de verificação, essa pista sozinha não é suficiente.

Para resolver esse problema, há uma instrução proeminente na parte superior central da janela para direcionar os usuários para o local certo.

**Aceitável:**

![captura de tela da caixa de diálogo Pesquisar com texto útil ](images/vis-layout-image17.png)

Neste exemplo, uma instrução proeminente na parte superior central da janela direciona os usuários para a caixa de pesquisa.

Sem as instruções, a janela não teria um ponto focal óbvio.

**Incorreto:**

![captura de tela da caixa de diálogo Pesquisar sem texto ](images/vis-layout-image18.png)

Este exemplo não tem nenhum ponto focal claro. Os usuários não sabem onde procurar.

Se você fornecer ênfase visual ao elemento da interface do usuário, certifique-se de que a atenção seja garantida. No exemplo de pesquisa do Windows anterior incorreto, o botão tudo realçado está no canto superior esquerdo e tem a ênfase mais visual, mas não é o ponto focal pretendido. Os usuários podem ficar presos olhando esse botão tentando descobrir o que fazer com ele.

**Incorreto:**

![captura de tela do botão tudo realçado ](images/vis-layout-image19.png)

Sem a instrução proeminente como o ponto focal, o botão realçado All é um ponto focal não intencional.

### <a name="flow"></a>Fluxo

Um layout tem fluxo quando os usuários são guiados suavemente e naturalmente por um caminho claro por meio de sua superfície, Localizando elementos da interface do usuário na ordem apropriada para seu uso. Depois que os usuários identificam o ponto focal, eles precisam determinar como concluir a tarefa. O posicionamento dos elementos da interface do usuário transmite sua relação e deve espelhar as etapas para executar a tarefa. Normalmente, isso significa que as etapas da tarefa devem fluir naturalmente em uma ordem da esquerda para a direita, de cima para baixo (em culturas ocidentais).

Você sabe que um layout tem um bom fluxo quando:

-   O posicionamento dos elementos da interface do usuário espelha as etapas que os usuários precisam para executar a tarefa.
-   Os elementos da interface do usuário que iniciam uma tarefa estão no canto superior esquerdo ou no centro superior.
-   Os elementos da interface do usuário que concluem uma tarefa estão no canto inferior direito.
-   Os elementos relacionados da interface do usuário estão juntos; elementos não relacionados são separados.
-   As etapas necessárias estão no fluxo principal.
-   As etapas opcionais estão fora do fluxo principal, possivelmente realçadas com o uso de um plano de fundo adequado ou divulgação progressiva.
-   Os elementos usados com frequência aparecem antes dos elementos usados com pouca frequência no caminho de verificação.
-   Os usuários sempre sabem o que fazer em seguida. Não há saltos ou quebras inesperados no fluxo de tarefas.

**Incorreto:**

![captura de tela do layout de caixa de diálogo confuso ](images/vis-layout-image20.png)

Neste exemplo, os usuários não sabem o que fazer em seguida. Há saltos inesperados e quebras no fluxo de tarefas.

**Correto:**

![captura de tela de uma caixa de diálogo bem planejada ](images/vis-layout-image21.png)

Neste exemplo, a apresentação dos elementos da interface do usuário espelha as etapas para executar a tarefa.

### <a name="grouping"></a>Agrupamento

Um layout tem agrupamento quando elementos da interface do usuário relacionados logicamente têm uma relação visual clara. Os grupos são importantes porque é mais fácil para os usuários entenderem e se concentrarem em um grupo de itens relacionados do que os itens individualmente. Os grupos fazem com que um layout pareça mais simples e fácil de analisar.

Você pode mostrar o agrupamento das seguintes maneiras (em maior pesado):

-   **Layout.** Você pode agrupar controles relacionados ao lado um do outro e colocar o espaçamento adicional entre controles não relacionados.

    ![Figura de quatro ícones mostrando quatro grupos de tarefas ](images/vis-layout-image22.png)

    Neste exemplo, layout sozinho é usado para mostrar relações de controle.

-   **Separadores.** Um separador é uma linha horizontal ou vertical que unifica um grupo de controles. Os separadores fornecem uma aparência mais simples e limpa. No entanto, ao contrário das caixas de grupo, elas funcionam melhor quando abrangem toda a superfície.

    ![captura de tela de três ícones e três separadores ](images/vis-layout-image23.png)

    Neste exemplo, os separadores rotulados são usados para mostrar relações de controle.

-   **Agregadores.** Um agregador é um gráfico que cria uma relação visual entre controles fortemente relacionados.

    ![captura de tela de controles dentro de uma linha elíptica ](images/vis-layout-image24.png)

    Neste exemplo, um agregador de limite é usado para enfatizar a relação entre os controles e fazer com que eles se sintam como um único controle em vez de oito.

-   **Caixas de grupo.** Uma caixa de grupo é um quadro retangular rotulado que circunda um conjunto de controles relacionados.

    ![captura de tela de caixas de seleção em uma borda Retangular ](images/vis-layout-image25.png)

    Neste exemplo, uma caixa de grupo circunda e rotula um conjunto de controles relacionados.

-   **Plano.** Você pode usar planos de fundo para enfatizar ou realçar diferentes tipos de conteúdo.

    ![captura de tela do lado esquerdo do painel de controle ](images/vis-layout-image26.png)

    Neste exemplo, o painel de tarefas painel de controle é usado para agrupar tarefas relacionadas e itens do painel de controle.

    Para evitar a desordem Visual, o agrupamento de peso mais leve que faz o trabalho bem é a melhor opção. Para obter mais informações, consulte [caixas de grupo](ctrl-group-boxes.md), [guias](ctrl-tabs.md), [separadores e planos de fundo](vis-graphic.md).

Independentemente do estilo de agrupamento, você pode usar recuo para mostrar a relação dos controles dentro de um grupo. Os controles que são pares entre si devem ser alinhados à esquerda e os controles dependentes são recuados 12 DLUs ou 18 pixels relativos.

![captura de tela de três níveis de controles recuados ](images/vis-layout-image27.png)

Os controles dependentes são recuados 12 DLUS ou 18 pixels relativos, que por design é a distância entre as caixas de seleção e os botões de opção de seus rótulos.

Você sabe que um layout tem um bom agrupamento quando:

-   A janela ou as páginas têm no máximo 7 grupos.
-   A finalidade de cada grupo é óbvia.
-   A relação dos controles dentro de cada grupo é óbvia, especialmente a dependência do controle.
-   O agrupamento simplifica o conteúdo em vez de torná-lo mais complexo.

### <a name="alignment"></a>Alinhamento

O alinhamento é o posicionamento coordenado dos elementos da interface do usuário. O alinhamento é importante porque torna o conteúdo mais fácil de examinar e afeta a percepção dos usuários da complexidade visual.

Há várias metas a serem consideradas ao determinar o alinhamento:

-   **Facilidade na verificação horizontal.** Os usuários podem ler horizontalmente e localizar itens relacionados ao lado um do outro, sem nenhuma lacuna estranha.
-   **Facilidade na verificação vertical.** Os usuários podem verificar colunas de itens relacionados e encontrar imediatamente o que estão procurando, com movimento de olho horizontal mínimo.
-   **Complexidade visual mínima.** Os usuários percebem que um layout é visualmente complexo se ele tiver linhas de grade de alinhamento vertical desnecessárias.

### <a name="horizontal-alignment"></a>Alinhamento horizontal

**Alinhamento à esquerda**

Devido à ordem de leitura da esquerda para a direita, o alinhamento à esquerda funciona bem para a maior parte do conteúdo. O alinhamento à esquerda torna os dados de coluna fáceis de serem verificados verticalmente.

**Alinhamento à direita**

O alinhamento à direita é a melhor opção para dados numéricos, especialmente [colunas de dados numéricos](ctrl-text-boxes.md). O alinhamento à direita também funciona bem para [botões de confirmação](glossary.md) , bem como controles alinhados com a borda direita da janela.

![captura de tela da pesquisa avançada botão de seta para baixo ](images/vis-layout-image28.png)

Neste exemplo, o controle de divulgação progressiva de pesquisa avançada está alinhado à direita porque ele é colocado na borda da janela direita.

**Alinhamento centralizado**

O alinhamento de centro é melhor reservado para situações em que o alinhamento à esquerda ou à direita é inadequado ou aparece desbalanceado.

![captura de tela dos controles do player de mídia centralizado ](images/vis-layout-image29.png)

Neste exemplo, o controle do Media Player é centralizado para dar uma aparência equilibrada.

Não Centralize o conteúdo da janela apenas para preencher o espaço.

**Incorreto:**

![captura de tela de uma janela com muito espaço em branco ](images/vis-layout-image30.png)

Neste exemplo, o conteúdo está incorretamente centralizado em uma janela redimensionável para preencher o espaço.

### <a name="vertical-alignment"></a>Alinhamento vertical

**Elemento tops**

Devido à ordem de leitura de cima para baixo, o alinhamento superior funciona bem para a maior parte do conteúdo. O alinhamento superior torna os elementos da interface do usuário fáceis de verificar horizontalmente.

**Linhas de base de texto**

Ao alinhar verticalmente controles com texto, alinhe as linhas de base de texto para dar um fluxo de leitura horizontal suave.

**Correto:**

![captura de tela do texto do botão e do rótulo alinhado ](images/vis-layout-image31.png)

**Incorreto:**

![captura de tela de texto de botão e rótulo não alinhado ](images/vis-layout-image32.png)

No exemplo correto, o controle e seu rótulo são alinhados verticalmente por suas linhas de base de texto.

Você sabe que um layout tem um bom alinhamento quando:

-   É fácil verificar horizontalmente e verticalmente.
-   Ele tem uma aparência visual simples.

### <a name="label-alignment"></a>Alinhamento de rótulo

As regras de alinhamento geral se aplicam a rótulos de controle, mas é um problema comum digno de atenção específica. O alinhamento do rótulo tem estes objetivos:

-   Facilidade na verificação vertical para localizar o controle certo.
-   Facilitar a verificação horizontal para associar rótulos a seus controles.
-   Facilidade na localização, manipulação de rótulos que diferem no comprimento entre os idiomas.
-   Funciona bem com uma mistura de comprimentos de rótulo diferentes.
-   Faz uso eficiente do espaço disponível ao mesmo tempo em que evita texto truncado.

O objetivo geral é reduzir a quantidade de movimento de olho necessário para encontrar o que os usuários estão procurando, mas a natureza dos controles e do que os usuários estão procurando depende do contexto.

Há quatro estilos de posicionamento e alinhamento de rótulo comum, cada um com seus benefícios:

-   Rótulos justificados à esquerda acima dos controles
-   Rótulos justificados à esquerda à esquerda dos controles
-   Rótulos justificados à esquerda à esquerda dos controles, controles desalinhados à esquerda
-   Rótulos justificados à direita à esquerda dos controles

**Rótulos justificados à esquerda acima dos controles**

Esse estilo é o mais fácil de localizar porque o layout não depende do comprimento dos rótulos, mas usa o espaço mais vertical.

![lista com duas colunas de rótulos acima dos controles ](images/vis-layout-image33.png)

Esse estilo usa o espaço mais vertical, mas é mais fácil de localizar. É uma opção melhor para rotular controles interativos em grande parte.

Melhor usado quando:

-   Os controles que estão sendo rotulados são interativos (não apenas texto).
-   A interface do usuário será localizada. Esse estilo geralmente proporciona espaço para dobrar ou até mesmo triplo do comprimento do rótulo.
-   A interface do usuário está usando uma tecnologia de layout fixo (como Win32).
-   Há dez ou menos controles. Com mais controles, os rótulos são difíceis de verificar.
-   Há espaço vertical suficiente para acomodar os rótulos.
-   O layout precisa ser um formato livre, não apenas colunas.

**Rótulos justificados à esquerda à esquerda dos controles**

Esse estilo é o mais fácil de digitalizar verticalmente e também funciona bem quando os rótulos diferem muito em comprimento, mas é mais difícil associar o rótulo a seu controle. Esse estilo pode usar rótulos de várias linhas, se necessário.

![lista com quatro colunas de rótulos à esquerda dos controles ](images/vis-layout-image34.png)

Esse estilo funciona bem. No entanto, há duas colunas, mas visualmente parece que há quatro fazendo com que os dados pareçam mais complexos.

Melhor usado quando:

-   É provável que os usuários verifiquem verticalmente para localizar rótulos específicos.
-   Os usuários provavelmente não lêem os rótulos e controles de uma maneira da esquerda para a direita, de cima para baixo.
-   Há espaço horizontal suficiente para acomodar os rótulos.
-   Os rótulos variam significativamente em comprimento.
-   Há muitos controles, como com formulários.
-   Há poucas colunas. Visualmente, os rótulos e os controles aparecem como duas colunas individuais.

**Rótulos justificados à esquerda à esquerda dos controles, controles desalinhados à esquerda**

Esse estilo facilita a verificação dos rótulos verticalmente e os rótulos e controles horizontalmente, além de ser muito eficiente em termos de espaço; Mas é mais difícil verificar os controles verticalmente. Os controles são justificados à direita para aproveitar ao máximo o espaço disponível.

![lista de duas colunas de rótulos com controles irregulares ](images/vis-layout-image35.png)

Esse estilo é compacto e fácil de ler, mas é difícil verificar os controles verticalmente.

Melhor usado quando:

-   A interface do usuário está usando uma tecnologia de layout variável (como Windows Presentation Foundation).
-   É provável que os usuários verifiquem verticalmente para localizar rótulos específicos.
-   É provável que os usuários leiam os rótulos e controles de uma maneira da esquerda para a direita, de cima para baixo.
-   Não é provável que os usuários verifiquem os controles verticalmente.
-   O texto de controle varia de comprimento e provavelmente seria truncado se outro estilo fosse usado.
-   Os controles são somente leitura, como caixas de texto somente leitura. Para outros controles, esse alinhamento parecerá impreciso. No entanto, os controles podem se tornar editáveis ao clicar em.
-   Há muitas colunas, mas poucos controles em uma coluna.

**Rótulos justificados à direita à esquerda dos controles**

Esse estilo é o mais fácil de ler horizontalmente para associar os rótulos aos seus controles, mas é difícil digitalizar os rótulos verticalmente e não funciona bem quando os rótulos com rótulos recuados e controles diferem muito no comprimento.

![lista com rótulos e controles recuados ](images/vis-layout-image36.png)

Esse estilo permite uma verificação vertical fácil dos controles, mas torna difícil digitalizar os rótulos verticalmente.

Melhor usado quando:

-   É provável que os usuários leiam os rótulos e controles de uma maneira da esquerda para a direita, de cima para baixo.
-   Os usuários provavelmente não serão examinados verticalmente para localizar rótulos específicos, possivelmente porque:
    -   Há poucos controles.
    -   Os rótulos são bem conhecidos.
    -   Os controles são basicamente auto-explicativos e raramente estão em branco (possivelmente com valores padrão para evitar controles em branco).
-   Há espaço horizontal suficiente para acomodar os rótulos.
-   Os rótulos não variam significativamente em comprimento.
-   Houver muitas colunas. Visualmente, os rótulos e os controles aparecem como uma única coluna.

No entanto, antes de adotar qualquer um desses estilos, considere mais dois fatores:

-   Prefira um estilo que você possa usar consistentemente em seu programa.
-   Os rótulos justificados à esquerda acima dos controles à esquerda dos controles são os estilos mais comuns, portanto, eles devem receber preferência.

### <a name="balance"></a>Saldo

Uma janela ou página tem saldo quando seu conteúdo é distribuído uniformemente em sua superfície. Se a superfície fisicamente tivesse o mesmo peso que ela tem visualmente, um layout equilibrado não se interdicaria a um lado.

O problema de saldo mais comum é ter muito conteúdo no lado esquerdo de uma janela ou página. Você pode criar um equilíbrio das seguintes maneiras:

-   Usando margens maiores no lado esquerdo do que a direita.
-   Colocando elementos da interface do usuário usados para concluir uma tarefa à direita.
-   Colocando elementos da interface do usuário usados em toda a tarefa no centro.
-   Aumentando os controles redimensionáveis ou de várias linhas.
-   Usando o alinhamento centralizado estrategicamente.

![captura de tela da impressora à esquerda e texto à direita ](images/vis-layout-image37.png)

Esse layout de página de assistente bem equilibrado mostra uma margem esquerda maior do que o direito de melhorar o saldo.

Se essas técnicas não alcançarem o saldo, considere reduzir a largura da janela ou da página para corresponder melhor ao conteúdo.

Para superfícies redimensionáveis, não Centralize o conteúdo apenas para obter o saldo. Em vez disso, mantenha uma origem fixa superior à esquerda, defina uma área de superfície máxima e equilibre o conteúdo dentro do espaço usado.

### <a name="grids"></a>Grades

Uma grade é um sistema de alinhamento subjacente invisível. As grades podem ser simétricas, mas as grades assimétricas também funcionam tão bem. Quando usado por uma única janela ou página, as grades ajudam a organizar o conteúdo em uma superfície. Quando reutilizados, as grades criam layout consistente entre superfícies.

O número de linhas de grade afeta a percepção da complexidade visual. Um layout com menos linhas de grade aparece mais simples do que um layout com mais linhas de grade.

**Visualmente complexo:**

![captura de tela de caixa de diálogo desorganizada ](images/vis-layout-image38.png)

**Visualmente simples:**

![captura de tela da caixa de diálogo organizada ](images/vis-layout-image39.png)

Linhas de grade desnecessárias criam complexidade visual.

Você sabe que um layout está usando grades com eficiência quando:

-   Janelas ou páginas com conteúdo ou função semelhante têm layout semelhante.
-   Elementos de design repetidos aparecem em locais semelhantes entre janelas e páginas.
-   Não há nenhuma linha de grade de alinhamento vertical e horizontal desnecessária.

### <a name="visual-simplicity"></a>Simplicidade Visual

A simplicidade Visual é a percepção de que um layout não é mais complicado do que precisa ser.

Você sabe que um layout tem simplicidade visual quando:

-   Elimina as camadas desnecessárias do Chrome do Windows.
-   Apresenta o conteúdo usando, no máximo, sete grupos facilmente identificáveis.
-   Usa o agrupamento leve, como layout e separadores em vez de caixas de grupo.
-   Usa controles leves, como links em vez de botões de comando para comandos secundários e listas suspensas em vez de listas para escolhas.
-   Reduz o número de linhas de grade de alinhamento vertical e horizontal.
-   Reduz o número de tamanhos de controle, por exemplo, usando apenas uma ou duas larguras de botão de comando em uma superfície.
-   Usa a divulgação progressiva para ocultar elementos da interface do usuário até que eles sejam necessários.
-   Usa espaço suficiente para que a janela ou a página não se sinta cramped.
-   Dimensiona as janelas e os controles adequadamente para eliminar a rolagem desnecessária.
-   Usa uma única fonte com um número pequeno de tamanhos e cores de texto.

Como regra geral, se um elemento de layout puder ser eliminado sem prejudicar a eficácia da interface do usuário, provavelmente deverá ser.

## <a name="guidelines"></a>Diretrizes

### <a name="screen-resolution-and-dpi"></a>Resolução de tela e DPI

-   **Suporte à resolução mínima efetiva do Windows de 800x600 pixels.** Para as interfaces de trabalho críticas que devem funcionar no modo de segurança, dê suporte a uma resolução efetiva de 640x480 pixels. Certifique-se de considerar o espaço usado pela barra de tarefas reservando 48 [pixels relativos](glossary.md) verticais para o Windows exibido com a barra de tarefas.
-   **Otimize layouts de janela redimensionáveis para uma resolução efetiva de 1024x768 pixels.** Redimensione automaticamente essas janelas para resoluções de tela mais baixa de uma maneira que ainda está funcional.
-   **Certifique-se de testar suas janelas em 96 pontos por polegada (DPI) (em 800x600 pixels), 120 DPI (a 1024x768 pixels) e 144 DPI (em 1200x900 pixels).** Verifique se há problemas de layout, como recorte de controles, texto e janelas, e alargamento de ícones e bitmaps.
-   **Para programas com cenários de uso móvel e de toque, otimize para 120 dpi.** As telas de alto dpi atualmente são predominantes em PCs móveis e de toque.

### <a name="window-size"></a>Tamanho da janela

-   **Escolha um tamanho de janela padrão apropriado para seu conteúdo.** Não tenha medo de usar tamanhos de janela iniciais maiores se você puder usar o espaço com eficiência.
-   **Use uma altura balanceada para a taxa de proporção da largura.** Uma taxa de proporção entre 3:5 e 5:3 é preferida, embora uma taxa de proporção de 1:3 possa ser usada para caixas de diálogo de mensagem (como erros e avisos).
-   **Use janelas redimensionáveis sempre que for prático para evitar barras de rolagem e dados truncados.** O Windows com conteúdo dinâmico, documentos, imagens, listas e árvores beneficiam-se mais do que as janelas redimensionáveis.
-   **Para documentos de texto, considere um comprimento máximo de linha de 80 caracteres** para facilitar a leitura do texto. (Os caracteres incluem letras, pontuação e espaços.)
-   Janelas de tamanho fixo:
    -   **O Windows de tamanho fixo deve ser totalmente visível e dimensionado para se ajustar na área de trabalho.**
-   Janelas redimensionáveis:
    -   **Janelas redimensionáveis podem ser otimizadas para resoluções mais altas, mas são dimensionadas conforme necessário no momento da exibição para a resolução de tela real.**
    -   **Tamanhos de janelas progressivamente maiores devem mostrar progressivamente mais informações.** Certifique-se de que pelo menos uma parte da janela ou controle tenha conteúdo redimensionável.
    -   **Mantenha a origem superior esquerda do conteúdo fixo, pois a janela é redimensionada.** Não mova a origem para balancear o conteúdo conforme o tamanho da janela é alterado.
    -   **Defina um tamanho de conteúdo máximo se o conteúdo puder ser muito extenso demais.** Se o conteúdo se tornar difícil, não redimensione a área de conteúdo além de sua largura máxima ou altere a origem do conteúdo à medida que a janela for mais redimensionada. Em vez disso, mantenha uma largura máxima e uma origem da parte superior esquerda fixa.
    -   **Defina um tamanho mínimo de janela se houver um tamanho abaixo do qual o conteúdo não seja mais utilizável.** Para controles redimensionáveis, defina tamanhos mínimos de elemento redimensionáveis para seus menores tamanhos funcionais, como larguras de coluna funcionais mínimas em exibições de lista. Elementos de interface do usuário opcionais devem ser completamente removidos.
    -   **Considere alterar a apresentação para tornar o conteúdo utilizável em tamanhos menores.**

        ![captura de tela dos controles do Media Player ](images/vis-layout-image16.png)

        Neste exemplo, o Windows Media Player altera seu formato quando a janela se torna muito pequena para o formato padrão.

### <a name="control-size"></a>Tamanho do controle

-   **Torne todos os controles interativos pelo menos com 16 pixels relativos.** Fazer isso funciona bem para todos os dispositivos de entrada, incluindo tecnologia Windows Tablet e Touch.
-   **Controles de tamanho para evitar dados truncados.** Não truncar os dados que devem ser lidos para executar uma tarefa. Colunas de exibição de lista de tamanho para evitar dados truncados.
-   **Controles de tamanho para eliminar a rolagem desnecessária.** Tornar os controles ligeiramente maiores se isso eliminar uma barra de rolagem. Deve haver poucas barras de rolagem verticais e nenhuma barra de rolagem horizontal desnecessária.

    ![captura de tela da lista dimensionada para evitar uma barra de rolagem ](images/vis-layout-image40.png)

    Neste exemplo, a lista suspensa é dimensionada para eliminar a barra de rolagem.

-   **Reduza o número de tamanhos de controle em uma superfície.** Prefira usar os [tamanhos de controle recomendados padrão](#recommended-sizing-and-spacing) e, quando necessário, usar alguns controles maiores ou menores consistentemente. Tente usar uma única largura para caixas de listagem e exibições de árvore, e não mais do que três larguras para botões de comando e listas suspensas. No entanto, as larguras da caixa de texto e da caixa de combinação devem sugerir o comprimento de sua entrada mais longa ou esperada.

    ![captura de tela da caixa de diálogo com listas e botões ](images/vis-layout-image41.png)

    Neste exemplo, um tamanho de caixa de listagem e de botão de comando é usado de forma consistente.

-   **Para controles que são dimensionados com base em seu texto, inclua mais 30% (até 200 por cento para texto mais curto) para qualquer texto que será localizado.** Essa diretriz pressupõe que o layout é projetado usando texto em inglês. Observe também que essa diretriz se refere a texto localizado, não a números.
-   **Estenda controles de texto estáticos, caixas de seleção e botões de opção para a largura máxima que caberá no layout.** Isso evita o truncamento da localização e do texto de comprimento variável.

    **Incorreto:**

    ![captura de tela de controle de progresso e texto parcial ](images/vis-layout-image42.png)

    Neste exemplo, o texto de controle está desnecessariamente truncado.

### <a name="control-spacing"></a>Espaçamento de controle

-   **Se os controles não estiverem tocando, tenha pelo menos 3 DLUs (5 pixels relativos) de espaço entre eles.** Caso contrário, os usuários poderão clicar no espaço inativo entre os controles. Como clicar em espaço inativo não tem nenhum resultado ou comentário visual, geralmente os usuários não têm certeza do que deu errado.

### <a name="placement"></a>Posicionamento

-   **Organize os elementos da interface do usuário em uma superfície para fluir naturalmente em uma ordem da esquerda para a direita, de cima para baixo (em culturas ocidentais).** O posicionamento dos elementos da interface do usuário transmite sua relação e deve espelhar as etapas para executar a tarefa.
-   **Coloque os elementos da interface do usuário que iniciam uma tarefa no canto superior esquerdo ou no centro superior.** Forneça ao elemento da interface do usuário que os usuários devem examinar primeiro a melhor ênfase Visual.
-   **Coloque os elementos da interface do usuário que concluem uma tarefa no canto inferior direito.**
-   **Coloque elementos de interface do usuário relacionados juntos e separe elementos não relacionados.**
-   **Coloque as etapas necessárias no fluxo principal.**
-   **Coloque as etapas opcionais fora do fluxo principal,** possivelmente realçadas, usando um plano de fundo adequado ou uma divulgação progressiva.
-   **Coloque elementos usados com frequência antes de elementos usados com pouca frequência** no caminho de verificação.

### <a name="focus"></a>Foco

-   **Escolha um único elemento de interface do usuário que os usuários precisam examinar primeiro para ser o ponto focal.** O ponto focal deve ser algo importante que os usuários precisam encontrar e entender rapidamente.
-   **Coloque o ponto focal no canto superior esquerdo ou no centro superior.**
-   **Dê ao ponto focal a maior ênfase Visual,** como texto proeminente, seleção padrão ou foco de entrada inicial.

### <a name="alignment"></a>Alinhamento

-   Normalmente, use o alinhamento à esquerda.
-   Use o alinhamento à direita para dados numéricos, especialmente colunas de dados numéricos.
-   Use o alinhamento à direita para botões de confirmação, bem como controles alinhados com a borda direita da janela.
-   Use o alinhamento do centro quando o alinhamento esquerdo ou direito for inadequado ou parecer desbalanceado.
-   Ao alinhar verticalmente controles com texto, alinhe as linhas de base de texto para dar um fluxo de leitura horizontal suave.
-   Para alinhamento de rótulo, consulte a seção [alinhamento de rótulo](#label-alignment) em conceitos de design.

### <a name="accessibility"></a>Acessibilidade

-   **Não use o layout como o único meio para transmitir informações importantes sobre uma interface do usuário.** Os usuários que têm deficiências visuais podem não ser capazes de interpretar esta apresentação. Por exemplo, verifique se os rótulos de controles comunicam sua relação com outros itens.
-   **Não incorpore controles subordinados dentro de rótulos de controle para criar uma frase ou frase.** Essas associações são baseadas puramente no layout e não são bem tratadas por navegação por teclado ou tecnologias assistenciais de acessibilidade. Além disso, essa técnica não é localizável porque a estrutura da frase varia de acordo com a linguagem.

    **Incorreto:**

    ![captura de tela de uma caixa de texto no meio de uma sentença ](images/vis-layout-image43.png)

    Neste exemplo, a caixa de texto é colocada incorretamente dentro do rótulo da caixa de seleção.

    **Correto:**

    ![captura de tela de uma caixa de texto no final de uma sentença ](images/vis-layout-image44.png)

    Aqui, a caixa de texto é colocada após o rótulo da caixa de seleção.

-   **Torne o agrupamento acessível.** Os grupos definidos por painéis de janela, caixas de grupo, separadores, rótulos de texto e agregadores são tratados automaticamente por auxílios de acessibilidade. No entanto, os grupos definidos somente por posicionamento e planos de fundo não são e devem ser definidos programaticamente para acessibilidade.

Para obter mais diretrizes, consulte [acessibilidade](inter-accessibility.md).

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

**Dimensionamento de controle**

A tabela a seguir lista os tamanhos recomendados (largura x altura ou altura se um único número) para elementos comuns da interface do usuário (para 9 pt. Segoe UI a 96 DPI). As larguras com base no item mais longo em inglês adicionam 30 por cento para localização (até 200 por cento para texto mais curto) para qualquer texto (mas não números) que serão localizados.



|                                                                                                 |                            |                                                                                                   |                                                                                                            |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
|                                                                                                 | **Controle**<br/>     | **Unidades de diálogo**<br/>                                                                       | **Pixels relativos**<br/>                                                                             |
| ![captura de tela de caixas de seleção e seus rótulos ](images/vis-layout-image45.png)<br/>       | Caixas de seleção<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![captura de tela da caixa de combinação ](images/vis-layout-image46.png)<br/>                          | Caixas de combinação<br/>     | largura do item mais longo + 30% x 14<br/>                                                       | largura do item mais longo + 30% x 23<br/>                                                                |
| ![captura de tela de um botão de comando ](images/vis-layout-image47.png)<br/>                   | Botões de comando<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![captura de tela de um dos dois links de comando selecionados ](images/vis-layout-image48.png)<br/>  | Links de comando<br/>   | 25 (uma linha) ou 35 (duas linhas)<br/>                                                        | 41 (uma linha) ou 58 (duas linhas)<br/>                                                                 |
| ![captura de tela de uma lista suspensa ](images/vis-layout-image49.png)<br/>                   | Listas suspensas<br/> | largura dos dados válidos mais longos + 30% x 14<br/>                                                 | largura do item mais longo + 30% x 23<br/>                                                                |
| ![captura de tela de uma caixa de listagem ](images/vis-layout-image50.png)<br/>                         | Caixas de listagem<br/>      | largura do item mais longo + 30% x um número integral de itens (mínimo de 3 itens)<br/>            |                                                                                                            |
| ![captura de tela de uma lista de arquivos de imagem ](images/vis-layout-image51.png)<br/>            | Modos de exibição de lista<br/>      | larguras de colunas que evitam dados truncados x um número integral de itens<br/>                 |                                                                                                            |
| ![captura de tela de uma barra de progresso ](images/vis-layout-image52.png)<br/>                     | Barras de progresso<br/>   | 107 ou 237 x 8<br/>                                                                         | 160 ou 355 x 15<br/>                                                                                 |
| ![captura de tela de botões de opção ](images/vis-layout-image53.png)<br/>                      | Botões de opção<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![captura de tela do controle deslizante ](images/vis-layout-image54.png)<br/>                     | Controles deslizantes<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![captura de tela de texto: ' selecionar fuso horário ' ](images/vis-layout-image55.png)<br/>           | Texto (estático)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![captura de tela da caixa de texto vazia ](images/vis-layout-image56.png)<br/>                     | Caixas de texto<br/>      | largura da entrada mais longa ou esperada + 30% x 14 (uma linha) + 10 para cada linha adicional<br/> | largura de dados válidos mais longos + 30% x 23 pixels relativos (uma linha) + 16 para cada linha adicional<br/> |
| ![captura de tela de pastas aninhadas no Windows Explorer ](images/vis-layout-image57.png)<br/> | Modos de exibição de árvore<br/>      | largura do item mais longo + 30% x um número integral de itens (mínimo de 5 itens)<br/>            |                                                                                                            |



 

**Espaçamento**

A tabela a seguir lista o espaçamento recomendado entre os elementos comuns da interface do usuário (para o 9 pt. Segoe UI a 96 DPI).



|                                                                                                   |                                                                                                       |                                                                                           |                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
|                                                                                                   | **Element**<br/>                                                                                | **Unidades de diálogo**<br/>                                                               | **Pixels relativos**<br/>                                                            |
| ![Imagem mostrando o espaçamento nas margens da caixa de diálogo ](images/vis_layout_image58.jpeg)<br/>        | Margens da caixa de diálogo<br/>                                                                         | 7 em todos os lados<br/>                                                                 | 11 em todos os lados<br/>                                                                |
| ![Imagem mostrando o espaçamento entre rótulos e controles ](images/vis_layout_image59.jpeg)<br/>  | Entre rótulos de texto e seus controles associados (por exemplo, caixas de texto e caixas de listagem)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Imagem mostrando o espaçamento entre controles relacionados ](images/vis_layout_image60.jpeg)<br/>     | Entre controles relacionados<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagem mostrando o espaçamento entre controles não relacionados ](images/vis_layout_image61.jpeg)<br/>   | Entre controles não relacionados<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Imagem mostrando o espaçamento do primeiro controle em um grupo ](images/vis_layout_image62.jpeg)<br/>  | Primeiro controle em uma caixa de grupo<br/>                                                               | 11 abaixo da parte superior da caixa de grupo; alinhar verticalmente ao título da caixa de grupo<br/> | 16 para baixo na parte superior da caixa de grupo; alinhar verticalmente ao título da caixa de grupo<br/> |
| ![Aa511279. Between – related (en-US, MSDN. 10). jpg](images/vis_layout_image60.jpeg)<br/>         | Entre controles em uma caixa de grupo<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagem mostrando o espaçamento entre os botões ](images/vis_layout_image63.jpeg)<br/>              | Entre os botões organizados horizontal ou verticalmente<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Imagem mostrando o espaçamento do último controle em um grupo ](images/vis_layout_image64.jpeg)<br/>   | Último controle em uma caixa de grupo<br/>                                                                | 7 acima da parte inferior da caixa de grupo<br/>                                            | 11 acima da parte inferior da caixa de grupo<br/>                                           |
| ![Imagem mostrando o espaçamento da borda esquerda da caixa de grupo ](images/vis_layout_image65.jpeg)<br/>  | Na borda esquerda de uma caixa de grupo<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Imagem mostrando o espaçamento do rótulo de texto ao lado do controle ](images/vis_layout_image66.jpeg)<br/> | Rótulo de texto ao lado de um controle<br/>                                                                | 3 abaixo da parte superior do controle<br/>                                             | 5 a partir da parte superior do controle<br/>                                             |
| ![Imagem mostrando o espaçamento entre parágrafos de texto ](images/vis_layout_image67.jpeg)<br/>   | Entre parágrafos de texto<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Menor espaço entre controles interativos<br/>                                                | 3 ou nenhum espaço<br/>                                                                  | 5 ou sem espaço<br/>                                                                  |
|                                                                                                   | Menor espaço entre um controle não interativo e qualquer outro controle<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

