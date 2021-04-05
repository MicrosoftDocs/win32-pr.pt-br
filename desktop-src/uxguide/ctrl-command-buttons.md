---
title: Botões de comando
description: Com um botão de comando, os usuários iniciam uma ação imediata.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 32c8c16cef275e1fefe44e579105515d3e61c497
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103663754"
---
# <a name="command-buttons"></a>Botões de comando

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um botão de comando, os usuários iniciam uma ação imediata.

![captura de tela do botão de comando Ok ](images/ctrl-command-buttons-image1.png)

Um botão de comando típico.

O botão de comando padrão é invocado quando os usuários pressionam a tecla Enter. Ele é atribuído pelo desenvolvedor, mas qualquer botão de comando torna-se o padrão quando os usuários a guiam.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **O botão de comando é usado para iniciar uma ação imediata?** Se não, use outro controle.
-   **Um link seria uma opção melhor?** Use um link se:
    -   A ação é navegar para outra página, janela ou tópico da ajuda. **Exceção**: a navegação do assistente usa botões de comando voltar e avançar.
    -   O comando é inserido em um corpo de texto.
    -   O comando é secundário por natureza. Ou seja, ele não se relaciona com a finalidade principal da janela. Nesse caso, um link ou botão de comando leve seria apropriado.
    -   O comando faz parte de um menu ou grupo de links relacionados.
    -   O rótulo é demorado, consistindo em cinco ou mais palavras, dando, assim, um botão de comando uma aparência estranha.
-   **Uma combinação de botões de opção e botões de comando genéricos seria uma opção melhor?** Frequentemente, os botões de opção são usados em conjunto com botões de comando genéricos (OK, cancelar) no lugar de um conjunto de botões de comando específicos quando qualquer uma das seguintes opções é verdadeira:
    -   Há cinco ou mais ações possíveis.
    -   Os usuários precisam exibir informações adicionais antes de tomar uma decisão.
    -   Os usuários precisam interagir com as opções (talvez para ver informações adicionais) antes de tomar uma decisão.
    -   Os usuários exibem as escolhas como opções em vez de comandos diferentes.

        **Correto:** ![ captura de tela de caixa de diálogo, botões de opção e texto ](images/ctrl-command-buttons-image2.png)

        Neste exemplo, os botões de opção são combinados com os botões OK e cancelar para fornecer informações adicionais sobre as opções.

        **Incorreto:** ![ captura de tela de mensagem com botões de comando ](images/ctrl-command-buttons-image3.png)

        Neste exemplo, os botões de comando sozinhos tornam difícil para os usuários tomar uma decisão informada.

## <a name="design-concepts"></a>Conceitos de design

**Usando reticências**

Embora os botões de comando sejam usados para ações imediatas, mais informações podem ser necessárias para executar a ação. **Indique um comando que precise de informações adicionais (incluindo confirmação) adicionando uma elipse ao final do rótulo do botão**.

![captura de tela do botão de comando Imprimir com reticências ](images/ctrl-command-buttons-image4.png)

Neste exemplo, a impressão... comando exibe uma caixa de diálogo de impressão para coletar mais informações.

![captura de tela do botão de comando Imprimir, sem reticências ](images/ctrl-command-buttons-image5.png)

Por outro lado, neste exemplo, o comando print imprime uma única cópia de um documento para a impressora padrão sem nenhuma interação adicional do usuário.

O **uso adequado de reticências é importante para indicar que os usuários podem fazer mais escolhas antes de executar a ação ou até mesmo cancelar a ação inteiramente**. A indicação visual oferecida por uma elipse permite que os usuários explorem seu software sem medo.

**Isso não significa que você deve usar uma elipse sempre que uma ação exibir outra janela** somente quando forem necessárias informações adicionais para executar a ação. Consequentemente, **qualquer botão de comando cujo verbo implícito é "mostrar outra janela" não leva uma elipse**, como com os comandos sobre, avançado, ajuda (ou qualquer outro comando vinculado a um tópico da ajuda), opções, propriedades ou configurações.

Em geral, as reticências são usadas em interfaces do usuário para indicar inintegridade. Comandos que mostram outras janelas não estão incompletos eles devem exibir outra janela e informações adicionais não são necessárias para executar a ação. Essa abordagem elimina a desordem na tela em situações em que as reticências têm pouco valor.

**Observação:** Ao determinar se um botão de comando precisa de uma elipse, não use a necessidade de [elevar privilégios](winenv-uac.md) como um fator. A elevação não é uma informação necessária para executar um comando (em vez disso, é para permissão) e a necessidade de elevação é indicada com a blindagem de segurança.

**Se você fizer apenas uma coisa...** Use um rótulo conciso, específico e auto-explicativo que descreva claramente a ação que o botão de comando executa e use uma elipse quando apropriado.

## <a name="usage-patterns"></a>Padrões de uso

Os botões de comando têm vários padrões de uso:



|                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botões de comando padrão** Você pode usar os botões de comando padrão para iniciar uma ação imediata.<br/>                                                           | ![captura de tela do botão de comando padrão (cinza) ](images/ctrl-command-buttons-image6.png)<br/> Um botão de comando padrão.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Botões de comando padrão** O botão de comando padrão em uma janela indica o botão de comando que será ativado quando os usuários pressionarem a tecla Enter.<br/>       | ![captura de tela do botão de comando padrão (azul) ](images/ctrl-command-buttons-image7.png)<br/> Um botão de comando padrão.<br/> Qualquer botão de comando torna-se o padrão quando os usuários a guiam. Se o foco de entrada estiver em um controle que não é um botão de comando, o botão de comando com o atributo de botão padrão se tornará o padrão. Somente um botão de comando em uma janela pode ser o padrão.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Botões de comando leves** Um botão de comando leve é semelhante a um botão de comando padrão, exceto que seu quadro de botão é mostrado apenas no foco do mouse. <br/> | ![captura de tela de um dos dois botões de impressão selecionados ](images/ctrl-command-buttons-image8.png)<br/> Neste exemplo, o comando tem uma aparência muito leve (semelhante a um [link](ctrl-links.md)) até que o usuário passe o mouse sobre o comando e, nesse ponto, ele é desenhado com um quadro de botão.<br/> Você pode usar botões de comando leves em situações em que você usaria um botão de comando padrão, mas deseja evitar sempre mostrar o quadro do botão. Os botões de comando leves são ideais para comandos que você deseja enfatizar e usar um link não seria apropriado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Botões de menu** Use um botão de menu quando precisar de um menu para um pequeno conjunto de comandos relacionados.<br/>                                                                 | ![captura de tela do botão de menu Formatar e seus comandos ](images/ctrl-command-buttons-image9.png)<br/> Um botão de menu com um pequeno conjunto de comandos relacionados.<br/> Use um botão de menu quando uma barra de menus não for desejável, como em uma caixa de diálogo, barra de ferramentas ou outra janela que não tenha uma barra de menus. Um único triângulo apontando para baixo indica que clicar no botão irá listar um menu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Botões de divisão** Use um botão de divisão para consolidar um conjunto de variações de um comando, especialmente quando um dos comandos for usado na maioria das vezes.<br/>          | ![captura de tela do botão abrir divisão sem comandos ](images/ctrl-command-buttons-image10.png)<br/> um botão de divisão recolhido.<br/> como um botão de menu, um único triângulo apontando para baixo indica que clicar na parte mais à direita do botão irá listar um menu.<br/> ![captura de tela do botão abrir divisão com comandos ](images/ctrl-command-buttons-image11.png)<br/> um botão de divisão descartada.<br/> Neste exemplo, um botão de divisão é usado para consolidar seis variações do comando Open. o comando normal Open é usado na maioria das vezes, de modo que os usuários normalmente não precisam ver os outros comandos. o uso de um botão de divisão economiza uma quantidade significativa de espaço na tela, além de fornecer opções poderosas.<br/> ao contrário de um botão de menu, clicar na parte esquerda do botão executa a ação diretamente no rótulo. os botões de divisão são eficazes em situações em que a próxima ação com uma ferramenta específica provavelmente será a mesma que a última ação. Nesse caso, o rótulo é alterado para a última ação, como com um seletor de cores:<br/> ![captura de tela do botão de divisão de preenchimento sem comandos ](images/ctrl-command-buttons-image12.png)<br/> Neste exemplo, o rótulo é alterado para a última ação.<br/> |
| **Botões de procura** Use um botão procurar para exibir uma caixa de diálogo para ajudar os usuários a selecionar um valor válido.<br/>                                                           | as caixas de diálogo iniciadas por um botão procurar ajudam os usuários a selecionar arquivos, pastas, computadores, usuários, cores e assim por diante. Normalmente, eles são combinados com um controle irrestrito, como uma caixa de texto. Normalmente, eles são rotulados como procurar, outros ou mais e sempre têm reticências para indicar que mais informações são necessárias. <br/> ![captura de tela da caixa de texto com o botão procurar ](images/ctrl-command-buttons-image13.png)<br/> uma caixa de texto com um botão procurar.<br/> para o Windows com muitos botões de procura, você pode usar uma versão curta:<br/> ![captura de tela do botão de navegação curto com reticências ](images/ctrl-command-buttons-image14.png)<br/> Um botão de navegação curto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Botões de divulgação progressiva** Use um botão de divulgação progressiva para mostrar ou Ocultar opções usadas com pouca frequência.<br/>                                            | Ocultar opções usadas raramente até que elas sejam necessárias é chamado de divulgação progressiva. as divisas duplas são usadas para indicar a divulgação progressiva e elas apontam na direção em que ocorrerá a revelação ou ocultação: <br/> ![captura de tela de botão com ' mais ' e setas à direita ](images/ctrl-command-buttons-image15.png)<br/> Depois que o botão é clicado, seu rótulo é alterado para indicar que o próximo clique terá o efeito oposto:<br/> ![captura de tela de botão com ' less ' e setas à esquerda ](images/ctrl-command-buttons-image16.png)<br/> Para obter mais informações e exemplos, consulte [controles de divulgação progressiva](ctrl-progressive-disclosure-controls.md). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Botões direcionais** Use um botão direcional para indicar a direção em que uma ação será realizada.<br/>                                               | Nesse caso, um único colchete angular é usado em vez de uma divisa dupla: <br/> ![captura de tela dos botões de seta à direita e à esquerda ](images/ctrl-command-buttons-image17.png)<br/> Um botão direcional indica a direção da ação.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Exibir um ponteiro ocupado se o resultado de clicar em um botão de comando não for instantâneo.** Sem comentários, os usuários podem assumir que o clique não aconteceu e clicar novamente.
-   Se o mesmo botão de comando aparecer em mais de uma janela, **tente usar o mesmo texto de rótulo e a chave de acesso e localize-o quase no mesmo local em cada janela quando for prático.**
-   **Para botões de comando com rótulos de texto, use uma largura de botão mínimo e a altura do botão de comando padrão.** Para obter mais informações, consulte [dimensionamento e espaçamento recomendados](#recommended-sizing-and-spacing).
-   Para cada janela, faça com que os **botões de comando tenham a mesma largura**. Se isso for impraticável, limite o número de larguras diferentes para botões de comando com rótulos de texto como dois.
-   Quando outro controle interopera com um botão de comando, como uma caixa de texto com um botão procurar, **denotará a relação colocando o botão de comando em um dos três locais:**
    -   À direita e alinhada na parte superior com o outro controle.
    -   Abaixo e alinhado à esquerda com o outro controle.
    -   Verticalmente centralizado entre controles que interoperam (como adicionar e remover botões entre duas caixas de listagem interoperação).
-   Se vários botões de comando interoperarem com o mesmo controle, **empilhe-os verticalmente à direita e alinhado na parte superior com o outro controle, ou coloque-os horizontalmente alinhados à esquerda sob o controle.**
-   Quando os botões de comando são subordinados a outros controles, **use o posicionamento acima e desabilite o botão de comando subordinado até que o controle superior seja selecionado.**
-   **Não use botões de comando estreitos, curtos ou altos com rótulos de texto** porque eles tendem a parecer não profissionais. Tente trabalhar com as larguras e alturas padrão.

**Correto:** ![ captura de tela do botão OK de tamanho padrão ](images/ctrl-command-buttons-image18.png)

Neste exemplo, o tamanho do botão é Standard e parece Professional.

**Incorreto:** ![ captura de tela de botão OK curto ](images/ctrl-command-buttons-image19.png)

Neste exemplo, o botão é muito pequeno.

**Incorreto:** ![ captura de tela de botão grande, quadrado Ok ](images/ctrl-command-buttons-image20.png)

Neste exemplo, o botão tem muito espaço em volta do rótulo.

-   **Evite combinar rótulos de texto e gráficos em botões de comando.** Combinar texto e gráficos geralmente adiciona uma desordem Visual desnecessária e não melhora a compreensão do usuário. Considere combinar texto e gráficos somente quando o elemento gráfico auxiliar na compreensão, como quando é um símbolo padrão para o comando ou ele ajuda os usuários a visualizar os resultados do comando. Caso contrário, prefira o texto, mas use texto ou elementos gráficos.

**Correto:** ![ captura de tela do comando girar com seta curva ](images/ctrl-command-buttons-image21.png)

Neste exemplo, o gráfico de seta ajuda os usuários a visualizar os resultados do comando.

**Correto:** ![ captura de tela da barra de endereços com ícones e texto ](images/ctrl-command-buttons-image22.png)

Neste exemplo, os símbolos padrão são combinados com texto para ajudar na compreensão

**Incorreto:** ![ captura de tela de botão com ícone x e cancelar ](images/ctrl-command-buttons-image23.png)

Neste exemplo, o gráfico cancelar não adiciona nada ao texto.

-   **Não use botões de comando para definir o estado**. Use botões de opção ou caixas de seleção em vez disso. Os botões de comando são apenas para ações de inicialização.

### <a name="split-buttons"></a>Botões de divisão

-   **Torne o comando mais provável o comportamento padrão**. Se houver mais de um comando provável, escolha um que não exija informações adicionais.
-   **Se o comando mais provável for a última seleção de usuário, altere o rótulo do botão para a última seleção.**
-   **Exiba o comando padrão usando texto em negrito no menu**. Isso facilita para os usuários a localização do comando padrão, especialmente quando o comando padrão é dinâmico ou o botão de divisão usa um elemento gráfico em vez de um rótulo de texto.

### <a name="default-values"></a>Valores padrão

-   Inclua um botão de comando padrão em cada caixa de diálogo. **Selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema) e o comando mais seguro para ser o padrão**. Se não houver fatores de segurança e segurança, selecione o comando mais provável ou conveniente.
-   **Não faça uma ação destrutiva no botão de comando padrão** , a menos que haja uma maneira fácil de desfazer o comando.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![diagrama de dimensões de botão em pixels e DLUs ](images/ctrl-command-buttons-image24.png)

Dimensionamento e espaçamento recomendados para botões de comando.

## <a name="labels"></a>Rótulos

-   Rotular cada botão de comando.
-   Se o botão tiver apenas um rótulo gráfico, atribua sua propriedade Name a um rótulo de texto apropriado. Isso permite que produtos de tecnologia assistencial, como leitores de tela, forneçam aos usuários informações alternativas sobre o gráfico.

    ![captura de tela dos botões para cima, para baixo e para copiar ](images/ctrl-command-buttons-image25.png)

    Este exemplo mostra botões gráficos; internamente, esses botões são rotulados como anterior, próximo e copiar.

-   Para botões de navegação curtos (rotulados como "..."), o rótulo interno deve ser procurado.
-   Atribua uma [chave de acesso](glossary.md)exclusiva. Para obter diretrizes, consulte [teclado](inter-keyboard.md).

    **Exceção**

    -   Não atribua chaves de acesso a botões OK e cancelar, pois Enter é a chave de acesso para o botão padrão (que geralmente é o botão OK) e ESC é a chave de acesso para cancelar. Isso torna as outras chaves de acesso mais fáceis de atribuir.
    -   Não atribua chaves de acesso aos botões de navegação breves (rotulados "..."), pois eles não podem ser atribuídos exclusivamente.

-   Prefira rótulos específicos sobre aqueles genéricos. Idealmente, os usuários não precisam ler mais nada para entender o rótulo. Os usuários têm muito mais probabilidade de ler rótulos de botão de comando do que texto estático.

    -   **Exceção:** Não renomeie o botão cancelar se o significado de Cancel não for ambíguo. Os usuários não devem ler todos os botões para determinar qual botão cancela uma ação. No entanto, renomeie cancelar se não estiver claro qual ação está sendo cancelada, como quando há várias ações pendentes.

    **Aceitável:**

    ![Captura de tela que mostra os botões ' OK ' e ' Cancelar '.](images/ctrl-command-buttons-image26.png)

    Neste exemplo, OK e cancelar são aceitáveis, mas rótulos não específicos.

    **Melhor:**

    ![captura de tela dos botões gravar CD e cancelar ](images/ctrl-command-buttons-image27.png)

    Neste exemplo, gravar CD é mais específico do que OK.

    **Incorreto:**

    ![captura de tela de gravar CD e não gravar botões de CD ](images/ctrl-command-buttons-image28.png)

    Neste exemplo, o cancelamento deve ser usado em vez de não gravar CD.

-   Inicie rótulos com um verbo imperativo e descreva claramente a ação que o botão executa. Não use pontuação final.
    -   **Exceção:** Os seguintes rótulos padrão são aceitáveis sem verbos: avançado, voltar, detalhes, avançar, menos, mais, novo, avançar, não, OK, opções, anterior, propriedades, configurações e sim.
-   Embora os rótulos curtos sejam preferenciais, use texto suficiente para explicar o comando suficientemente. Use um objeto direto (um substantivo após o verbo) quando o objeto não estiver aparente do contexto. Idealmente, os usuários não precisam ler mais nada para entender o rótulo.

    **Aceitável:**

    ![captura de tela de botão com Adicionar rótulo ](images/ctrl-command-buttons-image29.png)

    Neste exemplo, um rótulo curto é aceitável se seu significado no contexto é prontamente aparente.

    **Melhor:** (se Add não estiver claro)

    ![captura de tela do botão com o rótulo adicionar itens ](images/ctrl-command-buttons-image30.png)

    Neste exemplo, a adição de um substantivo ao verbo ajuda a compreensão dos usuários.

    **Melhor:** (se adicionar ou adicionar itens não estiver claro)

    ![captura de tela de botão com adicionar itens selecionados ](images/ctrl-command-buttons-image31.png)

    Neste exemplo, o rótulo é auto-explicativo.

-   Use [a capitalização no estilo de frase](glossary.md). Fazer isso é mais apropriado para o[Tom](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) do Windows de [Tom do Windows](text-style-tone.md)e o uso de frases curtas para botões de comando.
    -   **Exceção:** Para aplicativos herdados, você pode usar [a capitalização no estilo de título](glossary.md) , se necessário, para evitar a mistura de estilos de capitalização.
-   Não use agora nos rótulos do botão de comando porque o imediata do comando pode ser obtido para concedido.

    -   **Exceção:** Quando necessário, use agora para diferenciar comandos que iniciam uma tarefa a partir de comandos que executam uma tarefa imediatamente.

    ![captura de tela de botão com rótulo de download ](images/ctrl-command-buttons-image32.png)

    Neste exemplo, clicar no botão de comando vai para uma janela ou página que permite que os usuários façam o download.

    ![captura de tela de botão com rótulo baixar agora ](images/ctrl-command-buttons-image33.png)

    Neste exemplo, clicar no botão de comando executa o download.

    Somente um comando em um fluxo de tarefas deve ser rotulado com Now. Portanto, por exemplo, um comando **baixar agora** nunca deve ser seguido por outro comando **baixar agora** .

-   Não use mais tarde nos rótulos do botão de comando se ele implica uma ação que não acontecerá. Por exemplo, não use instalar mais tarde (em contraste para instalar agora), a menos que esse comando seja instalado posteriormente. Em vez disso, use não instalar ou cancelar.

    **Incorreto:**

    ![captura de tela de reinicialização agora e reinicialização posterior ](images/ctrl-command-buttons-image34.png)

    Neste exemplo, reiniciar mais tarde incorretamente significa que o comando é reiniciado automaticamente em um momento posterior.

-   Use um botão avançado somente para as opções que são relevantes para usuários avançados ou exigem conhecimento avançado do usuário. Não use um botão Avançado para recursos que são considerados tecnologicamente avançados. Por exemplo, o recurso de grampeamento de uma impressora não é uma opção avançada, mas seu sistema de gerenciamento de cores é.

    **Incorreto:** (se as opções realmente não forem avançadas)

    ![captura de tela de botão com rótulo avançado ](images/ctrl-command-buttons-image35.png)

    Neste exemplo, Advanced é enganoso.

    **Correto:**

    ![captura de tela de botão com rótulo mais opções ](images/ctrl-command-buttons-image36.png)

    Neste exemplo, o rótulo é mais específico e preciso.

-   Para botões de comando que abrem outras janelas, escolha um rótulo que use parte ou todo o texto da barra de título da janela secundária. Por exemplo, um botão de comando rotulado procurar pode abrir uma caixa de diálogo chamada procurar pasta. Usar a mesma terminologia em toda a tarefa ajuda a manter os usuários orientados.
-   Ao fazer uma pergunta, use rótulos que correspondam à pergunta. Não use OK/cancelar para responder a perguntas Sim/não.

    **Correto:**

    ![captura de tela dos botões Sim e não ](images/ctrl-command-buttons-image37.png)

    Neste exemplo, os botões respondem à pergunta.

    **Incorreto:**

    ![captura de tela dos botões OK e cancelar ](images/ctrl-command-buttons-image38.png)

    Neste exemplo, os botões não respondem à pergunta.

-   Termine o rótulo com uma elipse se o comando exigir informações adicionais a serem executadas.

    -   **Exceção:** Os rótulos gráficos não levam uma elipse.

    **Correto:** (se uma caixa de diálogo opções de impressão for exibida)

    ![captura de tela do botão Imprimir com reticências ](images/ctrl-command-buttons-image39.png)

    Neste exemplo, depois que o botão é clicado, a caixa de diálogo opções de impressão é exibida e requer mais informações do usuário.

-   Não use uma elipse quando a conclusão bem-sucedida da ação for simplesmente exibir outra janela. Os seguintes comandos nunca têm uma elipse: sobre, avançado, opções, propriedades, ajuda.

    **Incorreto:**

    ![captura de tela do botão Opções com reticências ](images/ctrl-command-buttons-image40.png)

    Neste exemplo, depois que o botão é clicado, a caixa de diálogo opções é exibida, mas mais informações do usuário não são necessárias.

-   No caso de ambiguidade (por exemplo, o rótulo de comando não tem um verbo), decida com base na ação do usuário mais provável. Se a simples exibição da janela for uma ação comum, não use reticências.

    **Correto:**

    Mais cores...

    Informações da versão

    No primeiro exemplo, os usuários provavelmente vão escolher uma cor, portanto, usar reticências está correto. No segundo exemplo, os usuários provavelmente irão exibir as informações de versão, tornando as reticências desnecessárias.

-   Para botões de procura, use botões de navegação curtos (rotulados "...") quando houver mais de dois botões de procura em uma janela. Sempre use a versão curta quando desejar exibir um botão procurar em uma grade.
-   Para botões direcionais, use um único colchete angular e o ponto na direção em que ocorre a ação.

A tabela a seguir mostra alguns rótulos de botão de comando comuns e seu uso.



|                             |                                                                                                              |                             |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Rótulo do botão**<br/> | **Significado**<br/>                                                                                       | **Chave de acesso**<br/>   |
| **Voltar**<br/>         | Em assistentes e fluxos de tarefas, vá para a página anterior.<br/>                                               | 'B'<br/>              |
| **Procurar...**<br/>    | Exiba uma caixa de diálogo para procurar um arquivo ou objeto.<br/>                                                | ' B ' ou ' r '<br/>       |
| **Opções**<br/>      | Exiba as opções disponíveis aos usuários para personalizar um programa.<br/>                                 | 'O'<br/>              |
| **Pausar**<br/>        | Nas caixas de diálogo em andamento, suspenda a tarefa.<br/>                                                       | DTI<br/>              |
| **Personalize**<br/>  | Personalize uma experiência básica que seja crucial para a identificação pessoal do usuário com um programa.<br/> | DTI<br/>              |
| **Preferências**<br/>  | Não use. Use as opções em vez disso.<br/>                                                                   | Não aplicável.<br/>  |
| **Propriedades**<br/>   | Exibe os atributos e as configurações de um objeto.<br/>                                                | ' P ' ou primeiro ' r '<br/> |
| **Salvar**<br/>         | Salve um grupo de configurações ou salve um arquivo ou objeto usando seu nome atual.<br/>                        | &<br/>              |
| **Salvar como...**<br/>   | Salvar um arquivo ou objeto usando um nome especificado.<br/>                                                     | Segundo ' a '<br/>       |
| **Configurações**<br/>     | Não use. Use as opções em vez disso.<br/>                                                                   | Não aplicável.<br/>  |
| **Solucionar problemas**<br/> | Não use. Em vez disso, use um link de ajuda específico.<br/>                                                      | Não aplicável.<br/>  |



 

Para obter diretrizes sobre rótulos de botão de confirmação (OK, cancelar, sim/não, fechar, parar, aplicar, avançar, concluir, concluído), consulte [texto da interface do usuário](text-ui.md).

## <a name="documentation"></a>Documentação

Ao fazer referência a botões de comando:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou reticências. Não inclua o botão Word.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: clique em **Imprimir** para imprimir o documento.

 

