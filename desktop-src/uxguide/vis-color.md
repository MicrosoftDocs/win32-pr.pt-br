---
title: Cor
description: Color é um elemento visual importante da maioria das interfaces de usuário.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ae58ddf232a3d8311a917ea0475c7aca1bae8949
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104091862"
---
# <a name="color"></a>Cor

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Color é um elemento visual importante da maioria das interfaces de usuário. Além das estética puras, a cor tem significados associados e extrairá respostas emocional. Para evitar confusão no significado, a cor deve ser usada de forma consistente. Para obter as respostas emocional desejadas, a cor deve ser usada adequadamente.

A cor costuma ser considerada em termos de um espaço de cores, em que RGB (vermelho, verde, azul), HSL (Matiz, saturação, luminosidade) e HSV (Matiz, saturação, valor) são os espaços de cores usados com mais frequência.

![Figura de um cubo mostrando relações de cor ](images/vis-color-image1.png)

O espaço de cores RGB pode ser visualizado como um cubo.

Embora a tecnologia de exibição use valores RGB e, consequentemente, os desenvolvedores considerem as cores em termos de RGB, o espaço de cores RGB não corresponde ao modo como as pessoas percebem a cor. Por exemplo, se você adicionar vermelho a ciano escuro, o resultado não será percebido como mais vermelho, mas como ciano mais claro.

![ilustração de quadrados ciano escuro e claro ](images/vis-color-image2.png)

Neste exemplo, adicionar vermelho ao ciano escuro torna-o mais claro, e não mais vermelho. O espaço de cores RGB não corresponde ao modo como as pessoas percebem a cor.

Os espaços de cores HSL/HSV consistem em três componentes: matiz, saturação e luminosidade ou valor. Esses espaços de cores geralmente são usados em vez de RGB, pois eles correspondem melhor à forma como as pessoas percebem a cor.

O espaço de cores HSL forma um cone duplo que é branco na parte superior, preto na parte inferior e neutro no meio:

-   **Matiz:** A cor básica no disco de cores, que varia de 0 a 360 graus, onde 0 e 360 graus são vermelhos.

    ![Figura de um círculo mostrando relações de cor ](images/vis-color-image3.png)

    O disco de cores, em que vermelho é de 0 graus, amarelo é 60 graus, verde é 120 graus, ciano é de 180 graus, azul é de 240 graus e magenta é de 300 graus.

-   **Saturação:** Como a cor é pura (vs. opaca), variando de 0 a 100, onde 100 está totalmente saturado e 0 é cinza.
-   **Luminosidade:** Quão claro a cor é, variando de 0 a 100, onde 100 é o mais leve possível (branco, independentemente do matiz e da saturação) e 0 é o mais escuro possível (preto).

    ![Figura ilustrando o espaço de cores HSL ](images/vis-color-image4.png)

    O espaço de cores HSL pode ser visualizado como um cone duplo.

O espaço de cores HSV é semelhante, exceto pelo fato de que seu espaço forma um único cone:

-   **Matiz:** A cor básica no disco de cores, que varia de 0 a 360 graus, onde 0 e 360 graus são vermelhos.
-   **Saturação:** Como a cor é pura (vs. opaca), variando de 0 a 100, onde 100 está totalmente saturado e 0 é cinza.
-   **Valor:** Quão brilhante é a cor, variando de 0 a 100, em que 100 é o mais claro possível (que é a metade da luminosidade no espaço HSL) e 0 é o mais escuro possível (preto).

    ![Figura ilustrando o espaço de cores HSV ](images/vis-color-image5.png)

    O espaço de cores HSV pode ser visualizado como um único cone.

Em ambos os espaços HSL e HSV, se a saturação for 0, a luminosidade especifica um tom de cinza. No Windows, os espaços HSL e HSV geralmente são remapeados para uma escala entre 0 e 240 para que as cores possam ser representadas com um valor de 32 bits.

**Observação:** As diretrizes relacionadas a [fontes](vis-fonts.md) e [acessibilidade](inter-accessibility.md) são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

O uso efetivo da cor pode tornar a interface do usuário do seu programa mais eficiente. A cor pode ajudar os usuários a entender determinados significados em um relance. A cor também pode fazer com que seu produto pareça mais estética e refinado.

Infelizmente, é muito fácil usar cores de forma ineficaz, especialmente se você não estiver treinado no Design Visual. Uso insatisfatório de resultados de cores em designs que parecem não profissionais, com data, confusos ou apenas ruins. Um uso insatisfatório da cor pode ser pior do que não usar cores.

Esta seção explica o que você precisa saber para usar a cor com eficiência.

### <a name="how-color-is-used"></a>Como a cor é usada

Normalmente, a cor é usada na interface do usuário para se comunicar:

-   **Significado.** O significado de uma mensagem pode ser resumido por cor. Por exemplo, a cor é geralmente usada para comunicar o status em que vermelho é um problema ou erro, amarelo é cuidado ou aviso e verde é bom.
-   **Status.** O estado de um objeto pode ser indicado por cor. Por exemplo, o Windows usa cor para indicar os Estados de seleção e de foco. Os links nas páginas da Web usam Blue para não visitado e roxo para visitado.
-   **Diferenciação.** As pessoas pressupõem que há uma relação entre os itens da mesma cor; portanto, a codificação por cores é uma maneira eficaz de diferenciar os objetos. Por exemplo, em um item do painel de controle, os painéis de tarefas usam um plano de fundo verde para separá-los visualmente do conteúdo principal. Além disso, o Microsoft Outlook permite que os usuários atribuam diferentes sinalizadores coloridos a mensagens.
-   **Ênfase.** A cor pode ser usada para atrair a atenção dos usuários. Por exemplo, o Windows usa [instruções azuis principais](text-ui.md) para ajudá-las a destacar o outro texto.

É claro que a cor é geralmente usada em gráficos por motivos puramente estéticos. Embora os estética sejam importantes, você deve escolher as cores dos elementos da interface do usuário, principalmente com base no que significam, e não como eles parecem.

### <a name="color-interpretation"></a>Interpretação de cores

**A interpretação de cores dos usuários costuma depender culturalmente.** Por exemplo, na Estados Unidos, o casamento vestido para a noiva está amplamente associado à cor branca, enquanto preto é associado a funerais. No entanto, há muito tempo no Japão, o símbolo de cor era apenas o oposto: White era a cor predominante em funerais, e Black foi considerado uma cor que traz boa sorte para casamentos.

Dito isso, **a interpretação de vermelho, amarelo e verde para o status é consistente globalmente.** Isso ocorre devido à [Convenção do UNESCO Viena em sinais de estrada e sinais](https://www.unece.org/trans/conventn/signalse.pdf), que definem a Convenção Mundial de semáforos (em que vermelho significa parar, verde significa continuar, e significa amarelo, continuar com cautela). Você pode usar essas cores de status sem preocupação com interpretações dependentes de cultura.

Além das cores de status, o Windows atribui significados a cores com base na Convenção, conforme apresentado na seção de diretrizes deste artigo. Certifique-se de que o uso de cores do seu programa seja compatível com essas convenções de cores.

### <a name="color-accessibility"></a>Acessibilidade de cores

O uso de cores afeta a acessibilidade do seu software para o público mais amplo possível. Os usuários com deficiências ou visões baixas podem não conseguir ver as cores bem, se houver. Aproximadamente 8% dos homens adultos têm alguma forma de confusão de cores (geralmente conhecida como "cegueira para cores"), da qual a confusão de cores vermelha-verde é a mais comum.

![Figura mostrando as cores primárias normalmente vistas ](images/vis-color-image6.png)

As cores primárias, como visto com a visão de cor normal.

![Figura mostrando as mesmas cores que vimos com Protanopia ](images/vis-color-image7.png)

As cores primárias, como visto com Protanopia (1% da população masculina).

![Figura mostrando as mesmas cores vistas com Deuteranopia ](images/vis-color-image8.png)

As cores primárias, como visto com Deuteranopia (6% da população macho).

![Figura mostrando as mesmas cores que vimos com Tritanopia ](images/vis-color-image9.png)

As cores primárias, como visto com Tritanopia (1% da população masculina).

Para obter mais informações, consulte [pode Color-Blind os usuários vejam seu site?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Usar cor para reforçar visualmente

A melhor solução para a interpretação de cores e problemas de acessibilidade é usar cores para reforçar visualmente o significado de um desses métodos principais de comunicação:

-   **Text.** O texto conciso geralmente é a comunicação primária mais eficaz diretamente na interface do usuário ou por meio de uma dica de ferramenta.

![captura de tela de pequeno ícone vermelho com dica de ferramenta ](images/vis-color-image10.png)

Neste exemplo, o texto da dica de ferramenta é usado para comunicar o significado de um ícone.

-   **Desenvolver.** Os ícones são facilmente diferenciados pelos designs, especialmente sua forma de estrutura de tópicos.

![captura de tela de ícones em tons de cinza (escala de cinza) ](images/vis-color-image11.png)

Neste exemplo, os ícones padrão são prontamente distinguiveis com base em seus designs.

-   **Local.** O local relativo também pode ser usado, mas essa abordagem é mais fraca do que as alternativas. Para ser eficaz, o local deve ser padrão e bem conhecido, assim como as luzes de tráfego.

Embora a cor seja o atributo mais óbvio de muitos designs, ela sempre deve ser redundante.

### <a name="designing-with-color"></a>Criando com cor

Ironicamente, a melhor maneira de criar uma cor é começar com a criação sem cores, usando [wireframe](glossary.md) ou monocromático e, em seguida, adicionar cores posteriormente. Isso ajuda a garantir que as informações não sejam comunicadas usando a cor sozinha. Ele também ajuda a garantir que suas impressões fiquem ótimas em Impressoras monocromáticas.

### <a name="use-theme-or-system-colors"></a>Usar cores de tema ou do sistema

Embora haja muitos fatores complexos no uso de cores com eficiência, na interface do usuário do Windows escolher a cor geralmente se resume a simplesmente escolher a cor do [tema](glossary.md) ou a cor do [sistema](glossary.md) apropriada de acordo com algumas regras simples. Os usuários podem selecionar e personalizar esses esquemas de cores à medida que escolherem.

Fazendo isso, não apenas você acomoda as preferências de cor de todos os seus usuários, mas elimina a carga de escolher um esquema de cores perfeito que funcione para todos os preferências, estilos e culturas (que, é claro, é impossível).

**Se você fizer apenas uma coisa...**

Escolha cores selecionando a cor de tema ou a cor do sistema apropriada. Nunca use a cor como método principal de comunicação, mas como um método secundário para reforçar o significado visualmente. Projete usando wireframe ou monocromático para ajudar a garantir que a cor seja secundária.

### <a name="use-theme-or-system-colors-correctly"></a>Usar cores de tema ou do sistema corretamente

Suponha que os usuários escolham cores de tema ou de sistema com base em suas necessidades pessoais e que as cores do tema ou do sistema sejam construídas adequadamente. Com base nessa suposição, se você sempre escolher cores de tema ou de sistema com base em seus propósitos pretendidos e pares com seus planos de fundo associados, as cores terão a garantia de serem legíveis e respeitarão os desejos dos usuários em todos os modos de vídeo, incluindo o [modo de alto contraste](glossary.md). Por exemplo, a cor do sistema de texto da janela é garantida para ser legível em relação à cor do sistema de plano de fundo da janela.

Especificamente, sempre:

-   **Escolha as cores com base em sua finalidade.** Não escolha as cores com base na aparência atual, pois essa aparência pode ser alterada pelo usuário ou por versões futuras do Windows.
-   **Corresponder cores de primeiro plano com suas cores de plano de fundo associadas.** As cores de primeiro plano têm a garantia de serem legíveis apenas em suas cores de plano de fundo associadas. Não misture e combine cores de primeiro plano com outras cores de plano de fundo, ou pior ainda, com outras cores de primeiro plano.
-   **Não misture tipos de cor.** Ou seja, sempre corresponder as cores de tema com suas cores de tema associadas, cores do sistema com suas cores de sistema associadas e cores conectadas com outras cores em si. Por exemplo, uma cor de texto de tema não é garantida para ser legível em relação a um plano de fundo vinculado.
-   **Se você precisar direcionar as cores, manipule o modo de alto contraste como um caso especial.**

**Se você fizer apenas uma coisa...**

Sempre escolha o tema ou as cores do sistema com base em sua finalidade pretendida e emparelhe o primeiro plano com seus planos de fundo associados.

### <a name="using-other-colors"></a>Usando outras cores

Embora o tema do Windows defina um conjunto abrangente de partes de tema, você pode descobrir que seu programa precisa de cores que não estão definidas no arquivo de tema. Embora você pudesse aplicar essas cores, uma abordagem melhor é derivar as cores do tema ou das cores do sistema. Usar essa abordagem estrategicamente oferece todos os benefícios do uso de cores de tema e do sistema, mas com muito mais flexibilidade.

Por exemplo, suponha que você precise de um plano de fundo da janela que seja mais escuro que a cor do plano de fundo da janela de tema. No espaço de cores HSL, ter uma cor mais escura significa uma cor com uma luminosidade menor. Portanto, você pode derivar uma cor de fundo de janela mais escura usando as seguintes etapas:

-   Obter a cor de tema do plano de fundo da janela RGB.
-   Converta o RGB em seu valor HSL.
-   Reduza o valor de luminosidade (por, digamos, 20 por cento).
-   Converta novamente em valores RGB.

Usando essa abordagem, é garantido que a cor derivada seja percebida como uma tonalidade mais escura da cor original (a menos que a cor original tenha sido muito escura para começar.)

![ilustração mostrando efeitos de luminosidade reduzida ](images/vis-color-image12.png)

Neste exemplo, uma cor de plano de fundo de janela mais escura é derivada da cor do tema.

### <a name="testing-colors"></a>Cores de teste

Para determinar se o uso do seu programa de cor está acessível e não usado como método principal de comunicação, recomendamos usar os utilitários [Fujitsu ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) ou [Vischeck](https://www.vischeck.com/) para verificar:

-   Dependência geral da cor usando o filtro de escala cinza.
-   Problemas específicos de confusão de cores usando os filtros protanopia, Deuteranopia e Tritanopia.

Para determinar se o uso do seu programa de cores está programado corretamente, teste o programa nos seguintes modos:

-   Eles são habilitados usando o tema padrão do Windows.
-   Eles são habilitados usando um tema não padrão.
-   Eles são desabilitados ("estilo clássico do Windows" nas configurações de tema no item do painel de controle de personalização).
-   Alto Contraste preto (texto em branco em um plano de fundo preto).
-   Alto Contraste branco (texto preto em um plano de fundo branco).

Todos os elementos da tela devem ser legíveis e aparecem conforme o esperado, mesmo imediatamente após as alterações do modo.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Nunca use a cor como método principal de comunicação,** mas como um método secundário para reforçar o significado visualmente.

### <a name="using-theme-and-system-colors"></a>Usando cores de tema e do sistema

-   Sempre que possível, **Escolha cores selecionando a cor de tema ou a cor do sistema apropriada.** Ao fazer isso, você sempre pode respeitar a preferência de cores dos usuários.
-   **Escolha o tema e as cores do sistema com base em sua finalidade.** Não escolha as cores com base na aparência atual, pois essa aparência pode ser alterada pelo usuário ou por versões futuras do Windows.
-   **Corresponder cores de primeiro plano com suas cores de plano de fundo associadas.** As cores de primeiro plano têm a garantia de serem legíveis apenas em suas cores de plano de fundo associadas. Não misture e combine cores de primeiro plano com outras cores de plano de fundo, ou pior ainda, com outras cores de primeiro plano.
-   **Não misture tipos de cor.** Ou seja, sempre corresponder as cores de tema com suas cores de tema associadas, cores do sistema com suas cores de sistema associadas e cores conectadas com outras cores em si. Por exemplo, uma cor de texto de tema não é garantida para ser legível em relação a um plano de fundo vinculado.
-   **Se você precisar usar uma cor que não seja uma cor de tema ou do sistema:**
    -   **Prefira derivar a cor de um tema ou de uma cor do sistema ao tornar o seu valor.** Use o processo descrito anteriormente neste artigo, em usando outras cores.
    -   **Manipule o modo de alto contraste como um caso especial.**
-   **Lidar com alterações de tema.** As alterações de tema são tratadas automaticamente pelo Windows com quadros de janela padrão e controles comuns. Janelas com quadros de janela personalizados, controles personalizados ou de desenho proprietário, e outro uso de cor devem tratar as alterações de tema explicitamente.
    -   **Desenvolvedores:** Você pode responder a eventos de alteração de tema manipulando a \_ mensagem themechanged do WM.

### <a name="color-meaning"></a>Significado da cor

-   Embora você deva usar cores de tema e de sistema (ou cores derivadas) sempre que puder, verifique se qualquer outro uso de cor é compatível com o uso de cor a seguir no Windows.



|                                      |                                                                               |                                                                                                                                                                 |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Matiz**<br/>                   | **Significado**<br/>                                                        | **Usar no Windows**<br/>                                                                                                                                   |
| azul/verde<br/>                | Marca do Windows<br/>                                                      | Plano de fundo: identidade visual do Windows.<br/>                                                                                                                        |
| vidro, preto, cinza, branco<br/> | neutro<br/>                                                            | Plano de fundo: quadros de janela padrão, menu Iniciar, barra de tarefas, barra lateral.<br/> Primeiro plano: texto normal.<br/>                                                |
| blue<br/>                      | Iniciar, confirmar<br/>                                                      | Plano de fundo: botões de comando padrão, Pesquisar, fazer logon.<br/> Ícones: informações, ajuda.<br/> Primeiro plano: instruções principais, links.<br/>           |
| vermelha<br/>                       | erro, parar, vulnerável, crítico, atenção imediata, restrito<br/> | Plano de fundo: status, progresso interrompido (barras de progresso).<br/> Ícones: erro, parar, fechar janela, excluir, entrada necessária, ausente, não disponível.<br/>     |
| yellow<br/>                    | aviso, cuidado, questionável<br/>                                     | Plano de fundo: status, progresso pausado (barras de progresso).<br/> Ícones: aviso<br/>                                                                       |
| green<br/>                     | Vá, continue, progresso, seguro<br/>                                        | Plano de fundo: status, progresso normal (barras de progresso).<br/> Ícones: ir, concluído, atualizar.<br/> Primeiro plano: caminhos e URLs (nos resultados da pesquisa).<br/> |
| purple<br/>                    | tenha<br/>                                                            | Primeiro plano: links visitados (para links no Windows Internet Explorer e documentos).<br/>                                                                |



 

-   **Para evitar a comunicação dos significados anteriores, as cores de escolha têm uma saturação de alta a baixa e alta ou baixa luminosidade.** Os usuários associam os significados anteriores a cores com saturação completa ou alta e luminosidade de nível intermediário, para que você possa evitar essas associações escolhendo sombras diferentes.

![Figura mostrando como a luminosidade afeta a cor ](images/vis-color-image13.png)

Neste exemplo, há três sombras diferentes de amarelo, mas apenas o sombreamento de luminosidade de nível intermediário altamente saturado comunica o aviso. O ícone de pasta amarelo não parece um aviso.

### <a name="using-color-with-data"></a>Usando cores com dados

-   Quando útil, **atribua cor aos dados para ajudar os usuários a diferenciá-los.** Observe que os usuários assumirão que os dados com cores semelhantes têm significados semelhantes.
-   **Atribua cores por padrão que sejam fáceis de distinguir.** Em geral, as cores são fáceis de distinguir se estão muito distantes umas das outras nos espaços de cores HSL/HSV, mantendo o alto contraste com seu plano de fundo:
    -   Ao escolher as cores, prefira Tríade Harmonies ou matizes complementares, mas não os matizes adjacentes.

        ![Figura mostrando como escolher cores de contraste ](images/vis-color-image14.png)

        Neste exemplo, se a primeira atribuição de cor for vermelha, a cor seguinte deverá ser azul, verde ou ciano, mas não magenta, roxo, laranja ou amarelo.

    -   As cores têm alto contraste se houver uma grande diferença em seu matiz, saturação ou luminosidade.

        ![Figura mostrando uma cor em diferentes planos de fundo ](images/vis-color-image15.png)

        Neste exemplo, a cor de base azul clara contrasta com planos de fundo com grandes diferenças em matiz, saturação ou luminosidade.

    -   O uso de um plano de fundo branco ou muito leve torna as cores de primeiro plano mais fáceis de distinguir.

        ![Figura ilustrando contraste bom e ruim ](images/vis-color-image16.png)

        Neste exemplo, as cores de plano de fundo branco e leve tornam a cor de primeiro plano mais fácil de distinguir.

-   **Permitir que os usuários personalizem essas atribuições de cores** porque a escolha de cores é subjetiva e uma preferência pessoal. Se houver muitas cores coordenadas, permita que os usuários as alterem como um grupo usando esquemas de cores.
-   **Permitir que os usuários etiquetem essas atribuições de cor.** Isso ajuda a facilitar a identificação e a localização.
-   **Diferentemente das cores da interface do usuário, os dados não devem ser alterados quando as cores do sistema mudam.**

## <a name="documentation"></a>Documentação

-   **Consulte os elementos da interface do usuário por seus nomes, não por suas cores.** Essas referências não estão acessíveis e as cores do sistema podem ser alteradas. Se o nome de um elemento de interface do usuário não for bem conhecido ou não for bastante descritivo, mostre uma captura de tela para esclarecer.

**Correto:**

![captura de tela da mensagem que contém a barra de informações ](images/vis-color-image17.png)

**Incorreto:**

![captura de tela de mensagem contendo ' barra de ouro ' ](images/vis-color-image18.png)

No exemplo incorreto, a mensagem se refere à barra de informações do Windows Internet Explorer por sua cor, em vez de seu nome.

