---
title: Assistentes
description: Apesar de o maravilhoso, o nome estranho, os assistentes não são, na verdade, uma forma especial de interface do usuário e têm apenas um determinado intervalo de utilitários.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6455c38228606932e9144c744dd217d0a7fa67e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103837558"
---
# <a name="wizards"></a>Assistentes

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Apesar de o maravilhoso, o nome estranho, os assistentes não são, na verdade, uma forma especial de interface do usuário e têm apenas um determinado intervalo de utilitários.

Os assistentes são usados para executar tarefas de várias etapas.

![Captura de tela que mostra o assistente para ' Adicionar impressora ' com ' que tipo de impressora você deseja instalar? ' aviso.](images/win-wizards-image1.png)

![Captura de tela que mostra o assistente ' Adicionar impressora ' ao procurar impressoras disponíveis.](images/win-wizards-image2.png)

![captura de tela do assistente para adicionar impressora ](images/win-wizards-image3.png)

Várias etapas de um assistente são apresentadas como uma sequência de páginas.

Os assistentes normalmente incluem os seguintes tipos de páginas:

-   As páginas de escolha são usadas para reunir informações e permitir que os usuários façam escolhas.
-   A página confirmar é usada para executar uma ação que não pode ser desfeita clicando em voltar ou cancelar.
-   A página progresso é usada para mostrar o progresso de uma operação demorada.

O design de assistente moderno coloca um prêmio em eficiência, tornando a página de progresso opcional para operações mais curtas e muitas vezes dispensando com a [página de boas-vindas](glossary.md) tradicional e a [página Parabéns](glossary.md) no início e no fim.

Todas as páginas de assistente têm estes componentes:

-   Uma barra de título para identificar o nome do assistente, com um botão voltar no canto superior esquerdo e um botão fechar com os botões minimizar/maximizar e restaurar opcionais. Observe que a barra de título também inclui um ícone para identificá-lo na barra de tarefas.
-   Uma instrução principal para explicar o objetivo do usuário com a página.
-   Uma área de conteúdo com texto opcional e, possivelmente, outros controles.
-   Uma área de comando com pelo menos um botão de confirmação para confirmar a tarefa ou prosseguir para a próxima etapa.

Embora um assistente tenha várias etapas, todas essas etapas devem ser adicionadas a uma única tarefa, do ponto de vista do usuário. Esse é o princípio fundamental de design do assistente de "um assistente, uma tarefa".

Portanto, neste artigo, uma tarefa é a função básica de um assistente (por exemplo, a tarefa de um assistente de instalação é instalar um programa). As subtarefas são aspectos da tarefa maior (por exemplo, uma sub-rotina de um assistente de instalação pode ser configurar o programa a ser instalado). Por fim, cada página do assistente é considerada uma etapa em uma determinada subtarefa ou tarefa (por exemplo, pode haver duas ou três etapas envolvidas na configuração do programa).

**Observação:** As diretrizes relacionadas à [instalação](exper-setup.md), [caixas de diálogo](win-dialog-box.md)e barras de [progresso](progress-bars.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Um assistente pode ser usado para qualquer tarefa que exija várias etapas de entrada. No entanto, os assistentes efetivos têm requisitos adicionais:

-   **O assistente executa uma única tarefa atômica?** Não use interações que não sejam tarefas únicas (um programa inteiro nunca deve ser um assistente, a menos que execute uma única tarefa). Não use assistentes para combinar tarefas independentes ou etapas amplamente não relacionadas.
-   **O número de perguntas necessárias pode ser reduzido? Há padrões aceitáveis que funcionam bem para a maioria dos casos ou podem ser ajustados conforme necessário mais tarde? Consequentemente, o número de páginas pode ser reduzido?** Nesse caso, tente simplificar a tarefa para que ela possa ser apresentada em uma única página (como uma caixa de diálogo) ou eliminar a necessidade de entrada completamente (permitindo que a tarefa seja executada diretamente).
-   **As perguntas necessárias devem ser fornecidas sequencialmente? Há várias perguntas prováveis, mas opcionais?** Nesse caso, considere uma caixa de diálogo ou caixa de diálogo com guias.

    **Correto:**

    ![captura de tela da caixa de diálogo opções de impressão ](images/win-wizards-image4.png)

    A caixa de diálogo opções de impressão do Microsoft PowerPoint contém muitas opções de entrada de usuário, portanto, você pode apresentá-las em um assistente. No entanto, não há necessidade de fornecê-las em sequência, portanto, uma caixa de diálogo é uma opção melhor.

Os assistentes são uma forma relativamente pesada de interface do usuário; Se houver uma solução adequada e mais leve disponível, use-a!

## <a name="design-concepts"></a>Conceitos de design

### <a name="overuse-of-wizards"></a>Uso excessivo de assistentes

Historicamente, os assistentes são diferentes da interface do usuário comum, pois foram projetados para ajudar os usuários a executar tarefas especialmente complexas (com as etapas que residem em locais diferentes) e geralmente tinham inteligência interna para ajudar os usuários a obter sucesso. Hoje, toda a interface do usuário deve ser projetada para tornar as tarefas o mais simples possível, portanto, não há necessidade de uma interface do usuário especial apenas para essa finalidade.

Ainda assim, a crença persiste que os assistentes são uma interface de usuário especial — em grande parte porque são chamados de "assistentes" (muito mais criativo do que, digamos, "caixas de diálogo" e "janelas de propriedades"). Em vez disso, é melhor considerá-los como tarefas de várias etapas e não emitir atenção especial para esse fato.

Antes de criar um assistente, considere se os usuários realmente devem ser interrompidos do fluxo principal do programa. Pode haver uma solução contextual, embutida e mais leve que, por fim, se sentirá mais útil e eficiente para os usuários. Por exemplo, um recurso mal projetado em um programa não garante que um assistente o explique e simplifique; Ele garante a reformulação do próprio recurso. Um assistente não deve ser usado como um recurso de banda para corrigir um problema mais básico com o programa.

### <a name="wizards-do-have-appropriate-functions"></a>Os assistentes têm funções apropriadas

Os assistentes são uma das chaves para simplificar a experiência do usuário. Eles permitem que você execute uma operação complexa, como a configuração de um programa, e divida-o em uma série de etapas simples. Em cada ponto do processo, você pode fornecer uma explicação do que é necessário e exibir controles que permitem ao usuário fazer seleções e inserir texto.

Determinados tipos de tarefas de várias etapas prestam-se ao formulário do assistente. Por exemplo, no Windows, vários assistentes envolvem funções de conectividade (para a Internet ou rede corporativa ou para dispositivos periféricos, como impressoras e máquinas de fax).

![captura de tela do assistente de conexão ](images/win-wizards-image5.png)

Conectar-se a uma rede é uma tarefa típica no Windows apropriada para um assistente.

Aqui, a função do assistente é mediar entre algo conhecido e estável (o sistema operacional pronto para uso) e algo desconhecido e variável (disposições de conectividade com uma empresa telefônica ou provedor de serviços de Internet). A complexidade dos ecossistemas de computação é suficientemente significativa agora que é autênticomente útil usar assistentes para reduzir essa complexidade.

Outros tipos de tarefas que funcionam bem como assistentes do Windows incluem funcionalidade de alto nível (como reconhecimento de fala e manuscrito) e experiências de mídia sofisticadas (como configuração de opções para fazer e publicar filmes). Os assistentes também podem ser implantados para tarefas mais básicas de várias etapas, como solução de problemas. Em suma, se for provável que usuários diferentes desejam experimentar seu programa de maneiras muito diferentes, isso pode indicar a necessidade de um assistente e sua capacidade para vários pontos de entrada do usuário.

Para o seu programa, vale um pouco tempo de design até o início para determinar qual função seu assistente está servindo e se essa função realmente aumenta para o nível de implantação de um assistente.

### <a name="wizard-length"></a>Comprimento do assistente

As perguntas de design surgem naturalmente em relação ao número e à organização de páginas e opções. Por exemplo:

-   Há um número ideal de páginas para um assistente? Ou pelo menos um intervalo desejável?
-   O assistente deve ser conciso e simplificado, para que os usuários possam concluí-lo o mais rápido possível?
-   Deve haver mais páginas que exigem menos opções? Ou menos páginas com mais complexidade? Qual design é considerado mais utilizável?
-   Você pode desenvolver experiências mais rápidas do assistente aplicando convenções de interface do usuário, como páginas com guias?

A Microsoft costumava aconselhar que os assistentes de três páginas ou menos sejam criados como assistentes simples, e que os de quatro ou mais páginas usem um design de assistente avançado (consulte as diretrizes de [experiência do usuário do Windows](/previous-versions/ms997609(v=msdn.10)) de 1999). Mas os padrões atuais de design do assistente dispensam o que tinha sido uma das principais diferenças entre os formulários simples e avançados (o uso das páginas de boas-vindas e de parabéns), portanto, essas categorias agora se sentem inadequadas e o número de páginas que determinam a escolha do design parece arbitrário.

O assistente deve ser tão longo ou curto quanto a tarefa é necessária; Não há nenhuma diretriz fixa para seu comprimento. Um assistente de uma página deve ser realmente apresentado como uma caixa de diálogo, portanto, duas páginas provavelmente são a forma mais condensada possível para um assistente.

**Correto:**

![captura de tela da caixa de diálogo criar disco ](images/win-wizards-image6.png)

Essa tarefa tem poucas opções que a apresentação como um assistente seria inútil. Uma caixa de diálogo é a forma apropriada para essa interface do usuário.

Na outra extremidade do espectro, se você tiver um assistente que inclui vários pontos de decisão e ramificações e, com frequência, os usuários perderão o controle de seu caminho de navegação, você excedeu um limite prático e deve reduzir o tamanho do assistente. Como alternativa, talvez você consiga dividir o assistente em várias tarefas distintas.

Conforme você determina o comprimento mais apropriado para o assistente, preste atenção especial aos usuários de destino. Os programas para usuários finais, como consumidores domésticos e funcionários do escritório tendem a usar assistentes para ocultar a complexidade; os assistentes são o mais curto possível, com um design de página simples e limpo, e padrões predefinidos para o máximo de opções possível. Por outro lado, os assistentes do servidor ou os programas destinados a profissionais de ti tendem a ser mais longos e complexos. Esse grupo de usuários de destino tem uma tolerância muito mais alta para tomar decisões de configuração e pode, na verdade, ser suspeito se uma grande complexidade estiver oculta.

Se um assistente por natureza simplificar uma tarefa complexa, ele deverá fazer isso relativamente minimamente para um público tecnicamente sofisticado e de forma relativamente agressiva para uma base de usuários iniciada.

**Correto:**

![captura de tela do assistente de idiomas de exibição ](images/win-wizards-image7.png)

Esta página de assistente é bem projetada para usuários finais, pois reduz um assunto potencialmente complexo para uma opção binária simples e lógica: instale ou desinstale o.

**Correto:**

![Captura de tela que mostra a página ' SQL Server instalação ' do assistente ' Seleção de recursos '.](images/win-wizards-image8.png)

No assistente de instalação do Microsoft SQL Server 2008, o design da página é mais ocupado e as inúmeras opções exigem mais pensamento, mas o público-alvo são administradores de banco de dados que esperam controle rígido da seleção de recursos.

Por fim, preste atenção à frequência com que a tarefa específica pode ser executada. Uma tarefa infrequente pode implantar um assistente mais longo, enquanto tarefas frequentes devem definitivamente favorecer a brevidade.

### <a name="branching"></a>Ramificação

Para assistentes mais longos, talvez seja necessário criar ramificações do fluxo de tarefas no qual a sequência de páginas pode diferir de acordo com a entrada do usuário fornecida "upstream". A ramificação é inerentemente desalocada para usuários, portanto, você deve projetar a experiência do usuário para transmitir a estabilidade. Recomendamos não mais do que dois pontos de decisão que causarão a ramificação em todo o assistente e não mais do que uma ramificação aninhada em uma única ramificação.

Para obter diretrizes sobre como criar uma experiência de usuário estável em um assistente de ramificação, consulte [ramificação](#branching) na seção de diretrizes deste artigo.

### <a name="providing-a-navigation-guide"></a>Fornecendo um guia de navegação

Os guias de navegação podem ser úteis quando há muitas etapas na tarefa, e os usuários podem perder seu lugar na sequência ou simplesmente deseja saber quanto mais tempo levará para ser concluído.

Os guias de navegação geralmente aparecem como uma lista de páginas ou seções do assistente, olhando um pouco como um sumário, em uma coluna ou painel no lado esquerdo de cada página. Embora a lista persista em todo o assistente (a mesma lista de páginas é exibida em cada página), há alguns meios visuais de indicar onde o usuário está atualmente na sequência (por exemplo, usando negrito para distinguir a página ou seção ativa).

Os guias de navegação podem ser sequenciais ou não sequenciais. O tipo sequencial apresenta as páginas anteriores juntamente com as páginas futuras conhecidas. Você poderá apresentar o futuro em termos de etapas em vez de páginas se as etapas forem conhecidas e as páginas forem dependentes. Em seguida, você pode preencher as páginas dinamicamente conforme elas se tornam conhecidas. Como a sequência de navegação é fixa, o guia de navegação não é interativo.

Os guias de navegação não sequenciais são interativos, para que os usuários possam visitar diretamente as páginas exibidas anteriormente. Eles também podem ignorar a sequência de navegação para páginas projetadas para serem opcionais. As páginas opcionais devem ter padrões aceitáveis na maioria das circunstâncias. Com este tipo de guia:

-   As páginas exibidas anteriormente sempre podem ser exibidas diretamente.
-   As páginas futuras não poderão ser exibidas se tiverem pré-requisitos.
-   As páginas que podem ser visitadas devem ser visivelmente diferenciadas das que não podem (por exemplo, usando links que estão ativos ou desabilitados), juntamente com páginas que são necessárias ou opcionais.

Os usuários podem ficar confusos sobre o significado do botão voltar neste cenário. Clicar em voltar levará você para a página ou seção anterior no guia de navegação, ou a última página ou seção exibida? Como os assistentes do Windows agora colocam o botão voltar no canto superior esquerdo das páginas do assistente, em vez de no canto inferior direito com os outros botões de confirmação, os usuários consideram a funcionalidade de volta como fazem na Web. Portanto, a melhor solução é dar ao botão voltar o significado da navegação na Web (clicar em voltar deve levar à última página ou seção exibida) e usar o guia de navegação do assistente para navegação seqüencial.

### <a name="page-integrity"></a>Integridade da página

O design do assistente envolve não apenas decisões relacionadas ao fluxo de tarefas inteiro, como a manipulação de navegação e a experiência de ramificação, mas também aquelas que pertencem a páginas individuais que compõem o assistente. **O princípio mais importante para a criação de boas páginas do assistente é a de integridade: o conteúdo de uma página deve pertencer.**

As páginas do assistente são significativamente mais utilizáveis se cada uma delas estiver em conjunto conceitualmente, lidando com apenas um aspecto da tarefa geral. A [principal instrução](glossary.md) é a principal maneira de conseguir isso. Identifique claramente a meta ou a finalidade da página para os usuários. As [instruções complementares](glossary.md)e todos os controles na página referem-se diretamente à instrução principal. Embora as páginas do assistente devam apresentar aos usuários as opções para as quais algumas idéias são necessárias, esse esforço não parece funcionar, pois está totalmente concentrado na integridade da própria página.

Infelizmente, os designers de assistentes muitas vezes confundam o clique rápido dos usuários no próximo botão como evidência da usabilidade, simplicidade e integridade de suas páginas. A experiência do assistente definitiva não é próxima, avançar, avançar, avançar. Embora essa experiência sugira que os padrões foram bem escolhidos, ele também sugere que o assistente não era realmente necessário, pois todas as opções são opcionais.

Em termos de visuais e texto, decrescente esses elementos para o básico. Resista na necessidade de agrupar várias subtarefas em uma única página (o "Assistente de burritos") ou para recorrer a guias para apresentar requisitos de entrada complexos. Uma única página deve abranger uma única subtarefa da tarefa geral do assistente.

**Incorreto:**

![captura de tela do assistente de instalação do SQL Server ](images/win-wizards-image9.png)

Com três guias de uma entrada de usuário razoavelmente densa necessária, esta página de assistente está tentando realizar muito.

Na maioria dos casos, mantenha o tamanho de cada página em todo o assistente para promover uma aparência consistente. Embora os assistentes do Windows permitam páginas redimensionáveis para que o tamanho de uma página corresponda à quantidade de conteúdo, apenas alguns usam essa opção.

E, finalmente, manter os elementos estruturais de cada página de assistente por meio da sequência. Por exemplo, não mova o botão voltar do canto superior esquerdo de volta para baixo até a área botões de confirmação de uma ou duas páginas. Esse nível de consistência de layout ajuda os usuários a se sentirem estáveis no assistente. Considere isso como uma linha de base para a integridade visual de uma página.

### <a name="finding-the-right-level-of-communication"></a>Encontrando o nível certo de comunicação

Os usuários têm uma baixa tolerância para ler grandes blocos de texto na tela e até mesmo menos em uma superfície de interface do usuário cuja finalidade expressa é mover desconectar por meio de uma tarefa.

Os assistentes têm uma tendência para se comunicar excessivamente. Eles ocupam muito espaço na tela, o que parece encorajar uma unidade a preencher o espaço. É como uma variação na lei de Parkinson: o texto da interface do usuário será expandido para preencher o espaço disponível.

Um culpado nesse excesso é a redundância. Devido aos modelos usados no início do design do assistente, o mesmo idioma pode aparecer em vários locais em uma página, como na barra de título, títulos, texto do corpo, rótulos de controle e assim por diante.

Vale a pena contratar um editor profissional para remover o texto do assistente ruthlessly. Elimine perguntas e opções desnecessárias em páginas individuais e elimine páginas inteiras do assistente como um todo (por exemplo, as páginas de boas-vindas tradicionais e parabéns). Fique à direita até o ponto da página com uma instrução principal escrita concisamente, usando o idioma que seu público-alvo usa para descrever a tarefa, não o jargão da tecnologia ou do recurso que você ou sua equipe usa internamente. Essa abordagem centrada no usuário é vital para melhorar a comunicação dos assistentes do programa.

Preste atenção especial ao Tom do seu assistente: às vezes, as impressões mais duradouras do seu programa são o resultado não do que você diz, mas como você diz! Em assistentes, os usuários estão familiarizados com um tom de conversação amigável, com liberal uso da segunda pessoa pronoun ("você") quando o programa está solicitando entrada. Para obter mais diretrizes, consulte [estilo e Tom](text-style-tone.md).

Reduzir a contagem de palavras na página do assistente geralmente é louvável, mas tenha cuidado para não ir muito longe. Se a tarefa for importante e garantir um assistente, os usuários apreciarão ter informações suficientes para fazer escolhas inteligentes. O exemplo a seguir mostra como o texto do assistente pode ser condensado sem sacrificar o significado.

**Antes:**

![captura de tela do assistente de ClearType, rascunho ](images/win-wizards-image10.png)

**Depois:**

![captura de tela do assistente de ClearType, revisado ](images/win-wizards-image11.png)

A versão editada desta página do assistente fornece uma instrução Main orientada a tarefas, remove o parágrafo explicativo desnecessário abaixo da instrução principal e revisa o rótulo da caixa de seleção para esclarecer a finalidade da caixa de seleção.

**Se você fizer apenas três coisas...**

1. Mapeie a tarefa que você está tentando realizar com a interface do usuário apropriada para fazer o trabalho; Não basta padrão para um assistente quando você considerar que precisa coletar uma grande quantidade de entradas de usuários.

2. Pense atentamente sobre o tamanho e a estrutura do assistente; prefira assistentes curtos e sem ramificações para manter a experiência o mais simples possível, para que os usuários possam voltar à sua tarefa principal ou a seus interesses em seu programa.

3. Verifique a integridade de cada página em seu assistente: o conteúdo de uma página deve pertencer claramente.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Considere as alternativas leves primeiro, como caixas de diálogo, painéis de tarefas ou páginas únicas.** Você não precisa usar assistentes — você pode fornecer informações úteis e assistência em qualquer interface do usuário.
-   **Use assistentes para tarefas de várias etapas.** Use caixas de diálogo de várias páginas para tarefas de uma única etapa com comentários. Para obter mais diretrizes, consulte [caixas de diálogo](win-dialog-box.md).

    **Correto:**

    ![captura de tela da caixa de diálogo diagnóstico ](images/win-wizards-image12.png)

    ![captura de tela dos comentários da caixa de diálogo de diagnóstico ](images/win-wizards-image13.png)

    Neste exemplo, o diagnóstico de rede do Windows consiste em páginas de progresso e resultados. Como a tarefa é apenas uma única etapa, ela não requer os botões de navegação que os usuários precisam em um assistente. Ele é efetivamente apresentado como uma caixa de diálogo de várias páginas.

### <a name="window-size"></a>Tamanho da janela

-   **Escolha um tamanho de janela que possa exibir todas as páginas de assistente sem rolagem de página vertical ou horizontal.** Embora os controles na página possam exigir rolagem, as próprias páginas do assistente não devem.
-   **Dimensione janelas grandes o suficiente para executar suas tarefas confortavelmente.** O layout da página não deve ser cramped ou exigir que os usuários rolem ou redimensionem excessivamente.
-   **Mas não torne o Windows excessivamente grande.** O Windows maior torna a tarefa mais complexa e requer movimento adicional para a interação.
-   **Use janelas redimensionáveis para um assistente que pode se beneficiar de mais espaço na tela, mas não exige isso.** Atribua um tamanho mínimo apropriado. Janelas redimensionáveis são úteis quando as páginas exigem interação com conteúdo redimensionável, como exibições de lista grandes.

    **Correto:**

    ![captura de tela da instalação do Visual Studio, lista parcial ](images/win-wizards-image14.png)

    **Melhor:**

    ![captura de tela da instalação do Visual Studio, lista completa ](images/win-wizards-image15.png)

    Neste exemplo, o redimensionamento da janela ajuda os usuários a ver a lista completa.

-   **Considere o uso de assistentes de tamanho dinâmico, cujo tamanho de página é alterado conforme necessário para seu conteúdo.** Isso permite que um assistente acomode layouts de página com uma ampla variedade de conteúdo.
-   **Prefira o dimensionamento estático em dinâmico se os usuários puderem perceber as alterações como uma falta de estabilidade em sua experiência com o assistente.** A estabilidade Visual geralmente supera a acomodação de conteúdo. A maioria dos assistentes deve adotar tamanhos de janela estáticos padrão, com dimensionamento dinâmico reservado para casos especiais.

### <a name="wizard-length"></a>Comprimento do assistente

-   **Torne seu assistente o mais conciso e simplificado possível.** Livrar-se de opções e perguntas desnecessárias e usar padrões inteligentes para reduzir o número de páginas necessárias para a entrada do usuário.
    -   **Exceção:** Os profissionais de ti e outros usuários técnicos têm uma tolerância mais alta para assistentes mais longos e requisitos de entrada detalhados.
-   **Torne o seu assistente um mínimo de duas páginas.** Um assistente de uma página deve ser reprojetado como uma caixa de diálogo em vez disso.
-   **Não reduza a contagem de páginas do assistente simplesmente aumentando a complexidade de cada página.** Por exemplo, uma página de assistente que inclui três guias que exigem entrada do usuário deve ser reformulada como três páginas separadas.
-   **Não aumente a contagem de páginas do assistente, tornando cada página tão simples que os usuários mindlesslym clique em avançar por toda a sequência.** Trata-se de uma falha de design comum do assistente. Se uma página de assistente não exigir pelo menos algum grau de pensamento, provavelmente não precisará estar no assistente.

### <a name="branching"></a>Ramificação

-   **Prefira o design de um assistente sem ramificação em relação à ramificação.** Os assistentes sem ramificação tendem a ser mais simples, menores e fáceis de navegar. Os assistentes de ramificação tornam mais difícil para os usuários determinar quantas etapas na tarefa e onde estão na sequência.
-   **Se você precisar ramificar, ajude os usuários a se orientarem usando uma das seguintes técnicas:**
    -   **Enumerar páginas.** Uma técnica comum é indicar o local do usuário na sequência em cada página, como com a etapa X de Y. Verifique se o ponto de extremidade (Y) está estável. Se ele mudar de valor, isso subminará a confiança dos usuários.
    -   **Inclua a noção de subetapas** (como a etapa 2a de 6).
    -   **Torne as etapas independentes das páginas, em que cada etapa pode envolver várias páginas.** Por exemplo, um serviço de viagem pode empregar a organização do assistente com base em convenções de comércio eletrônico bem estabelecidas para o setor.

        **Correto:**

        ![captura de tela da organização do assistente baseado em etapas ](images/win-wizards-image16.png)

        Os rótulos lógicos podem fornecer orientação adequada para usuários de um assistente de ramificação.

    -   **Trate as etapas opcionais como persistentes na sequência de enumeração.** Por exemplo, se uma ramificação estiver apenas ignorando algumas etapas opcionais, basta ignorar as etapas nos comentários também, em vez de renumerar. Portanto, se um usuário fizer uma escolha na página 2 que resulte em tornar as páginas 3 e 4 opcionais, mostre as etapas 1, 2, 5 e 6 de 6. Não renumere as etapas 5 e 6.
    -   **Se o assistente empregar uma única ramificação, e a ramificação ocorrer no início da tarefa, inicie a sequência nesse ponto e, em seguida, use a abordagem de não ramificação.** Ou seja, começando no ponto da ramificação, progredindo em sequência até o final da ramificação.

-   **Se você precisar ramificar, limite o número de branches a um ou dois em um único assistente.** Nunca inclua mais de uma ramificação em uma ramificação (uma ramificação "aninhada").

### <a name="commit-buttons"></a>Botões de confirmação

-   **Quando os usuários estão confirmando uma tarefa, use um botão confirmar que seja uma resposta específica para a instrução principal** (por exemplo, imprimir, conectar ou iniciar). Não use rótulos genéricos como Next (que não implicam em compromisso) ou Finish (que não é específico) para confirmar uma tarefa. Os rótulos desses botões de confirmação devem fazer sentido por conta própria. Sempre iniciar os rótulos do botão de confirmação com um verbo. **Exceção**
    -   Use concluir quando as respostas específicas ainda forem genéricas, como salvar, selecionar, escolher ou obter.
    -   Use concluir para alterar uma configuração específica ou uma coleção de configurações.
-   **Um único assistente pode ter vários pontos de confirmação, mas um único ponto é preferencial.**
-   **Se necessário, você pode renomear ou ocultar os botões de confirmação em uma página.** Essa flexibilidade é uma vantagem do novo design do assistente no Windows que não estava disponível em assistentes mais antigos. Observe que ocultar um botão de confirmação é diferente de desabilitá-lo.
-   **Evite desabilitar um botão de confirmação positivo.** Caso contrário, os usuários precisam deduzir por que os botões de confirmação estão desabilitados. É melhor deixar os botões de confirmação habilitados e fornecer uma mensagem de erro útil sempre que surgir um problema. Desabilitar o botão só será aceitável se o motivo para isso for óbvio e inambíguo.
-   **Não confunda botões de navegação (avançar e voltar) com botões de confirmação.** O próximo meio de progresso no assistente sem compromisso; O back deve estar sempre disponível na próxima página e clicar em voltar deve desfazer o efeito do último botão Avançar. Se isso não for possível, os usuários estão fazendo um compromisso e isso é indicado por meio de um rótulo específico no botão confirmar. Para obter mais diretrizes sobre os botões Avançar e voltar, consulte [navegação](#providing-a-navigation-guide).

### <a name="cancel-buttons"></a>Botões cancelar

-   **Não peça que os usuários confirmem se realmente pretendem cancelar.** Fazer isso pode ser irritante. **Exceção**
    -   A ação tem consequências significativas e, se incorreta, não é prontamente corrigível.
    -   A ação pode resultar em uma perda significativa do tempo ou esforço do usuário.
    -   A ação está claramente inconsistente com outras ações.
-   **Permitir que os usuários reiniciem os assistentes caso tenham cancelados por engano.**
-   **Não desabilite o botão Cancelar. Exceção**
    -   Se o cancelamento for prejudicial, o que pode ser o caso ao realizar uma tarefa em assistentes independentes.
    -   Se o cancelamento for impossível, o que poderá ser o caso quando o assistente não tiver controle sobre todas as etapas.

### <a name="close-buttons"></a>Botões de fechamento

-   **Use fechar para obter Follow-Up e páginas de conclusão.** Não use cancelar, pois fechar a janela não abandonará nenhuma alteração ou ação feita neste momento. Não use concluído, pois não é um verbo imperativo.
-   **Depois que a tarefa for executada, o cancelamento deve se tornar próximo (para assistentes independentes).** O efeito de fechar é simplesmente fechar a janela.

### <a name="other-controls"></a>Outros controles

-   **Use links de comando somente para escolhas, não para compromissos.** Botões de confirmação específicos indicam o compromisso muito melhor do que os links de comando em um assistente.
-   **Ao usar links de comando, oculte o botão Avançar, mas deixe o botão Cancelar.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Usando páginas (vs. caixas de diálogo ou interface de usuário embutida)

-   **Em geral, prefira páginas a caixas de diálogo.** Os usuários esperam que os assistentes sejam baseados em página.
-   **Use caixas de diálogo para auxiliar na conclusão de páginas,** como com seletores de objetos e navegadores.
-   **Use caixas de diálogo para fornecer mensagens de erro que se aplicam à página inteira e o resultado é clicar em um botão de confirmação.**
-   **Use a apresentação embutida para comportamentos dinâmicos simples,** como divulgação progressiva e interface do usuário contextual.
-   **Use a apresentação embutida para mensagens de erro que se aplicam a controles específicos.**

### <a name="wizard-pages"></a>Páginas do Assistente

-   **Concentre-se na tomada de decisão eficiente.** Reduza o número de páginas para se concentrar no Essentials. Consolide páginas relacionadas e faça páginas opcionais fora do fluxo principal. Fazer com que os usuários cliquem em Avançar completamente por meio do assistente pode parecer uma boa experiência inicialmente, mas se os usuários nunca precisarem alterar os padrões, as páginas provavelmente serão desnecessárias.
-   **Projete cada página para ter uma única finalidade e consistência Visual.** Para obter mais informações, consulte [integridade da página](#page-integrity).
-   **Não use páginas de boas-vindas — torne a primeira página funcional sempre que possível.** Use uma página de Introdução opcional somente quando:

    -   O assistente tem pré-requisitos que são necessários para concluir o assistente com êxito.
    -   Os usuários podem não entender a finalidade do assistente com base em sua primeira página de escolha e não há espaço para mais explicações.
    -   A instrução principal para as páginas Introdução é "antes de começar:".

    **Incorreto:**

    ![captura de tela da página de boas-vindas de instalação do MapPoint ](images/win-wizards-image17.png)

-   Os assistentes modernos optam pelas primeiras páginas funcionais. Aqui, não há nada a fazer, mas clique em Avançar. Por que forçar os usuários a pagar esse imposto sobre o token em seu tempo precioso?
-   **Em páginas nas quais os usuários são solicitados a fazer escolhas, otimize para os casos mais prováveis.** Esses tipos de páginas devem apresentar opções reais, não apenas instruções.
    -   Se você não usar uma página Introdução, explique a finalidade do assistente na parte superior da primeira página de opções.
-   **Use as páginas de confirmação para torná-las claras quando os usuários estiverem confirmando a tarefa.** Geralmente, a página de confirmação é a última página de opções e o botão Avançar é rotulado novamente para indicar a tarefa que está sendo confirmada.
    -   Não use páginas de resumo que meramente resumam as seleções anteriores do usuário, a menos que a tarefa seja arriscada (envolvendo segurança ou perda de tempo ou dinheiro) ou haja uma boa chance de os usuários precisarem revisar suas seleções.
-   **Use páginas de progresso para mostrar o status de uma operação demorada.** Após a conclusão bem-sucedida, a página de progresso deve avançar para a próxima etapa automaticamente. Ele deve permanecer na página de progresso somente se houver um problema que o usuário precisa ver. Clicar novamente em uma página de progresso não deve ter efeito colateral.
    -   **Use uma barra de progresso única e desterminada.** Siga as [diretrizes da barra de progresso de destérmino](progress-bars.md), incluindo:
        -   Indicar claramente a conclusão. Não deixe que uma barra de progresso vá para 100 por cento, a menos que a operação tenha sido concluída.
        -   Não reinicie o progresso. Uma barra de progresso perderá seu valor se ela for reiniciada (talvez porque uma etapa na operação seja concluída) porque os usuários não têm como saber quando a operação será concluída. Em vez disso, todas as etapas na operação compartilham uma parte do progresso e a barra de progresso passa para a conclusão uma vez.
    -   **Forneça uma descrição concisa da etapa atual acima da barra de progresso.** Para operações rápidas, tal texto é desnecessário; a barra de progresso sozinha é suficiente. Para operações que exigem um minuto ou mais, o texto pode ser útil.
        -   Use fragmentos de sentença, normalmente começando com um verbo e terminando com uma elipse. Exemplos: copiando arquivos..., instalando os componentes necessários....
        -   Coloque o texto acima da barra, não abaixo.
        -   **Incorreto:**
        -   ![captura de tela da barra de progresso com texto abaixo ](images/win-wizards-image18.png)
        -   Neste exemplo, o texto explicativo deve aparecer acima da barra de progresso.
        -   Evite desobstruir a página de progresso com detalhes desnecessários. Esta página não é para suporte técnico; é para os usuários.
        -   **Incorreto:**
        -   ![captura de tela da barra de progresso com muito detalhe ](images/win-wizards-image19.png)
        -   Neste exemplo, os detalhes técnicos, como GUIDs, não têm significado para os usuários.
-   **Não use páginas de parabenização que não façam nada, mas terminem o assistente.** Se os resultados do assistente forem claramente aparentes para os usuários, basta fechar o assistente no botão de confirmação final.
    -   Use Follow-Up páginas quando houver tarefas relacionadas que os usuários provavelmente executarão como acompanhamento. Evite tarefas de acompanhamento familiares, como "Enviar uma mensagem de email".
    -   Use as páginas de conclusão somente quando os resultados não estiverem visíveis e não houver uma maneira melhor de fornecer comentários para a conclusão da tarefa.
    -   Os assistentes que têm páginas de progresso devem usar uma página de conclusão ou Follow-Up para indicar a conclusão da tarefa. Para tarefas de execução longa, feche o assistente na página de confirmação e use as notificações para fornecer comentários.
-   **Use páginas de resumo somente se a entrada for complexa e os usuários precisarem examinar, se a tarefa envolver um risco significativo (como uma transição financeira) ou se o assistente executar uma ação com base na entrada do usuário que não é óbvia (para criar confiança por meio de transparência).** Muitas vezes, as páginas de resumo não atendem a essa barra de relevância e podem ser omitidas.
-   **Use páginas de erro se o assistente não puder ser concluído devido a um problema do qual a recuperação não é possível.** Nesta página, explique o que o problema está em um idioma claro, sem que os usuários do jargão técnico não compreendam. Também fornecem etapas práticas que os usuários podem executar para resolver o problema. Para obter mais diretrizes, consulte [mensagens de erro](mess-error.md).
    -   **Exceção:** Se o assistente for concluído com um problema secundário do qual a recuperação é possível, apresente o problema como uma tarefa adicional em vez de um erro. Use um idioma positivo, orientado a sucesso e incentivado, e não termos como erro, falha ou problema. Não use um ícone de erro.

### <a name="navigation"></a>Navegação

-   **Use o próximo somente ao avançar para a próxima página sem compromisso.** Avançar para a próxima página é considerado um compromisso quando seu efeito não pode ser desfeito ao clicar em voltar ou cancelar.
-   **Use novamente para corrigir erros.** Além de corrigir erros, os usuários não precisam clicar em voltar para fazer o progresso em uma tarefa.
-   **Preserve as seleções de usuário por meio de navegação.** Por exemplo, se o usuário fizer alterações, clicar em voltar e em avançar, essas alterações deverão ser preservadas. Os usuários não esperam ter de reinserir as alterações, a menos que decidam explicitamente desmarcá-las.
-   **Não desabilite o botão voltar, a menos que a repetição das etapas seja prejudicial.**
-   **Permitir que os usuários procurem ou revisem opções nos seguintes cenários de navegação:**
    -   O usuário dá entrada, clica no botão confirmar, clica em voltar para revisar as alterações anteriores, não altera nada e clica novamente no botão confirmar. Normalmente, isso deve ser possível e a segunda confirmação deve apenas avançar para a próxima página (porque a tarefa já foi feita).
    -   O usuário dá entrada, clica no botão confirmar, clica em voltar para revisar as alterações anteriores, altera algo e, em seguida, clica no botão confirmar novamente. Normalmente, isso deve ser possível e a segunda confirmação deve refazer a tarefa com a entrada alterada (substituindo ou desfazendo o efeito do primeiro).

### <a name="help"></a>Ajuda

-   **As páginas do assistente de design para fornecer informações suficientes para que a referência à documentação na ajuda do programa seja desnecessária.** Um assistente já está levando os usuários longe da sua interação direta com o programa; exigir que os usuários busquem ajuda externa remove-os ainda mais desse Estado. A ajuda deve ser a exceção, não a regra.
-   **Se você precisar fornecer um ponto de acesso para ajudar, use um link na parte inferior esquerda da área de conteúdo da página (acima da área de comando).** Esse link deve ser curto e, normalmente, fraseada na forma de uma pergunta que os usuários têm mais probabilidade de serem respondidos.
-   **Correto:**
-   ![captura de tela da página do assistente com o link de ajuda ](images/win-wizards-image5.png)
-   Esse link para ajudar é apropriado porque informações básicas gerais como essa poderiam obstruir a página do assistente muito.

## <a name="text"></a>Texto

### <a name="general"></a>Geral

-   Use você e seu para se referir ao usuário e ao computador do usuário, ao documento, às configurações e assim por diante. Não use a primeira pessoa (I, My) para fazer referência ao computador ou ao assistente. No entanto, é aceitável usar a primeira pessoa em opções que o usuário seleciona. **Exemplo: minha** caixa de seleção usar somente.
-   Cada página de assistente deve ter uma [instrução principal](glossary.md).

### <a name="titles"></a>Títulos

-   Coloque o nome do assistente na barra de título. Use [a capitalização de estilo de título](glossary.md).
-   Os títulos não devem incluir pontuação, exceto aqueles com pontos de interrogação.
-   Não inclua o assistente do Word em títulos de assistente. Por exemplo, use conectar a uma rede em vez do assistente de configuração de rede.

### <a name="buttons"></a>Botões

-   Não inclua texto no botão voltar. Em vez disso, use o glifo de seta sem rótulo.
-   Incluir texto no botão Avançar. Não use glifos (como > ou >>) Além da palavra Next.
-   Use rótulos de botão de confirmação específicos que fazem sentido por conta própria e são uma resposta para a instrução principal. Idealmente, os usuários não precisam ler mais nada para entender o rótulo. Os usuários têm muito mais probabilidade de ler rótulos de botão de comando do que texto estático.
-   Se possível, não use a palavra concluir para o rótulo do botão confirmar, pois geralmente há um botão de confirmação melhor e mais específico:
    -   Se você clicar no botão for confirmado na tarefa (para que a tarefa ainda não tenha sido executada), use um rótulo específico que comece com um verbo que seja uma resposta à instrução principal (exemplos: imprimir, conectar, iniciar).
    -   Se a tarefa já tiver sido executada no assistente, use fechar em vez disso.

        **Exceção**

        -   Você pode usar concluir quando o rótulo específico ainda for genérico, como salvar, selecionar, escolher ou obter.
        -   Você pode usar concluir quando a tarefa envolve alterar uma configuração ou uma coleção de configurações.

-   Inicie os rótulos do botão confirmar com um verbo. As exceções são OK, sim e não.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Não use pontuação final.

## <a name="documentation"></a>Documentação

-   Embora a maioria dos assistentes do Windows não tenha mais o assistente de palavra no título, é aceitável se referir a assistentes como assistentes na documentação. Essa referência deve estar em minúsculas.
-   **Correto:**
-   Se você estiver configurando uma rede pela primeira vez, poderá obter ajuda usando o assistente **conectar-se a uma rede** .
-   Alguns assistentes herdados de versões anteriores do Windows podem incluir o assistente no título. Ao fazer referência a um desses assistentes, é aceitável usar o \[ \] Assistente x para evitar dizer o \[ Assistente do assistente x \] .
-   Consulte uma tela individual dentro de um assistente como uma página.

 

 