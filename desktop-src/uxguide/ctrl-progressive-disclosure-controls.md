---
title: Controles de divulgação progressiva
description: Com um controle de divulgação progressiva, os usuários podem mostrar ou ocultar informações adicionais, incluindo dados, opções ou comandos.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1d561ea6e4f937c6e162f9eaa1f452e73d7de20c9f94c41785641062c21cd1a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676009"
---
# <a name="progressive-disclosure-controls"></a>Controles de divulgação progressiva

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com um controle de divulgação progressiva, os usuários podem mostrar ou ocultar informações adicionais, incluindo dados, opções ou comandos. A divulgação progressiva promove a simplicidade concentrando-se no essencial, mas revelando detalhes adicionais conforme necessário.

![captura de tela de controles de divulgação progressiva](images/progressive-disclosure-controls-image1.png)

Exemplos de controles de divulgação progressiva.

> [!Note]  
> As diretrizes relacionadas [ao layout,](vis-layout.md) [menus](cmd-menus.md)e barras de ferramentas são [apresentadas](cmd-toolbars.md) em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **Os usuários precisam ver as informações em alguns, mas não em todos os cenários ou em alguns, mas não o tempo todo?** Em caso afirmativos, exibir as informações usando a divulgação progressiva simplifica a experiência de linha de base, mas permite que os usuários acessem as informações facilmente.

    ![Captura de tela que mostra a exibição do status da central de segurança.](images/progressive-disclosure-controls-image2.png)

    Neste exemplo, a Central de Segurança exibe o status de segurança importante o tempo todo, mas usa a divulgação progressiva para exibir detalhes sob demanda.

-   **Se as informações são exibidas por padrão, é provável que os usuários optem por oprimá-la?** Há cenários em que os usuários precisarão de mais espaço? Os usuários estão suficientemente incentivados a personalizar a interface do usuário? Caso não, exibe as informações sem usar a divulgação progressiva.

    **Incorreto:**

    ![captura de tela das opções de dados exibidas por padrão ](images/progressive-disclosure-controls-image3.png)

    Neste exemplo, os usuários não serão incentivados a ocultar as informações.

-   **As informações adicionais são avançadas, substanciais, complexas ou relacionadas a uma subtarefa independente?** Nesse caso, considere exibir as informações [](ctrl-command-buttons.md) em uma janela separada usando botões de comando ou [links](ctrl-command-links.md) em vez de usar um controle de divulgação progressiva. (Informações adicionais serão avançadas se se destinam a usuários avançados. É complexo se torna outras informações difíceis de ler ou desajustar.)

    ![captura de tela do que você deseja executar esse arquivo? ](images/progressive-disclosure-controls-image4.png)

    Neste exemplo, as informações sobre o nome e o publicador do software são significativas principalmente para usuários avançados, portanto, os links para janelas separadas são usados.

-   **As informações adicionais são um fragmento de frase ou frase que descreve o que um item faz ou como ele pode ser usado?** Se sim, considere o uso de [uma dica de ferramenta](ctrl-tooltips-and-infotips.md) ou infotip.
-   **As informações adicionais estão relacionadas à tarefa atual, mas independente das informações exibidas no momento?** Se sim, considere usar guias em [vez](ctrl-tabs.md) disso. No entanto, listas reutíveis geralmente são preferíveis a guias porque são mais flexíveis e escalonáveis.
-   **Está mostrando ou ocultando as informações adicionais essencialmente um filtro de dados?** Em caso afirmado, considere usar uma [lista de](/windows/desktop/uxguide/ctrl-drop) listas ou caixas [de](ctrl-check-boxes.md) seleção para aplicar o filtro à lista inteira.

## <a name="design-concepts"></a>Conceitos de design

As metas da divulgação progressiva são:

-   **Simplifique uma** interface do usuário concentrando-se no essencial, mas revelando detalhes adicionais conforme necessário.
-   **Simplifique a aparência de uma interface do usuário** reduzindo a percepção de confusão.

Ambas as metas podem ser alcançadas usando controles de divulgação progressiva, em que os usuários clicam para ver mais detalhes. No entanto, você pode atingir a segunda meta de simplificar a aparência sem usar controles explícitos de divulgação progressiva:

-   **Mostrando detalhes contextuais somente no contexto.** Por exemplo, você pode mostrar comandos contextuais ou barras de ferramentas automaticamente quando relevante para o objeto ou modo selecionado.
-   **Reduzindo o peso das responsabilidades para a interface do usuário secundária.** [As propriedades de recursos](glossary.md) são propriedades visuais que sugerem como os objetos são usados. A tendência é ter a interface do usuário com a que os usuários podem interagir no local, mas ter toda essa interface do usuário desenhada para "clicar em mim!" leva a muita confusão visual. Para a interface do usuário secundária, geralmente é melhor usar recursos sutis e dar os efeitos completos sobre o mouse.

    ![captura de tela de ícones em estrela usados para taxar fotos ](images/progressive-disclosure-controls-image5.png)

    Neste exemplo, o campo Classificação é interativo, mas não aparece até que o mouse passe o mouse.

-   **Mostrar as etapas de acompanhamento somente depois que os pré-requisitos são feitos.** Essa abordagem é mais bem usada com tarefas conhecidas em que os usuários podem realizar as primeiras etapas com segurança.

    ![captura de tela das caixas de texto nome de usuário e senha ](images/progressive-disclosure-controls-image6.png)

    Neste exemplo, a página de nome de usuário e senha inicialmente mostra apenas o nome de usuário e as caixas de senha opcionais. As caixas de confirmação e dica são exibidas após o usuário inserir uma senha.

Embora a divulgação progressiva seja uma ótima maneira de simplificar as UIs, ela tem estes riscos:

-   **Falta de descoberta.** Os usuários podem supor que, se não puderem ver algo, ele não existirá. Os usuários podem não passar o mouse ou clicar se não veem o que estão procurando. Sempre há uma chance de os usuários não clicarem em coisas como Mais opções.
-   **Falta de estabilidade.** A divulgação progressiva deve ser esperada ou, pelo menos, parece natural. Se os controles aparecerem e desaparecerem inesperadamente, a interface do usuário resultante poderá parecer instável.

### <a name="progressive-disclosure-controls"></a>Controles de divulgação progressiva

Os controles de divulgação progressiva geralmente são exibidos sem rótulos diretos que descrevem seu comportamento, portanto, os usuários devem ser capazes de fazer o seguinte com base apenas na aparência visual do controle:

-   Reconheça que o controle fornece divulgação progressiva.
-   Determine se o estado atual está expandido ou recolhido.
-   Determine se informações adicionais, opções ou comandos são necessários para executar a tarefa.
-   Determine como restaurar o estado original, se desejado.

Embora os usuários possam determinar o acima por avaliação e erro, você deve tentar tornar essa experimentação desnecessária.

Os controles de divulgação progressiva têm um poder relativamente [fraco,](glossary.md)o que significa que suas propriedades visuais sugerem como eles são usados, embora fracamente. A tabela a seguir compara a aparência dos controles comuns de divulgação progressiva:



| Control | Finalidade  | Aparência | Glifo indica |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Divisas**<br/> ![captura de tela de divisas para a esquerda/direita e para cima/para baixo ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Mostrar tudo:** Mostrar ou ocultar os itens restantes em conteúdo completamente ou parcialmente oculto. Os itens são mostrados no local (usando uma única divisa) ou em um menu pop-up (usando uma divisa dupla).<br/> | Divisas apontam para a direção em que a ação ocorrerá.<br/>                                                        | Estado futuro<br/>        |
| **Setas**<br/> ![captura de tela das setas para a esquerda/direita e para cima/para baixo ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Mostrar opções:** Mostrar um menu de comando pop-up.<br/>                                                                                                                                                    | As setas apontam para a direção em que a ação ocorrerá.<br/>                                                          | Estado futuro<br/>        |
| **Controles de mais e menos**<br/> ![captura de tela de dois botões de a mais e menos pequenos ](images/progressive-disclosure-controls-image9.png)<br/> | **Expanda contêineres:** Expanda ou resvante o conteúdo do contêiner no local ao navegar por uma hierarquia.<br/>                                                                                        | Símbolos de mais e menos não apontam, mas a ação sempre ocorre à direita.<br/>                                    | Estado futuro<br/>        |
| **Rotação de triângulos**<br/> ![captura de tela de dois triângulos pequenos ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Mostrar detalhes:** Mostrar ou ocultar informações adicionais no local para um item individual. Eles também são usados para expandir contêineres.<br/>                                                                  | Triângulos girando um pouco se assemelham a alavancas giratórias, portanto, apontam para a direção em que a ação ocorreu.<br/> | Estado atual<br/>       |



 

**Se você fizer apenas uma coisa...**

Os usuários devem ser capazes de prever o comportamento de um controle de divulgação progressiva corretamente apenas pela inspeção. Para conseguir isso, selecione os padrões de uso apropriados e aplique a aparência, o local e o comportamento de forma consistente.

## <a name="usage-patterns"></a>Padrões de uso

Os controles de divulgação progressiva têm vários padrões de uso. Alguns deles são criados em controles comuns.

### <a name="chevrons"></a>Divisas

As divisas mostram ou ocultam os itens restantes em conteúdo completamente ou parcialmente oculto. Normalmente, os itens são mostrados em vigor, mas também podem ser mostrados em um menu pop-up. Quando em vigor, o item permanece expandido até que o usuário o recolha.

As divisas são usadas das seguintes maneiras:



|      Uso                                                                                                                                                          |    Exemplo                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Interface do usuário in-loco**<br/> o objeto associado recebe o foco de entrada e a divisa única é ativada com a barra de espaço.<br/>                       | ![captura de tela da exibição de status da central de segurança ](images/progressive-disclosure-controls-image11.png)<br/> Nesses exemplos, as divisas simples no local são posicionadas à direita de seu controle associado.<br/>                                                                            |
| **Botões de comando com rótulos externos**<br/> o botão de comando recebe o foco de entrada e a divisa única é ativada com a barra de espaço.<br/> | ![captura de tela de divisa com o rótulo ' mais opções ' ](images/progressive-disclosure-controls-image12.png)<br/> Neste exemplo, o botão de divisa única é rotulado e posicionado à esquerda do rótulo. Com esse padrão, o botão seria difícil de entender sem seu rótulo.<br/> |
| **Botões de comando com rótulos internos**<br/> o botão de comando recebe o foco de entrada e é ativado com a barra de espaço.<br/>                    | ![captura de tela dos botões de comando ' more ' e ' less ' ](images/progressive-disclosure-controls-image13.png)<br/> Nesses exemplos, os botões de comando normais têm a divisa dupla posicionada para sugerir seu significado.<br/>                                                                          |



 

### <a name="arrows"></a>Setas

As setas mostram um menu de comando pop-up. O item permanece expandido até que o usuário faça uma seleção ou clique em qualquer lugar.

Se o botão de seta for um controle independente, ele receberá o foco de entrada e será ativado com a barra de espaço. Se o botão de seta tiver um controle pai, o pai receberá o foco de entrada e a seta será ativada com as teclas Alt + seta para baixo e Alt + seta para cima, como no controle de lista suspensa.

As setas são usadas das seguintes maneiras:



|    Uso                                                                                   |    Exemplo                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Separar botões**<br/> a seta está em um controle de botão separado.<br/> | ![captura de tela de setas à direita dos controles ](images/progressive-disclosure-controls-image14.png)<br/> Nesses exemplos, os botões de seta separados posicionados à direita indicam um menu de comando.<br/>               |
| **Botões de comando**<br/> a seta faz parte de um botão de comando.<br/>      | ![captura de tela de rótulo e seta no botão de comando ](images/progressive-disclosure-controls-image15.png)<br/> Nesses exemplos, botões de menu e botões de divisão têm as setas posicionadas à direita do texto.<br/> |



 

### <a name="plus-and-minus-controls"></a>Mais e menos controles

Os controles de adição e subtração expandem ou recolhem para mostrar o conteúdo do contêiner em vigor ao navegar por uma hierarquia. O item permanece expandido até que o usuário o recolha. Embora eles pareçam botões, seu comportamento é in-loco.

O objeto associado recebe o foco de entrada. O sinal de adição é ativado com a tecla de seta para a direita e o menos com a tecla de seta para a esquerda.

Os controles Plus e menos são usados das seguintes maneiras:



|       Uso                                                                                         |       Exemplo                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árvores recolhíveis**<br/> uma hierarquia de vários níveis para mostrar o conteúdo do contêiner.<br/> | ![captura de tela que mostra uma árvore de pastas Windows Explorer com ' comportamento ' selecionado.](images/progressive-disclosure-controls-image16.png)<br/> Neste exemplo, os controles de adição e de subtração são posicionados à esquerda do contêiner associado.<br/>       |
| **Listas recolhíveis**<br/> uma hierarquia de dois níveis para mostrar o conteúdo do contêiner.<br/>   | ![captura de tela da lista expandida para mostrar dois níveis ](images/progressive-disclosure-controls-image17.png)<br/> Neste exemplo, os controles de adição e de subtração são posicionados à esquerda do cabeçalho de lista associado.<br/> |



 

### <a name="rotating-triangles"></a>Triângulos rotativo

Os triângulos giratórios mostram ou ocultam informações adicionais em vigor para um item individual. Eles também são usados para expandir contêineres. O item permanece expandido até que o usuário o recolha.

O objeto associado recebe o foco de entrada. O triângulo recolhido (apontado para a direita) é ativado com a tecla de seta para a direita e o triângulo expandido (apontando para baixo) com a tecla de seta para a esquerda.

Os triângulos giratórios são usados das seguintes maneiras:



|     Uso                                                                                                       |    Exemplo                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Árvores recolhíveis**<br/> uma hierarquia de vários níveis para mostrar o conteúdo do contêiner.<br/>             | ![captura de tela da árvore de pastas do Windows Explorer ](images/progressive-disclosure-controls-image18.png)<br/> Neste exemplo, os triângulos giratórios são posicionados à esquerda do contêiner associado.<br/>       |
| **Listas recolhíveis**<br/> uma hierarquia de dois níveis para mostrar informações adicionais em vigor.<br/> | ![captura de tela da lista exibindo dados adicionais ](images/progressive-disclosure-controls-image19.png)<br/> Neste exemplo, os triângulos giratórios estão posicionados à esquerda de seus itens de lista associados.<br/> |



 

### <a name="preview-arrows"></a>Setas de visualização

Como divisas, informações adicionais são mostradas ou ocultas no local. O item permanece expandido até que o usuário o recolha. Ao contrário das divisas, os glifos têm uma representação gráfica da ação, normalmente com uma seta indicando o que acontecerá.

![captura de tela de glifos de seta apontando diagonalmente ](images/progressive-disclosure-controls-image20.png)

nestes exemplos do Microsoft Windows Media Player, os glifos têm setas que sugerem a ação que ocorrerá.

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
-   **Certifique-se de que todo o conteúdo expandido possa ser recolhido e vice-versa e se a operação inversa é óbvia.** Isso incentiva a exploração e reduz a frustração. A melhor maneira de tornar a operação inversa óbvia é manter o controle no mesmo local fixo. Se você precisar mover o controle, mantenha-o no mesmo local relativo em uma área visualmente distinta.

    **Incorreto:**

    ![captura de tela do botão "substituir" por divisa ](images/progressive-disclosure-controls-image24.png)

    ![captura de tela do botão "substituir" sem divisa ](images/progressive-disclosure-controls-image25.png)

    Neste exemplo, clicar no botão Substituir pela divisa revela a **caixa de texto** Substituir por . Depois que isso for feito, o expansador Substituir se tornará o comando Substituir, portanto, não há como restaurar o estado original.

-   **Use apenas as chaves de acesso apropriadas para o padrão de divulgação progressiva**, conforme listado na seção Padrões de uso. Não use Enter para ativar a divulgação progressiva.

### <a name="presentation"></a>Apresentação

-   **Não use as setas em forma de triangular para uma finalidade diferente da divulgação progressiva.**

    **Incorreto:**

    ![captura de tela do rótulo com triângulo apontando para a direita ](images/progressive-disclosure-controls-image26.png)

    Embora este exemplo não seja um padrão de divulgação progressiva, usar uma seta aqui sugere que os comandos serão mostrados em uma janela pop-up.

    **Correto:**

    ![captura de tela do rótulo com marcador à esquerda do texto ](images/progressive-disclosure-controls-image27.png)

    Neste exemplo, um marcador é usado corretamente.

-   **Remova (não desabilite) controles de divulgação progressiva que não se aplicam ao contexto atual.** Os controles de divulgação progressiva sempre devem cumprir sua promessa, portanto, remova-os quando não houver mais informações a fornecer.

    **Incorreto:**

    ![captura de tela de um controle "mais opções" esmaecida ](images/progressive-disclosure-controls-image28.png)

    Neste exemplo, um controle de divulgação progressiva que não se aplica está desabilitado incorretamente.

### <a name="chevrons"></a>Divisas

-   **Use divisas simples para mostrar ou ocultar no local. Use divisas duplas para mostrar ou ocultar usando um menu pop-up.** No entanto, você sempre deve usar divisas duplas para botões de comando com rótulos internos.

    **Correto:**

    ![captura de tela do controle de opções de divisa única mais ](images/progressive-disclosure-controls-image29.png)

    **Incorreto:**

    ![captura de tela do controle de opções de divisa dupla mais ](images/progressive-disclosure-controls-image30.png)

    No exemplo incorreto, uma divisa dupla é usada para divulgação progressiva in-place.

    **Correto:**

    ![captura de tela do botão de comando divisa dupla mais ](images/progressive-disclosure-controls-image31.png)

    Neste exemplo, uma divisa dupla é usada para divulgação progressiva in-locar porque é um botão de comando com um rótulo interno.

-   **Forneça uma relação visual entre a divisa e seu controle associado.** Como as divisas in-locar são colocadas à direita de sua interface do usuário associada e alinhadas à direita, pode haver uma distância entre uma divisa e seu controle associado.

    **Correto:**

    ![captura de tela de sombreamento formado por trás de controles ](images/progressive-disclosure-controls-image32.png)

    Neste exemplo, há uma relação clara entre a divisa in-place e sua interface do usuário associada.

    **Incorreto:**

    ![captura de tela da tela de fundo em branco sólida para controles ](images/progressive-disclosure-controls-image33.png)

    Neste exemplo, não há nenhuma relação visual clara entre a divisa in-locar e sua interface do usuário associada, portanto, parece estar flutuante no espaço.

### <a name="arrows"></a>Setas

-   **Não use gráficos de seta que podem ser confundidos com Voltar, Avançar, Ir ou Reproduzir.** Use setas simples em forma de triangular (setas sem troncos) em plano de fundo neutro.

    **Correto:**

    ![captura de tela de dois triângulos pretos pequenos ](images/progressive-disclosure-controls-image34.png)

    Essas setas são controles claramente progressivos de divulgação.

    **Incorreto (para divulgação progressiva):**

    ![captura de tela de duas setas verdes pequenas ](images/progressive-disclosure-controls-image35.png)

    Essas setas não se parecem com controles de divulgação progressiva.

    **Incorreto (para Voltar, Avançar):**

    ![captura de tela de dois botões com triângulos pretos ](images/progressive-disclosure-controls-image36.png)

    Essas setas se parecem com controles de divulgação progressiva, mas não são.

## <a name="recommended-sizing-and-spacing"></a>Espaçamento e o espaçamento recomendados

![captura de tela do tamanho e espaçamento recomendados ](images/progressive-disclosure-controls-image37.png)

O espaçamento e o espaçamento recomendados para controles de divulgação progressiva.

## <a name="labels"></a>Rótulos

-   Para divisas em um botão de comando com um rótulo externo:
    -   Atribua uma chave [de acesso exclusiva.](glossary.md) Para diretrizes, consulte [Teclado](inter-keyboard.md).
    -   Use [a capitalização de estilo de frase](glossary.md).
    -   Escreva o rótulo como uma frase e não use nenhuma pontuação final.
    -   Escreva o rótulo para que ele descreva o efeito de clicar no botão e altere o rótulo quando o estado mudar.
    -   Se a superfície sempre exibir algumas opções, comandos ou detalhes, use os seguintes pares de rótulo:
        -   **Mais/menos opções.** Use para opções ou uma combinação de opções, comandos e detalhes.
        -   **Mais/Menos comandos.** Use somente para comandos.
        -   **Mais/menos detalhes.** Use somente para informações.
        -   **Mais/menos <object name> .** Use para outros tipos de objeto, como pastas.
    -   Caso contrário:
        -   **Opções Mostrar/Ocultar.** Use para opções ou uma combinação de opções, comandos e detalhes.
        -   **Comandos Show/Hide.** Use somente para comandos.
        -   **Mostrar/ocultar detalhes.** Use somente para informações.
        -   **Mostrar/Ocultar <object name> .** Use para outros tipos de objeto, como pastas.
-   Para divisas em um botão de comando com um rótulo interno, siga as [diretrizes do botão de comando](ctrl-command-buttons.md) padrão.

## <a name="documentation"></a>Documentação

Ao se referir a controles de divulgação progressiva:

-   Se o controle tiver um rótulo fixo, consulte o controle somente por seu rótulo; não tente descrever o controle. Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua o sublinhado da chave de acesso.
-   Se o controle não tiver nenhum rótulo ou não for corrigido, consulte o controle por seu tipo: divisa, seta, triângulo ou botão de mais/menos. Se necessário, descreva também o local do controle. Se o controle aparecer dinamicamente, como o [controle](glossary.md) de espaço de página, inicie a referência descrevendo como fazer com que o controle apareça.

    **Exemplo:** Para exibir os arquivos em uma pasta, mova o ponteiro para o início do nome da pasta e clique no triângulo ao lado da pasta.

-   Não se refira ao controle como um botão, a menos que contraste com outros controles de divulgação progressivos que não são botões.
-   Para descrever a interação do usuário, use clique. Se necessário para maior clareza, use clique... para expandir ou ressuar.
-   Quando possível, forja o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplos:

-   (Para uma divisa) Para determinar o tamanho do arquivo, clique em **Detalhes.**
-   (Para uma seta) Para ver todas as opções, clique na seta ao lado da **caixa** Pesquisar.
-   (Para mais/menos) Para exibir a imagem, clique em **imagens**.

