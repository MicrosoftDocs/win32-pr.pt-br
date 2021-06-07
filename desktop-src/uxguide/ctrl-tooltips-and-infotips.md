---
title: Dicas de ferramenta e infotips
description: Uma dica de ferramenta é uma pequena janela pop-up que rotula o controle sem rótulo que está sendo apontado, como controles de barra de ferramentas sem rótulo ou botões de comando.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8911c5a008d2de6cec2bd564fd786a23c670d633
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524530"
---
# <a name="tooltips-and-infotips"></a>Dicas de ferramenta e infotips

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma dica de ferramenta é uma pequena janela pop-up que rotula o controle sem rótulo que está sendo apontado, como controles de barra de ferramentas sem rótulo ou botões de comando.

![Captura de tela que mostra o botão imprimir com a dica de ferramenta 'Imprimir (Ctrl+P)' exibida.](images/ctrl-tooltips-and-infotips-image1.png)

Uma dica de ferramenta típica para um botão de barra de ferramentas.

Como as dicas de ferramenta se mostraram tão úteis, existe um controle relacionado chamado infotips, que fornece texto mais descritivo do que é possível com dicas de ferramenta.

Uma infotip é uma pequena janela pop-up que descreve concisamente o objeto que está sendo apontado, como descrições de controles de barra de ferramentas, ícones, elementos gráficos, links, objetos Windows Explorer, itens de menu Iniciar e botões da barra de tarefas. As infotips são uma forma de [controles de divulgação progressiva,](ctrl-progressive-disclosure-controls.md)eliminando a necessidade de sempre ter texto descritivo na tela.

![captura de tela do botão compartilhar com infotip ](images/ctrl-tooltips-and-infotips-image2.png)

Um infotip típico.

Para os fins deste artigo, dicas de ferramenta e infotips são conhecidas coletivamente como dicas.

As dicas ajudam os usuários a entender objetos desconhecidos ou desconhecidos que não são descritos diretamente na interface do usuário. Eles são exibidos automaticamente quando os usuários passarem o ponteiro sobre um objeto e removidos quando os usuários clicam no controle ou movem o mouse ou quando a dica se apaga.

**Desenvolvedores:** Não há controle de infotip; as infotips são implementadas com o controle de dica de ferramenta. A distinção está no uso, não na implementação.

> [!Note]  
> Diretrizes [relacionadas a balão,](ctrl-balloons.md) [barras de ferramentas](cmd-toolbars.md)e [Ajuda](winenv-help.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **As informações são exibidas com base no foco do ponteiro?** Se não, use outro controle. Exibir dicas somente como resultado da interação do usuário nunca as exibe por conta própria. Por outro lado, [os balão podem](ctrl-balloons.md) ser exibidos por conta própria (como fazem com notificações), para que eles tenham uma cauda que identifica sua origem.
-   **Um controle tem um rótulo de texto?** Se não, use uma dica de ferramenta para fornecer o rótulo. Observe que a maioria dos controles deve ser rotulada e, portanto, não tem dicas de ferramenta. Controles de barra de ferramentas e botões de comando com rótulos gráficos devem ter dicas de ferramenta.
-   **Um objeto se beneficia de uma descrição complementar ou informações adicionais?** Se sim, use uma infotip. No entanto, o texto deve ser suplementar ou seja, não essencial para as tarefas primárias. Se for essencial, coloque-o diretamente na interface do usuário para que os usuários não precisem procurar nem buscá-lo.
-   **As informações complementares são um erro, aviso ou status?** Nesse caso, use outro elemento de interface do usuário, como um balão, [mensagem de erro](mess-error.md)ou barra de [status](ctrl-status-bars.md). As infotips de ícone da área de notificação são uma exceção porque podem ser usadas para mostrar informações de status.
-   **Os usuários precisam interagir com a dica?** Nesse caso, use outro controle, como um balão. Os usuários não podem interagir com dicas porque mover o mouse faz com que elas desapareçam.
-   **Os usuários precisam imprimir as informações complementares?** Nesse caso, use outro controle, como um campo de comentário estático. No entanto, você também pode usar infotips para fornecer acesso mais direto a essas informações.

    ![captura de tela do balão de comentário ](images/ctrl-tooltips-and-infotips-image3.png)

    Neste exemplo, um campo de comentário estático no Microsoft Word permite que os usuários imprimam comentários.

-   **O contexto é tal que os usuários podem achar as dicas entediantes ou desalocar?** Nesse caso, considere usar outra solução, incluindo não fazer nada. Se você usar dicas nesses contextos, permita que os usuários as desliguem.

Quando usadas adequadamente, as dicas melhoram a comunicação com o usuário. **Nunca use dicas como um substituto para um bom design.** Se um gráfico, um botão ou outro objeto exigir que os usuários continuem verificando uma dica para entender isso, o design será ruim. Corrige o design em vez disso.

## <a name="design-concepts"></a>Conceitos de design

Dicas são uma maneira eficiente de simplificar uma interface do usuário. Eles fornecem informações de que os usuários precisam quando precisam dela, com esforço mínimo de sua parte. As dicas podem ajudá-lo a usar o espaço na tela com mais eficiência e reduzir a desorganização da tela. No entanto, dicas mal projetadas podem ser entediantes, desinteressante, insaciáveis, sobrecarregáveis ou no caminho. Os conceitos de design a seguir destinam-se a mostrar a diferença.

### <a name="discoverability"></a>Detectabilidade

As dicas são exibidas automaticamente quando os usuários passar o ponteiro sobre um objeto por um período de tempo. Esse mecanismo de atraso de tempo torna as dicas muito convenientes, mas também reduz sua capacidade de descoberta.

Ao longo do tempo, os usuários aprendem que determinados objetos padrão, como botões de barra de ferramentas, botões gráficos, menu Iniciar itens e ícones de área de notificação, têm dicas para que você possa usar sua descoberta como concedida.

Leva mais tempo para os usuários descobrirem dicas em locais não padrão. Não há nenhuma dica visual, como um ponto de contato ou alteração de ponteiro, que indica que um objeto tem uma gorjeta. Pior ainda, alguns usuários movem muito o mouse, especialmente quando estão aprendendo a navegar na interface do usuário. Os usuários têm que saber que um objeto tem uma dica, seja pela experiência passada ou pela experimentação.

Você pode melhorar a descoberta usando dicas consistentemente, o que, por sua vez, promove a previsibilidade. Se você fornecer dicas para alguns objetos, forneça-os para todos os objetos semelhantes para os quais os usuários provavelmente querem informações complementares. Às vezes, fazer isso pode ser um desafio, pois você também deve garantir que as dicas sejam úteis e não óbvias.

Se fornecer dicas de descoberta consistentemente úteis provam ser um problema, considere designs alternativos, como rótulos de controle autoexplicativos ou texto suplementar in-locar.

### <a name="appropriate-information"></a>Informações apropriadas

As informações apropriadas para dicas têm as seguintes características:

-   **Concisa.** As janelas pop-up usadas por dicas são perfeitas para frases curtas e fragmentos de frase, bem como texto formatado. Blocos grandes e não formatados de texto são difíceis de ler e sobrecarregáveis.
-   **Útil.** O texto da dica deve ser informativo. Não deve ser óbvio ou apenas repetir o que já está na tela.
-   **Suplementar.** Como o texto da dica nem sempre está visível, deve ser informações complementares que os usuários não têm que ler. Informações importantes devem ser comunicadas usando rótulos de controle autoexplicativos ou texto suplementar in-locar.
-   **Estático.** Os usuários não esperam que as dicas mudem de uma instância para outra, portanto, é improvável que eles observem alterações no conteúdo dinâmico, como informações de status. As dicas de ícone da área de notificação são uma exceção notável: os usuários têm maior probabilidade de descobrir alterações nas informações de gorjeta porque esses ícones se comunicam principalmente com o status.

### <a name="appropriate-timeouts"></a>Tempos de vida apropriados

A exibição e remoção automática apropriadas de dicas é crucial para a meta dos usuários manterem o controle de seu ambiente de interface do usuário. As dicas têm três valores de tempoout:

-   **Inicial.** O tempo em que o ponteiro deve permanecer estacionário para que a dica seja exibida. O tempo padrão é 0,5 segundos.
-   **Reshow.** O tempo em que o ponteiro deve permanecer estacionário à medida que o ponteiro se move de um destino para outro. O tempo padrão é 0,1 segundo.
-   **Remoção.** A hora após a qual a dica é removida automaticamente. O tempo padrão é de 5 segundos.

Ter valores iniciais e de remostr muito curtos resulta em uma experiência entediante e interrupção, pois eles geralmente seriam mostrados inadvertidamente, enquanto que muito tempo resulta em dicas sem resposta ou não sendo descobertas. O tempo de remoção padrão funciona bem para texto de dica curta, conforme usado em dicas de ferramenta. As infotips têm texto mais longo, portanto, precisam de tempos de exibição mais longos.

### <a name="appropriate-placement"></a>Posicionamento apropriado

As dicas devem ser colocadas perto do objeto que está sendo colocado, geralmente na parte final ou na cabeça do ponteiro, se possível. No entanto, eles nunca devem ser colocados de forma que interfira no que o usuário está fazendo ao obscurecer o objeto de interesse. Impedir esse problema pode exigir que você mova a ponta para longe do ponteiro, mas adjacente ao objeto. Isso não é um problema, desde que a relação entre o objeto e sua dica esteja clara. Certifique-se de que os usuários não movam o ponteiro apenas para que as dicas do programa fiquem ausentes.

### <a name="accessibility"></a>Acessibilidade

As dicas têm um efeito incomum na acessibilidade. Embora elas sejam normalmente disparadas ao passar o ponteiro do mouse sobre um objeto, as dicas são manipuladas por [leitores de tela](inter-accessibility.md) para controles com acesso ao teclado. Quando usadas adequadamente para informações concisas, úteis, estáticas e complementares, as dicas podem melhorar a acessibilidade geral. Na verdade, o padrão de dica de texto ALT é a maneira preferida de tornar os elementos gráficos acessíveis. No entanto, quando usados inadequadamente, eles danificam a acessibilidade tornando informações importantes ou dinâmicas mais difíceis de serem obtidas.

Forneça mais de uma maneira de acessar um controle se esse controle exigir uma dica que não tenha acesso ao teclado.

![captura de tela do botão Imprimir com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image4.png)

Neste exemplo, os usuários podem imprimir usando o botão da barra de ferramentas (que não é acessível pelo teclado) ou o atalho de teclado do comando Imprimir.

**Se você fizer apenas uma coisa...**

Crie dicas detectáveis que exibam informações mais concisa, úteis e estáticas no local apropriado no momento apropriado.

## <a name="usage-patterns"></a>Padrões de uso

As dicas têm vários padrões de uso:



|    Uso                                                                                                                             |    Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dicas de ferramentas**<br/> exibe o rótulo de um controle ou glifo sem rótulo. <br/>                                         | Como essas dicas servem como rótulos, seu texto segue as diretrizes de rótulo para o controle subjacente. <br/> ![captura de tela do botão Exportar lista com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image5.png)<br/> Neste exemplo, a dica de ferramenta fornece o rótulo de comando.<br/> ![captura de tela do botão fechar com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image6.png)![captura de tela do botão reproduzir com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image7.png)<br/> nesses exemplos, as dicas de ferramenta rotulam botões gráficos.<br/> ![captura de tela do glifo do menu Mostrar com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image8.png)<br/> Neste exemplo, a dica de ferramenta rotula um glifo.<br/> |
| **Infotips**<br/> forneça uma descrição ou explicação suplementar de um objeto ou controle. <br/>                  | Use Infotips para descrever ou explicar objetos e controles como controles [da barra de ferramentas](cmd-toolbars.md) , [ícones](vis-icons.md) (incluindo sobreposições de ícone), [links](ctrl-links.md), [guias](ctrl-tabs.md), [controles de divulgação progressivos](ctrl-progressive-disclosure-controls.md)e controles personalizados. <br/> ![captura de tela do botão de email com InfoTip ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![captura de tela do botão gravar com InfoTip ](images/ctrl-tooltips-and-infotips-image10.png)<br/> Nestes exemplos, Infotips fornece informações complementares sobre controles e objetos.<br/>                                                                                        |
| **Infotips de texto alt**<br/> Descreva um gráfico para acessibilidade. <br/>                                              | Esse padrão é usado principalmente para usuários que têm alguma forma de deficiência visual e podem estar usando um leitor de tela. <br/> ![captura de tela do botão Iniciar do Windows com InfoTip ](images/ctrl-tooltips-and-infotips-image11.png)<br/> Neste exemplo, o InfoTip descreve o gráfico do menu iniciar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Miniaturas**<br/> exibe uma imagem pequena de um item. <br/>                                                         | As miniaturas fornecem uma representação gráfica facilmente reconhecível de uma janela ou documento. <br/> ![captura de tela da miniatura das categorias do painel de controle ](images/ctrl-tooltips-and-infotips-image12.png)<br/> Neste exemplo, a barra de tarefas do Windows fornece dicas de miniatura para seus itens.<br/> ![captura de tela de miniatura de foto e seus dados ](images/ctrl-tooltips-and-infotips-image13.png)<br/> Neste exemplo, a Galeria de fotos do Windows fornece dicas de miniatura para seus itens.<br/>                                                                                                                                                                                                                      |
| **Infotips de detalhes**<br/> exibe informações detalhadas sobre um objeto. <br/>                                        | Infotips são uma maneira eficaz de mostrar informações detalhadas sobre um objeto ou fornecer dados. <br/> ![captura de tela da InfoTip da foto mostrando o tipo de arquivo ](images/ctrl-tooltips-and-infotips-image14.png)![captura de tela do grafo com valores de detalhes de InfoTip ](images/ctrl-tooltips-and-infotips-image15.png)<br/> Nestes exemplos, Infotips fornece informações detalhadas sobre um objeto ou dados.<br/>                                                                                                                                                                                                                                                                                                      |
| **Menu iniciar Infotips**<br/> Descreva um item no menu iniciar. <br/>                                              | O menu iniciar consiste em nomes de programas e destinos importantes do Windows, como documentos, imagens e painel de controle. essas dicas descrevem os itens do menu Iniciar, normalmente fornecendo uma breve descrição do programa ou destino, bem como as tarefas principais que os usuários podem executar com ele. Essas descrições também são indexadas pela caixa de pesquisa do menu Iniciar, ajudando ainda mais os usuários a localizar os programas de que precisam. <br/> ![captura de tela do centro de boas-vindas ](images/ctrl-tooltips-and-infotips-image16.png)<br/> Neste exemplo, o InfoTip descreve o que os usuários podem fazer com um programa no menu iniciar.<br/>                                                                                    |
| **Infotips do painel de controle**<br/> Descreva uma categoria ou tarefa do painel de controle. <br/>                                    | Essas dicas fornecem informações complementares para ajudar os usuários a escolher a categoria e o item do painel de controle corretos. <br/> ![captura de tela da categoria de contas de usuário com InfoTip ](images/ctrl-tooltips-and-infotips-image17.png)<br/> Neste exemplo, o InfoTip descreve a categoria do painel de controle de contas de usuário.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Nome completo Infotips**<br/> exibe o nome completo de um item quando o nome está truncado ou não está totalmente visível. <br/> | Essas dicas permitem que você exiba itens em um espaço mais compacto, reduzindo a necessidade de rolagem horizontal. Isso é especialmente importante quando o comprimento do conteúdo é desconhecido porque é dinâmico. ao contrário dos outros padrões, quando usados em listas e árvores, essas dicas são exibidas diretamente sobre o objeto de origem. <br/> ![captura de tela do grupo de botões de opção-título InfoTip ](images/ctrl-tooltips-and-infotips-image18.png)<br/> Neste exemplo, um InfoTip é usado para exibir o nome completo do item ao focalizar.<br/>                                                                                                                                                                                     |
| **Infotips de status**<br/> exibir informações de status para ícones da área de notificação. <br/>                              | Normalmente, as dicas devem ser estáticas porque os usuários não esperam que elas mudem de uma instância para a seguinte. os **ícones da área de notificação são uma exceção** porque esses ícones comunicam o status e não há nenhum outro espaço de tela disponível para o texto de status. <br/> ![captura de tela de ' Messenger não conectado ' InfoTip ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![captura de tela da InfoTip ' Messenger conectado ' ](images/ctrl-tooltips-and-infotips-image20.png)<br/> Nestes exemplos, Infotips fornece informações de status para ícones da área de notificação.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Diretrizes

### <a name="timeouts"></a>Tempos limite

-   **Use os tempos limite padrão inicial e de reexibição. Exception**
    -   As miniaturas que não são redundantes e exibidas no lado do objeto associado podem ser mostradas imediatamente (sem nenhum atraso). No entanto, use o tempo limite inicial padrão para miniaturas redundantes (como uma grande dica de miniatura para um pequeno objeto gráfico) ou miniaturas que abrangem o objeto associado.
-   **Para dicas de ferramenta, use o tempo limite de remoção da dica de cinco segundos padrão.**
-   **Para infotips, desative o tempo limite de remoção de gorjeta. Desenvolvedores:** como você não pode tecnicamente desativar o tempo limite de remoção, defina-o como seu maior valor.
-   Para acessibilidade, se você precisar definir os valores de tempo limite como algo diferente do valor máximo, torne-os múltiplos dos parâmetros de \_ sistema SPI GETMOUSEHOVERTIME e SPI \_ GETMESSAGEDURATION em vez de usar horários fixos. Isso ajusta os tempos limite para a velocidade do usuário.

### <a name="placement"></a>Posicionamento

-   **Evite abranger o objeto do qual o usuário está prestes a exibir ou interagir.** Sempre coloque a ponta no lado do objeto, mesmo se isso exigir a separação entre o ponteiro e a dica. Algumas separações não são um problema, contanto que a relação entre o objeto e sua gorjeta seja clara.

    -   **Exceção:** Dicas de ferramentas de nome completo usadas em listas e árvores.

    **Incorreto:**

    ![captura de tela da caixa de pesquisa de obscurecimento de InfoTip ](images/ctrl-tooltips-and-infotips-image21.png)

    **Correto:**

    ![captura de tela da InfoTip colocada abaixo da caixa de pesquisa ](images/ctrl-tooltips-and-infotips-image22.png)

    No exemplo correto, o InfoTip é colocado fora da caixa de pesquisa, embora isso exija espaço entre ela e o cursor.

    **Incorreto:**

    ![captura de tela do texto revisado de obscurecimento de InfoTip ](images/ctrl-tooltips-and-infotips-image23.png)

    **Correto:**

    ![captura de tela de infotip colocada acima do texto revisado ](images/ctrl-tooltips-and-infotips-image24.png)

    No exemplo correto, o texto subjacente é muito mais útil do que o Tip, portanto, o InfoTip é colocado bem fora do caminho.

-   **Para coleções de itens, evite abranger o próximo objeto do qual o usuário provavelmente exibirá ou interagirá.** Para itens organizados horizontalmente, evite colocar dicas à direita; para itens organizados verticalmente, evite colocar as dicas abaixo.

    **Incorreto:**

    ![captura de tela da lista de itens recentes de obscurecimento de InfoTip ](images/ctrl-tooltips-and-infotips-image25.png)

    **Correto:**

    ![captura de tela da InfoTip ao lado da lista de itens recentes ](images/ctrl-tooltips-and-infotips-image26.png)

    No exemplo incorreto, a dica cobre o objeto que o usuário tem mais probabilidade de interagir com o próximo.

-   **Para dicas potencialmente discadas (muitas vezes grandes), certifique-se de que as informações sejam úteis para a maioria dos usuários.** Se esse não for o caso, torne as dicas de distração opcionais ou até mesmo elimine-as. Caso contrário, a maioria dos usuários precisará mover o ponteiro para longe do objeto de destino para livrar-se da gorjeta.

### <a name="tooltips"></a>Dicas de ferramenta

-   **Use dicas de ferramenta para fornecer rótulos para controles sem rótulo.** Controles que normalmente têm dicas de ferramenta são [botões de barra de ferramentas](cmd-toolbars.md), botões gráficos e controles de [divulgação progressiva](ctrl-progressive-disclosure-controls.md). Controles com prompts são considerados rotulados, como [caixas de texto](ctrl-text-boxes.md) e [caixas de combinação](/windows/desktop/uxguide/ctrl-drop). Todos os outros controles devem ter rótulos explícitos.
-   Use fragmentos de frase sem pontuação final.
-   Use a capitalização com estilo de frase.
    -   **Exceção:** Essa diretriz é nova para o Windows Vista. Para aplicativos herdados, você pode usar a capitalização no estilo de título, se necessário, para evitar a mistura de estilos de capitalização.
-   Adicione uma [elipse](ctrl-command-buttons.md) se o rótulo for para um comando que precisa de informações adicionais.
-   Assim como acontece com rótulos normais, **Mantenha as dicas de ferramentas breves** geralmente cinco palavras ou menos, mas prefira rótulos específicos em relação a vagas.

    **Aceitável:**

    ![captura de tela da dica de ferramenta imprimir ](images/ctrl-tooltips-and-infotips-image27.png)

    **Melhor:**

    ![captura de tela da dica de ferramenta ' Imprimir para impressora padrão ' ](images/ctrl-tooltips-and-infotips-image28.png)

    **Recomendá**

    ![captura de tela da dica de ferramenta ' Imprimir (gravador de documento) ' ](images/ctrl-tooltips-and-infotips-image29.png)

    **Incorreto:**

    ![captura de tela da dica de ferramenta detalhada ](images/ctrl-tooltips-and-infotips-image30.png)

    Nesses exemplos, o melhor exemplo é conciso e específico, enquanto que o exemplo incorreto é desnecessariamente detalhado.

-   **Dicas de ferramenta também podem fornecer mais detalhes para botões de barra de ferramentas rotulados se isso for útil.** Não apenas repita ou dê uma renomeação de palavras do que já está no rótulo.

    **Correto:**

    ![captura de tela da dica de ferramenta ' Pesquisar todos os Outlook ' ](images/ctrl-tooltips-and-infotips-image31.png)

    Neste exemplo, a dica de ferramenta explica o que a pesquisa faz.

    **Incorreto:**

    ![captura de tela do rótulo do botão de repetição de dica de ferramenta ](images/ctrl-tooltips-and-infotips-image32.png)

    Neste exemplo, a dica de ferramenta apenas repete o que já está no rótulo.

-   **Você não precisa fornecer dicas de ferramentas de controles rotuladas simplesmente para fins de consistência.**

    ![captura de tela de botões rotulados e sem rótulo ](images/ctrl-tooltips-and-infotips-image33.png)

    Neste exemplo, os botões de barra de ferramentas sem rótulo têm dicas de ferramenta, mas os rotulados não.

-   Sempre que apropriado, **torne as dicas de ferramentas mais úteis fornecendo atalhos de teclado e valores padrão.** Coloque essas informações adicionais entre parênteses. Isso torna as dicas de ferramentas úteis para controles rotulados mesmo quando eles simplesmente repetim o rótulo. Não considere esse texto adicional ao avaliar a cocisão de uma dica de ferramenta.

    ![captura de tela da dica de ferramenta ' Imprimir (gravador de documento) ' ](images/ctrl-tooltips-and-infotips-image29.png)

    Neste exemplo, o Word exibe valores padrão e atalhos de teclado nas dicas de ferramenta da barra de ferramentas.

### <a name="infotips"></a>Infotips

-   **Para Infotips em locais não padrão, favorecer a consistência em relação à utilidade para melhorar a capacidade de descoberta.** Forneça dicas para todos os objetos para os quais os usuários provavelmente desejarão informações complementares, mesmo que alguns Infotips possam ser óbvios. Isso evita que os usuários aguardem um InfoTip que nunca será fornecido.
    -   **Exceção:** Se apenas alguns objetos tiverem Infotips úteis, não use o Infotips. Em vez disso, use rótulos de controle autoexplicativos ou texto suplementar in-loco.
-   Use frases completas com pontuação final.
    -   **Exceção:** Ícone da área de notificação [Infotips](winenv-notification.md) não use pontuação final.
-   Use a capitalização com estilo de frase.
-   Use conjugação presente e não futuro.
-   Usar construções gramaticais paralelas. O paralelismo exige que as palavras e frases que têm a mesma função tenham o mesmo formato.
    -   **Exceção:** Para o padrão InfoTip de nome completo, o texto InfoTip corresponde exatamente à frase, à capitalização e à Pontuação do controle subjacente.
-   **Evite grandes Infotips.** Grandes Infotips são difíceis de ler e são difíceis de se posicionar sem interferir no objeto subjacente.
-   **Formate Infotips para tornar seu conteúdo mais fácil de ler e verificar.** Blocos grandes de texto não formatado podem ser difíceis de ler.

    **Incorreto:**

    ![captura de tela de dica de ferramenta de execução longa, não estruturada ](images/ctrl-tooltips-and-infotips-image34.png)

    **Correto:**

    ![captura de tela da mesma dica de ferramenta com uma linha por item ](images/ctrl-tooltips-and-infotips-image35.png)

    No exemplo correto, o texto formatado é muito mais fácil de ler e examinar.

-   Na primeira utilização dentro de uma InfoTip, soletrar os nomes de acrônimos, seguido pelo acrônimo entre parênteses. Exemplo: "protocolo de configuração dinâmica de hosts (DHCP)".

### <a name="start-menu-infotips"></a>Menu iniciar Infotips

-   Use o menu iniciar Infotips para **descrever o item de forma concisa e listar as tarefas principais que os usuários podem executar com o item.**
-   **Seja útil.** Concentre-se no que os usuários podem fazer. Não basta repetir o nome do item ou até mesmo usá-lo na descrição.
-   **Seja específico.** Evite verbos genéricos e expressões catch-all como e outras tarefas. Se as informações forem importantes, liste-as especificamente; caso contrário, suponha que os usuários entendam que nem tudo está listado no Infotips.
-   **Seja conciso.** Use 25 palavras ou menos. Infotips mais desejando a leitura.
-   **Comece com um verbo conjugação, imperativo,** como criar, editar, mostrar e enviar. Prefira verbos específicos sobre verbos genéricos, como gerenciar e abrir, que realmente se aplicam à maioria dos itens do menu iniciar. Fique à direita até o ponto.

    **Incorreto:**

    ![captura de tela da dica de ferramenta: abre a pasta música ](images/ctrl-tooltips-and-infotips-image36.png)

    **Melhor:**

    ![captura de tela da dica de ferramenta: armazenar e reproduzir música ](images/ctrl-tooltips-and-infotips-image37.png)

    No exemplo incorreto, o InfoTip começa com um verbo genérico. O exemplo melhor Obtém-se diretamente no ponto com verbos específicos, mas continua usando as frases "e outras" desnecessárias no final da gorjeta.

-   **Não use um idioma que pareça marketing.**

    **Incorreto:**

    ![captura de tela do InfoTip ' ponto de partida ' One-Stop ](images/ctrl-tooltips-and-infotips-image38.png)

    Neste exemplo, o InfoTip soa como marketing.

-   Como esses Infotips são indexados para a caixa de pesquisa do menu Iniciar, **Descreva as tarefas importantes do seu programa usando os termos para os quais os usuários têm mais probabilidade de Pesquisar. Considere o uso de palavras-chave e sinônimos comuns.**

    **Incorreto:**

    ![captura de tela da dica de ferramenta: criar dvds ](images/ctrl-tooltips-and-infotips-image39.png)

    **Correto:**

    ![captura de tela da dica de ferramenta: criar (gravar) cds, dvds ](images/ctrl-tooltips-and-infotips-image40.png)

    No exemplo correto, a infotip tem sinônimos comuns.

-   Use a capitalização com estilo de frase.
-   **Desenvolvedores:** O menu Iniciar do infotip do item vem do campo Comentário do item.

### <a name="quick-launch-tooltips"></a>Início Rápido dicas de ferramenta

-   **Use uma dica de ferramenta com o formato:** Iniciar (nome completo do programa)
-   Não use pontuação final.
-   Não use texto adicional para descrever o programa ou o que ele faz. Como os usuários escolhem os programas exibidos na barra Início Rápido, eles já sabem sua finalidade.

### <a name="control-panel-infotips"></a>Painel de Controle infotips

-   Use Painel de Controle infotips para descrever **concisamente as tarefas Painel de Controle e o hardware e o software configurados.**
-   **Painel de Controle nomes e ícones devem ter infotips.** Tarefas individuais não têm dicas de ferramenta.
-   **Ser útil.** Concentre-se no que os usuários podem fazer. Não apenas repita o nome Painel de Controle item ou até mesmo use-o na descrição.
-   **Seja específico.** Evite verbos genéricos e catch-all frases como e outro hardware. Se as informações são importantes, liste-as especificamente; caso contrário, suponha que os usuários entendam que nem tudo está listado nas infotips.

    **Incorreto:**

    ![captura de tela da dica de ferramenta: configura o mouse ](images/ctrl-tooltips-and-infotips-image41.png)

    **Correto:**

    ![captura de tela da dica de ferramenta detalhada para configurações do mouse ](images/ctrl-tooltips-and-infotips-image42.png)

    No exemplo correto, os tipos de hardware configurados são listados especificamente.

-   **Seja conciso.** Use 25 palavras ou menos. Infotips mais longos não desestimuem a leitura.
-   **Comece com um verbo imperativo e presente.**

    **Correto:**

    Definir configurações de conexão e exibição da Internet.

    Ajuste as configurações de visão, auditiva e mobilidade.

-   **Vá direto para o ponto.** Não use o idioma que se aplica a qualquer Painel de Controle, como "Usar para exibir e definir configurações para a aparência e a funcionalidade do seu..." ou "Fornece opções para você..."
-   Não use uma linguagem que pareça marketing.

    **Incorreto:**

    Seu ponto de partida único para todas as suas necessidades de configuração de disco.

-   Como essas infotips são indexadas para a Painel de Controle de pesquisa, descreva os itens que usam termos para os quais os usuários têm maior probabilidade **de pesquisar.** Considere o uso de sinônimos comuns para tarefas e objetos populares.

    ![captura de tela da dica de ferramenta com tarefas do controlador de jogo ](images/ctrl-tooltips-and-infotips-image43.png)

    Neste exemplo, o item é descrito usando termos para os quais os usuários têm maior probabilidade de pesquisar.

-   Se um Painel de Controle item for provavelmente confundido com outras pessoas, explique como ele é diferente na dica de informação.

    **Incorreto:**

    ![captura de tela do infotip sem detalhes específicos ](images/ctrl-tooltips-and-infotips-image44.png)

    Neste exemplo, os Painel de Controle itens configuram o som, mas o infotip não esclarece a diferença.

    **Correto:**

    ![captura de tela do infotip com detalhes específicos ](images/ctrl-tooltips-and-infotips-image45.png)

    Neste exemplo, a diferença entre os dois itens é mais evidente devido à gorjeta.

### <a name="icons"></a>Ícones

Ao contrário das versões anteriores do Windows, o Windows Vista permite que as dicas tenham ícones.

-   Para dicas de ferramenta, não use ícones.
-   Para infotips, use ícones somente se eles ajudarem no reconhecimento ou na compreensão ou fornecerem contexto. A maioria das infotips não deve ter ícones.

    ![captura de tela da infotip de volume com o ícone de fone de ouvido ](images/ctrl-tooltips-and-infotips-image46.png)

    Neste exemplo, a infotip tem um ícone para ajudar a associar o ícone ao seu significado.

-   O ícone deve usar o [estilo Aero](vis-icons.md) e ter uma aparência não discreta.

Para ver exemplos e diretrizes gerais de ícone, consulte [Ícones](vis-icons.md).

## <a name="documentation"></a>Documentação

Ao se referir a dicas:

-   Na programação e em outras documentações técnicas, consulte o tipo de dica (dica de ferramenta ou infotip). Em qualquer outro lugar, basta chamá-lo de dica.
-   As seguintes variações estão incorretas: dica de ferramenta, Dica de ferramenta e Dica de Ferramenta.
-   Para descrever a interação do usuário, use hover.

