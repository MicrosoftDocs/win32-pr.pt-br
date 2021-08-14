---
title: Acessibilidade (noções básicas de Design)
description: A criação de software para acessibilidade significa garantir que os programas e a funcionalidade estejam facilmente disponíveis para a maior variedade de usuários, incluindo aqueles que têm deficiências e deficiências.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c38eb3993880d820a4e65fa25a1e910e9e842de823779aaf3ef24dab8635e60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212419"
---
# <a name="accessibility-design-basics"></a>Acessibilidade (noções básicas de Design)

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

A criação de software para acessibilidade significa garantir que os programas e a funcionalidade estejam facilmente disponíveis para a maior variedade de usuários, incluindo aqueles que têm deficiências e deficiências.

O número de usuários que os recursos de acessibilidade podem ajudar a surpreender você; por exemplo, no Estados Unidos, as pesquisas mostraram que mais da metade de todos os usuários do computador enfrentam dificuldades ou deficiências relacionadas à acessibilidade, e provavelmente se beneficiarão do uso da tecnologia acessível. Além disso, abordar o design de software com a flexibilidade e a inclusividade que são os diferenciais da acessibilidade geralmente resulta em maior usabilidade e satisfação do cliente.

![captura de tela da caixa de diálogo "facilidade de acesso da central" ](images/inter-accessibility-image1.png)

O centro de facilidade de acesso, disponível no painel de controle, fornece um local central onde os usuários podem escolher e personalizar os recursos de acessibilidade que desejam.

**Observação:** As diretrizes relacionadas ao [teclado](inter-keyboard.md), ao [mouse](inter-mouse.md), à [cor](vis-color.md)e ao [som](vis-sound.md) são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

Muitos fatores físicos, perceptiva e cognitivas entram em jogo quando os usuários interagem com hardware e software do computador. Antes de considerar maneiras de tornar os recursos do seu programa mais acessíveis, ele ajuda a saber quais tipos de deficiências e deficiências existem e algumas das tecnologias assistenciais com as quais esses usuários podem trabalhar enquanto interagem com computadores.

### <a name="types-of-impairments"></a>Tipos de deficiências

A tabela a seguir descreve as deficiências e os deficiências de usuários comuns e lista algumas das soluções mais importantes usadas para tornar os computadores mais acessíveis.



| Deficiência    | Descrição   | Soluções  |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visual<br/>             | Varia de leve (afetando 17% dos usuários) a graves (afetando 9% dos usuários).<br/>                                                                                                   | Ampliação, cores e contraste personalizáveis; Utilitários de braille; leitores de tela.<br/>                                                                                       |
| Audição<br/>            | Varia de leve (afetando 18% dos usuários) a graves (afetando 2% dos usuários).<br/>                                                                                                   | Redundância de informações: som usado apenas como suplemento para a comunicação de texto ou Visual.<br/>                                                                                     |
| Destreza<br/>          | Varia de leve (afetando 19 por cento dos usuários) a graves (afetando 5% dos usuários). Esse desemparelhamento geralmente envolve dificuldade para executar determinadas habilidades motoras com o teclado ou o mouse.<br/> | Redundância de método de entrada: recursos de programa acessados por mouse ou equivalentes de teclado.<br/>                                                                                       |
| Cognitiva<br/>          | Inclui deficiências de memória e diferenças de perceptiva. Afeta 16 por cento dos usuários.<br/>                                                                                                         | Interface do usuário altamente personalizável (IU); uso de [divulgação progressiva](ctrl-progressive-disclosure-controls.md) para ocultar a complexidade; uso de ícones e outros auxílios visuais.<br/> |
| Tomada<br/>            | Inclui sensibilidade visual para movimentação e intermitência.<br/>                                                                                                                                        | Abordagem conservadora para interfaces modulating, como o uso de animações; evitando a cintilação da tela no intervalo entre 2 hertz (Hz) e 55 Hz.<br/>                        |
| Fala ou linguagem<br/> | Inclui dificuldades de comunicação de dislexia e oral.<br/>                                                                                                                                       | Utilitários de verificação ortográfica e verificação gramatical; reconhecimento de fala e tecnologia de conversão de texto em fala.<br/>                                                                                 |



 

Para obter mais diretrizes sobre como ajudar os usuários com esses deficiências, consulte [resolvendo deficiências específicas](#addressing-particular-impairments) posteriormente neste artigo.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Tipos de tecnologias assistenciais e recursos de acessibilidade

**Leitores de tela**

Um leitor de tela permite que os usuários com deficiências visuais ou deficiências naveguem por uma interface do usuário transformando visuais em áudio. Assim, o texto da interface do usuário, controles, menus, barras de ferramentas, elementos gráficos e outros elementos da tela são falados pela voz em computador do leitor de tela. Para criar um programa otimizado para tecnologia assistencial do leitor de tela, você deve planejar como o leitor de tela identificará cada elemento da interface do usuário.

Cada elemento da interface de usuário com o qual o usuário pode interagir deve ser acessível pelo teclado, bem como ser exposto por meio de uma API (interface de programação de aplicativo) de acessibilidade. é recomendável usar a automação da interface do usuário, a nova estrutura de acessibilidade para todas as versões do Microsoft Windows que dão suporte ao Windows Presentation Foundation (WPF). A automação da interface do usuário fornece acesso programático à maioria dos elementos na área de trabalho, permitindo que os produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário e manipulem a interface do usuário por meio de uma entrada padrão (por exemplo, em vez de ou além de manipular o mouse ou o teclado). Para obter mais informações, consulte [visão geral da automação da interface do usuário](/dotnet/framework/ui-automation/ui-automation-overview).

Lembre-se de que, embora os leitores de tela sejam uma tecnologia assistencial muito importante, também há outros. Para obter mais informações sobre a variedade de tecnologias disponíveis, consulte [tipos de produtos de tecnologia assistencial](https://www.microsoft.com/enable/at/types.aspx).

**Reconhecimento de fala**

o reconhecimento de fala é um recurso de acessibilidade no Windows que permite que os usuários interajam com seus computadores por voz, reduzindo a necessidade de interação do motor com o mouse ou o teclado. Os usuários podem ditar documentos e emails, usar comandos de voz para iniciar e alternar entre programas, controlar o sistema operacional e até mesmo preencher formulários na Web.

**Lupa**

A ampliação ajuda os usuários com pouca visão, aumentando os itens na tela em qualquer lugar, de 2 a 16 vezes o original. Os usuários podem definir esse recurso para rastrear o mouse (para ver uma versão ampliada do que o mouse está apontando), o teclado (para ver a área em que o ponteiro se move ao usar a tabulação) ou a edição de texto (para ver o que estão digitando).

**Configurações visuais e esquemas de cores**

Além de tornar as coisas na tela maiores, os usuários com deficiência visual podem se beneficiar das configurações do sistema como o [modo de alto contraste](glossary.md) ou a capacidade de personalizar esquemas de cores em primeiro plano e em segundo plano.

**Narrator**

o narrator é um leitor de tela reduzido em Windows que permite aos usuários ouvir o texto na tela e os elementos da interface do usuário lidos em voz alta, inclusive alguns eventos (incluindo mensagens de erro) que acontecem espontaneamente. O usuário pode ouvir os menus do narrador sem sair da janela ativa.

![captura de tela da caixa de diálogo ' Microsoft Narrator ' ](images/inter-accessibility-image2.png)

Os usuários podem personalizar a extensão para a qual o Microsoft Narrator é usado.

**Teclado virtual**

Para usuários que têm dificuldade com teclados físicos e precisam usar um dispositivo de entrada alternativo, como um comutador, teclados na tela são uma necessidade. Os usuários podem selecionar chaves usando o mouse ou outro dispositivo apontador, um pequeno grupo de chaves ou apenas uma chave, dependendo de como você configurou o teclado virtual.

**Teclas do mouse**

Com as teclas do mouse habilitadas, os usuários que preferem o teclado podem usar as teclas de direção no teclado numérico para mover o ponteiro do mouse.

para obter uma lista completa dos recursos de acessibilidade, consulte [acessibilidade no Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) no site da Microsoft.

### <a name="keyboard-based-navigation"></a>Navegação baseada em teclado

A tecla Tab, as teclas de direção, a barra de espaço e a tecla Enter são importantes para navegação baseada em teclado. Pressionar os ciclos de tabulação de [entrada enfoca](glossary.md) os diferentes grupos de controle e pressionar as teclas de seta se move dentro de um controle ou entre controles dentro de um grupo. Pressionar a barra de espaço é o mesmo que clicar no controle com foco de entrada, enquanto pressionar Enter é o mesmo que clicar no botão de comando padrão ou link de comando, independentemente do foco de entrada.

![captura de tela da caixa de diálogo ' lixeira vazia ' ](images/inter-accessibility-image3.png)

Neste exemplo, os usuários podem pressionar TAB até que a opção desejada tenha o foco de entrada e, em seguida, pressionar Enter para abrir o objeto.

### <a name="access-keys"></a>Chaves de acesso

As chaves de acesso permitem que os usuários escolham opções e iniciem comandos diretamente sem precisar navegar até o controle primeiro. As chaves de acesso são indicadas por meio do sublinhado de um dos caracteres no rótulo de cada controle. Em seguida, os usuários ativam a opção ou o comando pressionando a tecla ALT junto com o caractere sublinhado. Chaves de acesso não diferenciam maiúsculas de minúsculas.

![captura de tela do menu arquivo e teclas de acesso ](images/inter-accessibility-image4.png)

Neste exemplo, pressionar ALT + O ativa o comando abrir.

A escolha de chaves de acesso lógico para controles geralmente não representa dificuldade; Quanto mais controles houver em uma janela, maior será a possibilidade de você se esgotar das opções de chave de acesso. Nesse caso, atribua chaves de acesso para grupos de controle em vez de cada uma delas.

![captura de tela de grupos de controle e chaves de acesso ](images/inter-accessibility-image5.png)

Neste exemplo, as chaves de acesso são atribuídas a grupos de controle, em vez de controles individuais.

As chaves de acesso geralmente são confundidas com teclas de atalho, mas as teclas de atalho são atribuídas de forma diferente das chaves de acesso e têm metas diferentes. Por exemplo, as teclas de atalho usam as sequências de teclas CTRL e Function e se destinam principalmente a um atalho para usuários avançados em vez de para acessibilidade.

Para obter mais informações, consulte [teclado](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Design para acessibilidade: três práticas fundamentais

Os programas acessíveis ajudam todos os usuários de alguma forma, pois os objetivos de acessibilidade e de usabilidade se sobrepõem. Por exemplo, os recursos projetados para tornar os usuários avançados tão eficientes quanto possível também beneficiam os usuários que preferem usar o teclado devido a deficiências físicas.

Três práticas fundamentais ajudarão você com o design acessível: permita um grau de flexibilidade em sua interface do usuário, para que as preferências e as necessidades dos usuários tenham uma função importante nas decisões de design e forneçam acesso programático à sua interface de usuário.

**Fornecendo interface do usuário flexível**

O design acessível é, pelo menos, em parte, sobre a concessão de opções aos usuários. Não é uma matriz frustrante, espantosa de opções, mas um número limitado de opções que antecipam de forma inteligente as necessidades dos usuários. "Não gosta de navegar por meio do mouse? Aqui, você pode fazer as mesmas coisas usando apenas o teclado. Não gosta de teclados físicos? Aqui está um virtual que você pode usar na tela. "

Por exemplo, forneça flexibilidade:

-   Fornecendo equivalentes selecionáveis pelo usuário para elementos que não são de texto (por exemplo, texto ALT para gráficos e legendas para áudio).

    ![captura de tela do botão de entrada](images/inter-accessibility-image6.png)

    ![captura de tela de texto ALT para botão de entrada](images/inter-accessibility-image7.png)

    Os usuários que optaram por não renderizar os elementos gráficos devem ver o texto alt em vez disso, descrevendo o que o controle faz e como interagir com ele.

-   Fornecendo alternativas à cor (por exemplo, diferenciação de ícone ou o uso de sons).

    ![captura de tela de ícones em tons de cinza (escala de cinza) ](images/inter-accessibility-image8.png)

    Neste exemplo, os ícones padrão são prontamente distinguiveis com base em seus designs.

-   Garantir o acesso ao teclado (por exemplo, uma parada de tabulação para cada controle interativo) para que os usuários possam realizar as mesmas coisas em seu programa com o mouse ou o teclado.
-   Garantir que seu programa ofereça boas opções de contraste de cores para os usuários. Windows fornece uma opção de alto contraste, mas isso é realmente projetado para ser uma solução para um grave deficiência visual. Outras opções de contraste atendem melhor aos usuários com deficiência leve, como visão baixa e cegueira para cores.
-   Garantir que os usuários tenham uma maneira de ajustar o tamanho do texto na interface do usuário do programa (por exemplo, por meio de um controle deslizante ou de uma caixa suspensa para o tamanho da fonte). Se possível, dê suporte ao modo DPI (pontos por polegada).
-   Garantir que seu programa seja multimodal, o que significa que, se o modo principal do programa estiver inacessível para alguns, esses usuários terão uma forma de contornar o problema. Por exemplo, quando a animação é exibida, as informações devem ser displayáveis em pelo menos um modo de apresentação não animado na opção do usuário.

As interfaces multimodal e a navegação flexível essencialmente oferecem ao usuário a arquitetura de redundância de informações. As redundâncias às vezes têm connotações negativas; no texto da interface do usuário, por exemplo, aconselhamos a remoção da redundância para simplificar a experiência de leitura. Mas, no contexto de acessibilidade, a redundância denota mecanismos e experiências positivas e com falhas.

**Respeitando os usuários**

Como um princípio geral, a concepção é vital para a criação de programas acessíveis. Mesmo como um exercício intelectual, imagine o que deve ser semelhante a encontrar seu programa como um usuário que está desabilitado. Reserve um tempo para testar as telas da interface do usuário no modo de alto contraste e em várias resoluções, para garantir que a experiência seja uma boa para os usuários com deficiências visuais. Teste a acessibilidade do teclado marcando a caixa de seleção **sublinhar atalhos de teclado e chaves de acesso** no item do painel de controle de facilidade de acesso (para que as chaves de acesso estejam sempre visíveis). Você pode até mesmo além de testes rigorosos contratando desenvolvedores e designers que têm uma aptitude natural para Empathizing com outras pessoas começarem.

Você também deve demonstrar respeito ao:

-   Usando configurações de todo o sistema (por exemplo, cor do sistema) em vez de configurações de logoff para seu programa específico. Respeite não apenas os parâmetros que os usuários selecionaram especificamente para interagir com seus programas, mas também recursos de acessibilidade incorporados ao sistema operacional que o usuário deseja em vigor, independentemente do programa que estiverem usando. para obter mais informações, consulte [sobre Windows recursos de acessibilidade](/previous-versions//ms695605(v=vs.85)).
-   preferir controles comuns a controles personalizados, pois os controles comuns já implementaram as APIs de acessibilidade do Windows.
-   Documentar todas as opções e recursos de acessibilidade (por exemplo, todos os atalhos de teclado). Os usuários com deficiências são altamente motivados a descobrir recursos de acessibilidade e, muitas vezes, esperam que informações abrangentes sejam coletadas na ajuda.
-   Criando documentação acessível em formatos acessíveis. Portanto, a documentação em si deve aderir às mesmas regras de acessibilidade que a interface do usuário principal, incluindo a capacidade de aumentar o tamanho da fonte, o uso de texto ALT para gráficos e a arquitetura de informações redundantes (por exemplo, usando codificação de cores somente como um suplemento para texto).

Em produtos de software, o respeito aos usuários pode se manifestar em usabilidade e pesquisa de mercado, em serviços de suporte do efficacious e documentação e, obviamente, em decisões de design. Por exemplo, pensando novamente em termos de design para usuários avançados: você está colocando esse novo recurso de ponta no porque deseja, ou porque você sabe que seus usuários avançados foram solicitados a fazê-lo? O último caso indica que o processo de tomada de decisão de design é bem informado pelo valor de respeito.

**Fornecendo acesso programático**

Fornecer acesso programático à interface do usuário é essencial para que as tecnologias assistenciais (como leitores de tela, dispositivos de entrada alternativos e programas de reconhecimento de fala) interpretem a tela corretamente para seus usuários. Ao criar um "mapa" de cada tela da interface do usuário em seu programa, você o disponibiliza para os usuários de tecnologias assistenciais.

Faça isso de forma bem:

-   Habilitando o acesso programático a todos os elementos e texto da interface do usuário (por exemplo, usando a interface COM Acessibilidade Ativa, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Colocar nomes (ou títulos) e descrições em objetos, quadros e páginas da interface do usuário (por exemplo, usando a propriedade nome do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ).
-   Garantir eventos programáticos é disparado por todas as atividades da interface do usuário (por exemplo, eventos de foco para todas as atividades de interface do usuário envolvendo o movimento de

**Se você fizer apenas quatro coisas...**

1.  Garanta que cada usuário possa aproveitar todo o potencial do seu programa.
2.  Considere a acessibilidade como uma oportunidade para a solução criativa de problemas e outro meio de aumentar a satisfação geral do usuário.
3.  Respeitar as configurações do sistema.
4.  Use controles comuns sempre que possível.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não interrompa nem desabilite os recursos ativados do sistema operacional ou outros produtos identificados como recursos de acessibilidade.** Você pode identificar esses recursos consultando a documentação do sistema operacional ou produto em questão.
-   **Não force os usuários a interagir com seu programa como a janela superior na tela.** Se uma função ou uma janela for necessária continuamente para que os usuários executem uma tarefa, essa janela sempre deverá permanecer visível, se o usuário escolher, independentemente de sua posição em relação a outras janelas. Por exemplo, se o usuário tiver um teclado móvel na tela que esteja na parte superior de todas as outras janelas para que fique visível o tempo todo, o programa nunca deverá obscurecer o posicionamento obrigatório na parte superior da [ordem Z](glossary.md).
-   **Use cores do sistema, fontes e controles comuns sempre que possível.** Ao fazer isso, você reduz significativamente o número de problemas de acessibilidade que os usuários encontram.

### <a name="addressing-particular-impairments"></a>Endereçamento de deficiências específicas

**Visualizar**

-   **Nunca confie apenas na cor para transmitir significado.** Use a cor apenas como um meio de rereforçar o significado fornecido por texto, design, local ou som.

    ![captura de tela do ícone e da dica de ferramenta do Communicator vermelho ](images/inter-accessibility-image9.png)

    O principal método de comunicação neste exemplo é o texto de dica de ferramenta conciso. O uso de ajuda de cores na comunicação do significado, mas é secundário.

-   **Use Infotips de texto alternativo (Alt) para descrever os gráficos.**
-   **Não use texto em elementos gráficos.** Os usuários com deficiências visuais podem ter gráficos desativados (por exemplo, em um navegador da Web) ou simplesmente não podem ver ou procurar texto colocado em gráficos.
-   **Verifique se as caixas de diálogo e janelas têm nomes significativos,** para que um usuário que esteja ouvindo em vez de ver a tela (por exemplo, usando um leitor de tela) obtenha informações contextuais apropriadas.
-   **respeite as configurações do usuário para exibição visual** sempre obtendo tipos de fonte, tamanhos e cores, Windows exibir tamanhos de elemento e definições de configuração do sistema das APIs de tema e GetSystemMetrics.
-   **Mantenha o texto conciso em balão** para facilitar a leitura e minimizar a interrupção nos leitores de tela.

    ![captura de tela de balão indicando limites de código PIN ](images/inter-accessibility-image10.png)

    Embora os balões possam usar corpo de texto adicional, se necessário, este exemplo mostra que, às vezes, o título de texto sozinho atinge o mesmo objetivo de uma maneira mais econômica e acessível.

**Audição**

-   **Nunca confie apenas no som para transmitir significado.** Use o som apenas como um meio de rereforçar o significado fornecido pelo texto, design, local ou cor.
-   **Permitir que os usuários controlem o volume de saída de áudio.** Use o Mixer Windows Volume para essa finalidade. Para obter mais informações, consulte [som](vis-sound.md).
-   **Direcione o som do seu programa para ocorrer em um intervalo entre 500 Hz e 3000 Hz** ou ser facilmente ajustável pelo usuário nesse intervalo. Os sons nesse intervalo têm maior probabilidade de serem detectáveis por pessoas com deficiência auditiva.

**Destreza**

-   **Torne os valores de tempo limite da interface do usuário relativos a GetDoubleClickTime () em vez de usar horários absolutos.** Isso ajusta os tempos limite para a velocidade do usuário.
-   **Atribua chaves de acesso a todos os itens de menu** para que os usuários que preferem trabalhar com o teclado tenham a mesma capacidade de navegar pelo seu programa como usuários que trabalham com o mouse.
-   **Não faça um clique duplo e arraste a única maneira de executar uma ação.** Eles podem ser movimentações difíceis para alguns usuários.
-   **Não remova as barras de menu do seu programa.** As barras de menu são mais fáceis do que as barras de ferramentas para que os usuários do teclado acessem. Se você não quiser que a barra de menus fique visível por padrão, oculte-a.
-   **Torne a ajuda acessível do teclado fornecendo paradas de tabulação para botões e links de ajuda.**
-   **Para melhorar a conscientização das atribuições de chave de acesso em seu programa, você pode exibi-las em todos os momentos.** No painel de controle, acesse a central de facilidade de acesso e clique em **facilitar o uso do teclado**; em seguida, marque a caixa de seleção **sublinhar atalhos de teclado e chaves de acesso** .

**Cognitiva**

-   **Use a divulgação progressiva** para ocultar a complexidade.

    ![captura de tela de botões de divisão com triângulos inferiores ](images/inter-accessibility-image11.png)

    Nesses exemplos, as opções disponíveis no botão de comando ficam ocultas por padrão e os usuários podem optar por exibir as opções aproveitando os controles de divulgação progressiva.

-   **Use ícones, barras de ferramentas e outros auxílios visuais** para reduzir a carga cognitiva de leitura de texto.
-   Quando possível, **forneça a funcionalidade de preenchimento automático em caixas de texto e listas suspensas editáveis** para que os usuários não precisem digitar o nome inteiro de comandos, nomes de arquivos ou opções semelhantes de um conjunto limitado de opções. Isso reduz a carga cognitiva para todos os usuários e reduz a quantidade de digitação para usuários para os quais a ortografia ou a digitação é difícil, lenta ou complicada.
-   **Demonstre conceitos difíceis na Ajuda incluindo tutoriais e animações.** Observe que as animações podem ser difíceis para usuários com deficiências e, portanto, devem ser usadas somente quando necessário.

**Apreensão**

-   **Não use texto piscando ou piscando, objetos ou outros elementos com uma frequência de flash ou piscar no intervalo entre 2 e 55 Hz.**
-   **Limite o uso de animações.** Alguns usuários são particularmente sensíveis à movimentação da tela, especialmente na periférico do campo visual. Se você usar a animação para chamar a atenção para algo, certifique-se de que a atenção seja ressupida e meso de interromper o usuário.

**Fala ou idioma**

-   **Organize e escreva texto claro, conciso e facilmente compreendido.** Os testes de usabilidade mostram que o desenrolamento das principais informações no final de uma frase melhora a compreensão. Para obter mais diretrizes, consulte [Estilo e tom.](text-style-tone.md)

**Incorreto:**

Três são o próximo dígito?

Clique em OK para começar.

**Correto:**

O próximo dígito é três?

Para começar, clique em OK.

### <a name="access-keys"></a>Chaves de acesso

-   **Prefira caracteres com larguras largas,** como w, m e letras maiúsculas.
-   **Prefira uma consoante distinta ou uma voga,** como "x" em "Exit".
-   Evite usar caracteres que dificultam a viagem do **sublinhado,** como (da mais problemática para a menos problemática):
    -   Caracteres que têm apenas um pixel de largura, como i e l.
    -   Caracteres com descendentes, como g, j, p, q e y.
    -   Caracteres ao lado de uma letra com um descendente.

### <a name="menu-access-keys"></a>Teclas de acesso de menu

-   **Atribua chaves de acesso a todos os itens de menu.** Nenhuma exceção.
-   **Para itens de menu dinâmico (como arquivos usados recentemente), atribua chaves de acesso numericamente.**

    ![captura de tela do menu aberto com arquivos usados recentemente ](images/inter-accessibility-image12.png)

    Neste exemplo, o programa Paint em Windows atribui chaves de acesso numéricas a arquivos usados recentemente.

-   **Atribua chaves de acesso exclusivas em um nível de menu.** Você pode reutilizar chaves de acesso em diferentes níveis de menu.
-   **Tornar as chaves de acesso fáceis de encontrar:**
    -   Para os itens de menu usados com mais frequência, escolha caracteres no início da primeira ou segunda palavra do rótulo, preferencialmente o primeiro caractere.
    -   Para itens de menu usados com menos frequência, escolha letras que sejam uma consoantes distintas ou uma voga no rótulo.

### <a name="dialog-box-access-keys"></a>Chaves de acesso da caixa de diálogo

-   **Sempre que possível, atribua chaves de acesso exclusivas a todos os controles interativos ou seus rótulos.** [As caixas de texto somente leitura](ctrl-text-boxes.md) são controles interativos (porque os usuários podem rolar e copiar texto), portanto, eles se beneficiam das chaves de acesso. **Não atribua chaves de acesso a:**
    -   **Botões OK, Cancelar e Fechar.** Enter e Esc são usados para suas chaves de acesso. No entanto, sempre atribua uma chave de acesso a um controle que significa OK ou Cancelar, mas tem um rótulo diferente.

        ![captura de tela de controles com chaves de acesso atribuídas ](images/inter-accessibility-image13.png)

        Neste exemplo, o botão de confirmação positiva tem uma chave de acesso atribuída.

-   **Rótulos de grupo.** Normalmente, os controles individuais em um grupo são atribuídos a chaves de acesso, portanto, o rótulo do grupo não precisa de uma. No entanto, atribua uma chave de acesso ao rótulo do grupo e não aos controles individuais se houver uma falta de chaves de acesso.
-   **Botões de Ajuda Genérica,** que são acessados com F1.
-   **Rótulos de link.** Geralmente, há muitos links para atribuir chaves de acesso exclusivas e sublinhados de link ocultam os sublinhados da chave de acesso. Fazer com que os usuários acessem links com a tecla Tab.
-   **Nomes de tabulação.** As guias são ciclodas usando Ctrl+Tab e Ctrl+Shift+Tab.
-   **Procure os botões rotulados como "...".** Elas não podem ser atribuídas exclusivamente a chaves de acesso.
-   **Controles sem rótulo, como controles** de rotação, botões de comando gráfico e controles de divulgação progressiva sem rótulo.
-   **Texto estático sem rótulo ou rótulos para controles que não são interativos,** como barras de progresso.
-   **Atribua primeiro as chaves de acesso do botão de confirmação para garantir que elas tenham as atribuições de chave padrão.** Se não houver uma atribuição de chave padrão, use a primeira letra da primeira palavra. Por exemplo, a chave de acesso para botões Sim e Não de confirmação sempre deve ser "Y" e "N", independentemente dos outros controles na caixa de diálogo.
-   **Para botões de confirmação negativos (diferente de Cancelar) formulados como "Não", atribua a chave de acesso ao "n" em "Não fazer".** Se não for formulado como "Não", use a atribuição de chave de acesso padrão ou atribua a primeira letra da primeira palavra. Ao fazer isso, todos os Don'ts e No têm uma chave de acesso consistente.
-   Para tornar as chaves de acesso fáceis de encontrar, atribua as chaves de acesso a um caractere que aparece no início do **rótulo,** idealmente o primeiro caractere, mesmo que haja uma palavra-chave que apareça posteriormente no rótulo.

Para obter mais diretrizes e exemplos, consulte [Teclado](inter-keyboard.md).

## <a name="text"></a>Texto

-   **Use dois-pontos no final dos rótulos de controle externo.** Algumas tecnologias adaptativas procurarão dois-pontos para identificar rótulos de controle.
-   **Posiciona rótulos de forma consistente em relação aos elementos que eles estão rotulando.** Isso ajuda a tecnologia adaptativa a associar corretamente os rótulos aos controles correspondentes e ajuda os usuários de ampliadores de tela a saber onde procurar um rótulo ou controle.

    ![captura de tela de rótulos colocados consistentemente ](images/inter-accessibility-image14.png)

    Neste exemplo, os rótulos de cada uma das listas listadas são colocados de forma consistente e usam dois-pontos.

-   **Limite o texto alt a um máximo de 150 caracteres.** Descreva a ação para ativar o controle (por exemplo, clique, clique com o botão direito do mouse e assim por diante) e descreva a função do controle.

    **Aceitável:**

    Botão.

    Blue blue blue.

    **Melhor:**

    Clique para entrar em sua conta.

    Foto de um arco distante mostrando como as cores esmaecem ao longo da distância.

-   **Não use texto para desenhar linhas, caixas ou outros símbolos gráficos.** Os caracteres usados dessa maneira podem confundir os usuários de leitores de tela. Por exemplo, uma caixa desenhada com a letra "X" em torno de uma área de texto é lida pelo software de leitor de tela como "X X X X X X X" na primeira linha, seguida por "X" e o conteúdo e "X".

## <a name="documentation"></a>Documentação

-   Documente todas as opções e recursos de acessibilidade (por exemplo, todos os atalhos de teclado).
-   Crie documentação acessível em formatos acessíveis. Portanto, a própria documentação deve seguir as mesmas regras de acessibilidade que a interface do usuário primária.
-   Consulte chaves de acesso, não teclas de atalho (que têm um significado e uso diferentes), teclas mnemônicas ou aceleradores.
-   Em geral, consulte uma pessoa com um tipo de deficiência, não uma pessoa desabilitada. Considere a pessoa primeiro, não o rótulo.



| Usar esses termos           | Em vez de                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| Tem limitação de agilidade, tem deficiências de movimento<br/>     | Comcodado, ao mesmo tempo<br/>                                                        |
| Sem deficiências<br/>                               | Normal, apto, ntente<br/>                                          |
| Com uma mão, pessoas que digitam com uma mão<br/>          | De mão única <br/>                                                        |
| Pessoas com deficiências<br/>                           | As pessoas desabilitadas, desabilitadas, as pessoas com deficiências, as pessoas com deficiência<br/> |
| Deficiências cognitivas, deficiências de desenvolvimento<br/> |                                                                                  |



 

