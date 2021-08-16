---
title: Acessibilidade (noções básicas de design)
description: Projetar software para acessibilidade significa garantir que programas e funcionalidades sejam facilmente disponíveis para a maior variedade de usuários, incluindo aqueles que têm deficiências e deficiências.
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
# <a name="accessibility-design-basics"></a>Acessibilidade (noções básicas de design)

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Projetar software para acessibilidade significa garantir que programas e funcionalidades sejam facilmente disponíveis para a maior variedade de usuários, incluindo aqueles que têm deficiências e deficiências.

O número de usuários que os recursos de acessibilidade podem ajudar pode lhe fazer uma surpresa; por exemplo, no Estados Unidos, pesquisas mostraram que mais da metade de todos os usuários de computador têm dificuldades ou deficiências relacionadas à acessibilidade e provavelmente se beneficiarão do uso de tecnologia acessível. Além disso, abordar o design de software com a flexibilidade e a inclusão que são as marcas de acessibilidade geralmente resulta em usabilidade geral aprimorada e satisfação do cliente.

![captura de tela da caixa de diálogo 'facilidade de acessar o centro' ](images/inter-accessibility-image1.png)

O Central de Facilidade de Acesso, disponível no Painel de Controle, fornece um local central em que os usuários podem escolher e personalizar os recursos de acessibilidade desejados.

**Observação:** Diretrizes relacionadas [ao teclado,](inter-keyboard.md) [mouse,](inter-mouse.md) [cor](vis-color.md) [e som](vis-sound.md) são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

Muitos fatores físicos, perceptcionais e cognitivos entra em jogo quando os usuários interagem com hardware e software do computador. Antes de considerar maneiras de tornar os recursos do programa mais acessíveis, ele ajuda a saber quais tipos de deficiências e deficiências existem e algumas das tecnologias adaptativas com as quais esses usuários podem estar trabalhando enquanto interagem com computadores.

### <a name="types-of-impairments"></a>Tipos de deficiências

A tabela a seguir descreve deficiências e deficiências comuns do usuário e lista algumas das soluções mais importantes usadas para tornar os computadores mais acessíveis.



| Deficiência    | Descrição   | Soluções  |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visual<br/>             | Varia de 17% dos usuários (afetando 17% dos usuários) a graves (afetando 9% dos usuários).<br/>                                                                                                   | Ampliação, cores e contraste personalizáveis; Utilitários de Utilities de Utilities; leitores de tela.<br/>                                                                                       |
| Audição<br/>            | Varia de grave (afetando 18% dos usuários) a graves (afetando 2% dos usuários).<br/>                                                                                                   | Redundância de informações: som usado apenas como suplemento para comunicação visual ou de texto.<br/>                                                                                     |
| Destreza<br/>          | Varia de grave (afetando 19% dos usuários) a graves (afetando 5% dos usuários). Essa deficiência geralmente envolve dificuldade para executar determinadas habilidades motoras com teclado ou mouse.<br/> | Redundância de método de entrada: recursos de programa acessados por equivalentes de mouse ou teclado.<br/>                                                                                       |
| Cognitiva<br/>          | Inclui deficiências de memória e diferenças perceptivas. Afeta 16% dos usuários.<br/>                                                                                                         | Interface do usuário altamente personalizável; uso da [divulgação progressiva](ctrl-progressive-disclosure-controls.md) para ocultar a complexidade; uso de ícones e outros auxílios visuais.<br/> |
| Apreensão<br/>            | Inclui a sensibilidade visual ao movimento e ao piscar.<br/>                                                                                                                                        | Abordagem conservadora para modular interfaces, como o uso de animações; evitando a cintilação de tela no intervalo entre 2 Hertz (Hz) e 55 Hz.<br/>                        |
| Fala ou idioma<br/> | Inclui dificuldades de comunicação de dislexia e de dislexia.<br/>                                                                                                                                       | Utilitários de verificação orttical e verificação de gramática; reconhecimento de fala e tecnologia de texto em fala.<br/>                                                                                 |



 

Para obter mais diretrizes sobre como ajudar os usuários com essas deficiências, consulte [Endereçamento de deficiências específicas](#addressing-particular-impairments) mais adiante neste artigo.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Tipos de tecnologias adaptativas e recursos de acessibilidade

**Leitores de tela**

Um leitor de tela permite que usuários com deficiências visuais ou deficiências naveguem em uma interface do usuário transformando visuais em áudio. Portanto, texto da interface do usuário, controles, menus, barras de ferramentas, elementos gráficos e outros elementos de tela são falados pela voz computadorizada do leitor de tela. Para criar um programa otimizado para tecnologia auxiliar de leitor de tela, você deve planejar como o leitor de tela identificará cada elemento de interface do usuário.

Cada elemento de interface do usuário com o que o usuário pode interagir deve ser acessível por teclado, bem como ser exposto por meio de uma API (interface de programação de aplicativo) de acessibilidade. É recomendável usar Automação da Interface do Usuário, a nova estrutura de acessibilidade para todas as versões do Microsoft Windows que oferecem suporte Windows Presentation Foundation (WPF). Automação da Interface do Usuário fornece acesso programático à maioria dos elementos na área de trabalho, permitindo que produtos de tecnologia adaptativa, como leitores de tela, forneçam informações sobre a interface do usuário para os usuários e manipulem a interface do usuário por meio diferente da entrada padrão (por exemplo, falando em vez de ou além de manipular o mouse ou o teclado). Para obter mais informações, consulte a [Automação da Interface do Usuário Visão geral.](/dotnet/framework/ui-automation/ui-automation-overview)

Esteja ciente de que, embora os leitores de tela sejam uma tecnologia auxiliar muito importante, há outros também. Para obter mais informações sobre a variedade de tecnologias disponíveis, consulte [Tipos de produtos de tecnologia adaptativa](https://www.microsoft.com/enable/at/types.aspx).

**Reconhecimento de fala**

O reconhecimento de fala é um recurso de acessibilidade no Windows que permite que os usuários interajam com seus computadores por voz, reduzindo a necessidade de interação motora com o mouse ou teclado. Os usuários podem ditar documentos e email, usar comandos de voz para iniciar e alternar entre programas, controlar o sistema operacional e até mesmo preencher formulários na Web.

**Lupa**

A ampliação ajuda os usuários com baixa visão ampliando itens na tela de 2 a 16 vezes o original. Os usuários podem definir esse recurso para acompanhar o mouse (para ver uma versão ampliada do que o mouse está apontando), o teclado (para ver a área para a qual o ponteiro se move durante a tabulação) ou a edição de texto (para ver o que está digitando).

**Configurações visuais e esquemas de cores**

Além de tornar as coisas na tela maiores, os usuários com [](glossary.md) deficiência visual podem se beneficiar das configurações do sistema, como o modo de alto contraste ou a capacidade de personalizar esquemas de cor em segundo plano e tela de fundo.

**Narrator**

O Narrador é um leitor de tela escalado para baixo no Windows que permite que os usuários escutam texto na tela e elementos da interface do usuário lidos em voz alta, mesmo incluindo alguns eventos (incluindo mensagens de erro) que ocorrem com segurança. O usuário pode ouvir os menus do Narrador sem sair da janela ativa.

![captura de tela da caixa de diálogo 'microsoft narrador' ](images/inter-accessibility-image2.png)

Os usuários podem personalizar a extensão até a qual o Microsoft Narrador é usado.

**Teclado na tela**

Para usuários que têm dificuldade com teclados físicos e precisam usar um dispositivo de entrada alternativo, como um comutadores, os teclados na tela são uma necessidade. Os usuários podem selecionar chaves usando o mouse ou outro dispositivo que aponta, um pequeno grupo de chaves ou apenas uma tecla, dependendo de como você configura o Teclado na Tela.

**Teclas do mouse**

Com as Teclas do Mouse habilitadas, os usuários que preferem o teclado podem usar as teclas de direção no teclado numérico para mover o ponteiro do mouse.

Para ver uma lista completa dos recursos de acessibilidade, consulte [Acessibilidade Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) no site da Microsoft.

### <a name="keyboard-based-navigation"></a>Navegação baseada em teclado

A tecla Tab, as teclas de direção, a barra de espaços e a tecla Enter são importantes para a navegação baseada em teclado. Pressionar Tab faz com que o [foco](glossary.md) de entrada entre os diferentes grupos de controle e pressionar as teclas de seta se mova dentro de um controle ou entre controles dentro de um grupo. Pressionar barra de espaço é o mesmo que clicar no controle com o foco de entrada, enquanto pressionar Enter é o mesmo que clicar no botão de comando padrão ou no link de comando, independentemente do foco de entrada.

![captura de tela da caixa de diálogo "lixeira vazia" ](images/inter-accessibility-image3.png)

Neste exemplo, os usuários podem pressionar Tab até que a opção desejada tenha o foco de entrada e pressione Enter para abrir o objeto.

### <a name="access-keys"></a>Chaves de acesso

As chaves de acesso permitem que os usuários escolham opções e iniciem comandos diretamente sem precisar navegar até o controle primeiro. As chaves de acesso são indicadas sublinhando um dos caracteres no rótulo de cada controle. Em seguida, os usuários ativam a opção ou o comando pressionando a tecla Alt junto com o caractere sublinhado. As chaves de acesso não são sensíveis a minúsculas.

![captura de tela do menu de arquivo e das chaves de acesso ](images/inter-accessibility-image4.png)

Neste exemplo, pressionar Alt+O ativa o comando Abrir.

Escolher chaves de acesso lógico para controles geralmente não representa nenhuma dificuldade; quanto mais controles houver em uma janela, maior será a possibilidade de você ficar sem opções de chave de acesso. Nesse caso, atribua chaves de acesso a grupos de controle em vez de cada um deles.

![captura de tela de grupos de controle e chaves de acesso ](images/inter-accessibility-image5.png)

Neste exemplo, as chaves de acesso são atribuídas a grupos de controle, em vez de controles individuais.

As chaves de acesso geralmente são confundidas com teclas de atalho, mas as teclas de atalho são atribuídas de maneira diferente das chaves de acesso e têm metas diferentes. Por exemplo, as teclas de atalho usam ctrl e sequências de teclas de função e são destinadas principalmente como um atalho para usuários avançados em vez de para acessibilidade.

Para obter mais informações, consulte [Teclado](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Projetando para acessibilidade: três práticas fundamentais

Programas acessíveis ajudam todos os usuários de alguma forma porque os objetivos de acessibilidade e usabilidade se sobrepõem. Por exemplo, os recursos projetados para tornar os usuários avançados o mais eficientes possível também beneficiam os usuários que preferem usar o teclado devido a deficiências de complexidade.

Três práticas fundamentais ajudarão você com design acessível: permitir um grau de flexibilidade em sua interface do usuário, permitir que o respeito às necessidades e preferências do usuário desempenham um papel importante nas decisões de design e fornecer acesso programático à sua interface do usuário.

**Fornecendo interface do usuário flexível**

O design acessível é, pelo menos em parte, sobre dar opções aos usuários. Não é uma matriz de escolhas frustrante, mas um número limitado de opções que antecipa com inteligência as necessidades do usuário. "Não gosta de navegar pelo mouse? Aqui, você pode fazer as mesmas coisas usando apenas o teclado. Não gosta de teclados físicos? Aqui está um virtual que você pode usar na tela."

Por exemplo, forneça flexibilidade:

-   Fornecendo equivalentes selecionáveis pelo usuário para elementos que não são de texto (por exemplo, texto alt para gráficos e legendas para áudio).

    ![captura de tela do botão de login](images/inter-accessibility-image6.png)

    ![captura de tela do texto alt para o botão de entrada](images/inter-accessibility-image7.png)

    Os usuários que optaram por não renderizar gráficos devem ver texto alt, descrevendo o que o controle faz e como interagir com ele.

-   Fornecendo alternativas à cor (por exemplo, diferenciação de ícone ou uso de sons).

    ![captura de tela de ícones em tons de cinza (escala de cinza) ](images/inter-accessibility-image8.png)

    Neste exemplo, os ícones padrão são prontamente distinguíveis com base em seus designs.

-   Garantir o acesso ao teclado (por exemplo, uma parada de tabulação para cada controle interativo) para que os usuários possam realizar as mesmas coisas em seu programa com o mouse ou o teclado.
-   Garantir que seu programa ofereça boas opções de contraste de cores para os usuários. Windows fornece uma opção de alto contraste, mas que é realmente projetada para ser uma solução para deficiência visual grave. Outras opções de contraste melhor atendem aos usuários com deficiências deficiências, como visão baixa e falta de cor.
-   Garantir que os usuários tenham uma maneira de ajustar o tamanho do texto na interface do usuário do programa (por exemplo, por meio de um controle deslizante ou caixa de lista de lista para o tamanho da fonte). Se possível, suporte ao modo dpi (pontos altos por polegada).
-   Garantir que seu programa seja multimodal, o que significa que, se o modo primário do programa estiver inacessível para alguns, esses usuários terão uma maneira de resolver o problema. Por exemplo, quando a animação é exibida, as informações devem ser exibidas em pelo menos um modo de apresentação não animado na opção do usuário.

Interfaces multimodal e navegação flexível oferecem essencialmente ao usuário a arquitetura de redundância de informações. Às vezes, a redundância tem conotações negativas; no texto da interface do usuário, por exemplo, recomendamos remover a redundância para simplificar a experiência de leitura. Mas, no contexto de acessibilidade, a redundância indica mecanismos e experiências positivos e seguros.

**Respeitando seus usuários**

O respeito como um princípio geral e orientador é essencial para a criação de programas acessíveis. Mesmo como um exercício intelectual, imagine como deve ser encontrar seu programa como um usuário desabilitado. Aproveite o tempo para testar telas de interface do usuário no modo de alto contraste e em várias resoluções, para garantir que a experiência seja uma boa para usuários com deficiências visuais. Teste a acessibilidade do teclado selecionando a caixa de seleção Atalhos de teclado sublinhados e teclas de acesso no item Central de Facilidade de Acesso Painel de Controle (para que as **teclas** de acesso sempre sejam visíveis). Você pode até mesmo ir além de testes rigorosos contratando desenvolvedores e designers que têm uma capacidade natural para empatia com outras pessoas para começar.

Você também deve demonstrar o respeito por:

-   Usando configurações de todo o sistema (por exemplo, Cor do Sistema) em vez de definir as configurações de hardwiring para seu programa específico. Respeita não apenas os parâmetros que os usuários selecionaram especificamente para interagir com seus programas, mas também recursos de acessibilidade integrados ao sistema operacional que o usuário deseja em vigor, independentemente do programa que está usando. Para obter mais informações, consulte [Sobre Windows recursos de acessibilidade.](/previous-versions//ms695605(v=vs.85))
-   Preferir controles comuns a controles personalizados, porque os controles comuns já implementaram as APIs Windows acessibilidade.
-   Documentando todas as opções e recursos de acessibilidade (por exemplo, todos os atalhos de teclado). Os usuários com deficiências são altamente incentivados a descobrir recursos de acessibilidade e geralmente esperam que informações abrangentes sejam coletadas na Ajuda.
-   Criando documentação acessível em formatos acessíveis. Portanto, a documentação em si deve seguir as mesmas regras de acessibilidade que a interface do usuário primária, incluindo a capacidade de ampliar o tamanho da fonte, o uso de texto alt para gráficos e a arquitetura de informações redundantes (por exemplo, usando a codificação de cores apenas como um suplemento para texto).

Em produtos de software, o respeito aos usuários pode se manifestar na usabilidade e na pesquisa de mercado, em documentação e serviços de suporte inequisidores e, obviamente, em decisões de design. Por exemplo, pensando novamente em termos de design para usuários avançados: você está colocando esse novo recurso de ponta porque você o deseja ou porque sabe que os usuários avançados estão solicitando isso? O último caso indica que seu processo de tomada de decisão de design é bem informado pelo valor de respeito.

**Fornecendo acesso programático**

Fornecer acesso programático à interface do usuário é essencial para que tecnologias adaptativas (como leitores de tela, dispositivos de entrada alternativos e programas de reconhecimento de fala) interpretem a tela corretamente para seus usuários. Ao criar um "mapa" de cada tela de interface do usuário em seu programa, você o disponibiliza aos usuários de tecnologias adaptativas.

Faça isso bem:

-   Habilitando o acesso programático a todos os elementos e textos da interface do usuário (por exemplo, usando a interface COM Acessibilidade Ativa, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Colocar nomes (ou títulos) e descrições em objetos, quadros e páginas da interface do usuário (por exemplo, usando a propriedade [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Name).
-   Garantir que os eventos programáticos sejam disparados por todas as atividades da interface do usuário (por exemplo, eventos de foco para todas as atividades de interface do usuário que envolvem a movimentação de foco).

**Se você fizer apenas quatro coisas...**

1.  Verifique se cada usuário pode aproveitar todo o potencial do seu programa.
2.  Pense na acessibilidade como uma oportunidade para solução de problemas criativos e outro meio de aumentar a satisfação geral do usuário.
3.  Respeitar as configurações do sistema.
4.  Use controles comuns sempre que possível.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não interromper ou desabilitar recursos ativados do sistema operacional ou outros produtos identificados como recursos de acessibilidade.** Você pode identificar esses recursos referindo-se à documentação do sistema operacional ou produto em questão.
-   **Não force os usuários a interagir com seu programa como a janela superior na tela.** Se uma função ou uma janela for necessária continuamente para que os usuários executem uma tarefa, essa janela sempre deverá permanecer visível, se o usuário escolher, independentemente de sua posição em relação a outras janelas. Por exemplo, se o usuário tiver um teclado móvel na tela que está sobre todas as outras janelas para que ele seja visível em todos os momentos, seu programa nunca deverá obscurecer por posicionamento obrigatório na parte superior da ordem [Z.](glossary.md)
-   **Use cores do sistema, fontes e controles comuns sempre que possível.** Ao fazer isso, você reduz significativamente o número de problemas de acessibilidade encontrados pelos usuários.

### <a name="addressing-particular-impairments"></a>Endereçamento de deficiências específicas

**Visual**

-   **Nunca confie apenas na cor para transmitir significado.** Use a cor apenas como um meio de reforçar o significado fornecido pelo texto, design, localização ou som.

    ![captura de tela do ícone de comunicador vermelho e dica de ferramenta ](images/inter-accessibility-image9.png)

    O principal método de comunicação neste exemplo é o texto conciso da dica de ferramenta. O uso de cores ajuda a comunicar o significado, mas é secundário.

-   **Use infotips de texto alternativos (alt) para descrever gráficos.**
-   **Não use texto em gráficos.** Os usuários com deficiências visuais podem ter gráficos desligados (por exemplo, em um navegador da Web) ou simplesmente não podem ver ou procurar texto colocado em gráficos.
-   **Verifique se as caixas de diálogo** e as janelas têm nomes significativos, para que um usuário que está ouvindo em vez de ver a tela (por exemplo, usando um leitor de tela) obtém informações contextuais apropriadas.
-   Respeitar as configurações do usuário para exibição **visual** sempre obtendo faces de tipo de fonte, tamanhos e cores Windows, tamanhos e tamanhos de elemento de exibição e definições de configuração do sistema das APIs Theme e GetSystemMetrics.
-   **Mantenha o texto de balão conciso** para que seja mais fácil de ler e minimize a interrupção dos leitores de tela.

    ![captura de tela do balão indicando limites de código de pino ](images/inter-accessibility-image10.png)

    Embora os balão possam usar texto de corpo adicional, se necessário, este exemplo mostra que, às vezes, o texto do título sozinho atinge a mesma meta de maneira mais econômica e acessível.

**Audição**

-   **Nunca confie em som sozinho para transmitir significado.** Use o som apenas como um meio de reforçar o significado fornecido pelo texto, design, localização ou cor.
-   **Permitir que os usuários controlem o volume de saída de áudio.** Use o Windows volume Mixer para essa finalidade. Para obter mais informações, consulte [Som](vis-sound.md).
-   Direcionar o som do programa para ocorrer em um intervalo entre **500 Hz e 3000 Hz** ou ser facilmente ajustável pelo usuário nesse intervalo. Sons nesse intervalo têm maior probabilidade de serem detectáveis por pessoas com deficiência auditiva.

**Destreza**

-   **Faça valores de tempo de tempo de interface do usuário relativos a GetDoubleClickTime() em vez de usar tempos absolutos.** Isso ajusta os tempos limite à velocidade do usuário.
-   **Atribua chaves de acesso** a todos os itens de menu para que os usuários que preferem trabalhar com o teclado tenham a mesma capacidade de navegar pelo programa que os usuários que trabalham com o mouse.
-   **Não faça clique duas vezes e arraste a única maneira de executar uma ação.** Esses podem ser movimentos difíceis para alguns usuários.
-   **Não remova barras de menu do programa.** As barras de menu são mais fáceis do que as barras de ferramentas para os usuários de teclado acessarem. Se você não quiser que a barra de menus seja visível por padrão, o hide-lo.
-   **Tornar a Ajuda acessível por meio do teclado fornecendo paradas de tabulação para botões e links de Ajuda.**
-   **Para melhorar o reconhecimento das atribuições de chave de acesso em seu programa, você pode exibi-las o tempo todo.** No Painel de Controle, vá para o Central de Facilidade de Acesso e clique em Tornar **o teclado mais fácil de usar;** em seguida, **marque a caixa de seleção Atalhos de teclado sublinhados e teclas de** acesso.

**Cognitiva**

-   **Use a divulgação progressiva** para ocultar a complexidade.

    ![captura de tela de botões divididos com triângulos para baixo ](images/inter-accessibility-image11.png)

    Nesses exemplos, as opções disponíveis no botão de comando ficam ocultas por padrão e os usuários podem optar por exibir as opções aproveitando os controles de divulgação progressiva.

-   **Use ícones, barras de ferramentas e outros auxílios visuais** para reduzir a carga cognitiva de leitura de texto.
-   Quando **possível,** forneça a funcionalidade de conclusão automática em caixas de texto e listas de listas listadas editáveis, para que os usuários não tenham que digitar todo o nome de comandos, nomes de arquivo ou opções semelhantes de um conjunto limitado de opções. Isso reduz a carga cognitiva para todos os usuários e reduz a quantidade de digitação para usuários para os quais a ortografia ou a digitação é difícil, lenta ou complicada.
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



 

