---
title: Princípios da interface do usuário
description: este tópico discute como implementar uma interface de usuário intuitiva e princípios de design de experiência do usuário em um Windows aplicativos.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57781ab2cb0a2d9574288000f65805c981afa391d49263bd21e23eeed432416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021410"
---
# <a name="user-interface-principles"></a>Princípios da interface do usuário

este tópico discute como implementar uma interface de usuário intuitiva e princípios de design de experiência do usuário em um Windows aplicativos.

-   [Introdução](#introduction)
-   [Os princípios básicos da interface do usuário apropriada](#the-basic-principles-of-proper-ui)
    -   [Espaçamento e posicionamento](#spacing-and-positioning)
    -   [Tamanho](#size)
    -   [Agrupamento](#grouping)
    -   [Intuição](#intuitiveness)
-   [20 Dicas para uma experiência de usuário melhor e funcional](#20-tips-for-a-better-functional-user-experience)
    -   [Usar padrões](#use-standards)
    -   [Chame a atenção para botões importantes](#draw-attention-to-important-buttons)
    -   [Simplifique o reconhecimento com ícones](#simplify-recognition-with-icons)
    -   [Simplificar o reconhecimento com cabeçalhos](#simplify-recognition-with-headers)
    -   [Usar caixas de mensagem personalizadas](#use-custom-message-boxes)
    -   [Incluir comandos alternativos](#include-alternate-commands)
    -   [Como lidar com ações críticas](#how-to-handle-critical-actions)
    -   [Botões de opção ou caixas de combinação?](#radiobuttons-or-comboboxes)
    -   [Nunca interrompa o usuário!](#never-disrupt-the-user)
    -   [Fornecer status de progresso](#provide-progress-status)
    -   [Simplificar etapas complexas com assistentes](#simplify-complex-steps-with-wizards)
    -   [Obter o tom do texto à direita](#get-the-tone-of-your-text-right)
    -   [Às vezes, um ListView é melhor](#sometimes-a-listview-is-better)
    -   [Simplifique a navegação com controles de navegação estrutural e barras laterais](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Usar elementos gráficos bastante](#use-pretty-graphics)
    -   [Fornecer formulários redimensionáveis quando possível](#provide-resizable-forms-when-possible)
    -   [Fornecer mais funcionalidade com painéis de tarefas/barras laterais](#provide-more-functionality-with-sidebarstask-panes)
    -   [Dê uma opção de notificação](#give-a-notification-choice)
    -   [Fornecer dicas de ferramentas!](#provide-tooltips)
    -   [Não se esqueça das pequenas coisas](#do-not-forget-the-little-things)
-   [Conclusão](#conclusion)

## <a name="introduction"></a>Introdução

Os desenvolvedores geralmente não levam a perspectiva do usuário final em conta. Os desenvolvedores trabalham duro para fazer o aplicativo funcionar — os clientes apenas esperam que ele funcione e sua percepção dos centros de software em relação a esse requisito. Isso é especialmente verdadeiro se você desenvolve software comercial ou algo que será usado por pessoas não técnicas. Os desenvolvedores devem estar cientes das necessidades do usuário final durante todo o processo de design de software.

Um aplicativo de software deve ser fácil de navegar e usar possível. Com a quantidade de software que está sendo criada, um total de 4 aplicativos de software tem uma interface do usuário realmente ótima, que ele realmente gosta e é imediatamente confortável usando.

Uma grande quantidade de software de uso interno é criada para as corporações. Se ele é desenvolvido internamente ou sob o cuidado de um consultor, geralmente um mínimo de tempo, esforço ou dinheiro, é investido na criação de uma interface do usuário melhor. a função ' designer ' é rara no ciclo de desenvolvimento, especialmente no mundo dos aplicativos Windows.

Há algumas regras básicas a serem seguidas para ter uma interface do usuário de funcionamento muito mais atraente para seu aplicativo. Ele não exige muito investimento de tempo ou dinheiro de sua parte e acrescenta um bom retorno sobre o investimento.

Antes de continuarmos, vamos nos diferenciar entre a interface do usuário e a experiência do usuário — pelo menos no escopo deste artigo. Interface do usuário, ou UI, refere-se aos elementos visuais e controles do seu aplicativo, enquanto a experiência do usuário, ou UX, abrange tanto a interface do usuário quanto o comportamento do aplicativo relacionado à interface do usuário, bem como a "sensação" que ele obtém de seu aplicativo. Não se trata apenas de criar uma interface do usuário excelente, mas garantir que ela funcione muito bem.

Aqui, discutiremos 20 pontos de design de UX que você pode integrar facilmente à sua fase de design de aplicativos. O resultado será um aplicativo mais rico com funcionalidade intuitiva, uma "experiência humana". como todos sabemos, a geração de aplicativos Windows Vista precisará se parecer diferente. Este tópico ajudará você a se preparar para aplicativos futuros enquanto dá a seus usuários atuais um gosto do futuro.

As seções a seguir discutem os conceitos básicos do design adequado da interface do usuário.

## <a name="the-basic-principles-of-proper-ui"></a>Os princípios básicos da interface do usuário apropriada

Um UX de aparência profissional depende desses quatro fatores:

-   Espaçamento e posicionamento
-   Tamanho
-   Agrupamento
-   Intuição

com versões do Microsoft Visual Studio anteriores a 8,0, o espaçamento e o dimensionamento eram abaixo do ideal. Uma grade 4x4 ou 8x8 nem sempre funciona. Com a inclusão de SnapLines, o processo foi bastante simplificado. Alinhar um rótulo com uma caixa de texto, ou ainda pior, alinhar vários rótulos com suas caixas de texto correspondentes era extremamente difícil em versões anteriores do Visual Studio. As SnapLines simplificaram muito esse processo.

As seções a seguir descrevem quatro dos aspectos mais importantes do design Professional UX.

### <a name="spacing-and-positioning"></a>Espaçamento e posicionamento

O espaçamento entre dois controles é importante. A captura de tela a seguir demonstra um formulário de entrada de **informações de usuário** mal projetado – as duas caixas de texto principais são muito próximas, a lista sob elas está muito longe e há muito espaço não utilizado no formulário.

![captura de tela de um formulário mal projetado.](images/humanux-01.png)

Na captura de tela a seguir, você pode ver uma caixa de diálogo de aparência mais profissional com espaçamento adequado e controles de tamanho adequado. Essa é a mesma forma da captura de tela anterior, mas foi modificada para usar o espaçamento recomendado pelas SnapLines. É sempre recomendável alinhar um rótulo com a linha de base de texto da caixa de Text ou outro controle ao lado dele, em vez da borda inferior real do controle. As SnapLines desativam uma cor diferente quando esse alinhamento é atingido, normalmente apenas alguns pixels acima da borda inferior.

![captura de tela de um formulário mais bem projetado.](images/humanux-02.png)

Embora não haja regras exatas para espaçamento, as SnapLines fornecem diretrizes extremamente úteis para o espaçamento adequado. Outras ferramentas para ajudá-lo a manter o espaçamento adequado são os controles de layout no grupo caixa de ferramentas contêineres. O TableLayoutPanel também é muito útil para a criação de caixas de diálogo de estilo de formulário de entrada.

### <a name="size"></a>Tamanho

As mesmas considerações se aplicam ao tamanho. Quando você arrasta um botão da caixa de ferramentas para o formulário, ele tem a altura e a largura perfeita. A largura máxima recomendada (o bloqueio de qualquer motivo seriamente importante) é dobrar a largura original.

se você olhar a janela **executar** no menu **iniciar** ou a caixa de diálogo **propriedades** de qualquer objeto Windows Explorer, os tamanhos dos botões serão ' apenas à direita '. Se você tiver uma função muito importante que você precisa que seu usuário final perceba sem falhar, há outros métodos do que usar um botão grande ou extravagante cores não padrão (mais sobre isso posteriormente).

Na imagem a seguir, você pode ver três botões. O primeiro botão é o tamanho mais recomendado e é o tamanho criado por padrão quando arrastado (ou clicado duas vezes) na caixa de ferramentas. Às vezes, o texto extra exige que você torne o botão maior. O segundo botão mostra um tamanho grande, porém aceitável. Ele não criaria uma bagunça para dispor outros controles. O terceiro botão, no entanto, é um tamanho completamente inaceitável. você pode ver que ele até ligeiramente distorce os bitmaps de tema Windows usa para desenhar controles com tema. Também será difícil alinhar outros controles intuitivamente.

![imagem de três botões, aumentando de tamanho da esquerda para a direita.](images/humanux-03.png)

### <a name="grouping"></a>Agrupamento

Normalmente, um aplicativo contém muitos controles. Somente pelo agrupamento intuitivo adequado, você pode tornar todos esses controles mais fáceis de usar. O agrupamento baseado em função ou Categorizado é feito melhor por controles de guia. Por exemplo, ' contas, ' ' relatórios, ' ' funcionários, ' e ' projetos ' seriam candidatos perfeitos para guias em um aplicativo de negócios típico. Agrupamento irmão – os controles que contribuem para o mesmo resultado final — são melhor feitos por controles de grupo. Não é recomendável usar painéis com bordas para esse agrupamento. Os controles de grupo economizam o peso adicional de um controle de rótulo — especialmente se os subcontroles são auto-explicativos.

Controles de grupo dentro de controles de grupo não são recomendados, a menos que não haja mais de 2 ou três deles dentro de um controle de grupo grande.

### <a name="intuitiveness"></a>Intuição

Esse é o aspecto mais importante de uma excelente experiência do usuário. O UX intuitivo diminui a necessidade de explicações. O usuário só sabe o que os controles fazem.

Um tópico importante em design intuitivo é a codificação por cores. um bom exemplo é apresentado no Windows XP, que apresentou novos botões de soft-quadrado para funções como navegação em aplicativos com tema, **logoff e desligamento de caixas** de diálogo de **computador** e outros.

A cor desses controles foi determinada com base na severidade do resultado que esse botão está sendo enviado por push. A navegação é verde, assim como uma luz de tráfego "Go". O desligamento, que resultaria em uma possível perda de trabalho, é vermelho colorido, como um sinal de aviso. Botões semicríticos, como logoff ou hibernação, são amarelos. Botões neutros que não têm nenhum efeito crítico sobre os processos de trabalho do usuário, como a ajuda, são um azul suave. Ao criar uma interface do usuário com revestimento, esses aspectos de cor devem ser mantidos em mente.

um exemplo muito bom de reconhecimento de conteúdo por cores é Microsoft Office OneNote. as guias do aplicativo podem ser definidas para cores diferentes e, ao mesmo tempo, se parecem com uma parte adequada do design geral do estilo Windows XP.

Outro aspecto importante é o texto em seus aplicativos. recentemente, houve vários esforços para simplificar a linguagem usada para as instruções escritas em Windows software. O uso do texto dentro do software será discutido posteriormente, mas observe os detalhes pequenos, mas importantes, a seguir.

O MSN Messenger tinha uma caixa de seleção em seu diálogo de **Opções** marcada como "compartilhar recursos de webcam". Os desenvolvedores e as pessoas com tecnologia amigável sabem o que isso significa, mas um usuário novato pode, possivelmente, imaginar que você poderia deixar outro usuário na outra extremidade do seu chat usar sua Web Cam também. Em uma versão recente, elas foram alteradas para "minha webcam: permitir que outras pessoas vejam que eu tenho uma webcam". Isso é perfeito para o público-alvo que pode não ter conhecimento técnico e é usado para linguagem simples.

Embora a linguagem mais simples facilite a compreensão, também há uma vantagem adicional. Estudos científicos mostram que nossa ideia funciona mais facilmente com uma linguagem mais simples ao tentar entender algo novo. Muitas vezes, nosso cérebro processa palavras como ' it ', ' ' para, ' ' que, ' e outras palavras comuns, portanto, speedily e sem esforço, que mais ' largura de banda ' é alocada para entender as palavras que se destacam, como ' Webcam ' ou ' outros ', no exemplo acima.

Títulos de caixa de mensagem, legendas de GroupBox e outros blocos de texto, facilitam a transmissão da função de um grupo de controles para o usuário final com apenas algumas palavras.

A intuição também nasceu da familiaridade. Por exemplo, o posicionamento dos botões **OK** e **Cancelar** é tão uniforme e bem colocado em nossas mentes que, se uma caixa de diálogo mantiver esses botões em uma sequência inversa (**Cancelar**, **OK**; em vez de **OK**, em seguida, **Cancelar**) — você pode clicar em **Cancelar** . depois de usar um padrão específico para fazer coisas — aplicativos baseados em Windows, por exemplo — por mais de um ano, os hábitos desenvolvem. Os padrões do setor a seguir (porém informados podem ser) tornam o software mais fácil de usar.

em uma das versões prévias de visualização do Windows Vista, os botões **minimizar**, **maximizar** e **fechar** de qualquer janela se tornaram diferentes. nas versões anteriores do Windows (especialmente ao usar um único monitor), você desenvolve um hábito de mover o cursor no canto superior direito da tela e clicar em. Isso sempre resultou no fechamento da janela. agora, neste build específico do Windows Vista, havia aproximadamente 8 pixels de espaço entre o botão fechar e a borda à direita da janela. O espaço extra fazia com que pareça legal (e, provavelmente, era necessário para a animação de brilho frio do botão), mas foi irritante porque não permitia que os usuários fechassem o Windows aberto com facilidade. A recondicionação de sua ideia pode ser difícil. Felizmente, na compilação a seguir, esse problema foi resolvido. Agora, ainda há espaço entre a borda da janela e o botão fechar, mas clicar nesse espaço também faz com que a janela seja fechada.

Um fator muito importante do design intuitivo é a quantidade de "mental bandwidth' – a quantidade de tempo que pode levar em consideração a compreensão de algo — ele usa. Quanto menor for o uso da ' largura de banda ', melhor a experiência do usuário.

Essas são pequenas coisas que contribuem para a "experiência" de usar um aplicativo de software. Os exemplos a seguir fornecem dicas sobre como aprimorar seus aplicativos com dicas e truques do mundo real.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 Dicas para uma experiência de usuário melhor e funcional

A meta de uma experiência de usuário melhor é ter uma interface de usuário mais simples, mais fácil e funcional que também parece boa. Essas dicas ajudarão você a formatar sua interface do usuário para que ela seja mais eficiente.

### <a name="use-standards"></a>Usar padrões

Os padrões estabelecidos de qualquer ambiente de software — seja no nível do sistema operacional, no nível da marca ou no nível do aplicativo — são muito importantes. Além da identidade visual, os padrões atuam como um esquema provérbio na mente do usuário. Quando o usuário passa longos períodos de tempo trabalhando com um aplicativo de software, ele aumentará a produtividade automaticamente devido à familiaridade crescente.

Antes de discutir os padrões, vamos discutir primeiro o que são exatamente esses padrões. os padrões incluem tudo, desde o layout dos controles de uma maneira específica nas caixas de diálogo, como os botões **OK** e **cancelar** , a forma da interface do usuário – cantos arredondados da parte superior da janela, como em caixas de diálogo Windows XP, estilos de ícones, estilos de qualquer outro gráfico, comportamento interativo do seu aplicativo e assim por diante.

Se seu aplicativo se enquadrar em um nicho específico, pode ser melhor seguir um conjunto diferente de padrões. por exemplo, se seu aplicativo dá suporte a, aplicativo ou um complemento do, Office OneNote 2003, é prudente seguir os estilos de padrões de interface do usuário e interatividade de Office — e OneNote em particular. isso inclui o uso das barras de comando de estilo Office em vez das barras de ferramentas padrão, além de outras coisas, visuais e comportamentais. se seu aplicativo for fazer parte da categoria Microsoft Visual Studio .net, você terá um conjunto separado de padrões. Na verdade, para esses aplicativos complementares ou de suporte, as empresas, como a Microsoft, lançam diretrizes escritas. Observe também que, às vezes, os conceitos gráficos e de design são propriedades intelectuais protegidas. Sempre verifique a documentação correta para ter certeza de que você tem a licença para criar esses designs.

Um terceiro exemplo de padrões seria o ambiente do Tablet PC. Esses padrões cruzam os limites entre as diretrizes do sistema operacional e as diretrizes do aplicativo. A [documentação do SDK do Tablet PC](/previous-versions/ms840465(v=msdn.10)) contém algumas informações muito úteis no tópico "planejando seu aplicativo". ao contrário das diretrizes do office 2003 ou Visual Studio, essas recomendações de design afetam diretamente como o usuário irá interagir com seu aplicativo e como ele deve se comportar por vez. Por exemplo, se você estiver encaixando janelas em seu aplicativo, a documentação recomenda que você verifique se ela pode detectar quando a orientação da tela é alterada e se as janelas de encaixe se reorganizam corretamente em uma orientação retrato ou paisagem, conforme necessário. Mesmo que você não esteja projetando seu aplicativo para ser específico do Tablet, você deve seguir essas diretrizes.

Com o aumento dos Smart Clients, agora os aplicativos estão ultrapassando os limites entre hardwares diferentes – computadores normais, Tablet PCs, dispositivos móveis ou ultra móveis, PCs do Media Center e assim por diante. Cada situação chama um conjunto de padrões diferente (ou adicional) a ser seguido.

Quando os aplicativos compartilham os padrões no nível do sistema operacional ou do aplicativo, os usuários sentem-se mais em casa com o software, o que torna mais fácil aprender e usar. Esse resultado é um aumento direto para a produtividade. Os usuários desejam ser capazes de se tornar produtivos com o novo software o mais rápido possível.

### <a name="draw-attention-to-important-buttons"></a>Chame a atenção para botões importantes

Às vezes, você precisa direcionar o usuário para os botões mais importantes mesmo quando tiver quatro ou cinco outros botões que pertençam a ele. Se você experimentar o tamanho, a cor ou a fonte, quebraria os padrões, o que não é recomendado. Em vez disso, você pode usar alguns truques simples para fazer isso.

A primeira é converter os outros botões não críticos em LinkLabels, conforme mostrado na imagem a seguir. Dessa forma, o usuário saberá que esses links executarão uma tarefa, mas sua atenção entrará em primeiro lugar ao botão que se destaca — sem perder as diretrizes de design padrão.

![imagem de três botões convertidos em linklabels.](images/humanux-04.png)

A segunda é colocar o botão crítico primeiro em linha, seja à esquerda para layouts horizontais, conforme mostrado na imagem a seguir, ou na parte superior para layouts verticais. Observe que isso pode mudar dependendo da cultura do usuário de destino – você poderá se concentrar melhor se posicionar o botão em questão na extrema direita se seu aplicativo for qualquer idioma escrito da direita para a esquerda.

![imagem de três botões em que o botão crítico está mais à esquerda em um layout horizontal.](images/humanux-05.png)

A opção recomendada é definir para receber o foco por padrão. Por exemplo, em uma caixa de diálogo de confirmação de exclusão, a opção **não** deve ser realçada, pois isso impede que o usuário exclua algo acidentalmente.

### <a name="simplify-recognition-with-icons"></a>Simplifique o reconhecimento com ícones

ícones — especialmente os ícones Windows XP e Office 2003 e bitmaps de barra de ferramentas — ajudam a acelerar a cognição da interface do usuário e a tarefa que ele precisa executar.

Por exemplo, quando você vê o ícone de exclamação mais frequentemente visto na caixa de mensagem, fica imediatamente atento ao nível de risco associado aos controles ao lado desse ícone. Da mesma forma, quando seu aplicativo coloca muitos controles, independentemente de como organizados corretamente, pode ser assustador encontrar o conjunto de controles que você está procurando.

no Windows XP Service Pack 2, uma guia atualizada é adicionada ao miniaplicativo do painel de controle **propriedades do sistema** chamado "Atualizações Automáticas". Há quatro opções presentes – baixar atualizações automaticamente, baixar atualizações, mas permitir que o usuário decida quando instalá-las, notificar o usuário se as atualizações estiverem disponíveis, mas não iniciar o download e desabilitar completamente as atualizações automáticas.

Um novo usuário de PC pode não estar ciente do que são essas atualizações e pode não saber qual opção é melhor escolher. Portanto, a Microsoft colocou um ícone de escudo verde com uma grande marca de seleção na ti, ao lado do mais recomendado, que significa uma opção "segura", e um ícone de escudo vermelho com um grande "x" nele próximo daquele que seria potencialmente prejudicial ao usuário. Isso é muito útil em situações críticas, especialmente quando o usuário não tem tempo para ler muito texto.

No mesmo applet **Propriedades do sistema** , cada guia tem várias groupboxs com controles diferentes para tarefas diferentes. Um gráfico relativo é colocado ao lado de cada grupo que significaria facilmente a tarefa do grupo de controle. Esse tipo de código gráfico é semelhante à codificação por cores em arquivos físicos ou estacionamentos. Isso também funciona no mesmo princípio de ter pelo menos alguns elementos visuais em um artigo de revista – ele mantém o interesse do leitor.

Escolher o ícone à direita também é importante. a Microsoft fornece muitos gráficos padrão como parte do Visual Studio 2005. Essa seria a melhor opção. Se você criar seus próprios ícones, é altamente recomendável que você siga os padrões no nível do sistema operacional ou do aplicativo para esses gráficos, conforme mencionado na seção de [padrões de uso](#use-standards) acima.

a [Windows diretrizes de interação da experiência do usuário](/windows/apps/desktop/) contém um guia muito útil para criar [ícones](https://msdn.microsoft.com/library/aa511280.aspx)de Windows estilo.

### <a name="simplify-recognition-with-headers"></a>Simplificar o reconhecimento com cabeçalhos

Os cabeçalhos são a maneira perfeita de explicar a caixa de diálogo inteira em uma única frase (e, opcionalmente, um gráfico). Às vezes, os cabeçalhos podem até mesmo ajudá-lo a acomodar a navegação e os comandos dentro deles também. Os cabeçalhos funcionam com mais eficiência do que rótulos de descrição normais porque são a primeira coisa que um usuário vê quando a caixa de diálogo é exibida.

os assistentes de Windows Installer são talvez os cabeçalhos mais populares: um ícone simples na extrema direita; um rótulo de título que descreve a caixa de diálogo (por exemplo, Selecionar pasta de instalação); e um subtítulo que descreva a finalidade da caixa de diálogo (por exemplo, selecione a pasta onde os arquivos de software serão instalados).

Digamos que tenhamos um aplicativo de negócios típico com uma seção de contas. seguindo o paradigma de design criado pelo Windows Vista, podemos fornecer informações críticas e comandos relacionados no cabeçalho (ou no rodapé, se o cenário o chamar). Nosso usuário abriu o arquivo de conta para "grande empresa", e o cabeçalho ficaria parecido com o mostrado na captura de tela a seguir.

![captura de tela de uma caixa de diálogo que contém um rodapé detalhado.](images/humanux-06.png)

A captura de tela a seguir mostra um exemplo de um cabeçalho detalhado em uma caixa de diálogo.

![captura de tela de uma caixa de diálogo que contém um cabeçalho detalhado.](images/humanux-07.png)

da mesma forma, você pode evitar ter que adicionar Windows painéis de tarefas no estilo XP, especialmente quando há apenas alguns comandos, o que desperdiçaria muito espaço vertical, movendo esses comandos para o cabeçalho.

Há algumas coisas que você deve ter em mente ao criar cabeçalhos:

-   Verifique se a cor do plano de fundo é diferente da cor do plano de fundo da caixa de diálogo. com mais frequência do que não, um cabeçalho branco sobre uma cor de face de controle intrínseco de Windows padrão fará. Mas se você realmente quiser ter certeza de que nenhum tema especial ou cores personalizadas bagunçam o cabeçalho, desenhe um **LinearGradient** usando o **Color. FromKnownColor** com as cores **ControlLight** e **ControlDark**.
-   Se possível, mantenha a altura do cabeçalho abaixo de 150 pixels. Geralmente, uma altura de 100 ou 120 fará. Como regra geral, verifique se ele é inferior a 1/4 da altura do formulário inteiro.
-   Se você quiser adicionar a edição in-loco para obter informações mostradas no cabeçalho acima, substitua dinamicamente o LinkLabel por uma caixa de texto e troque-os novamente quando a edição for concluída.
-   Se você tiver um rótulo de título com uma fonte de tamanho de 10 pt, use Arial ou Franklin Gothic Medium. MS Sans Serif parecerá muito irregular e não será profissional. o Franklin Gothic medium é a recomendação na documentação de diretrizes de Design do Windows XP. para aplicativos voltados para o Windows Vista, use a fonte Segoe UI que é a fonte padrão do sistema.

### <a name="use-custom-message-boxes"></a>Usar caixas de mensagem personalizadas

as opções disponíveis na caixa de mensagem de Windows padrão são muito limitadas. Quando você precisa perguntar ao usuário uma pergunta que não pode ser respondida com um simples sim/não ou OK/cancelar, ela se torna complicada.

os aplicativos Windows agora estão se tornando mais simples de usar devido ao alto volume de usuários não técnicos. Às vezes, pode ser muito mais simples fornecer botões com textos mais amigáveis e até mesmo alguns controles adicionais – LinkLabels, por exemplo, para facilitar a realização da tarefa em questão.

o Microsoft .NET Framework facilita a implementação de caixas de diálogo personalizadas. Ao atribuir apenas algumas propriedades em seu formulário de diálogo personalizado ou com uma única linha de código, seu formulário pode funcionar como uma caixa de mensagem padrão. Em um evento de clique de botão, defina a propriedade **DialogResult** da caixa de diálogo como **DialogResult. ok** ou **DialogResult. Cancel**. Use o método **ShowDialog ( \[ OwnerForm \] )** do formulário pai. Esse método de método retorna o valor **DialogResult** .

Você pode usar todos os membros do **DialogResult** . Essas mesmas opções são usadas pelo método **MessageBox. show** padrão.

Como alternativa, você pode apenas definir a propriedade **AcceptButton** da caixa de diálogo como **btnOK** e a propriedade **CancelButton** como **btnCancel**. Isso mapeará automaticamente as chaves **Enter** e **ESC** para os respectivos eventos de clique dos botões **btnOK** e **btnCancel** .

Aqui estão algumas dicas para aprimorar suas caixas de diálogo personalizadas:

-   Para tópicos complicados, forneça links para a ajuda local ou online com um LinkLabel dizendo "Saiba mais" no rótulo de texto apropriado.
-   Em vez de **Sim** / **nenhum** / botão **Cancelar** , use textos que declaram claramente o resultado de clicar no botão, como "salvar arquivo e sair", sair sem salvar, "e" não sair ". No entanto, não fique com os botões padrão **Yes** / **no**, **OK** / **Cancel** e tais Standard sempre que possível. A familiaridade possibilita uma grande produtividade.
-   Mantenha 50 pixels de espaço de margem no lado esquerdo (ou no lado direito, dependendo das configurações de cultura de destino) e adicione um ícone que represente o cenário da caixa de diálogo. Se for uma caixa de diálogo de informações, você poderá usar o ícone "i" usado por caixas de mensagem padrão; Se for uma caixa de diálogo de segurança, você poderá usar um ícone de cadeado ou um ícone de chave. o Visual Studio 2005 é fornecido com alguns gráficos ótimos de alta qualidade.
-   Sempre certifique-se de fornecer navegação de teclado adequada para esses botões – os usuários usam os atalhos de teclado para caixas de mensagem (por exemplo, O para Ok, Y para Sim, C para cancelar e assim por diante) de forma intensiva. Eles certamente achariam irritantes se sua caixa de diálogo personalizada não os utilizasse.

### <a name="include-alternate-commands"></a>Incluir comandos alternativos

Dois fatores importantes determinam a necessidade de métodos de entrada alternativos – frustração e a prenossa. A frustração é uma coisa que ocorre com muita frequência para usuários de computador. Quando estiver frustrado, você deseja que a tarefa seja feita rapidamente. Um clique extra ou uma espera extra de alguns segundos realmente infuriates uma pessoa sob estresse – você sabe como eles estão lá. A precerteza geralmente solicita que você conclua a tarefa apenas com o teclado ou o mouse – o que estiver usando no momento. Mas, a não ser por esses dois fatores, ter métodos de entrada alternativos torna mais fácil para o usuário realizar tarefas.

Por exemplo, se você tiver uma caixa de listagem com dois botões — "Adicionar" e "remover" — em ambos os lados, deverá adicionar um menu de contexto para essa caixa de listagem com comandos de menu análogos a esses botões. Isso dá ao usuário uma oportunidade de escolher o método que ele encontra o mais adequado. os usuários iniciantes, como o Windows estado das diretrizes de experiência do usuário Vista, usam os menus de contexto muito e esperam que eles estejam em qualquer lugar que cliquem com o botão direito do mouse.

Da mesma forma, usamos controles visuais para texto ou entrada numérica. Por exemplo, os controles deslizantes são usados para especificar números inteiros e o calendário é usado para entrada de data. Às vezes, pode ser mais confortável apenas inserir digitando. Em geral, ele pode fazer uma diferença para o usuário se você adicionar um controle de Up-Down numérico vinculado a um controle deslizante ou usar um DateTimePicker em vez do controle Calendar.

### <a name="how-to-handle-critical-actions"></a>Como lidar com ações críticas

Ao executar uma função crítica e irrecuperável, geralmente é uma boa prática fazer com que um pop-up da caixa de mensagem confirme a ação. Vamos pegar um entalhe. Na captura de tela a seguir, você pode ver uma caixa de mensagem personalizada semelhante, mas com uma vantagem adicional — um temporizador mostrado visualmente com a ajuda de uma barra de progresso.

![captura de tela de uma caixa de diálogo de ação crítica.](images/humanux-08.png)

Há algumas variações específicas de cenário que você pode usar. Se a ação a ser executada for muito crítica (desde sobrecarregar uma planta de energia nuclear para excluir arquivos permanentemente), a ação padrão depois que o temporizador for executado deverá ser cancelada. A caixa de diálogo não deve desaparecer, mas o rótulo de texto é alterado para mostrar que a ação foi cancelada. O usuário pode optar por confirmar o comando ou o cancelamento.

Sempre certifique-se de que os botões que executam operações críticas estejam claramente marcados – sempre use texto não criptografado que descreva com precisão a ação. Se a ação for a exclusão de arquivos, não grave "remover arquivos do repositório"; Escreva "excluir arquivos do repositório". Ao trabalhar com listas de arquivos, se um comando de menu Excluir exclui os arquivos selecionados do disco rígido em si (em oposição à remoção apenas da lista de arquivos), você deve enfatizar adequadamente a natureza crítica desse e enfatizar explicitamente que a ação excluirá permanentemente os arquivos.

Alguém disse, "você é tão bom quanto seu pior trabalho". A mesma coisa se aplica a aplicativos de software. Uma única experiência inadequada com seu aplicativo pode fazer uma grande impressão negativa no usuário. Para certificar-se de que isso não acontece, é possível garantir que, se o aplicativo falhar, ele ficará inativo normalmente. Se você puder adicionar a recuperação de dados ou permitir que o usuário tente salvar uma cópia desses dados, poderá ser um grande sinal de mais. O usuário deverá ser notificado corretamente se o aplicativo falhar. Um JIT-Debugger ou uma caixa de diálogo de erro crítico não é algo bom. Embora falar sobre como lidar com falhas ultrapasse o escopo deste artigo, recomendarei que uma caixa de diálogo simples que pedisse desculpas ao usuário e informe a ele ou a sua situação (e, possivelmente, com um link para obter mais informações sobre como se recuperar dessa falha) seja muito útil para o usuário.

Se você quiser levá-lo um passo além, poderá fazer o que um dos meus aplicativos de design gráfico favorito faz. Se ele falhar, ele mostrará uma caixa de diálogo de recuperação que permitiria salvar uma cópia separada do arquivo que está sendo trabalhado e, em seguida, forneceria uma caixa de diálogo de comentários onde você pode inserir informações sobre a falha (informações pessoais opcional, é claro) e enviá-las aos criadores.

### <a name="radiobuttons-or-comboboxes"></a>Botões de opção ou caixas de combinação?

À primeira vista, o método para fazer uma seleção um-de-muitos não parece tão difícil ou importante. Às vezes, pode ser, especialmente se o cenário for um aplicativo usado para o trabalho com detecção de hora.

Vamos dar uma olhada em um exemplo de vida real. A Microsoft lançou recentemente uma versão de visualização de um aplicativo de gráficos, o designer de gráficos de expressão (anteriormente denominado "acrílico"). Tive cerca de 20 objetos gráficos para os quais tive que atribuir uma determinada propriedade separadamente neste aplicativo. Era um processo dreary. Para fazer isso, precisei selecionar o objeto, clicar no botão para colocar a janela Configurações e definir as opções. Em uma dessas opções, duas escolhas precisavam ser escolhidas de uma ComboBox, como você pode ver na captura de tela a seguir.

![captura de tela da caixa de diálogo de textura da borda do designer de elementos gráficos do Expression.](images/humanux-09.png)

Quando você precisa selecionar a lista de caixas de combinação e seleciona o segundo item (somente de 2 itens), ele pode ser realmente irritante. O que geralmente não percebemos é o tempo que leva para a lista suspensa aparecer. Ele pode perder muito tempo e pode ser frustrante. Isso pode ser resolvido facilmente colocando-se em uma GroupBox com dois botões de opção, especialmente quando há muito espaço disponível. Eu encontrei problemas semelhantes em aplicativos como o CorelDRAW, o Microsoft Access e outros.

Além de perder tempo devido à animação suspensa, ele também desperdiça nossa "largura de banda mental". Com dois botões de opção "sempre visíveis", nossa mente seria subliminally saber a posição para o cursor clicar. Com a ComboBox, ela será processada somente depois que a lista tiver sido desenhada. Embora possa parecer muito não importante, na verdade é muito importante.

Às vezes, é melhor usar os botões de opção, especialmente se você tiver quatro opções ou menos.

### <a name="never-disrupt-the-user"></a>Nunca interrompa o usuário!

Curto de colocar uma arma em seus cabeçotes, essa é a coisa mais destrutiva que um desenvolvedor pode fazer para os usuários. Quando seu aplicativo, desnecessariamente ou de outra forma, interrompe o usuário enquanto trabalha em outro aplicativo com uma caixa de mensagem ou uma barra de tarefas flash, você ganha pontos negativos do usuário.

A barra de tarefas pisca pode ser útil, é claro, mas deve ser chamada somente quando o processo do aplicativo exigir entrada do usuário para continuar ou se você tiver algo crítico para transmitir ao usuário. Se o usuário mantiver a barra de tarefas em ocultar automaticamente, um botão de barra de tarefas piscando pode obstruir o usuário de acessar a barra de status ou outros controles de baixa ancoragem, já que a barra de tarefas estaria sobre ela e não será ocultada novamente até que o usuário tenha clicado no botão piscando.

![captura de tela de uma janela do sistema.](images/humanux-10.png)

As janelas "do sistema" (veja a Figura 10), feitas por clientes de mensagens instantâneas como o MSN Messenger, são uma ótima solução para informar o usuário sobre algo sem desagradáveis ou interromper seu fluxo de trabalho. Há um ótimo artigo ( https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) por Bill Wagner sobre a criação de janelas de notificação. É uma boa política (e modos) não incomodar as notificações de qualquer outro aplicativo. A obstrução dessas janelas pode ser irritante e não-técnica. Uma solução é usar o mutex ToastSemaphore (/library/WinMessenger/winmessenger/overview/toast.asp) fornecido pelo sistema operacional para evitar a colisão do sistema.

Às vezes, talvez seja necessário mostrar vários itens pelo sistema de notificação. O pop-up de três ou mais torradeiras não seria realmente aconselhável. Em vez disso, fazer o ciclo de cada uma das exibições/esmaecimento de uma notificação após a outra seria melhor. o Microsoft Outlook implementa uma solução semelhante ao notificar o usuário sobre emails de entrada.

### <a name="provide-progress-status"></a>Fornecer status de progresso

Muitas vezes, há tarefas que exigem que o usuário aguarde. É claro que isso é uma das coisas que o usuário simplesmente odeia a fazer. Mas o pior é quando estão aguardando sem saber o que está acontecendo. Às vezes, seu aplicativo pode precisar se conectar a um serviço Web ou a um computador remoto, ou talvez ele esteja processando grandes partes de dados — seja qual for o motivo, o usuário deve se lembrar ou, pelo menos, de forma indesejada, o que está acontecendo nos bastidores. Há métodos diferentes de fazer isso com base na situação.

Se você estiver se conectando a um objeto distante como um serviço Web ou algo colocado em um servidor de rede ou de Internet, seria aconselhável mostrar uma caixa de diálogo de progresso simples (consulte a imagem a seguir) ou uma barra de progresso hospedada na barra de status. Um rótulo de acompanhamento deve descrever o status atual do processo. Por exemplo, se você estiver se conectando a um serviço Web para processar alguns dados, basta dizer "conectando-se ao serviço Web... "ou" Aguarde, processando... "Se esse processo for síncrono, é aconselhável desabilitar todos os controles que o usuário pode acessar até que o processo seja concluído ou apenas mostrar o progresso como uma caixa de diálogo modal.

![captura de tela de uma caixa de diálogo de barra de progresso.](images/humanux-11.png)

É altamente recomendável que você defina o estilo de barra de progresso como modo de letreiro se estiver usando uma barra de progresso e o tempo de processamento for desconhecido ou se você não tiver um valor máximo.

Outro método que está se tornando popular é uma janela fixa "do sistema" que exibe o progresso. O Microsoft AntiSpyware Downloader/atualizador ou as notificações de verificação de email do Norton antivírus são bons exemplos disso. É claro que isso deve ser usado somente para processos assíncronos. Caso contrário, o usuário pode sentir-se incerto. Essas janelas são mais bem usadas para processamento em segundo plano, como baixar uma atualização ou executar uma tarefa agendada, e nunca devem ser definidas como "Always on Top".

### <a name="simplify-complex-steps-with-wizards"></a>Simplificar etapas complexas com assistentes

É seguro pressupor que, se enfrentar uma grande quantidade de controles em um único Formulário, um usuário típico será confundido sem fim. Às vezes, nenhuma quantidade de agrupamento, dimensionamento ou espaçamento pode ajudá-lo quando você tem muitos controles importantes.

Um assistente é a melhor coisa para esses cenários. Você pode dividir os controles por tarefa ou categorias conforme aplicável e colocá-los em etapas separadas. Isso pode ajudar o usuário a se manter focado e não ser intimidado pela tarefa. Você pode fornecer ajuda específica de etapas ou tarefas com um botão de ajuda. você pode encontrar as diretrizes de criação do assistente no Biblioteca MSDN.

Os assistentes também são uma boa maneira de ajudar a configurar a configuração inicial do seu aplicativo. Muitos aplicativos usam esse assistente para definir a configuração personalizada logo após a conclusão da instalação ou na primeira utilização. Esse assistente inicial também deve se tornar opcional, se possível — se o usuário cancelar a qualquer momento, as configurações não especificadas vão para valores padrão. Se você puder tornar o assistente um gráfico de bits (consulte a seção [usar elementos gráficos](#use-pretty-graphics) ), ele tornará a tarefa de configuração muito mais fácil.

### <a name="get-the-tone-of-your-text-right"></a>Obter o tom do texto à direita

no [Windows diretrizes de interação da experiência do usuário](/windows/apps/desktop/), um ponto muito importante foi feito sobre "tom de texto". Essa é a impressão e a sensação fornecida pelo texto em seu aplicativo. Isso pode ser qualquer coisa, desde uma dica de ferramenta simples, até um controle de rótulo de instrução.

Anteriormente, discutimos a alteração de texto na opção de webcam no MSN Messenger. Isso é chamado de Tom de texto adequado. Ao lidar com usuários não técnicos ou iniciantes, fazer com que a mensagem entre em um aspecto diferente.

Se você escrever "caminho de destino" acima de uma caixa de texto em um aplicativo de extração automática, um usuário técnico poderá saber facilmente que você insere algo como "C: \\ temp \\ MYPATH". Um usuário novato (imagine "Mom") pode ser facilmente desnorteadodo e precisaria fazer referência ao manual, ligar para o suporte técnico ou pior – desistir. Uma boa alternativa é especificar o que você deseja que o usuário faça: "Selecione a pasta na qual você gostaria de colocar esses arquivos". Você pode até mesmo renomear a "procurar... "botão que reside ao lado dessa caixa de texto para" Selecionar pasta... "

Fornecer uma descrição clara do que você deseja que o usuário também reduz a necessidade de arquivos de ajuda ou, pelo menos, diminui os detalhes que você precisa incluir nos arquivos de ajuda.

uma sugestão muito boa do [Windows diretrizes de interação da experiência do usuário](/windows/apps/desktop/) se aplica a qualquer software. Ele afirma que o gravador deve manter o texto de conversa. As diretrizes definem isso como "Evite palavras que você não diria a outra pessoa pessoalmente".

Algumas dicas para escrever texto:

-   Evite falar sobre o usuário na terceira pessoa. Diga "você" em vez de "o usuário".
-   Sempre que possível, use criteriosamente "meu nome:" ou "meu endereço de email:" em vez de "nome:" ou "email:"
-   Ao fornecer várias opções, escreva o texto da perspectiva do usuário. Por exemplo, se você tiver dois botões de opção em um rótulo como "selecionar permissão para \[ nome de usuário \] nesta rede" acima de dois botões de opção, como "permitir" e "negar", substitua o texto do botão de opção por "desejo permitir \[ nome \] de usuário" e "quero não permitir o \[ nome de usuário" \] .
-   Sublinhar texto somente se ele for usado para links. Ele confunde o usuário se o texto sublinhado não for um link.
-   Chame atenção para informações importantes com um rótulo em negrito, mas use-a com cuidado. Muito texto em negrito é confuso e reduz o impacto geral do formulário.
-   Ao gravar o texto de uma caixa de seleção, certifique-se de que é fácil saber o que acontecerá quando ela for selecionada e quando ela estiver desmarcada ou apagada. A opção recomendada é gravar o texto diretamente como o resultado da caixa de seleção que está sendo selecionada. Por exemplo, escreva "Envie-me informações úteis de seus parceiros" em vez de "não enviar informações úteis de seus parceiros". Embora eu possa imaginar muitas pessoas de marketing discutir sobre esse exemplo específico, tenho certeza de que você sabe o que quero dizer.
-   Se você tiver um controle de botão (geralmente um RadioButton com uma aparência de botão de comando) que controla habilitado/desabilitado, certifique-se de rotulá-lo corretamente. Se o processo estiver habilitado, escreva "habilitado" em vez de "habilitar" ou "Desabilitar". Se você tiver habilitado, ele mostrará o status atual. Se o botão for clicado (habilitado) e o botão indicar "habilitar", ele poderá ser confuso e problemático. "Habilitar" pode solicitar que o usuário clique nele pensando que o processo não está ativo.

### <a name="sometimes-a-listview-is-better"></a>Às vezes, um ListView é melhor

geralmente, periremos para DataGrid ou ListBox ou até mesmo ComboBox para tarefas de seleção, mas com Windows XP e versões posteriores do Windows, usar um ListView pode fornecer opções maiores.

Os pontos finos do controle ListView:

-   Acelera o reconhecimento de itens com ícones e bitmaps.
-   Exibe informações adicionais com detalhes ou exibições de bloco.
-   com o Visual Studio 2005, você pode até mesmo ter grupos para categorização adicional. Os grupos se estendem por todas as exibições e são flexíveis. Os grupos também podem ser usados para mesclar uma exibição de hierarquia (como uma TreeView) em que há mais nós filho do que os nós pai. um bom exemplo disso é a caixa de diálogo conexões de rede no Windows XP, quando exibida com "mostrar em grupos" e a exibição definida como detalhes.
-   Para personalizar um controle ListView, pinte-o manualmente definindo a propriedade **OwnerDraw** e usando os eventos **DrawItem** e **DrawSubItem** .
-   Dá suporte à edição rápida in-loco de itens ListView.
-   Dá suporte facilmente à reordenação manual.
-   Permite que os usuários selecionem o modo de exibição (ícones grandes, ícones pequenos, lista e assim por diante) com os quais estão mais familiarizados.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Simplifique a navegação com controles de navegação estrutural e barras laterais

A "subnavegação" é a chave para a interface do usuário complexa. Às vezes, você não pode escapar ter uma interface do usuário complicada. A melhor coisa a fazer nessa situação é tornar a experiência o mais fácil possível para o usuário. Uma barra lateral que consiste em rótulos de link ou em um TreeView para navegação baseada em hierarquia, sugere uma navegação de nível irmão para a tarefa da caixa de diálogo atual. Ele torna muito fácil para o usuário saltar entre as etapas do processo e saber onde ela está.

Se você for para uma navegação baseada em hierarquia com TreeViews ou outra navegação complexa semelhante, um bom utilitário para o usuário seria um controle de navegação estrutural. embora Visual Studio ainda não seja fornecido com um controle interno para isso, consulte [criando um controle de navegação estrutural](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) para obter informações sobre como criar um por conta própria. Um controle de amplitude facilita a localização atual em relação à hierarquia.

A navegação breadcrumb pode ser facilmente mesclada no header se o formulário tiver um. Consulte a seção anterior em [headers](#simplify-recognition-with-headers).

### <a name="use-pretty-graphics"></a>Usar elementos gráficos

Todos gostam de aplicativos com gráficos interessantes– a maioria, pelo menos. Embora uma interface do usuário com elementos gráficos interessantes não seja uma opção lógica para todos os aplicativos, ela ajuda a dar uma boa impressão e pode ser um prazer trabalhar. É claro que os gráficos não devem impedir a produtividade, mas se usados corretamente, eles podem aumentar isso!

Não precisa haver muitos gráficos, nem eles exigem necessariamente muito trabalho. Uma tela inicial projetada profissionalmente ou um header (como aquele sobre o qual falamos anteriormente) faz o truque. Se o orçamento permitir, você poderá usar gráficos bem projetados para barras de ferramentas, assistentes e muito mais. Eles também fazem com que seu aplicativo pareça muito mais profissional. É um efeito sutil, mas uma aparência profissional transmite confiança e estabilidade. Se você for uma empresa relativamente pequena que cria aplicativos de varejo, esse é um aspecto importante a ser considerado.

Sempre faça questão de usar gráficos projetados profissionalmente. Gráficos sem royalties são facilmente disponíveis e acessíveis. Você também pode contratar um designer. Mas se os gráficos não são seu forte, não tente você mesmo. Se você não puder adquirir ou usar gráficos projetados profissionalmente, é melhor não usá-los.

Para gráficos pequenos, você sempre pode ir para os ícones e bitmaps que são Visual Studio 2005. (Os gráficos fornecidos com versões anteriores não são recomendados!)

### <a name="provide-resizable-forms-when-possible"></a>Fornecer formulários reizáveis quando possível

Janelas reizáveis são um pouco parecidos com janelas independentes de resolução. As janelas independentes de resolução são iguais se você usa telas 96DPI ou 300DPI. Se a interface do usuário do aplicativo for independente de resolução ou não, ela será melhor se for resizável. É claro que isso não se aplicaria a muitos cenários, mas é uma boa regra de uso geral.

Se sua janela lida com listas de qualquer tipo, especialmente ListViews, isso se torna ainda mais importante. O resizing permite que o usuário veja mais dados ao mesmo tempo.

Por exemplo, temos um aplicativo em que o usuário precisa selecionar uma imagem de uma coleção grande. A caixa de diálogo aberta permite que você selecione uma exibição miniatura, mas a caixa de diálogo tem tamanho fixo e a lista de miniaturas mostra apenas quatro miniaturas por vez. Se a coleção tiver centenas de imagens, rolar e procurar – uma tarefa repetitiva – poderá ser bastante cansativa e uma diminuição na eficiência. Se a caixa de diálogo for reizável, o usuário poderá torná-la tão grande quanto for confortável ou pelo menos tão grande quanto a tela permitir e ser capaz de concluir a tarefa rapidamente. Se sua lista tiver rolagem horizontal, como um ListView ou DataGrid detalhado, isso será ainda mais cansativa! Janelas reizáveis são muito úteis nessa situação.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Fornecer mais funcionalidade com barras laterais/painéis de tarefa

Assim como os headers que falamos anteriormente, as barras laterais e os painéis de tarefas são uma ótima maneira de fornecer funcionalidade extra e comandos de utilitário. Por exemplo, os painéis de tarefa Office Word 2003 são muito convenientes, acessíveis e não intrusivos. Eles também funcionam de forma assíncrona ao se conectar a recursos online, fornecendo ao usuário a opção de várias tarefas.

Criar um painel de tarefas ou barra lateral é tão fácil quanto criar um painel de encaixe, com a opção de colocar um gráfico na parte superior para atuar como uma barra de título. Você pode até mesmo usar um controle Rótulo colorido para isso. As oportunidades para painéis de tarefas são muitas!

Se você tiver funcionalidade adicional e quiser forneciá-la de forma não intrusiva ao usuário, não haverá nenhum lugar como o painel de tarefas. Você também pode fazer com que os painéis de tarefas "Ocultar Automaticamente" ou se ressumente como as janelas Visual Studio ferramentas.

### <a name="give-a-notification-choice"></a>Dar uma opção de notificação

Anteriormente, vimos como fazer uma caixa de mensagem personalizada. Se uma caixa de mensagem em seu aplicativo for exibida com frequência para o usuário, pode ser uma boa opção adicionar uma caixa de seleção que o usuário pode selecionar para desabilitar que a caixa de diálogo seja mostrada no futuro. Essa opção é especialmente boa para mensagens mais óbvias.

Um exemplo familiar disso é a caixa Visual Studio caixa de diálogo Encontrar. Quando você pesquisa ou substitui texto, Visual Studio mostra uma caixa de mensagem informando os resultados. Mas você também tem a opção de desabilitar essa caixa de mensagem. Isso pode ser muito entediante se você tiver que clicar em Enter ou clicar em OK toda vez que pesquisar.

Outra coisa interessante Visual Studio é que, mesmo que a caixa de diálogo esteja desabilitada, ela ainda exibirá os resultados dessa operação na barra de status.

### <a name="provide-tooltips"></a>Forneça dicas de ferramenta!

Às vezes, dicas de ferramenta podem economizar muito tempo. Botões, caixas de seleção e outros controles podem ser ambíguos e o usuário pode não ter certeza do que fazer. As dicas de ferramenta fornecem a melhor forma de Ajuda contextitivo em apenas uma única linha. O usuário pode decidir rapidamente o que fazer sem pesquisar nada no arquivo de Ajuda ou abrir outra janela.

As pessoas geralmente ignoram isso em seus aplicativos. Faça questão de adicionar dicas de ferramenta a todos os controles ambíguos ou a todos os controles, se possível. Não repita o texto de um rótulo de acompanhamento ou do próprio texto desse controle, mas forneça informações adicionais sobre esse controle. O texto deve explicar a função do controle em apenas algumas palavras.

### <a name="do-not-forget-the-little-things"></a>Não se esqueça das pequenas coisas

As pequenas coisas podem desabordá-lo, mas ignorá-los pode afetar a impressão que você tem. Uma vez, usei um aplicativo feito por uma pessoa importante no setor de software que tinha o BorderStyle do formulário definido como Sizeable, mas os controles no lado direito do formulário não estavam ancorados. Por isso, o aplicativo criado por um profissional do setor tinha uma sensação não profissional.

Esses tipos de "pequenas coisas" são o núcleo da impressão geral. A interface do usuário e a UX do aplicativo são o que os usuários vão avaliar seu aplicativo– pelo menos, primeiro. Se eles veem bugs óbvios em sua interface do usuário, eles podem perceber que seu aplicativo é menos eficiente e eficiente.

## <a name="conclusion"></a>Conclusão

Nós tocamos apenas em uma pequena parte da experiência do usuário humano. À medida que a experiência do usuário se torna mais simples, eficaz, divertida e mais amigável, a tarefa de criar essa experiência do usuário se torna muito mais complexa. Mas com alguma previsão e bom planejamento, você pode criar uma ótima experiência do usuário.

A melhor maneira de criar a experiência do usuário perfeita é fazer testes de usabilidade direcionados especialmente à interface do usuário, seja com um grupo de teste especial ou por conta própria. Quanto mais tempo você gastar testando a experiência do usuário antes de liberar seu aplicativo, melhor. Isso lhe causará muitos problemas posteriormente.

 

 