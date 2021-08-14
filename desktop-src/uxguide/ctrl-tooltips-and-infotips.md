---
title: Dicas de ferramenta e Infotips
description: Uma dica de ferramenta é uma pequena janela pop-up que rotula o controle sem rótulo que está sendo apontado, como controles de barra de ferramentas ou botões de comando sem rótulo.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4df7950529b2ac78c9d9bbf51c8996f17bcd985898a286f8d58e05db3b94d27e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118040977"
---
# <a name="tooltips-and-infotips"></a>Dicas de ferramenta e Infotips

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma dica de ferramenta é uma pequena janela pop-up que rotula o controle sem rótulo que está sendo apontado, como controles de barra de ferramentas ou botões de comando sem rótulo.

![Captura de tela que mostra o botão Imprimir com a dica de ferramenta ' Print (Ctrl + P) ' exibida.](images/ctrl-tooltips-and-infotips-image1.png)

Uma dica de ferramenta típica para um botão da barra de ferramentas.

Como as dicas de ferramentas provaram tão úteis, um controle relacionado chamado Infotips existe, que fornece um texto mais descritivo do que é possível com dicas de ferramenta.

um infotip é uma pequena janela pop-up que descreve de forma concisa o objeto que está sendo apontado, como descrições de controles da barra de ferramentas, ícones, elementos gráficos, links, objetos do Windows Explorer, itens de menu Iniciar e botões da barra de tarefas. Infotips são uma forma de [controles de divulgação progressivos](ctrl-progressive-disclosure-controls.md), eliminando a necessidade sempre de ter texto descritivo na tela.

![captura de tela do botão compartilhar com InfoTip ](images/ctrl-tooltips-and-infotips-image2.png)

Um InfoTip típico.

Para os fins deste artigo, tooltips e Infotips são referidos coletivamente como dicas.

Dicas ajudar os usuários a entender objetos desconhecidos ou desconhecidos que não são descritos diretamente na interface do usuário. Eles são exibidos automaticamente quando os usuários focalizam o ponteiro sobre um objeto e são removidos quando os usuários clicam no controle ou movem o mouse, ou quando a gorjeta atinge o tempo limite.

**Desenvolvedores:** Não há controle InfoTip; Infotips são implementados com o controle ToolTip. A distinção está em uso, não na implementação.

> [!Note]  
> As diretrizes relacionadas a [balões](ctrl-balloons.md), [barras de ferramentas](cmd-toolbars.md)e [ajuda](winenv-help.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **As informações são exibidas com base no foco do ponteiro?** Se não, use outro controle. Exibir dicas somente como resultado da interação do usuário nunca exibi-las por conta própria. Por outro lado, os [balões](ctrl-balloons.md) podem ser exibidos por conta própria (como acontece com notificações), portanto, eles têm uma cauda que identifica sua origem.
-   **Um controle tem um rótulo de texto?** Se não, use uma dica de ferramenta para fornecer o rótulo. Observe que a maioria dos controles deve ser rotulada e, portanto, não ter dicas de ferramenta. Os controles da barra de ferramentas e os botões de comando com rótulos gráficos devem ter dicas de ferramenta.
-   **Um objeto se beneficia de uma descrição complementar ou mais informações?** Nesse caso, use um InfoTip. No entanto, o texto deve ser suplementar, ou seja, não essencial para as tarefas principais. Se for essencial, coloque-o diretamente na interface do usuário para que os usuários não precisem procurar nem buscá-lo.
-   **As informações complementares são um erro, aviso ou status?** Nesse caso, use outro elemento de interface do usuário, como um balão, uma [mensagem de erro](mess-error.md)ou uma [barra de status](ctrl-status-bars.md). Ícone de área de notificação Infotips são uma exceção porque podem ser usadas para mostrar informações de status.
-   **Os usuários precisam interagir com a dica?** Nesse caso, use outro controle, como um balão. Os usuários não podem interagir com dicas porque mover o mouse faz com que elas desapareçam.
-   **Os usuários precisam imprimir as informações complementares?** Nesse caso, use outro controle, como um campo de comentário estático. No entanto, você também pode usar o Infotips para fornecer acesso direto a essas informações.

    ![captura de tela do balão de comentário ](images/ctrl-tooltips-and-infotips-image3.png)

    neste exemplo, um campo de comentário estático no Microsoft Word permite que os usuários imprimam comentários.

-   **O contexto é para que os usuários possam encontrar as dicas irritantes ou distraindo?** Nesse caso, considere usar outra solução, incluindo fazer nada. Se você usar dicas em tais contextos, permita que os usuários os desativem.

Quando usado adequadamente, as dicas melhoram a comunicação com o usuário. **Nunca use dicas como um substituto para um bom design.** Se um elemento gráfico, um botão ou outro objeto exigir que os usuários continuem verificando uma dica para entender, o design é inadequado. Em vez disso, corrija o design.

## <a name="design-concepts"></a>Conceitos de design

Dicas são uma maneira poderosa de simplificar uma interface do usuário. Eles fornecem informações de que os usuários precisam quando precisam, com esforço mínimo de sua parte. Dicas pode ajudá-lo a usar o espaço da tela com mais eficiência e reduzir a desordem na tela. No entanto, dicas mal projetadas podem ser irritantes, distração, não auxiliares, incorretas ou no caminho. Os conceitos de design a seguir destinam-se a mostrar a diferença.

### <a name="discoverability"></a>Detectabilidade

Dicas exibir automaticamente quando os usuários passarem o ponteiro do mouse sobre um objeto por um período de tempo. Esse mecanismo de atraso de tempo torna as dicas muito convenientes, mas também reduz a sua capacidade de descoberta.

ao longo do tempo, os usuários aprendem que determinados objetos padrão, como botões da barra de ferramentas, botões gráficos, itens de menu Iniciar e ícones da área de notificação, têm dicas, para que você possa levar sua capacidade de descoberta para a concessão.

Leva os usuários mais tempo para descobrir dicas em locais não padrão. Não há nenhuma pista visual, como uma alteração de ponteiro ou ponto de acesso, que indica que um objeto tem uma gorjeta. Pior ainda, alguns usuários movem o mouse em excesso, especialmente quando eles estão aprendendo a navegar pela interface do usuário. Os usuários precisam saber que um objeto tem uma gorjeta, seja por experiência passada ou por experimentação.

Você pode melhorar a descoberta usando dicas de forma consistente, o que, por sua vez, promove a previsibilidade. Se você fornecer dicas para alguns objetos, deverá fornecê-los para todos os objetos semelhantes para os quais os usuários provavelmente desejarão informações complementares. Às vezes, fazer isso pode ser desafiador, pois você também deve ter certeza de que as dicas são úteis e não óbvias.

Se fornecer dicas detectáveis, úteis de forma consistente, comprova ser um problema, considere designs alternativos, como rótulos de controle autoexplicativos ou texto suplementar in-loco.

### <a name="appropriate-information"></a>Informações apropriadas

As informações apropriadas para obter dicas têm as seguintes características:

-   **Visão.** As janelas pop-up usadas por dicas são perfeitos para frases curtas e fragmentos de sentença, bem como texto formatado. Blocos de texto Grandes e não formatados são difíceis de ler e sobrecarregar.
-   **Complementos.** O texto da dica deve ser informativo. Não deve ser óbvio ou apenas repetir o que já está na tela.
-   **Complementares.** Como o texto da dica nem sempre está visível, ele deve ser uma informação complementar que os usuários não precisam ler. Informações importantes devem ser comunicadas usando rótulos de controle autoexplicativos ou texto suplementar in-loco.
-   **Auto-estática.** Os usuários não esperam que as dicas mudem de uma instância para outra, portanto, é improvável que eles percebam alterações no conteúdo dinâmico, como informações de status. Dicas de ícone da área de notificação são uma exceção notável: os usuários têm mais probabilidade de descobrir alterações nas informações de Tip porque esses ícones se comunicam principalmente com o status.

### <a name="appropriate-timeouts"></a>Tempos limite apropriados

A exibição automática apropriada e a remoção de dicas são cruciais para a meta de usuários que mantêm o controle de seu ambiente de interface do usuário. Dicas ter três valores de tempo limite:

-   **This.** A hora em que o ponteiro deve permanecer fixo para que a dica apareça. O tempo padrão é de 0,5 segundos.
-   **Reexibir.** A hora em que o ponteiro deve permanecer estacionário como o ponteiro se move de um destino para outro. O tempo padrão é de 0,1 segundos.
-   **Removidos.** O tempo após o qual a gorjeta é automaticamente removida. O tempo padrão é de 5 segundos.

Ter valores iniciais e remostrados muito curtos resulta em uma experiência irritante e sem interrupções, pois eles geralmente seriam mostrados inadvertidamente, enquanto muito longos resultam em dicas que não respondem ou não estão sendo descobertos. O tempo de remoção padrão funciona bem para texto de dica curta, conforme usado nas dicas de ferramenta. Infotips têm texto mais longo, portanto, eles precisam de mais tempo de exibição.

### <a name="appropriate-placement"></a>Posicionamento apropriado

Dicas deve ser colocado perto do objeto que está sendo focalizado, geralmente na parte final ou na cabeça do ponteiro, se possível. No entanto, eles nunca devem ser colocados de uma maneira que interfere no que o usuário está fazendo ocultando o objeto de interesse. Evitar esse problema pode exigir que você mova a dica para fora do ponteiro, mas adjacente ao objeto . Isso não é um problema, desde que a relação entre o objeto e sua dica seja clara. Certifique-se de que os usuários não movam o ponteiro apenas para obter as dicas do programa para desaparecer.

### <a name="accessibility"></a>Acessibilidade

Dicas têm um efeito incomum na acessibilidade. Embora eles normalmente sejam disparados ao passar o ponteiro [](inter-accessibility.md) sobre um objeto, as dicas são manipuladas pelos leitores de tela para controles com acesso ao teclado. Quando usadas adequadamente para informações concisas, úteis, estáticas e complementares, as dicas podem melhorar a acessibilidade geral. Na verdade, o padrão de dica de texto alt é a maneira preferencial de tornar os gráficos acessíveis. No entanto, quando usadas inadequadamente, elas prejudicam a acessibilidade, dificultando a obtenção de informações importantes ou dinâmicas.

Forneça mais de uma maneira de acessar um controle se esse controle exigir uma dica que não tenha acesso ao teclado.

![captura de tela do botão imprimir com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image4.png)

Neste exemplo, os usuários podem imprimir usando o botão da barra de ferramentas (que não é acessível pelo teclado) ou o atalho de teclado do comando Imprimir.

**Se você fizer apenas uma coisa...**

Projete dicas que exibem informações concisas, úteis, estáticas e complementares no local apropriado no momento apropriado.

## <a name="usage-patterns"></a>Padrões de uso

Dicas vários padrões de uso:



|    Uso                                                                                                                             |    Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dicas de ferramentas**<br/> exibe o rótulo de um controle ou glifo sem rótulo. <br/>                                         | Como essas dicas servem como rótulos, seu texto segue as diretrizes de rótulo para o controle subjacente. <br/> ![captura de tela do botão exportar lista com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image5.png)<br/> neste exemplo, a dica de ferramenta fornece o rótulo de comando.<br/> ![captura de tela do botão Fechar com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image6.png)![captura de tela do botão reproduzir com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image7.png)<br/> nesses exemplos, dicas de ferramenta rotulam botões gráficos.<br/> ![captura de tela de mostrar glifo de menu com dica de ferramenta ](images/ctrl-tooltips-and-infotips-image8.png)<br/> Neste exemplo, a dica de ferramenta rotula um glifo.<br/> |
| **Infotips**<br/> fornecem uma descrição ou explicação complementar de um objeto ou controle. <br/>                  | Use infotips para descrever ou explicar [](cmd-toolbars.md) objetos e [controles,](vis-icons.md) como controles de barra [](ctrl-progressive-disclosure-controls.md)de ferramentas, ícones (incluindo sobreposições de ícone), links , [guias,](ctrl-links.md) [controles](ctrl-tabs.md)de divulgação progressiva e controles personalizados. <br/> ![captura de tela do botão de email com infotip ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![captura de tela do botão gravar com infotip ](images/ctrl-tooltips-and-infotips-image10.png)<br/> Nesses exemplos, as infotips fornecem informações complementares sobre controles e objetos.<br/>                                                                                        |
| **Dicas de informações de texto alt**<br/> descrever um gráfico para acessibilidade. <br/>                                              | Esse padrão é principalmente para usuários que têm alguma forma de deficiência visual e podem estar usando um leitor de tela. <br/> ![captura de tela do botão Iniciar do Windows com infotip ](images/ctrl-tooltips-and-infotips-image11.png)<br/> Neste exemplo, a infotip descreve o gráfico menu Iniciar dados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Miniaturas**<br/> exibe uma pequena imagem de um item. <br/>                                                         | As miniaturas dão uma representação gráfica facilmente reconhecível de uma janela ou documento. <br/> ![captura de tela da miniatura de categorias do painel de controle ](images/ctrl-tooltips-and-infotips-image12.png)<br/> neste exemplo, a barra de tarefas do Windows fornece dicas em miniatura para seus itens.<br/> ![captura de tela da miniatura da foto e seus dados ](images/ctrl-tooltips-and-infotips-image13.png)<br/> Neste exemplo, o Windows Galeria de Fotos fornece dicas em miniatura para seus itens.<br/>                                                                                                                                                                                                                      |
| **Infotips de detalhes**<br/> exibe informações detalhadas sobre um objeto . <br/>                                        | As infotips são uma maneira eficaz de mostrar informações detalhadas sobre um objeto ou fornecer dados. <br/> ![captura de tela da infotip da foto mostrando o tipo de arquivo ](images/ctrl-tooltips-and-infotips-image14.png)![captura de tela do grafo com valores detalhados de infotip ](images/ctrl-tooltips-and-infotips-image15.png)<br/> Nesses exemplos, as infotips dão informações detalhadas sobre um objeto ou dados.<br/>                                                                                                                                                                                                                                                                                                      |
| **Dicas de informações do menu Iniciar**<br/> descrever um item no menu Iniciar. <br/>                                              | O menu Iniciar consiste em nomes de programas e destinos importantes do Windows, como documentos, imagens e painel de controle. Essas dicas descrevem itens de menu iniciar, normalmente, dando uma breve descrição do programa ou destino, bem como as tarefas primárias que os usuários podem executar com ele. essas descrições também são indexadas pela caixa de pesquisa do menu Iniciar, ajudando ainda mais os usuários a encontrar os programas necessários. <br/> ![captura de tela da infotip do centro de boas-vindas ](images/ctrl-tooltips-and-infotips-image16.png)<br/> Neste exemplo, o infotip descreve o que os usuários podem fazer com um programa no menu Iniciar.<br/>                                                                                    |
| **Painel de Controle infotips**<br/> descrever uma categoria ou tarefa do painel de controle. <br/>                                    | Essas dicas fornecem informações complementares para ajudar os usuários a escolher a categoria e o item do painel de controle corretos. <br/> ![captura de tela da categoria de contas de usuário com infotip ](images/ctrl-tooltips-and-infotips-image17.png)<br/> Neste exemplo, a infotip descreve a categoria contas de usuário Painel de Controle usuário.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Infotips de nome completo**<br/> exibe o nome completo de um item quando o nome é truncado ou não está totalmente visível. <br/> | Essas dicas permitem exibir itens em um espaço mais compacto, reduzindo a necessidade de rolagem horizontal. isso é especialmente importante quando o comprimento do conteúdo é desconhecido porque ele é dinâmico. ao contrário dos outros padrões, quando usadas em listas e árvores, essas dicas são exibidas diretamente sobre o objeto de origem. <br/> ![captura de tela da infotip group-title do botão de rádio ](images/ctrl-tooltips-and-infotips-image18.png)<br/> Neste exemplo, uma infotip é usada para exibir o nome completo do item ao passar o mouse.<br/>                                                                                                                                                                                     |
| **Infotips de status**<br/> exibir informações de status para ícones de área de notificação. <br/>                              | Normalmente, as dicas devem ser estáticas porque os usuários não esperam que eles alterem de uma instância para outra. **ícones de área de notificação** são uma exceção porque esses ícones comunicam o status e não há nenhum outro espaço de tela disponível para o texto de status. <br/> ![captura de tela do infotip "messenger não está assinado" ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![captura de tela da infotip 'messenger signed in' ](images/ctrl-tooltips-and-infotips-image20.png)<br/> Nesses exemplos, as infotips dão informações de status para ícones de área de notificação.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Diretrizes

### <a name="timeouts"></a>Tempos limite

-   **Use o padrão inicial e os tempos de vida de remostr. Exceção:**
    -   As miniaturas que não são redundantes e exibidas no lado do objeto associado podem ser mostradas imediatamente (sem nenhum atraso). No entanto, use o tempo máximo inicial padrão para miniaturas redundantes (como uma dica de miniatura grande para um objeto gráfico pequeno) ou miniaturas que abrangem seu objeto associado.
-   **Para dicas de ferramenta, use o tempo de remoção de gorjeta padrão de cinco segundos.**
-   **Para infotips, desligue o tempo de remoção da gorjeta. Desenvolvedores:** como tecnicamente não é possível desativar o tempo de remoção, de definido como seu maior valor.
-   Para acessibilidade, se você precisar definir os valores de tempo limite para algo diferente do valor máximo, faça com que eles façam múltiplos dos parâmetros do sistema SPI \_ GETMOUSEHOVERTIME e SPI GETMESSAGEDURATION em vez de usarem tempos \_ fixos. Isso ajusta os tempos limite à velocidade do usuário.

### <a name="placement"></a>Posicionamento

-   **Evite cobrir o objeto com o que o usuário está prestes a exibir ou interagir.** Sempre coloque a dica no lado do objeto, mesmo que isso exija separação entre o ponteiro e a dica. Alguma separação não é um problema, desde que a relação entre o objeto e sua dica seja clara.

    -   **Exceção:** Dicas de ferramenta de nome completo usadas em listas e árvores.

    **Incorreto:**

    ![captura de tela da caixa de pesquisa de obscuring infotip ](images/ctrl-tooltips-and-infotips-image21.png)

    **Correto:**

    ![captura de tela da infotip colocada abaixo da caixa de pesquisa ](images/ctrl-tooltips-and-infotips-image22.png)

    No exemplo correto, a infotip é colocada fora da caixa Pesquisar, mesmo que isso exija espaço entre ele e o a caret.

    **Incorreto:**

    ![captura de tela do infotip ocultando o texto revisado ](images/ctrl-tooltips-and-infotips-image23.png)

    **Correto:**

    ![captura de tela da infotip colocada acima do texto revisado ](images/ctrl-tooltips-and-infotips-image24.png)

    No exemplo correto, o texto subjacente é muito mais útil do que a dica, portanto, o infotip é colocado bem fora do caminho.

-   **Para coleções de itens, evite abranger o próximo objeto com o que o usuário provavelmente exibirá ou interagirá.** Para itens organizados horizontalmente, evite colocar dicas à direita; para itens organizados verticalmente, evite colocar dicas abaixo.

    **Incorreto:**

    ![captura de tela de infotip ocultando a lista de itens recentes ](images/ctrl-tooltips-and-infotips-image25.png)

    **Correto:**

    ![captura de tela da infotip ao lado da lista de itens recentes ](images/ctrl-tooltips-and-infotips-image26.png)

    No exemplo incorreto, a dica abrange o objeto com o maior probabilidade de o usuário interagir com o próximo.

-   **Para dicas potencialmente distração (geralmente grandes), certifique-se de que as informações são úteis para a maioria dos usuários.** Se esse não for o caso, faça as dicas de distração opcionais ou até mesmo elimine-as. Caso contrário, a maioria dos usuários terá que mover o ponteiro para fora do objeto de destino para se desfazer da gorjeta.

### <a name="tooltips"></a>Dicas de ferramenta

-   **Use dicas de ferramenta para fornecer rótulos para controles sem rótulo.** Controles que normalmente têm dicas de ferramenta são botões de barra de [ferramentas,](cmd-toolbars.md)botões gráficos e controles [de divulgação progressiva.](ctrl-progressive-disclosure-controls.md) Os controles com prompts são considerados rotulados, como caixas [de texto](ctrl-text-boxes.md) e caixas [de combinação](/windows/desktop/uxguide/ctrl-drop). Todos os outros controles devem ter rótulos explícitos.
-   Use fragmentos de frase sem terminar a pontuação.
-   Use a capitalização com estilo de frase.
    -   **Exceção:** Essa diretriz é nova para o Windows Vista. Para aplicativos herdado, você pode usar a capitalização de estilo de título, se necessário, para evitar a combinação de estilos de capitalização.
-   Adicione uma [reellipse](ctrl-command-buttons.md) se o rótulo for para um comando que precisa de informações adicionais.
-   Assim como com rótulos normais, **mantenha as dicas de ferramenta breves** normalmente com cinco palavras ou menos, mas prefira rótulos específicos em vez de outros.

    **Aceitável:**

    ![captura de tela da dica de ferramenta de impressão ](images/ctrl-tooltips-and-infotips-image27.png)

    **Melhor:**

    ![captura de tela da dica de ferramenta 'imprimir na impressora padrão' ](images/ctrl-tooltips-and-infotips-image28.png)

    **Melhor:**

    ![captura de tela da dica de ferramenta 'imprimir (document writer)' ](images/ctrl-tooltips-and-infotips-image29.png)

    **Incorreto:**

    ![captura de tela da dica de ferramenta detalhada ](images/ctrl-tooltips-and-infotips-image30.png)

    Nesses exemplos, o melhor exemplo é conciso e específico, enquanto o exemplo incorreto é detalhado desnecessariamente.

-   **Dicas de ferramenta também podem fornecer mais detalhes para botões de barra de ferramentas rotulados se isso for útil.** Não apenas repita ou dê uma restatementação wordy do que já está no rótulo.

    **Correto:**

    ![captura de tela da dica de ferramenta "pesquisar todas as perspectivas" ](images/ctrl-tooltips-and-infotips-image31.png)

    Neste exemplo, a dica de ferramenta explica o que a Pesquisa faz.

    **Incorreto:**

    ![captura de tela do rótulo do botão de repetição da dica de ferramenta ](images/ctrl-tooltips-and-infotips-image32.png)

    Neste exemplo, a dica de ferramenta apenas repete o que já está no rótulo.

-   **Você não precisa dar dicas de ferramenta de controles rotulados apenas por questão de consistência.**

    ![captura de tela de botões rotulados e sem rótulo ](images/ctrl-tooltips-and-infotips-image33.png)

    Neste exemplo, os botões da barra de ferramentas sem rótulo têm dicas de ferramenta, mas os rotulados não têm.

-   Sempre que apropriado, **torna as dicas de ferramenta mais úteis fornecendo atalhos de teclado e valores padrão.** Coloque essas informações adicionais entre parênteses. Isso torna as dicas de ferramenta úteis para controles rotulados, mesmo quando, de outra forma, apenas repetem o rótulo. Não considere esse texto adicional ao avaliar a conciso de uma dica de ferramenta.

    ![captura de tela da dica de ferramenta 'imprimir (document writer)' ](images/ctrl-tooltips-and-infotips-image29.png)

    Neste exemplo, o Word exibe valores padrão e atalhos de teclado nas dicas de ferramenta da barra de ferramentas.

### <a name="infotips"></a>Infotips

-   **Para infotips em locais não padrão, favoreça a consistência sobre a ajuda para melhorar a capacidade de descoberta.** Forneça dicas para todos os objetos para os quais os usuários provavelmente querem informações complementares, mesmo que algumas dicas de informações possam ser óbvias. Isso evita que os usuários aguardem por um infotip que nunca virá.
    -   **Exceção:** Se apenas alguns objetos têm infotips úteis, não use infotips. Em vez disso, use rótulos de controle autoexplicativos ou texto suplementar in-locar.
-   Use frases completas com pontuação final.
    -   **Exceção:** As [infotips de ícone da área de](winenv-notification.md) notificação não usam pontuação final.
-   Use a capitalização com estilo de frase.
-   Use o tempo presente, não o futuro.
-   Use construções gramaticais paralelas. O paralelismo requer que palavras e frases que têm a mesma função tenham a mesma forma.
    -   **Exceção:** Para o padrão de infotip de nome completo, o texto de infotip corresponde exatamente à frase, à capitalização e à pontuação do controle subjacente.
-   **Evite infotips grandes.** Infotips grandes são difíceis de ler e difíceis de posicionar sem interferir no objeto subjacente.
-   **Formatar infotips para facilitar a leitura e a verificação do conteúdo.** Grandes blocos de texto não formatado podem ser difíceis de ler.

    **Incorreto:**

    ![captura de tela de dica de ferramenta longa, não estruturada e em run on ](images/ctrl-tooltips-and-infotips-image34.png)

    **Correto:**

    ![captura de tela da mesma dica de ferramenta com uma linha por item ](images/ctrl-tooltips-and-infotips-image35.png)

    No exemplo correto, o texto formatado é muito mais fácil de ler e examinar.

-   No primeiro uso em uma infotip, esnohe os nomes de acrônimos, seguidos pelo acrônimo entre parênteses. Exemplo: "Protocolo DHCP".

### <a name="start-menu-infotips"></a>Dicas de informações do menu Iniciar

-   Use menu Iniciar infotips para **descrever o item de forma concisa** e listar as tarefas principais que os usuários podem executar com o item.
-   **Ser útil.** Concentre-se no que os usuários podem fazer. Não apenas repita o nome do item ou até mesmo use-o na descrição.
-   **Seja específico.** Evite verbos genéricos e catch-all frases como e outras tarefas. Se as informações são importantes, liste-as especificamente; caso contrário, suponha que os usuários entendam que nem tudo está listado nas infotips.
-   **Seja conciso.** Use 25 palavras ou menos. Infotips mais longos não desestimuem a leitura.
-   **Comece com um verbo presente e imperativo,** como criar, editar, mostrar e enviar. Prefira verbos específicos em vez de verbos genéricos, como gerenciar e abrir, que realmente se aplicam à maioria menu Iniciar itens. Vá direto para o ponto.

    **Incorreto:**

    ![captura de tela da dica de ferramenta: abre a pasta de música ](images/ctrl-tooltips-and-infotips-image36.png)

    **Melhor:**

    ![captura de tela da dica de ferramenta: armazenar e reproduzir música ](images/ctrl-tooltips-and-infotips-image37.png)

    No exemplo incorreto, a infotip começa com um verbo genérico. O melhor exemplo chega ao ponto com verbos específicos, mas continua a usar a frase desnecessária "e outras" no final da dica.

-   **Não use uma linguagem que pareça marketing.**

    **Incorreto:**

    ![captura de tela da infotip 'ponto de partida de uma parada' ](images/ctrl-tooltips-and-infotips-image38.png)

    Neste exemplo, o infotip parece marketing.

-   Como essas infotips são indexadas para a menu Iniciar de pesquisa, descreva as tarefas importantes do programa usando termos para os quais os usuários têm maior probabilidade de **pesquisar. Considere o uso de palavras-chave e sinônimos comuns.**

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
-   Não use texto adicional para descrever o programa ou o que ele faz. Como os usuários escolhem os programas exibidos na Início Rápido, eles já sabem sua finalidade.

### <a name="control-panel-infotips"></a>Painel de Controle infotips

-   Use Painel de Controle infotips para descrever de forma concisa as **tarefas Painel de Controle e o hardware e o software configurados.**
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

-   **Vá direto para o ponto.** Não use o idioma que se aplica a Painel de Controle, como "Usar para exibir e definir configurações para a aparência e a funcionalidade do seu..." ou "Fornece opções para você..."
-   Não use uma linguagem que pareça marketing.

    **Incorreto:**

    Seu ponto de partida único para todas as suas necessidades de configuração de disco.

-   Como essas infotips são indexadas para a Painel de Controle de pesquisa, descreva os itens que usam termos para os quais os usuários têm maior probabilidade **de pesquisar.** Considere o uso de sinônimos comuns para tarefas e objetos populares.

    ![captura de tela da dica de ferramenta com tarefas do controlador de jogo ](images/ctrl-tooltips-and-infotips-image43.png)

    Neste exemplo, o item é descrito usando termos para os quais os usuários têm maior probabilidade de pesquisar.

-   Se um Painel de Controle item for provavelmente confundido com outros, explique como ele é diferente na infotip.

    **Incorreto:**

    ![captura de tela do infotip sem detalhes específicos ](images/ctrl-tooltips-and-infotips-image44.png)

    Neste exemplo, os Painel de Controle itens configuram o som, mas o infotip não esclarece a diferença.

    **Correto:**

    ![captura de tela do infotip com detalhes específicos ](images/ctrl-tooltips-and-infotips-image45.png)

    Neste exemplo, a diferença entre os dois itens é mais evidente devido à dica.

### <a name="icons"></a>Ícones

Ao contrário das versões Windows, Windows Vista permite que as dicas tenham ícones.

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

