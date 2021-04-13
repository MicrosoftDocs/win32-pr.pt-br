---
title: Controles de divulgação progressiva
description: Com um controle de divulgação progressiva, os usuários podem mostrar ou ocultar informações adicionais, incluindo dados, opções ou comandos.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 22c74f60b3184f7fa7f7cdb2b4f2e9d9f64995ea
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297870"
---
# <a name="progressive-disclosure-controls"></a>Controles de divulgação progressiva

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um controle de divulgação progressiva, os usuários podem mostrar ou ocultar informações adicionais, incluindo dados, opções ou comandos. A divulgação progressiva promove a simplicidade concentrando-se no essencial, ainda revelando detalhes adicionais conforme necessário.

![captura de tela de controles de divulgação progressiva](images/progressive-disclosure-controls-image1.png)

Exemplos de controles de divulgação progressiva.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md), aos [menus](cmd-menus.md)e às [barras de ferramentas](cmd-toolbars.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **Os usuários precisam ver as informações em alguns, mas não em todos os cenários, ou alguns, mas não o tempo todo?** Nesse caso, a exibição das informações usando a divulgação progressiva simplifica a experiência de linha de base, mas permite que os usuários acessem as informações facilmente.

    ![Captura de tela que mostra a exibição do status da central de segurança.](images/progressive-disclosure-controls-image2.png)

    Neste exemplo, a central de segurança exibe o status de segurança importante o tempo todo, mas usa a divulgação progressiva para exibir detalhes sob demanda.

-   **Se as informações forem exibidas por padrão, os usuários provavelmente poderão optar por ocultá-lo?** Há situações em que os usuários precisarão de mais espaço? Os usuários estão suficientemente motivados para personalizar a interface do usuário? Caso contrário, exiba as informações sem usar a divulgação progressiva.

    **Incorreto:**

    ![captura de tela de opções de dados exibidas por padrão ](images/progressive-disclosure-controls-image3.png)

    Neste exemplo, os usuários não serão motivados a ocultar as informações.

-   **As informações adicionais são avançadas, substanciais, complexas ou relacionadas a uma subtarefa independente?** Nesse caso, considere exibir as informações em uma janela separada usando [botões de comando](ctrl-command-buttons.md) ou [links](ctrl-command-links.md) em vez de usar um controle de divulgação progressiva. (Informações adicionais serão avançadas se forem destinadas a usuários avançados. É complexo se torna outras informações difíceis de ler ou dispor.)

    ![captura de tela de você deseja executar este arquivo? ](images/progressive-disclosure-controls-image4.png)

    Neste exemplo, as informações sobre o nome do software e o Publicador são significativas principalmente para usuários avançados, de modo que são usados links para janelas separadas.

-   **As informações adicionais são um fragmento de sentença ou frase que descreve o que um item faz ou como ele pode ser usado?** Nesse caso, considere usar uma [dica de ferramenta](ctrl-tooltips-and-infotips.md) ou InfoTip.
-   **São as informações adicionais relacionadas à tarefa atual, mas independentes das informações exibidas no momento?** Nesse caso, considere o uso de [guias](ctrl-tabs.md) em vez disso. No entanto, as listas recolhíveis geralmente são preferidas para guias porque são mais flexíveis e escaláveis.
-   **Está mostrando ou ocultando as informações adicionais, essencialmente, um filtro de dados?** Em caso afirmativo, considere usar uma [lista suspensa](/windows/desktop/uxguide/ctrl-drop) ou [caixas de seleção](ctrl-check-boxes.md) para aplicar o filtro à lista inteira.

## <a name="design-concepts"></a>Conceitos de design

As metas de divulgação progressiva são:

-   **Simplifique uma interface do usuário** concentrando-se no essencial, mas ainda revelando detalhes adicionais conforme necessário.
-   **Simplifique a aparência de uma interface do usuário** , reduzindo a percepção da desordem.

Ambas as metas podem ser obtidas usando controles de divulgação progressivos, em que os usuários clicam para ver mais detalhes. No entanto, você pode obter o segundo objetivo de simplificar a aparência sem usar controles de divulgação progressivos explícitos:

-   **Mostrando somente detalhes contextuais no contexto.** Por exemplo, você pode mostrar comandos ou barras de ferramentas contextuais automaticamente quando relevante para o objeto ou modo selecionado.
-   **Reduzindo o peso do capacidades para a interface do usuário secundária.** [Capacidades](glossary.md) são propriedades visuais que sugerem como os objetos são usados. A tendência é ter a interface do usuário com a qual os usuários possam interagir no local, mas ter toda essa interface do usuário desenhada para Scream "Click me!" leva a muita bagunça Visual. Para a interface do usuário secundária, geralmente é melhor usar capacidades sutis e dar os efeitos totais sobre o mouse.

    ![captura de tela de ícones de estrela usados para classificar fotos ](images/progressive-disclosure-controls-image5.png)

    Neste exemplo, o campo de classificação é interativo, mas não aparecerá até que o mouse seja focalizado.

-   **Mostrando etapas de acompanhamento somente após a conclusão dos pré-requisitos.** Essa abordagem é melhor usada com tarefas familiares em que os usuários podem executar as primeiras etapas com segurança.

    ![captura de tela de caixas de texto de nome de usuário e senha ](images/progressive-disclosure-controls-image6.png)

    Neste exemplo, a página nome de usuário e senha inicialmente mostra apenas as caixas nome de usuário e senha opcional. As caixas de confirmação e de dica são exibidas depois que o usuário insere uma senha.

Embora a divulgação progressiva seja uma ótima maneira de simplificar as UIs, ela tem estes riscos:

-   **Falta de detectabilidade.** Os usuários podem pressupor que, se não conseguirem ver algo, ele não existirá. Os usuários não podem focalizar ou clicar se não verão o que estão procurando. Sempre há a chance de que os usuários não possam clicar em coisas como mais opções.
-   **Falta de estabilidade.** A divulgação progressiva deve ser esperada ou pelo menos se parecer natural. Se os controles aparecerem inesperadamente e desaparecerem, a interface do usuário resultante poderá se sentir instável.

### <a name="progressive-disclosure-controls"></a>Controles de divulgação progressiva

Os controles de divulgação progressiva geralmente são exibidos sem rótulos diretos que descrevem seu comportamento, de modo que os usuários devem conseguir fazer o seguinte com base na aparência visual do controle sozinho:

-   Reconheça que o controle fornece divulgação progressiva.
-   Determine se o estado atual é expandido ou recolhido.
-   Determine se são necessárias informações adicionais, opções ou comandos para executar a tarefa.
-   Determine como restaurar o estado original, se desejado.

Embora os usuários possam determinar os acima por tentativa e erro, você deve tentar tornar essa experimentação desnecessária.

Os controles de divulgação progressiva têm um [capacidades](glossary.md)bastante fraco, o que significa que suas propriedades visuais sugerem como eles são usados, embora de forma fraca. A tabela a seguir compara a aparência dos controles de divulgação progressivos comuns:



|                                                                                                                                                          |                                                                                                                                                                                                             |                                                                                                                                |                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Controle**<br/>                                                                                                                                   | **Finalidade**<br/>                                                                                                                                                                                      | **Aparência**<br/>                                                                                                      | **Glifo indica**<br/> |
| **Divisas**<br/> ![captura de tela das divisas esquerda/direita e para cima/para baixo ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Mostrar tudo:** Mostrar ou ocultar os itens restantes em conteúdo completamente ou parcialmente oculto. Os itens são mostrados no local (usando uma única divisa) ou em um menu pop-up (usando uma divisa dupla).<br/> | Ponto de divisas na direção em que a ação ocorrerá.<br/>                                                        | Estado futuro<br/>        |
| **Setas**<br/> ![captura de tela das setas esquerda/direita e para cima/para baixo ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Mostrar opções:** Mostrar um menu de comando pop-up.<br/>                                                                                                                                                    | Ponto de setas na direção em que a ação ocorrerá.<br/>                                                          | Estado futuro<br/>        |
| **Mais e menos controles**<br/> ![captura de tela de dois botões pequenos de adição e menos ](images/progressive-disclosure-controls-image9.png)<br/> | **Expandir contêineres:** Expanda ou recolha o conteúdo do contêiner em vigor ao navegar por uma hierarquia.<br/>                                                                                        | Além disso, os símbolos de menos não apontam, mas a ação sempre ocorre à direita.<br/>                                    | Estado futuro<br/>        |
| **Triângulos rotativo**<br/> ![captura de tela de dois triângulos pequenos ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Mostrar detalhes:** Mostrar ou ocultar informações adicionais em vigor para um item individual. Eles também são usados para expandir contêineres.<br/>                                                                  | Os triângulos giratórios se assemelham às alavancas giratórias, para que apontem para a direção em que a ação ocorreu.<br/> | Estado atual<br/>       |



 

**Se você fizer apenas uma coisa...**

Os usuários devem ser capazes de prever o comportamento de um controle de divulgação progressiva corretamente apenas por inspeção. Para conseguir isso, selecione os padrões de uso apropriados e aplique a aparência, o local e o comportamento de forma consistente.

## <a name="usage-patterns"></a>Padrões de uso

Os controles de divulgação progressiva têm vários padrões de uso. Alguns deles são criados em controles comuns.

### <a name="chevrons"></a>Divisas

As divisas mostram ou ocultam os itens restantes em conteúdo completamente ou parcialmente oculto. Normalmente, os itens são mostrados em vigor, mas também podem ser mostrados em um menu pop-up. Quando em vigor, o item permanece expandido até que o usuário o recolha.

As divisas são usadas das seguintes maneiras:



|                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Interface do usuário in-loco**<br/> o objeto associado recebe o foco de entrada e a divisa única é ativada com a barra de espaço.<br/>                       | ![captura de tela da exibição de status da central de segurança ](images/progressive-disclosure-controls-image11.png)<br/> Nesses exemplos, as divisas simples no local são posicionadas à direita de seu controle associado.<br/>                                                                            |
| **Botões de comando com rótulos externos**<br/> o botão de comando recebe o foco de entrada e a divisa única é ativada com a barra de espaço.<br/> | ![captura de tela de divisa com o rótulo ' mais opções ' ](images/progressive-disclosure-controls-image12.png)<br/> Neste exemplo, o botão de divisa única é rotulado e posicionado à esquerda do rótulo. Com esse padrão, o botão seria difícil de entender sem seu rótulo.<br/> |
| **Botões de comando com rótulos internos**<br/> o botão de comando recebe o foco de entrada e é ativado com a barra de espaço.<br/>                    | ![captura de tela dos botões de comando ' more ' e ' less ' ](images/progressive-disclosure-controls-image13.png)<br/> Nesses exemplos, os botões de comando normais têm a divisa dupla posicionada para sugerir seu significado.<br/>                                                                          |



 

### <a name="arrows"></a>Setas

As setas mostram um menu de comando pop-up. O item permanece expandido até que o usuário faça uma seleção ou clique em qualquer lugar.

Se o botão de seta for um controle independente, ele receberá o foco de entrada e será ativado com a barra de espaço. Se o botão de seta tiver um controle pai, o pai receberá o foco de entrada e a seta será ativada com as teclas Alt + seta para baixo e Alt + seta para cima, como no controle de lista suspensa.

As setas são usadas das seguintes maneiras:



|                                                                                       |                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Separar botões**<br/> a seta está em um controle de botão separado.<br/> | ![captura de tela de setas à direita dos controles ](images/progressive-disclosure-controls-image14.png)<br/> Nesses exemplos, os botões de seta separados posicionados à direita indicam um menu de comando.<br/>               |
| **Botões de comando**<br/> a seta faz parte de um botão de comando.<br/>      | ![captura de tela de rótulo e seta no botão de comando ](images/progressive-disclosure-controls-image15.png)<br/> Nesses exemplos, botões de menu e botões de divisão têm as setas posicionadas à direita do texto.<br/> |



 

### <a name="plus-and-minus-controls"></a>Mais e menos controles

Os controles de adição e subtração expandem ou recolhem para mostrar o conteúdo do contêiner em vigor ao navegar por uma hierarquia. O item permanece expandido até que o usuário o recolha. Embora eles pareçam botões, seu comportamento é in-loco.

O objeto associado recebe o foco de entrada. O sinal de adição é ativado com a tecla de seta para a direita e o menos com a tecla de seta para a esquerda.

Os controles Plus e menos são usados das seguintes maneiras:



|                                                                                                |                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árvores recolhíveis**<br/> uma hierarquia de vários níveis para mostrar o conteúdo do contêiner.<br/> | ![Captura de tela que mostra uma árvore de pastas do Windows Explorer com ' comportamento ' selecionado.](images/progressive-disclosure-controls-image16.png)<br/> Neste exemplo, os controles de adição e de subtração são posicionados à esquerda do contêiner associado.<br/>       |
| **Listas recolhíveis**<br/> uma hierarquia de dois níveis para mostrar o conteúdo do contêiner.<br/>   | ![captura de tela da lista expandida para mostrar dois níveis ](images/progressive-disclosure-controls-image17.png)<br/> Neste exemplo, os controles de adição e de subtração são posicionados à esquerda do cabeçalho de lista associado.<br/> |



 

### <a name="rotating-triangles"></a>Triângulos rotativo

Os triângulos giratórios mostram ou ocultam informações adicionais em vigor para um item individual. Eles também são usados para expandir contêineres. O item permanece expandido até que o usuário o recolha.

O objeto associado recebe o foco de entrada. O triângulo recolhido (apontado para a direita) é ativado com a tecla de seta para a direita e o triângulo expandido (apontando para baixo) com a tecla de seta para a esquerda.

Os triângulos giratórios são usados das seguintes maneiras:



|                                                                                                            |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árvores recolhíveis**<br/> uma hierarquia de vários níveis para mostrar o conteúdo do contêiner.<br/>             | ![captura de tela da árvore de pastas do Windows Explorer ](images/progressive-disclosure-controls-image18.png)<br/> Neste exemplo, os triângulos giratórios são posicionados à esquerda do contêiner associado.<br/>       |
| **Listas recolhíveis**<br/> uma hierarquia de dois níveis para mostrar informações adicionais em vigor.<br/> | ![captura de tela da lista exibindo dados adicionais ](images/progressive-disclosure-controls-image19.png)<br/> Neste exemplo, os triângulos giratórios estão posicionados à esquerda de seus itens de lista associados.<br/> |



 

### <a name="preview-arrows"></a>Setas de visualização

Como divisas, informações adicionais são mostradas ou ocultas no local. O item permanece expandido até que o usuário o recolha. Ao contrário das divisas, os glifos têm uma representação gráfica da ação, normalmente com uma seta indicando o que acontecerá.

![captura de tela de glifos de seta apontando diagonalmente ](images/progressive-disclosure-controls-image20.png)

Nestes exemplos do Microsoft Windows Media Player, os glifos têm setas que sugerem a ação que ocorrerá.

As setas de visualização são mais bem reservadas para situações em que uma divisa padrão não comunica adequadamente o comportamento do controle, como quando a divulgação é complexa ou há mais de um tipo de divulgação.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Selecione o padrão de divulgação progressiva com base em seu uso.** Para obter uma descrição de cada padrão de uso, consulte a tabela anterior.
-   **Não use links para controles de divulgação progressiva.** Use somente os controles de divulgação progressiva apresentados na seção padrões de uso. No entanto, use links para navegar até [Tópicos da ajuda](winenv-help.md).

    **Correto:**

    ![captura de tela de divisa com o rótulo ' show Mixer ' ](images/progressive-disclosure-controls-image21.png)

    **Incorreto:**

    ![captura de tela do texto do link ' Mostrar Mixer ' ](images/progressive-disclosure-controls-image22.png)

    No exemplo incorreto, um link é usado para mostrar mais opções no local. Esse uso estaria correto se o link navegou para outra página ou caixa de diálogo, ou exibia um tópico da ajuda.

### <a name="interaction"></a>Interação

-   **Para divisas e setas que não são rotuladas diretamente, use dicas de ferramenta para descrever o que eles fazem.**

    ![captura de tela da dica de ferramenta ' expandir o construtor de consultas ' ](images/progressive-disclosure-controls-image23.png)

    Neste exemplo, a dica de ferramenta indica o efeito de um controle de divisa sem rótulo.

-   **Se um usuário expandir ou recolher um item, faça o estado persistir para que ele entre em vigor na próxima vez que a janela for exibida**, a menos que os usuários provavelmente prefiram iniciar no estado padrão. Faça o estado persistir em uma base por janela por usuário.
-   **Verifique se todo o conteúdo expandido pode ser recolhido e vice-versa, e se a operação inversa é óbvia.** Isso incentiva a exploração e reduz a frustração. A melhor maneira de tornar a operação inversa óbvia é manter o controle no mesmo local fixo. Se você precisar mover o controle, mantenha-o no mesmo local relativo dentro de uma área visualmente distinta.

    **Incorreto:**

    ![captura de tela do botão ' substituir ' com divisa ](images/progressive-disclosure-controls-image24.png)

    ![captura de tela do botão ' substituir ' sem divisa ](images/progressive-disclosure-controls-image25.png)

    Neste exemplo, clicar no botão substituir com a divisa revela a caixa de texto **substituir por** . Quando isso é feito, o expansor de substituição se torna o comando Replace, portanto, não há como restaurar o estado original.

-   **Use somente as chaves de acesso apropriadas para o padrão de divulgação progressiva**, conforme listado na seção padrões de uso. Não use Enter para ativar a divulgação progressiva.

### <a name="presentation"></a>Apresentação

-   **Não use pontas de seta em forma triangular para uma finalidade diferente de divulgação progressiva.**

    **Incorreto:**

    ![captura de tela de rótulo com triângulo apontando para a direita ](images/progressive-disclosure-controls-image26.png)

    Embora esse exemplo não seja um padrão de divulgação progressiva, o uso de uma seta aqui sugere que os comandos serão mostrados em uma janela pop-up.

    **Correto:**

    ![captura de tela de rótulo com marcador à esquerda do texto ](images/progressive-disclosure-controls-image27.png)

    Neste exemplo, um marcador é usado corretamente em seu lugar.

-   **Remova (não desabilite) controles de divulgação progressiva que não se aplicam no contexto atual.** Os controles de divulgação progressiva sempre devem entregar sua promessa, portanto, remova-os quando não houver mais informações para dar.

    **Incorreto:**

    ![captura de tela de um controle ' mais opções ' esmaecida ](images/progressive-disclosure-controls-image28.png)

    Neste exemplo, um controle de divulgação progressiva que não se aplica está desabilitado incorretamente.

### <a name="chevrons"></a>Divisas

-   **Use uma única divisa para mostrar ou ocultar no local. Use divisas duplas para mostrar ou ocultar usando um menu pop-up.** No entanto, você sempre deve usar as divisas duplas para botões de comando com rótulos internos.

    **Correto:**

    ![captura de tela do controle de mais opções de uma única divisa ](images/progressive-disclosure-controls-image29.png)

    **Incorreto:**

    ![captura de tela de mais controle de opções de divisa dupla ](images/progressive-disclosure-controls-image30.png)

    No exemplo incorreto, uma divisa dupla é usada para divulgação progressiva in-loco.

    **Correto:**

    ![captura de tela do botão de comando mais de divisa dupla ](images/progressive-disclosure-controls-image31.png)

    Neste exemplo, uma divisa dupla é usada para divulgação progressiva in-loco porque é um botão de comando com um rótulo interno.

-   **Forneça uma relação visual entre a divisa e seu controle associado.** Como as divisas in-loco são colocadas à direita de sua interface do usuário associada e alinhada à direita, pode haver uma distância muito entre uma divisa e seu controle associado.

    **Correto:**

    ![captura de tela de sombreamento graduado por trás dos controles ](images/progressive-disclosure-controls-image32.png)

    Neste exemplo, há uma relação clara entre a divisa in-loco e sua interface do usuário associada.

    **Incorreto:**

    ![captura de tela de plano de fundo sólido-branco para controles ](images/progressive-disclosure-controls-image33.png)

    Neste exemplo, não há nenhuma relação visual clara entre a divisa in-loco e sua interface do usuário associada, portanto, parece estar flutuante no espaço.

### <a name="arrows"></a>Setas

-   **Não use gráficos de seta que possam ser confundidos com voltar, avançar, ir ou reproduzir.** Use pontas de seta simples em forma de triangulares (setas sem hastes) em planos de fundo neutros.

    **Correto:**

    ![captura de tela de dois pequenos triângulos pretos ](images/progressive-disclosure-controls-image34.png)

    Essas setas são controles de divulgação de forma clara.

    **Incorreto (para divulgação progressiva):**

    ![captura de tela de duas setas verdes pequenas ](images/progressive-disclosure-controls-image35.png)

    Essas setas não são semelhantes aos controles de divulgação progressiva.

    **Incorreto (para voltar, avançar):**

    ![captura de tela de dois botões com triângulos pretos ](images/progressive-disclosure-controls-image36.png)

    Essas setas se parecem com controles de divulgação progressiva, mas não são.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![captura de tela de dimensionamento e espaçamento recomendados ](images/progressive-disclosure-controls-image37.png)

Dimensionamento e espaçamento recomendados para controles de divulgação progressiva.

## <a name="labels"></a>Rótulos

-   Para divisas em um botão de comando com um rótulo externo:
    -   Atribua uma [chave de acesso](glossary.md)exclusiva. Para obter diretrizes, consulte [teclado](inter-keyboard.md).
    -   Use [a capitalização no estilo de frase](glossary.md).
    -   Escreva o rótulo como uma frase e não use pontuação final.
    -   Escreva o rótulo para que ele descreva o efeito de clicar no botão e alterar o rótulo quando o estado for alterado.
    -   Se a superfície sempre exibir algumas opções, comandos ou detalhes, use os seguintes pares de rótulos:
        -   **Mais/menos opções.** Use para opções ou uma combinação de opções, comandos e detalhes.
        -   **Mais/menos comandos.** Use somente para comandos.
        -   **Mais/menos detalhes.** Use apenas para fins informativos.
        -   **Mais/menos <object name> .** Use para outros tipos de objeto, como pastas.
    -   Caso contrário:
        -   **Mostrar/Ocultar opções.** Use para opções ou uma combinação de opções, comandos e detalhes.
        -   **Mostrar/ocultar comandos.** Use somente para comandos.
        -   **Mostrar/ocultar detalhes.** Use apenas para fins informativos.
        -   **Mostrar/ocultar <object name> .** Use para outros tipos de objeto, como pastas.
-   Para divisas em um botão de comando com um rótulo interno, siga as diretrizes do [botão de comando](ctrl-command-buttons.md) padrão.

## <a name="documentation"></a>Documentação

Ao fazer referência a controles de divulgação progressivos:

-   Se o controle tiver um rótulo fixo, consulte o controle somente por seu rótulo; Não tente descrever o controle. Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua o sublinhado da chave de acesso.
-   Se o controle não tiver nenhum rótulo ou não for corrigido, consulte o controle por seu tipo: divisa, seta, triângulo ou botão mais/menos. Se necessário, também Descreva o local do controle. Se o controle aparecer dinamicamente, como o controle de [espaço de página](glossary.md) , inicie a referência, descrevendo como fazer o controle aparecer.

    **Exemplo:** Para exibir os arquivos em uma pasta, mova o ponteiro para o início do nome da pasta e clique no triângulo ao lado da pasta.

-   Não faça referência ao controle como um botão, a menos que seja necessário comparar com outros controles de divulgação progressivos que não são botões.
-   Para descrever a interação do usuário, use clique. Se necessário para maior clareza, use clique em... para expandir ou recolher.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplos:

-   (Para uma divisa) Para determinar o tamanho do arquivo, clique em **detalhes**.
-   (Para uma seta) Para ver todas as opções, clique na seta ao lado da caixa de **pesquisa** .
-   (Para mais/menos) Para exibir a imagem, clique em **imagens**.

