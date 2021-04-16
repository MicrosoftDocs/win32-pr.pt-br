---
title: Animações e transições
description: O uso estratégico de animações e transições pode tornar seu programa mais fácil de entender, se sentir mais suave, mais natural e de maior qualidade e ser mais atrativo.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6d57c696bd78df9c9505bb85453456f10631a00d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104557197"
---
# <a name="animations-and-transitions"></a>Animações e transições

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

O uso estratégico de animações e transições pode tornar seu programa mais fácil de entender, se sentir mais suave, mais natural e de maior qualidade e ser mais atrativo. Mas o uso gratuito de animações e transições pode deixar seu programa confuso e até mesmo irritante.

As animações dão a aparência de movimento ou alteração ao longo do tempo. Use a animação para fornecer comentários, Visualizar o efeito de uma ação, mostrar a relação entre objetos, chamar a atenção para alterar ou explicar uma tarefa visualmente.

![figura do teclado numérico com uma chave realçada ](images/vis-animations-image1.png)

O Microsoft Windows usa uma animação flash em segundo plano para fornecer comentários de que o objeto foi clicado.

As transições são animações usadas para manter os usuários orientados durante alterações de estado da interface do usuário e manipulações de objetos e fazer com que essas alterações se sintam suaves em vez de dissonante. Boas transições sentem-se naturais, geralmente dando a ilusão de que os usuários estão interagindo com objetos do mundo real.

![Captura de tela que mostra três tamanhos de gadgets meteorológicos.](images/vis-animations-image2.png)

Os gadgets do Windows Desktop usam transições suaves entre seus Estados conciso e detalhados.

Em geral, as melhores animações e transições são usadas para se comunicar com os usuários de forma não verbal, e para fazer alterações de estado mais naturais e menos perceptíveis. Por outro lado, o menos eficaz é gratuito, pois eles não se comunicam nada nem desenham atenção desnecessária. As animações são mais bem usadas como uma forma secundária de comunicação. Eles devem comunicar informações que são úteis, mas não são essenciais, e para serem acessíveis, os usuários devem ser capazes de determinar informações equivalentes por meio de outros meios.

**Observação:** As diretrizes relacionadas à [identidade visual](exper-branding.md), [som](vis-sound.md)e [acessibilidade](inter-accessibility.md) de software são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere as perguntas a seguir.

### <a name="animations"></a>Animações

As seguintes condições se aplicam?

-   A animação comunica visualmente algo útil, como fornecer comentários, mostrar relações, causas e efeitos ou dar atenção à alteração importante.
-   Ver a animação não é essencial. Informações equivalentes podem ser obtidas de outra maneira. Os usuários podem não se beneficiar da animação se:
    -   Eles desligaram as animações.
    -   Sua atenção é em outro lugar.
    -   Eles são visualmente prejudicados.
    -   A animação é obscurecida por outra janela.
    -   A animação não é reproduzida devido ao desempenho insuficiente do sistema.
-   A animação não afeta a produtividade do usuário. Ou:
    -   Isso ocorre rapidamente (200 milissegundos ou menos).
    -   Ele não interfere na interação ou pode ser interrompido.
    -   O usuário precisa esperar de qualquer forma.
-   A animação não afeta o fluxo do usuário.
    -   Ele está no centro do usuário de atenção ou chama atenção para algo fora do centro de atenção que é importante ou útil para a conclusão de uma tarefa.
    -   Ele é facilmente ignorável, sem distração ou irritante.
    -   Ele não se torna cansativo. Os usuários ainda acham apropriado e agradável mesmo após a exibição repetida.

Nesse caso, considere usar uma animação.

### <a name="transitions"></a>Transições

É um estado de alteração de objeto ou de cena e todas as condições acima para usar animações, bem como qualquer uma das seguintes condições se aplicam?

-   A alteração de estado é, de forma conceitual, desorientada, confusa ou difícil de entender.
-   A alteração de estado é visualmente dissonante, não tem continuidade ou suavidade, ou pisca; ou parecer innatural, inaprimored ou de baixa qualidade, especialmente se envolver uma área de tela grande.
-   O uso de uma transição faria com que a alteração de estado fosse mais rápida.
-   A alteração de estado é digna de atenção especial do usuário.

Nesse caso, considere usar uma transição.

## <a name="design-concepts"></a>Conceitos de design

Animações e transições são uma maneira eficaz de comunicar informações visualmente que, de outra forma, exigem texto para explicar ou podem ser perdidas por usuários.

**Incorreto:**

![captura de tela da caixa de diálogo com a mensagem ](images/vis-animations-image3.png)

**Correto:**

![Figura de comunicação visual de animação ](images/vis-animations-image4.png)

O uso de uma animação comunica as mesmas informações, mas de forma natural e discreta. Qual seria o que você veria em milhares de vezes?

**Animações e transições não precisam exigir atenção para serem bem-sucedidas.** Na verdade, eles costumam ser usados para evitar a atenção da mecânica para programar a qual os usuários não precisam estar cientes. Muitas animações bem-sucedidas são tão naturais que os usuários nem mesmo estão cientes delas; em vez disso, os usuários observarão apenas sua ausência. A frequência de ocorrências aumenta a necessidade de sutilezas, portanto, salve os efeitos que exigem atenção para eventos infrequentes que realmente merecem a atenção.

![captura de tela de todos os programas mudando para seta para voltar ](images/vis-animations-image5.png)

Uma transição do menu iniciar que evita a atenção do desenho.

Além de tornar seu programa mais fácil de entender e se sentir mais suave, **animações e transições bem projetadas são uma ótima maneira de adicionar personalidade, caractere e estilo ao seu programa.** Eles podem tornar a experiência do usuário mais imersiva e envolvente, dando a ele uma sensação natural e real.

![Figura mostrando como o foco afeta a cor do botão ](images/vis-animations-image6.png)

O Windows 7 realça os botões da barra de tarefas em foco com base na posição atual do mouse e na cor do ícone do programa. Essa abordagem é visualmente atraente, mas sutil, que transmite uma personalidade modesta.

**No entanto, animações e transições são mais eficazes e boas-vindas quando atendem a uma finalidade clara.** Eles devem ser usados para melhorar a usabilidade, a suavidade e o fluxo, bem como a percepção da qualidade, sem prejudicar o desempenho de forma significativa.

Embora alguns tipos de animações sejam usados para atrair a atenção do usuário, certifique-se de que a atenção seja bem merecida e digno de interrupção do treinamento de pensamento do usuário. O olho humano é sensível ao movimento, especialmente o movimento periférico. Pode ser difícil para os usuários se concentrarem quando houver um botão de barra de tarefas piscando ou um ícone de área de notificação girando. **Evite usar animações para interromper ou distrair os usuários ou chamar a atenção para coisas que não asseguram a atenção do usuário.**

**Incorreto:**

![figura do botão da barra de tarefas realçado sem motivo ](images/vis-animations-image7.png)

Os programas não devem piscar o botão da barra de tarefas a menos que os usuários devam fazer algo importante imediatamente. Nesse caso, a única coisa que o usuário precisa fazer é ativar o programa.

**Use animações e transições porque seu programa precisa delas, não apenas porque você pode.** E para acessibilidade, não use animação como a única maneira de transmitir informações essenciais. Certifique-se de que os usuários possam obter informações equivalentes de uma maneira diferente.

### <a name="attributes-of-good-animations-and-transitions"></a>Atributos de boas animações e transições

Boas animações e transições têm o equilíbrio certo entre estes atributos:

-   **São claramente intencionais.** As boas animações estão lá porque precisam se comunicar com informações, fazer uma interação real ou chamar a atenção para algo digno de opinião. E as animações intencionais são precisas; se uma animação mostrar que uma tarefa está sendo feita, é porque a tarefa está sendo realmente executada.

**Incorreto:**

![captura de tela do ícone de bateria e rótulo com cobrança total ](images/vis-animations-image8.png)

Neste exemplo, a animação mostra que uma bateria totalmente carregada está sendo cobrada.

-   **Parecer suave e contínuo.** Boas animações removem suavemente as emendas entre as alterações de estado da cena ou do elemento mostrando relações e fornecendo uma noção de lugar e contexto. A continuidade ajuda os usuários a entender como eles têm onde eles estão e como voltar para onde eles vieram.

![captura de tela de três visualizações da janela da barra de tarefas ](images/vis-animations-image9.png)

A janela da barra de tarefas do Windows 7 visualização é metamorfoseada para fins de continuidade à medida que o usuário passa de um programa para outro.

-   **São realistas.** Boas animações simulam as propriedades físicas e o comportamento de um objeto no mundo real. Isso ajuda os usuários a prever e entender os resultados de suas interações. Você não precisa modelar o mundo real exatamente, mas se você usar animações realistas, deverá mantê-las consistentes com o mundo real. Os usuários nunca devem ficar surpresos ou confusos com os resultados, especialmente com animações usadas para manipulação direta.

![figura do botão da barra de tarefas arrastada para nova posição ](images/vis-animations-image10.png)

Neste exemplo, a animação "sair da forma" usada pela barra de tarefas do Windows 7 se sente mais realista do que um ponto de inserção estático.

-   **São autênticos.** Até mesmo os objetos que não são encontrados no mundo real podem parecer naturais com base no comportamento real de um objeto diferente, mas relacionado. Essa metáfora só funcionará se a relação se comunicar claramente com a finalidade e o comportamento pretendidos.

![captura de tela do efeito gerado por trás da janela movida ](images/vis-animations-image11.png)

Neste exemplo, a animação de janela "Squeegee" usada pelo Windows 7 é autêntica porque é consistente com a forma como as janelas de vidro podem se comportar no mundo real.

-   **Use o mapeamento natural.** Os mapeamentos naturais são físicos ou culturais. Um mapeamento natural baseado em cultura, por exemplo, pode começar do fato que nas culturas ocidentais, as pessoas lêem da esquerda para a direita. Consequentemente, para expressar uma sequência de tempo de objetos, o objeto do meio é atual, os objetos à esquerda são do passado e os objetos à direita estão no futuro. O avanço no tempo é indicado pelo movimento da esquerda para a direita.

![captura de tela da barra de progresso do player de mídia ](images/vis-animations-image12.png)

Neste exemplo, o controle do Windows Media Player tem um mapeamento natural porque a reprodução move a posição da esquerda para a direita.

-   **Têm personalidade.** As animações bem escolhidas são ótimas maneiras de adicionar personalidade, caractere e estilo ao seu programa. Eles podem tornar a experiência do usuário mais envolvente e envolvente. Embora o tipo de animação determine o que ele comunica, a maneira específica na qual a animação é executada mostra a personalidade do programa. Boas animações projetam a personalidade certa para seu programa, seja sério ou estranho ou em algum lugar entre eles.

![captura de tela da interface Zune criada de forma criativa ](images/vis-animations-image13.png)

Neste exemplo, o uso Zune do texto animado e da ajuda de perspectiva dinâmica forma sua personalidade.

-   **Aparência responsiva.** Boas animações não prejudicam a produtividade do usuário, bloqueando os usuários de outras interações ou forçando os usuários a assistirem. Não importa quão naturais e envolvem as animações de seu programa, ninguém deseja esperar por elas exclusivamente. Boas animações também parecem responsivas sem serem dissonantedas tendo um início rápido com uma aterrissagem flexível. Animações responsivas também se beneficiam da comunicação rápida da sua finalidade. Os usuários não precisam observar uma animação por muito tempo apenas para descobrir o que está fazendo ou quando isso é feito. Para a manipulação direta, animações responsivas são essenciais para manter uma sensação direta e envolvente do mundo real. Para se sentir direto, os pontos de contato de um objeto devem permanecer sob o ponteiro sem problemas em toda a manipulação. Qualquer atraso, resposta instável ou perda de contato destrói a percepção da manipulação direta.

![figura do dedo tocando em uma tela sensível ao toque ](images/vis-animations-image14.png)

Neste exemplo, a transição de panorâmica de toque se sente responsivo mantendo o ponto de contato sob o dedo do usuário em toda a manipulação.

-   **Atraia o nível certo de atenção.** Boas animações são geralmente sutis e desenham apenas a atenção necessária para atender às suas finalidades. Como resultado, eles não são confusos, irritantes, excessivamente complexos, excessivamente longos ou repetitivos. Eles não se tornam cansativo após as exibições repetidas.

![captura de tela do realce de esmaecimento em nomes de arquivo ](images/vis-animations-image15.png)

Neste exemplo, o Windows Search chama temporariamente a atenção para correspondência de palavras de pesquisa e, em seguida, desaparece.

-   **Só se parece especial se for autêntico.** A frequência aumenta a necessidade de sutilezas, portanto, as interações comuns precisam de animações simples que comunicam uma ideia simples de uma maneira simples. Reserve animações especiais e complexas para experiências especiais e frequentes.

![captura de tela de quatro círculos se tornando o logotipo do Windows ](images/vis-animations-image16.png)

Neste exemplo, o Windows usa uma animação com atenção na inicialização para fazer com que a experiência se sinta especial, mas essa animação seria inadequada em outro lugar.

Você saberá que atingiu o equilíbrio certo quando a experiência geral for prejudicada se qualquer um desses atributos fosse removido.

### <a name="creating-an-animation-vocabulary"></a>Criando um vocabulário de animação

Boas animações são sobre a comunicação visual eficaz, e a consistência é crucial para sua eficácia. Se você usar uma transição específica, como enviar por push uma cena da direita para avançar para a próxima cena, essa deve ser a única transição usada para essa finalidade e essa transição não deve ser usada para nenhuma outra finalidade. A atribuição de diferentes significados à mesma animação prejudica sua capacidade de comunicação. Ao atribuir animações específicas e transições para significados específicos, você está criando um vocabulário de animação.

Esse problema se aplica a animações e transições que têm significado, e não genéricos, que os usuários não têm probabilidade de atribuir significado ou aqueles cuja finalidade seja não perceptível. Por exemplo, animações como efeitos especiais e fades, como dessoluções, não têm significado específico, para que possam ser usadas livremente.

Um bom vocabulário atribui animações que modelam o comportamento físico de um objeto. Se você precisar atribuir uma animação a um objeto ou ação que não tenha um equivalente do mundo real, escolha uma animação que mostre como o objeto pode se comportar era real.

![captura de tela de como o hover torna o brilho do logotipo do Windows ](images/vis-animations-image17.png)

Embora o menu Iniciar não seja um objeto do mundo real, seu efeito de foco aparece como um objeto do mundo real pode ser quando ativado.

Cada animação em um vocabulário precisa ser claramente distinta. As animações devem ter comportamentos semelhantes somente se suas ações associadas estiverem relacionadas de forma semelhante. Por exemplo, as transições de movimento sugerem navegação, para que você possa usar transições de movimento de direções diferentes para indicar diferentes tipos de navegação.

Você saberá que suas animações e transições não estão se comunicando bem quando os usuários encontram os resultados confusos, surpreendentes ou inesperados. Geralmente, é melhor conseguir uma única finalidade bem do que várias finalidades não tão bem.

Idealmente, seu vocabulário de animação deve ser abrangente em todas as áreas do seu programa que precisam delas. Se apenas algumas interações tiverem animações naturais, isso chamará a atenção para as que não o fizerem.

Para saber mais sobre o vocabulário de animação do Windows, consulte a seção [padrões de uso](#usage-patterns) deste artigo.

### <a name="designing-the-right-personality"></a>Projetando a personalidade correta

Embora o tipo de animação determine o que ele comunica, a maneira específica na qual a animação é executada fala sobre a personalidade do programa e reforça sua marca.

A personalidade do seu programa deve refletir a natureza de suas tarefas e a personalidade de seus usuários, portanto, não é uma opção arbitrária. Em vez disso, uma personalidade bem projetada deve parecer autêntica; Nunca tente forçá-lo. A personalidade deve fazer uma conexão emocional com o usuário. Alguns fatores a considerar:

-   **Tarefas:** Sério ou divertido; opcional ou obrigatório.
-   **Consequências:** Sério ou secundário.
-   **Custo:** Gratuito ou adquirido; Se adquirido, com preço moderado ou caro.
-   **Foco do usuário:** Grupo relativamente estreito de usuários de destino ou público geral amplo.
-   **Ambiente do usuário:** Profissional, casual ou doméstica.
-   **Idade do usuário:** Mais jovem ou mais antigo.
-   **Frequência de uso:** Frequente ou frequente.

A combinação desses fatores ajuda a determinar uma personalidade apropriada para o seu programa. Aqui estão algumas combinações adequadas para tipos comuns de programas:

**Aplicativos de produtividade**

Naturalmente, os aplicativos de produtividade devem se concentrar na produtividade. Embora algumas experiências especiais possam se destacar, a maioria das outras animações deve ter essas características:

-   Small
-   Natural, realista
-   Sutil, subdued
-   Rápido e eficiente
-   Reduzido

**Utilitários**

Os utilitários normalmente são usados rapidamente, portanto, o uso da animação pode ser mais agressivo:

-   Realista, ilustrativo e auto-explicativo
-   Safe
-   Envolventes

**Entretenimento, jogos**

Como o objetivo desses programas é envolver e fascinamr os usuários, as animações e transições podem ser muito mais agressivas com essas características:

-   Grande (possivelmente se tornando parte integrante da experiência)
-   Artificial, surreal
-   Impactado, vibrante
-   Emocional, filhotes, estranho
-   Energético

Fazer uma conexão emocional é tão importante para os programas de entretenimento que é aceitável entortar algumas regras, caso isso ajude a tornar os usuários ficarem em amor com o programa. Por exemplo, é aceitável que uma animação ou transição se torne cansativo após o tempo centésimo, se a maioria dos usuários for improvável de usar o programa que geralmente.

Em geral, animações e transições que são pequenas, naturais, subdueds, eficientes, porém relaxadas são a aposta mais segura. As transições com essas características normalmente levam o caminho mais curto do início ao fim, começam rapidamente, terminam de forma flexível e não estão superlançadas. Além disso, as transições bem projetadas são projetadas para funcionar bem em todo o intervalo de distâncias em que serão usadas.

### <a name="animation-performance"></a>Desempenho da animação

Ao projetar animações, certifique-se de que elas não afetem a capacidade dos usuários de usar seu programa com eficiência. Em geral, torne suas animações lentas o suficiente para atender à sua finalidade, mas rápido o suficiente para que elas não interfiram na capacidade de resposta, exigem muita atenção ou se tornam cansativo.

**Incorreto:**

![Figura de folheio de página da direita para a esquerda ](images/vis-animations-image18.png)

Embora esta página virando a animação tenha uma aparência envolvente e real, ela diminui a produtividade dos usuários ao levar mais tempo para transformar as páginas.

As transições breves (200 milissegundos ou menos) são um caso especial (especialmente quando elas geralmente funcionam de um atraso) porque os usuários terão que esperar um segundo dividido para elas. Os usuários estão dispostos a esperar por tais animações se:

-   A espera percebida é extremamente breve (200 milissegundos ou menos).
-   A transição faz com que a interação fique mais suave e natural.
-   A transição faz com que a interação fique mais responsiva.
-   Qualquer atraso ajuda a manter o usuário no controle da interação.

![Figura dos botões da barra de tarefas arrastados para a nova posição ](images/vis-animations-image19.png)

Os usuários aceitarão um breve atraso para o botão da barra de tarefas reordenar a animação porque ela é muito breve e torna a interação mais natural.

Há três maneiras pelas quais as animações podem afetar negativamente o desempenho: velocidade, capacidade de resposta e percepção.

Para velocidade, algumas animações são visuais veneerss sobre tarefas de uso intensivo de CPU, portanto, a última coisa que você deve fazer é tornar essas tarefas mais lentas com animações com uso intensivo de CPU. A maioria das animações com uso intensivo de CPU (animações "pesadas") tendem a:

-   Envolvem muitos elementos que se movem de forma independente.
-   Jogue por uma longa duração ou distância.
-   Envolver uma grande quantidade de espaço na tela.
-   São matematicamente intensivas.

Animações com menos impacto no desempenho:

-   Envolve um único objeto.
-   Jogue por uma curta duração ou distância.
-   Envolve uma pequena quantidade de espaço na tela.
-   Não são matematicamente intensivas.

Para garantir um bom desempenho, animações pesadas devem ser usadas apenas para tarefas que não são intensivas na CPU, enquanto animações leves podem ser usadas em qualquer lugar.

Para capacidade de resposta, a maioria das animações e transições deve ser projetada para que os usuários possam interagir enquanto a animação estiver em execução. A menos que uma animação faça parte de um processo, torne-a independente da interação principal do usuário e permita que os usuários a interrompam.

Uma animação pode não afetar negativamente o desempenho de uma tarefa na realidade, mas os usuários podem ter a percepção que ela faz. Por exemplo, não use uma animação que pareça pesada para uma tarefa lenta de uso intensivo de CPU, mesmo que não danifique o desempenho, pois os usuários podem concluir que a animação é o motivo pelo qual a tarefa está lenta. **Se algo parecer lento, ele ficará lento, portanto, é melhor usar animações que se sintam simples, leves e rápidas.** O uso de animações com inícios instantâneos para tarefas de uso intensivo de CPU ajuda.

**Situação**

![captura de tela da caixa de diálogo de cópia com barra de progresso ](images/vis-animations-image20.png)

Embora a animação na caixa de diálogo de cópia de arquivos do Windows não danifique o desempenho da cópia do arquivo, ela corre o risco de que os usuários considerem isso.

**Também arriscado:**

![captura de tela do progresso exibido na barra de endereços ](images/vis-animations-image21.png)

Neste exemplo, a animação de progresso de aparência lenta na barra de endereços do Windows Explorer faz com que algumas tarefas pareçam muito lentas.

Animações e transições não têm valor se sua qualidade for tão ruim que tornam a experiência menos suave e menos atraente. Para manter sua qualidade, as animações devem ser projetadas para degradar normalmente sempre que recursos do sistema suficientes não estiverem disponíveis. As animações podem diminuir com a existência de variações que exigem menos recursos (como comprimentos menores ou taxas de quadros inferiores) ou até mesmo não sendo executadas. Independentemente dos recursos disponíveis, verifique se as animações têm alta qualidade e se parecem com animações em vez de bugs de software.

Por fim, se os usuários acreditarem que as animações e as transições do programa reduzem sua produtividade, há uma boa chance de que alguns usuários desejarão desativá-las. Para dar suporte a essa capacidade, respeite a opção de desativar **todas as animações desnecessárias** encontradas na central de facilidade de acesso do Windows.

### <a name="attracting-the-right-level-of-attention"></a>Atraindo o nível certo de atenção

Embora apenas alguns tipos de animações e transições sejam projetados especificamente para atrair a atenção do usuário, eles devem ser projetados para atrair o nível certo de atenção para atender bem às suas finalidades. Quais são as diferentes maneiras de atrair atenção e como escolher a correta?

**Efeitos de animação**

Efeitos de animação diferentes atraiem níveis diferentes de atenção. A lista a seguir resume os métodos mais comuns, começando com a obtenção de mais atenção:

-   **Piscando rapidamente.** Exige atenção imediata. Pode interromper a concentração dos usuários, independentemente de onde a intermitência está ocorrendo.
-   **Intermitência moderada.** Mesmo, mas exige menos atenção com a frequência mais baixa.
-   **Saltando.** Notável na visão periférica e relativamente exigente de natureza. É provável que os usuários percebam, mas podem continuar a se concentrar em outro lugar somente se a duração for curta.
-   **Motion.** Notável na visão periférica, mas não exige. No entanto, as animações complexas ou 3D atraiem mais atenção do que os movimentos simples ou 2D. É provável que os usuários percebam, mas podem continuar a se concentrar em outro lugar.
-   **Pulsing moderado.** Perceptível, mas sem distração na visão periférica. Os usuários podem continuar a se concentrar em outro lugar. Pode pulsar brilho, cores e tamanhos.
-   **Pulsing/brilho lento.** Perceptível, mas sutil. Atrai mais atenção do que um efeito estático, mas os usuários talvez não percebam a animação, a menos que já estejam olhando.
-   **Efeito.** Ainda menos perceptível. Atrai mais atenção do que um efeito estático, mas os usuários talvez não percebam a animação, a menos que já estejam olhando.
-   **Realce estático/gleam.** É perceptível se os usuários optarem por procurar, mas não exigirá atenção se estiver em outro lugar.
-   **Ambiente/natural.** Não é intencionalmente perceptível por ter uma aparência natural e real.

Para determinar a abordagem certa para seu programa ou recurso, considere como esses fatores se relacionam aos cenários do seu recurso.

Por exemplo, suponha que você está criando um programa de mensagens instantâneas e alguém acabou de enviar uma mensagem para o usuário. Esse cenário requer a atenção do usuário, deve ser perceptível em qualquer lugar e, geralmente, o usuário desejará responder rapidamente. Esse cenário sugere que uma animação de intermitência moderada seria uma boa opção. Por outro lado, suponha que você queira informar aos usuários que um trabalho de impressão foi concluído. Os usuários devem ser capazes de continuar a se concentrar e trabalhar de forma produtiva em outro lugar, e é aceitável se os usuários não notarem. Esse cenário sugere que a Pulsing ou o brilho de moderado a lento seria uma boa opção.

**Duration**

A duração apropriada para uma atenção ao obter animação depende do cenário e do tipo específico de animação usado. Quanto mais atenção um efeito de animação exigir, menor será a duração. Embora efeitos muito sutis que exigem pouca atenção (como Pulsing lentas) possam ser reproduzidos indefinidamente, a atenção dos efeitos deve ser reproduzida apenas entre 1 e 3 segundos. Os riscos mais longos tornam a animação incômodo e irritante.

![captura de tela do botão da barra de tarefas realçado ](images/vis-animations-image22.png)

No Windows 7, a barra de tarefas pisca em atenção apenas por um segundo. Qualquer um mais incômodo seria irritante.

**Decaimento de efeito**

Você deve planejar a atenção-obtendo animações com base na suposição de que, se os usuários não responderem imediatamente, isso ocorre porque estão ocupados fazendo alguma outra coisa e não querem ser interrompidos. Portanto, seu objetivo deve ser atrair atenção sem exigir.

Para obter o equilíbrio certo de atrair atenção sem exigir isso, decaimento a intensidade de um efeito ao longo do tempo. Por exemplo, para atrair a atenção, você pode tornar o efeito inicialmente forte, mas retardar o efeito rapidamente. Ao fazer isso, a potência atrativa é basicamente determinada pelo efeito inicial, mas a impressão geral do usuário é determinada principalmente pelo seu término.

![captura de tela demonstrando a taxa de flash reduzida ](images/vis-animations-image23.png)

No Windows 7, o efeito de flash da barra de tarefas fica mais lento no final.

### <a name="what-about-powerpoint"></a>E o PowerPoint?

As transições do Microsoft PowerPoint geralmente violam deliberadamente essas diretrizes porque elas foram projetadas para chamar a atenção para as transições de slides e exigem que os usuários aguardem. Além disso, eles não têm nenhum significado específico para que não se comuniquem nada além do fato de que um slide está mudando.

Transições de estilo do PowerPoint, quando usadas corretamente, têm estas finalidades:

-   Elas dividem apresentações longas em partes menores forçando o apresentador a pausar.
-   Eles desenham a atenção do público em direção às alterações na apresentação, ajudando as pessoas a se concentrarem se suas mentes se perguntou.
-   Eles fornecem à apresentação uma ritmo para que ela não fique monótono ou exagerada.
-   Seu estilo reflete a personalidade do apresentador ou do material.

Embora essas sejam metas importantes para uma apresentação, essas transições Desenhariam atenção desnecessária na interface do usuário da maioria dos tipos de programas e se tornaram cansativo rapidamente.

**Linha inferior:** Não use as transições de estilo do PowerPoint como um modelo para o seu programa.

**Se você fizer apenas seis coisas...**

1.  Use animações e transições para facilitar a compreensão do seu programa e se sentir mais suave e envolvente. Eles devem ter uma finalidade clara. Não use animações apenas porque você pode ou para desenhar atenção desnecessária ao seu programa.
2.  Defina um vocabulário de animação e use-o consistentemente em todo o programa. Use o vocabulário de animação do Windows 7 quando apropriado.
3.  Use as características de suas animações para dar à sua personalidade do programa e reforçar sua marca.
4.  Torne a maioria das animações simples, breve e sutil. Lembre-se de que as animações não precisam exigir atenção para serem bem-sucedidas. Se uma animação for apropriada e natural, os usuários perceberão apenas sua ausência.
5.  Torne suas animações rápidas e responsivas e dê a elas uma sensação leve. Não importa o quanto envolvem suas animações, ninguém vai querer sentir como estão esperando por elas. Crie animações mais pesadas para ter uma degradação normal.
6.  Design para a longa execução. Se uma animação for irritante, distraindo ou cansativo, recrie-a ou remova-a.

## <a name="usage-patterns"></a>Padrões de uso

As animações têm vários padrões de uso:



|                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentários de foco**<br/> para mostrar onde está o ponto de interação. <br/>                                | Indica que o ponto de interação está ativo. o foco pode ser mostrado também por meio de um efeito estático.<br/> vocabulário do Windows: Exibir efeito de foco (retângulo delimitador, realce, ampliação) com um efeito de fade in/fade out para suavidade. <br/> ![captura de tela de uma das seis tampas do álbum realçadas ](images/vis-animations-image24.png)<br/> No player de mídia digital do Zune, o álbum cobre realce e adicione controles de reprodução ao focalizar.<br/>                                                                                                                                                                                                                 |
| **Clique em comentários**<br/> para mostrar que um objeto clicável é responsivo e recebeu um clique. <br/>    | Indica que um objeto foi clicado.<br/> vocabulário do Windows: plano de fundo do objeto flash no evento clique para baixo. para mostrar contato de toque, use um efeito de ondulação. <br/> ![foto do dedo na tela sensível ao toque mostrando as copiadas ](images/vis-animations-image25.png)<br/> O Touch exibe uma animação ondulada para que o usuário saiba que a interação foi reconhecida.<br/>                                                                                                                                                                                                                                                                                                         |
| **Comentários da seleção**<br/> para mostrar que um objeto está selecionado. <br/>                                | Indica que um objeto está selecionado. a seleção também pode ser mostrada por meio de um efeito estático.<br/> vocabulário do Windows: desenhar retângulo de seleção com um efeito de fade in/fade out para suavização. <br/> ![Figura de uma capa de álbum clicada e selecionada ](images/vis-animations-image26.png)<br/> No Zune, o álbum cobre piscar de clique e, em seguida, obter um retângulo de seleção na seleção.<br/>                                                                                                                                                                                                                                                                      |
| **Comentários de progresso**<br/> para mostrar que uma tarefa está sendo executada. <br/>                             | Os comentários de progresso indicam que uma tarefa está progredindo, normalmente com indicadores de atividade, barras de progresso ou animações que ilustram a tarefa. Os comentários de progresso de destérmino mostram aproximadamente quanto da tarefa foi feita e o quanto resta, enquanto o progresso indeterminado apenas indica que a tarefa está sendo feita.<br/> vocabulário do Windows: indicadores de atividade de rotação, barras de progresso, planos de fundo de progresso, animações de ilustração. <br/> ![captura de tela da caixa de diálogo com texto ' entrando ' ](images/vis-animations-image27.png)<br/> Neste exemplo, o Windows Live Messenger exibe os comentários de progresso indeterminados durante a entrada.<br/> |
| **Atraidor**<br/> para mostrar que algo precisa da atenção do usuário. <br/>                          | Atraia o nível certo de atenção quando objetos significativos são criados ou precisam de atenção (geralmente devido a alterações) ou eventos importantes ou urgentes acontecem. consulte [atraindo o nível certo de atenção](#attracting-the-right-level-of-attention) para técnicas de design.<br/> vocabulário do Windows: piscando, movendo, Pulsing, brilhando, gleam. <br/> ![captura de tela demonstrando animação de barra de ferramentas ](images/vis-animations-image28.png)<br/> A barra de ferramentas do Windows Live anima na primeira aparência para deixá-la óbvia onde está.<br/>                                                                                                                                 |
| **Relação**<br/> para mostrar a relação entre objetos ou causalidade em efeitos. <br/>        | Mostrar relações, especialmente quando a relação pode não ser compreendida ou esperada, de uma forma que não seja confuso ou confusa.<br/> vocabulário do Windows: metamorfose, transporte, alteração física, como inverter, aumentando de uma fonte de ponto, reduzindo para um destino de ponto. <br/> ![captura de tela da caixa de diálogo de calibragem de cor](images/vis-animations-image29.png)<br/> Neste exemplo, a animação mostra a relação entre a configuração gama e seu efeito na exibição.<br/>                                                                                                                                                    |
| **Ilustração/visualização**<br/> para explicar visualmente um conceito, uma tarefa ou o efeito de um comando. <br/> | Uma animação ou vídeo que explica um conceito ou como algo funciona visualmente, seja para complementar ou substituir uma explicação textual. Isso permite que os usuários executem tarefas ou escolham comandos com eficiência e confiança. <br/> ![captura de tela de erro de ortografia de correção de caneta ](images/vis-animations-image30.png)<br/> Neste exemplo, os comandos "Mostre-me" do painel de entrada do Tablet PC usam ilustrações para mostrar como corrigir, excluir, dividir e unir.<br/>                                                                                                                                                                                                        |



 

As transições têm vários padrões de uso:



|                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objeto aumentar/reduzir/aparecer**<br/> para alterar o tamanho ou o estado de um objeto sem problemas. <br/>                                                                                                         | Alterações de objeto entre os Estados, possivelmente ao mover. a transição mantém os usuários orientados durante as alterações.<br/> vocabulário do Windows: Morph, altere o tamanho, os slides de objeto para dentro ou para fora. <br/> ![captura de tela de três tamanhos de gadgets meteorológicos ](images/vis-animations-image31.png)<br/> Neste exemplo, o gadget meteorológico é metamorfose de seu estado conciso para exibir sua caixa de diálogo opções.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Mostrar/ocultar/alterar conteúdo**<br/> para mostrar, ocultar ou alterar o conteúdo sem problemas, normalmente para divulgação progressiva. <br/>                                                                       | As reformulações do interior da janela para exibir conteúdo mais, menor ou diferente. a transição mantém os usuários orientados durante as alterações.<br/> vocabulário do Windows: painel de slides para dentro ou para fora. janelas de submenu fade in e out. um conteúdo diferente desaparece ou se acumula. <br/> ![captura de tela de três tamanhos de calculadora ](images/vis-animations-image32.png)<br/> A calculadora do Windows tem uma transição suave entre modos de exibição.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Controle ou custo mostrar/ocultar**<br/> para mostrar ou ocultar de forma suave os controles ou suas capacidades na movimentação do mouse ou do rato a fim de simplificar a aparência normal do Visual. <br/>                | Exibe controles quando os usuários estão passando o ponteiro sobre uma área de comando ou exibem capacidades quando os usuários estão focalizando um controle. passar o mouse sobre essas áreas indica que o usuário pretende interagir. capacidades poderá ocultar se o ponteiro se tornar estático. <br/> ![captura de tela de controles esmaecidas antes de passar o mouse ](images/vis-animations-image33.png)<br/> Neste exemplo, os controles do Windows Media Player esmaecem ao focalizar quando estiver no modo de tela inteira.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Transições de cena**<br/> fazer uma transição de cena tranqüila e perfeita para evitar atenção. <br/>                                                                                   | Alterações de cena abrupta podem ser dissonante, especialmente para áreas de tela grandes, portanto, use transições de cena para criar suavidade e continuidade e para fornecer contexto. as transições de cena são projetadas para serem de chave natural e baixa, para evitar a atenção ao processo de transição em si.<br/> vocabulário do Windows: fade in/out; esmaecimento cruzado; deslizando para/esquerda, para fora/direita, para cima, para baixo; envios por push e capas. <br/> ![captura de tela de uma foto esmaecida em outra ](images/vis-animations-image34.png)<br/> Neste exemplo, o papel de parede da área de trabalho do Windows se cruzou suavemente entre imagens para fazer com que a transição fique tranqüila e controlada.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Transições especiais de cena**<br/> chamar a atenção para uma alteração de cena para torná-la especial ou refocar a atenção do usuário. <br/>                                                               | Embora a maioria das transições de cena não deva chamar atenção para o processo de transição, algumas foram projetadas para interromper o fluxo e chamar a atenção para enfatizar que algo diferente está prestes a acontecer. para chamar a atenção, as transições especiais de cena são projetadas para não serem naturais e têm alto impacto visual. <br/> ![captura de tela de atenção – slide de transição de captura ](images/vis-animations-image35.png)<br/> Neste exemplo, o PowerPoint usa a atenção – obter transições para desenhar o público na alteração.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulações diretas**<br/> para mostrar o efeito de manipulações diretas (como mover, rolar/panorâmica, girar e aplicar zoom). <br/>                                                                   | A transição mostra o efeito da manipulação em tempo real. o efeito deve parecer suave, contínuo e consistente com o mundo real. a movimentação e a rotação podem não ser contínuas em alguns lugares para indicar restrições ou escolhas preferenciais prováveis. o zoom torna o conteúdo maior ou menor, possivelmente alterando o nível de detalhes de acordo. <br/> ![captura de tela de três tamanhos de lupa ](images/vis-animations-image36.png)<br/> Neste exemplo, a lupa amplia suavemente os níveis.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulações diretas incorretas**<br/> para indicar que uma manipulação direta (como mover, rolar/panorâmica) foi tentada, mas não pôde ser feita. <br/>                                           | A transição mostra a tentativa de manipulação, mas reverte para o estado original. Geralmente, o efeito parece que a manipulação não pode ser executada devido a alguma restrição física do mundo real. essas animações são usadas em vez de mensagens de erro baseadas em texto, o que pode atrapalhar a sensação do mundo real da manipulação.<br/> vocabulário do Windows: elástico <br/> ![Figura de comunicação visual de animação ](images/vis-animations-image4.png)<br/> Neste exemplo, o documento salta para mostrar que o usuário atingiu o final.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Classificar, filtrar, reordenar transições**<br/> para indicar que a apresentação ou o conteúdo de uma coleção de itens foi alterado. <br/>                                                            | A transição mostra (ou para alterações complexas, sugere) o efeito da alteração. <br/> ![captura de tela de câmeras de linhas com três removidas ](images/vis-animations-image37.png)<br/> ![captura de tela semelhante com câmeras diferentes removidas ](images/vis-animations-image38.png)<br/> ![captura de tela semelhante com outras câmeras removidas ](images/vis-animations-image39.png)<br/> Neste exemplo, a pesquisa visual do Bing usa uma transição de filtro.<br/> ![captura de tela da capa do álbum alterando sua aparência ](images/vis-animations-image40.png)<br/> Neste exemplo, o Windows Media Center usa uma transição de reordenação como uma experiência especial enquanto uma música está sendo reproduzida.<br/>                                                                                                                                                                                                                                                                                   |
| **Transições de desempenho**<br/> para fazer com que uma ação pareça mais rápida. <br/>                                                                                                              | Embora qualquer transição tenha o potencial de fazer com que uma ação pareça mais rápida, a principal finalidade dessas transições é melhorar a percepção do desempenho e da capacidade de resposta. uma boa técnica é mostrar a tarefa que está sendo executada em etapas deliberadas. por outro lado, atrasar a ação, renderizar os resultados de maneira aleatória ou usar um indicador de atividade se sentirá lento.<br/> vocabulário do Windows: executar ação em estágios, com transições suaves entre os estágios. <br/> ![captura de tela da lista de atalhos adicionando destinos ](images/vis-animations-image41.png)<br/> Neste exemplo, uma lista de atalhos da barra de tarefas exibe imediatamente os itens padrão e, em seguida, os slides para exibir os destinos quando a lista estiver pronta. Fazer isso disfarça o tempo necessário para criar a lista. Por outro lado, atrasar a exibição inicial sentiria sem resposta, e exibir uma lista incompleta ou comentários de progresso sentiria muito mais lento.<br/> |
| **Experiências especiais**<br/> para envolver e fascinamr os usuários durante [experiências especiais](glossary.md) e raras que são importantes para seu programa e ter a atenção total do usuário. <br/>    | Embora qualquer transição tenha o potencial de ser uma experiência especial, essas transições são mais bem reservadas para experiências pouco frequentes que são realmente especiais para seu programa. as transições personalizadas são usadas para dar uma ideia especial. a identidade visual e a personalidade são geralmente elementos de design importantes. ao contrário de outros padrões, experiências especiais podem exigir atenção, ser pesadas e exigem que os usuários aguardem um momento. Consequentemente, essas transições são desgastas rapidamente se estiverem sobreutilizadas porque a experiência não é mais especial. <br/> ![captura de tela da alteração do logotipo do Windows para nova tela ](images/vis-animations-image42.png)<br/> Neste exemplo, o Windows Media Center exibe uma animação durante o carregamento para envolver os usuários imediatamente.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Diretrizes

### <a name="effective-communication"></a>Comunicação eficaz

-   **Defina e use um vocabulário de animação** para garantir que suas animações e transições tenham um significado consistente e use-as de forma consistente em todo o programa. A maioria dos vocabulários deve incluir entradas para aspecto e aparência do objeto e desaparecimento, navegação, interação básica (passando o mouse, selecionando, clicando), manipulação e interação de objetos (movendo, soltando, redimensionamento, rolagem, panorâmica, zoom, rotação, filtragem) e atraindo a atenção. O significado consistente é crucial para a comunicação efetiva.
-   **Sempre que for prático, use o vocabulário de animação do Windows.** Embora seu programa possa ter um público diferente e necessidades diferentes, muitas vezes os benefícios da consistência e da familiaridade superam os benefícios de serem diferentes. Se o vocabulário do programa precisar ser diferente, use os mesmos tipos básicos de animação que o Windows, mas dê a eles a personalidade certa para seu programa.
-   **Não atribua significados específicos a animações genéricas e transições em um vocabulário de animação.** Transições genéricas como efeitos especiais e fades, como dessoluções, não têm significado específico (além de aparecer ou desaparecerem), para que possam ser usadas livremente.

    **Incorreto:**

    ![captura de tela de uma caixa de diálogo esmaecida em outra ](images/vis-animations-image43.png)

    Neste exemplo, um esmaecimento cruzado é usado incorretamente para navegar para o próximo item. Como os esmaecimentos cruzados não têm nenhum significado específico, essa transição não fornece contexto.

-   **Torne as entradas de vocabulário claramente distintas.** As ações relacionadas podem ter efeitos semelhantes (por exemplo, ampliar e reduzir deve ter transições inversas), mas as ações não relacionadas devem ter efeitos claramente distintos (por exemplo, aplicar zoom nunca deve ser confundido com a rotação).
-   **Mantenha os efeitos do mundo real realistas e consistentes.** Se você usar animações e transições realísticas, mantenha a experiência consistente com o mundo real. Os usuários nunca devem ficar surpresos, confusos ou enganar pelos resultados. E, para fins de consistência, não misture metáforas.
-   **Atribua animações inversas de ações inversas.** Fazer isso atende às expectativas dos usuários e simplifica o vocabulário. Por exemplo, se um painel aparecer deslizando em, remova-o, deslizando não com algum outro efeito.
-   **Torne as animações abrangente.** Os usuários devem ser capazes de entender rapidamente a finalidade de uma animação. É possível tornar uma animação muito pequena, muito breve (menos de 50 milissegundos) ou tão sutil que os usuários não podem compreender sua finalidade. Nesses casos, Reprojete para tornar o significado claro ou remover.

    **Incorreto:**

    ![captura de tela da animação na caixa de diálogo de exclusão ](images/vis-animations-image44.png)

    Neste exemplo, o efeito é tão pequeno e sutil que poucos usuários podem compreender sua finalidade. Melhor reprojetar ou remover.

### <a name="patterns"></a>Padrões

**Comentários de foco**

-   **Para aparecer responsivo, busque a animação de reprodução em 50 milissegundos de entrar ou sair do estado de foco.**
-   **Para aparecer rapidamente, torne a duração das animações de foco menos de 50 milissegundos.**
-   **Use um fade in/fade out do efeito de foco.** Isso torna os efeitos de foco claramente diferentes dos comentários de clique e seleção.

**Clique em comentários**

-   **Para aparecer responsivo, busque a animação de reprodução dentro de 50 milissegundos de evento de clique para baixo.** Eventos de clique para cima não precisam de clique em comentários.
-   **Para aparecer rapidamente, faça a duração das animações de clique com menos de 50 milissegundos.**
-   **Use um piscar de fundo ou efeito de intermitência.** Fazer isso torna os efeitos de clique claramente distintos dos comentários de foco e seleção. Como clicar em requer o passar o mouse, faça com que o clique de comentários uma adição suave aos comentários em foco.

**Comentários da seleção**

-   **Para aparecer responsivo, busque a animação de reprodução dentro de 50 milissegundos de seleção ou desmarcação.**
-   **Para aparecer rapidamente, torne a duração das animações de seleção menos de 50 milissegundos.**
-   **Use um efeito de retângulo de seleção de fade in/fade out.** Fazer isso torna a seleção claramente distinta dos comentários de mouse e clique.

**Comentários de progresso**

-   **Use um indicador de atividade quando uma ação não puder ser executada em um segundo.** Isso indica que o comando foi recebido.
-   **Use uma barra de progresso quando uma tarefa levar mais de cinco segundos.** Para obter mais diretrizes, consulte [barras de progresso](progress-bars.md).
-   **Use animações de comentários de progresso que ajudam os usuários a visualizar o efeito de tarefas de execução longa.** Evite animações de comentários de progresso desnecessárias se uma animação não comunicar algo útil, use uma barra de progresso.
-   **Ter Estados de conclusão e falha claramente identificáveis.** Os usuários devem ser capazes de determinar esses Estados finais rapidamente.
-   **Parar de mostrar o progresso quando a tarefa subjacente não estiver progredindo.** Os usuários precisam ser capazes de determinar se o andamento não está sendo feito e reagir de acordo.

**Atraidores**

-   **Use os atraidores com retentor.** A menos que as informações sejam urgentes, críticas ou provavelmente afetem o comportamento imediato do usuário, geralmente é melhor alterar o estado de forma inferível e permitir que os usuários descubram a alteração por conta própria. [Resolva distrações, não detectabilidade](/windows/desktop/uxguide/how-to-design-desktop-ux).

    ![captura de tela de ícones de status sem fio ](images/vis-animations-image45.png)

    Neste exemplo, o ícone da área de notificação de rede sem fio usa uma animação para problemas críticos, mas permite que os usuários descubram sinais fracos por conta própria.

-   **Escolha uma animação que desenha o nível certo de atenção.** As animações do atraitor devem desenhar apenas a atenção para si mesmos para atender a suas finalidades, mas não mais. Se o usuário precisar agir imediatamente, escolha um efeito que exija atenção, independentemente de onde o usuário esteja olhando. Para outras situações, consulte a seção [atraindo o nível certo de atenção](#attracting-the-right-level-of-attention) para obter a combinação certa de atenção, notabilidade e urgência.

    **Incorreto:**

    ![captura de tela do assistente do Office de clipe ](images/vis-animations-image46.png)

    Os assistentes de Microsoft Office atraíram atenção desnecessária a si mesmos.

-   **Se o usuário não responder, não repita a animação ou use animações contínuas.** Em vez disso, suponha que o usuário optou por não agir agora, mas pode agir mais tarde. Animações contínuas dificultam os usuários a se concentrarem em qualquer outra coisa.

**Animações de relação**

-   **Use animações de relação para mostrar onde os objetos vieram ou onde eles foram.**
-   **As animações de relação devem começar ou terminar com o objeto selecionado.** Não mostrar relações entre objetos com os quais o usuário não está interagindo no momento. Se os usuários perceberem, o que eles observarão é a distração.

**Ilustrações/visualizações**

-   **Use visualizações para mostrar o efeito de um comando sem que os usuários precisem executá-lo primeiro.** Usando as visualizações úteis, você pode melhorar a eficiência e a facilidade de aprendizado de seu programa e reduzir a necessidade de avaliação e erro.
-   **Use ilustrações e visualizações que tenham uma interpretação clara.** Eles têm pouco valor, se confuso.
-   **Jogue apenas uma ilustração por vez** para evitar sobrecarregar usuários. Se várias ilustrações simultâneas forem possíveis, use o mouse focalizado ou um botão reproduzir para permitir que os usuários indiquem seu interesse.
-   **Reproduza uma ilustração automaticamente se for a principal finalidade da janela ou da página.** Caso contrário, se for opcional, permita que os usuários o joguem quando estiverem prontos.
-   **Reproduzir animações na velocidade ideal**: não tão rápido eles são difíceis de entender, mas não tão lentos são entediantes a serem inspecionados.

**Aumento/redução de objeto**

-   **Não cortar conteúdo durante um redimensionamento.** Expanda contêineres antes de adicionar conteúdo. Remova o conteúdo antes de reduzir os contêineres.

    **Incorreto:**

    ![captura de tela da calculadora truncada ](images/vis-animations-image47.png)

    Neste exemplo, o conteúdo é recortado durante um redimensionamento.

**Mostrar/ocultar/alterar conteúdo**

-   **Exibir informações importantes estaticamente.** Os usuários não devem ter que acessar informações importantes por meio de divulgação progressiva.

**Controle ou custo mostrar/ocultar**

-   **Exibe controles importantes quando o usuário posiciona o ponteiro em qualquer lugar dentro da janela ou painel, ou, se houver tela inteira, ao mover o mouse.** Os usuários não devem ter de procurar esses controles, portanto, faça a descoberta certa.

    ![Figura mostrando como os controles de cursor são exibidos ](images/vis-animations-image48.png)

    Neste exemplo, o Windows Media Center exibe seus controles sempre que o ponteiro está sobre a janela.

-   **Exiba controles secundários ou controle capacidades quando o usuário posicionar o ponteiro ou próximo dos comandos.** Para facilitar a descoberta, torne o local óbvio e o destino grande.

    ![captura de tela de ponteiro revelando o comando secundário ](images/vis-animations-image49.png)

    Neste exemplo, o Windows Live Messenger exibe um comando secundário quando o ponteiro está próximo do canto superior direito.

**Transições de cena**

-   **Torne as transições de cena física consistentes com o mapeamento natural.** As pessoas lêem da esquerda para a direita em culturas ocidentais e diagramas hierárquicos fluem de cima para baixo. Consequentemente, avançar no tempo é indicado pelo movimento da esquerda para a direita. As seguintes transições de cena física têm mapeamento natural:



    | Transição                          | Significado                                     |
    |---------------------------|--------------------------------------|
    | Da esquerda<br/>      | Retroceder no fluxo de tarefas<br/>    |
    | Da direita<br/>     | Avançar no fluxo de tarefas<br/> |
    | Da parte superior<br/>       | Mover hierarquia de tarefas para cima<br/>    |
    | Da parte inferior<br/>    | Mover hierarquia de tarefas para baixo<br/>  |



 

-   **Se o seu programa reproduzir som, projete transições de cena e transições de áudio juntas.** Por exemplo, se uma cena esmaecer gradualmente, qualquer som também deverá desaparecer gradualmente. Não arruinar transições visuais suaves tendo transições de som abruptas. Para obter mais diretrizes de som, consulte [som](vis-sound.md).

**Manipulações diretas**

-   **Ao usar gestos físicos na interação (como a criação), crie a animação para parecer uma resposta natural ao gesto.** Vincule a causa de interação com o efeito de transição. Dê à animação características físicas do mundo real, como aceleração, desaceleração, impulso, resistência, peso, devolução e rotação.
-   **Para manter uma sensação direta, mantenha os pontos de contato de um objeto sob o ponteiro suavemente em toda a interação.** Qualquer atraso, resposta instável ou perda de contato destrói a percepção da manipulação direta. Os objetos nunca devem desaparecer enquanto estiverem sendo manipulados.

**Classificar, filtrar ou reordenar transições**

-   **Para alterações simples, mostre a transição inteira.** Os usuários poderão seguir facilmente a transição inteira. As alterações simples envolvem quatro itens ou menos.
-   **Para alterações complexas, enfatize o fim do movimento à medida que ele fica mais lento e deixe o preenchimento dos olhos no restante.** Isso faz com que o movimento se sinta muito mais responsivo e ordenado.

**Transições de desempenho**

-   **Considere a execução de transições lentas em dois ou três estágios para que sejam exibidas mais rapidamente e imediatamente interativas.** Use a seguinte ordem de composição quando apropriado:
    -   Quadro externo
    -   Tela de fundo
    -   Conteúdo inicial (usando uma representação temporária, se necessário)
    -   Controles primários (para que os usuários possam interagir imediatamente)
    -   Controles secundários e quaisquer elementos restantes da interface do usuário
    -   O conteúdo final (se uma representação temporária foi usada) usa transições como fades e slides para fazer com que a composição pareça suave, ordenada e refinada.

![captura de tela de mapa com foto e grade satélite ](images/vis-animations-image50.png)

Ao rolar no modo de exibição "olho de pássaro", o Bing Maps exibe uma tela de fundo de grade temporária. Isso permite que os usuários continuem a rolar imediatamente, bem antes que o conteúdo final seja renderizado.

**Animações de experiência especial**

-   **Reconsidere as telas de abertura animadas (bem como telas de abertura estáticas).** Muitas vezes, as telas de abertura apenas desenham o quanto tempo um programa leva para ser carregado e eles esgotam suas boas-vindas rapidamente. Embora as telas de abertura sejam aceitáveis se forem exibidas somente quando a interação do usuário não for possível, sempre que for prática, uma alternativa melhor é criar seu programa para que os usuários possam interagir com ele imediatamente, mesmo que ainda esteja carregando.
-   **Forneça um comando ignorar introdução se uma tela inicial animada levar mais de três segundos.** Clicar em qualquer lugar na tela inicial também deve descartá-la. Como alternativa, use uma versão curta da animação após um período inicial.

### <a name="performance"></a>Desempenho

-   **Não faça os usuários aguardarem as animações e as transições do programa.** Use breves animações e transições (menos de 200 milissegundos) sempre que for prático. Use animações mais rápidas (100 milissegundos) para operações mais frequentes. Crie animações mais longas (mais de um segundo geralmente os comentários de progresso, a ilustração e os padrões de experiência especiais) para que os usuários possam continuar a trabalhar enquanto estiverem em execução.
-   **Projete animações de execução longa para deixar claro para os usuários que eles podem interagir enquanto a animação está em execução.** Os usuários não tentarão continuar a trabalhar se as pistas visuais sugerirem que não podem.

    ![captura de tela de uma barra de progresso em uma barra de status ](images/vis-animations-image51.png)

    Neste exemplo do Windows Internet Explorer, a barra de progresso de chave baixa na barra de status sugere que os usuários não precisam aguardar a conclusão antes que possam interagir.

-   **Use animações leves para tarefas de uso intensivo de CPU.** Isso oferece poder de processamento completo para a tarefa. Além disso, os usuários não perceberão que a animação leve é o motivo pelo qual a tarefa tem uso intensivo de CPU.
-   **Não exibir um indicador de atividade durante uma animação ou transição.** Isso destrói o efeito. Crie animações e transições para que elas sejam capazes de iniciar imediatamente.
-   **Projete animações para degradar normalmente sempre que houver recursos do sistema insuficientes.** As animações podem diminuir com a existência de variações que exigem menos recursos (como comprimentos menores ou taxas de quadros inferiores) ou até mesmo não sendo executadas. Independentemente dos recursos disponíveis, verifique se as animações têm alta qualidade e se parecem com animações em vez de bugs de software.

    **Incorreto:**

    ![captura de tela do quadro de programa esmaecida na área de trabalho ](images/vis-animations-image52.png)

    Neste exemplo, a transição de restauração de janela é usada mesmo que não haja recursos suficientes do sistema para reproduzi-lo bem. Consequentemente, o quadro congelado parece ser um bug. Se os recursos não estiverem disponíveis, é melhor exibir apenas a janela sem uma transição.

### <a name="animation-characteristics"></a>Características da animação

Animações e transições bem projetadas geralmente têm estas características:

-   **Breve duração.** A maioria das animações deve estar entre 100 e 300 milissegundos, preferivelmente 1/6 segundo (167 milissegundos) ou 1/4 segundo (250 milissegundos). (Experiências especiais e comentários de progresso podem ser mais longos.) Use tempos de animação mais rápidos para operações mais frequentes. Geralmente, as animações mais longas levam mais tempo para serem concluídas, levam mais tempo para entender e se sentem lentas.
-   **Resposta.** As animações devem começar dentro de 50 milissegundos do evento de inicialização ou da ação do usuário. Os horários de início mais longos parecem não responder.
-   **Aceleração/desaceleração.** Para parecer natural, a maioria dos efeitos de animação precisa acelerar ao iniciar e desacelerar ao parar. Para parecer responsivo, Crie animações para começar rapidamente. Para parecer controlado, Crie animações para que as mídias sejam feitas no final. Embora isso se aplique a efeitos de movimento, ele também se aplica a qualquer efeito que sugira movimento, como zooms e até mesmo fades.

    ![Figura de um gráfico que mostra a velocidade reduzida ao longo do tempo ](images/vis-animations-image53.png)

    A maioria das animações deve ter inícios rápidos e inflexíveis para que haja uma sensação responsiva, embora controlada.

-   **Motion.** Animações que detratam o movimento em particular precisam acelerar e desacelerar, portanto, não use o movimento linear, a menos que a duração da animação seja muito curta. Os movimentos devem levar o caminho breve do início ao fim, sem sobreissor. O caminho de movimento completo nem sempre é necessário. Quando apropriado, enfatize o fim do movimento à medida que ele fica mais lento, e deixe o preenchimento dos olhos no restante. Isso faz com que o movimento se sinta muito mais responsivo e ordenado. Ao animar o movimento de vários objetos simultaneamente, dê a eles caminhos um pouco diferentes com intervalos ligeiramente diferentes para se sentirem mais naturais.
-   **Taxa de quadros.** A maioria das animações deve usar uma taxa de quadros de 20 quadros por segundo. Se a animação for para uma experiência especial ou estiver relacionada à finalidade principal do programa, considere usar uma taxa mais alta de 24 30 quadros por segundo para melhorar a suavidade e o realm.
-   **Escalonáve.** Crie animações para funcionar bem em todo o seu intervalo de uso pretendido. Por exemplo, as transições de página devem ser projetadas para funcionar para todos os tamanhos de página.
-   **Personalidade.** Crie animações para se sentir natural, subdued e eficiente em vez de artificial, estranho ou lento.

### <a name="animated-text"></a>Texto animado

-   Embora você possa exibir texto usando uma transição, **não anime continuamente o texto.** O texto animado geralmente é confuso e mais difícil de ler do que o texto estático. **Exceção**
    -   Você pode animar o texto em situações em que ele é tradicionalmente animado e fornecer uma alternativa acessível.
    -   Você poderá animar texto se a finalidade do texto for essencialmente decorativa.

![captura de tela da interface Zune criada de forma criativa ](images/vis-animations-image13.png)

Neste exemplo, o Zune anima o texto, mas sua finalidade é basicamente decorativo. Não há problema se os usuários não lerem atentamente o texto.

### <a name="reducing-power-consumption"></a>Reduzindo o consumo de energia

-   **Projete suas animações para reduzir o consumo de energia.** Quando projetado corretamente, as animações não devem aumentar significativamente o consumo de energia. Para reduzir o consumo de energia:
    -   **Parar animação quando a exibição estiver desativada.** A exibição pode estar desligada com a finalidade de economizar energia.
    -   **Não use animações de longa execução que não são iniciadas pelo usuário.** As animações que usam temporizadores periódicos de alta resolução reduzem a eficiência do gerenciamento de energia do processador. Além disso, certifique-se de desabilitar todos os temporizadores periódicos de alta resolução quando as animações forem concluídas.
    -   **Suspende todas as animações quando o sistema se torna ocioso.** O período de inatividade do usuário para se tornar ocioso é determinado pelas opções de energia no painel de controle.

### <a name="accessibility"></a>Acessibilidade

-   **Não use a animação como a única maneira de transmitir informações essenciais.** As animações devem comunicar informações que sejam úteis, mas não críticas, porque elas não estão acessíveis aos usuários com deficiências visuais.
-   **Verifique se as informações equivalentes estão disponíveis por outros meios,** como:

    -   **Por inspeção.** Os usuários podem determinar informações equivalentes examinando a tela ou os objetos envolvidos na animação.
    -   **Por uma simples interação.** Os usuários podem determinar informações equivalentes passando o mouse, clicando ou clicando duas vezes.

    ![captura de tela do Bing home page com pontos de acesso ](images/vis-animations-image54.png)

    O home page do Bing tem uma animação inicial que revela vários pontos de acesso. Os usuários também podem exibir os pontos de acesso movendo o cursor ao lado deles.

    Observe que "informações equivalentes" não significam informações idênticas. As informações podem estar em um formato diferente ou exigir dedução simples.

-   **Quando apropriado, defina o foco de entrada no objeto alterado durante uma transição.** Isso permite que as tecnologias assistenciais detectem onde a alteração ocorreu. Mas não altere o foco de entrada quando o usuário estiver usando o teclado.
-   **Não use animações ou transições que piscam ou redimensionam objetos rapidamente.** Alterações de tela rápidas e intermitentes podem causar problemas para pessoas com deficiências de captura e outros autoimunes neurological.
-   **Permitir que os usuários desliguem as animações e transições do programa.** Para dar suporte a essa capacidade, respeite a opção Desativar todas as animações desnecessárias na central de facilidade de acesso no Windows.

    **Desenvolvedores:** Você pode determinar se as animações estão habilitadas usando a API SystemParametersInfo.

-   **Criar tarefas, supondo que os usuários desligarão as animações do programa.** Certifique-se de que isso não interrompa o fluxo de tarefas de forma significativa.

Para obter mais diretrizes de acessibilidade, consulte [acessibilidade](inter-accessibility.md).

## <a name="documentation"></a>Documentação

-   Evite se referir a animações sempre que possível. Em vez disso, consulte o objeto que está sendo animado e, se necessário, o tipo de animação.
-   Não faça referência a transições, exceto na documentação técnica. Em vez disso, consulte o objeto em seu estado final ou inicial.
-   Se o usuário iniciar explicitamente uma animação, use a reprodução de verbo; caso contrário, use o uso de verbo para documentação técnica.

Exemplos:

-   Você saberá que um item precisa de sua atenção quando seu ícone começar a ser saltado.
-   Primeiro, selecione as fotos que você gostaria de imprimir (Observe que as fotos são ampliadas na seleção).
-   Use uma transição de esmaecimento cruzado para alterar o estado de um objeto sem problemas.

