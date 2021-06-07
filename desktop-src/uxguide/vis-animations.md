---
title: Animações e transições
description: O uso estratégico de animações e transições pode tornar seu programa mais fácil de entender, se sentir mais suave, mais natural e de maior qualidade e ser mais envolvente.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 546c1d0a59808b54f4ffa12fc7cd034554521ca3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444757"
---
# <a name="animations-and-transitions"></a>Animações e transições

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

O uso estratégico de animações e transições pode tornar seu programa mais fácil de entender, se sentir mais suave, mais natural e de maior qualidade e ser mais envolvente. Mas o uso gratuito de animações e transições pode tornar seu programa uma distração e até mesmo entediante.

Animações dão a aparência de movimento ou alteração ao longo do tempo. Use a animação para fazer comentários, visualizar o efeito de uma ação, mostrar a relação entre objetos, chamar a atenção para a alteração ou explicar uma tarefa visualmente.

![figura do teclado numérico com uma chave realçada ](images/vis-animations-image1.png)

O Microsoft Windows usa uma animação flash em segundo plano para dar comentários de que o objeto foi clicado.

As transições são animações usadas para manter os usuários orientados durante as alterações de estado da interface do usuário e manipulações de objeto e fazer com que essas alterações se sintam suaves em vez de jarring. As boas transições são naturais, geralmente dando a ilusão de que os usuários estão interagindo com objetos do mundo real.

![Captura de tela que mostra três tamanhos de weather weather.](images/vis-animations-image2.png)

Os Desktop Desktops do Windows usam transições suaves entre seus estados concisos e de detalhes.

Em geral, as melhores animações e transições são usadas para se comunicar com usuários não verbais e para tornar as alterações de estado mais naturais e menos perceptíveis. Por outro lado, os menos eficazes são gratuitos, já que eles não comunicam nada ou chamam atenção desnecessária. As animações são mais bem usadas como uma forma secundária de comunicação. Eles devem comunicar informações úteis, mas não críticas, e para serem acessíveis, os usuários devem ser capazes de determinar informações equivalentes por outros meios.

**Observação:** Diretrizes relacionadas à identidade visual [de](vis-sound.md) [software,](exper-branding.md)som [e acessibilidade](inter-accessibility.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere as perguntas a seguir.

### <a name="animations"></a>Animações

As condições a seguir se aplicam?

-   A animação comunica visualmente algo útil, como dar comentários, mostrar relações, causas e efeitos ou chamar a atenção para mudanças importantes.
-   Ver a animação não é essencial. Informações equivalentes podem ser obtidas de outra maneira. Os usuários podem não se beneficiar da animação se:
    -   Eles desligaram animações.
    -   A atenção deles está em outro lugar.
    -   Eles são visualmente prejudicados.
    -   A animação é obscurecida por outra janela.
    -   A animação não é tocada devido ao desempenho insuficiente do sistema.
-   A animação não afeta a produtividade do usuário. Ou:
    -   Isso ocorre rapidamente (200 milissegundos ou menos).
    -   Ele não interfere na interação ou pode ser interrompido.
    -   O usuário precisa aguardar mesmo assim.
-   A animação não afeta o fluxo do usuário.
    -   Ele está no centro da atenção do usuário ou chama a atenção para algo fora do centro da atenção que é importante ou útil na conclusão de uma tarefa.
    -   Ele é facilmente ignorável, não é desapregável nem entediante.
    -   Isso não se torna cansativa. Os usuários ainda o acharão apropriado e agradável mesmo após a exibição repetida.

Se sim, considere o uso de uma animação.

### <a name="transitions"></a>Transições

Um objeto ou um estado de alteração de cena e todas as condições acima para usar animações, bem como qualquer uma das condições a seguir, se aplicam?

-   A alteração de estado é conceitualmente confusa, confusa ou difícil de entender.
-   A alteração de estado é visualmente jarring, não tem continuidade ou suavidade ou flashes; ou aparece desinteressado, desbaixado ou de baixa qualidade, especialmente se envolver uma área de tela grande.
-   Usar uma transição faria a alteração de estado aparecer mais rapidamente.
-   A alteração de estado é o que vale a atenção especial do usuário.

Se sim, considere o uso de uma transição.

## <a name="design-concepts"></a>Conceitos de design

Animações e transições são uma maneira eficaz de comunicar informações visualmente que, de outra forma, exigiriam texto para explicar ou que poderiam ser perdidas pelos usuários.

**Incorreto:**

![captura de tela da caixa de diálogo com mensagem ](images/vis-animations-image3.png)

**Correto:**

![figura de animação se comunicando visualmente ](images/vis-animations-image4.png)

O uso de uma animação comunica as mesmas informações, mas de maneira natural e não discreta. Qual você prefere ver milhares de vezes?

**Animações e transições não têm que exigir atenção para serem bem-sucedidas.** Na verdade, elas geralmente são usadas para evitar chamar a atenção para a mecânica do programa que os usuários não precisam estar cientes. Muitas animações bem-sucedidas são tão naturais que os usuários nem estão cientes delas; em vez de os usuários perceberem apenas sua ausência. A frequência de ocorrência aumenta a necessidade de sutileza, portanto, salve os efeitos que exigem atenção para eventos pouco frequentes que realmenteam a atenção.

![captura de tela de todos os programas mudando para seta para voltar ](images/vis-animations-image5.png)

Uma menu Iniciar transição que evita chamar a atenção.

Além de tornar seu programa mais fácil de entender e se sentir mais suave, animações e transições bem projetadas são uma ótima maneira de adicionar personalidade, caractere e **estilo ao seu programa.** Eles podem tornar a experiência do usuário mais imersiva e envolvente, dando a ele uma sensação natural e real.

![figura mostrando como o foco afeta a cor do botão ](images/vis-animations-image6.png)

O Windows 7 realça os botões da barra de tarefas ao passar o mouse com base na posição atual do mouse e na cor do ícone do programa. Essa abordagem é visualmente atraente, mas sutil, transmitindo uma personalidade descarada.

**No entanto, animações e transições são mais eficazes e bem-vindas quando atendem a uma finalidade clara.** Eles devem ser usados para melhorar a usabilidade, a suavidade e o fluxo e a percepção da qualidade, sem prejudicar significativamente o desempenho.

Embora alguns tipos de animações sejam usados para chamar a atenção do usuário, certifique-se de que a atenção seja bem animada e meso de interromper o treinamento de pensamento do usuário. O olhar humano é sensível ao movimento, especialmente o movimento periférico. Pode ser difícil para os usuários se concentrarem quando há um botão de barra de tarefas piscando ou um ícone de área de notificação giratória. **Evite usar animações para interromper ou desviar os usuários ou chamar a atenção para coisas que não garantem a atenção do usuário.**

**Incorreto:**

![figura do botão de barra de tarefas realçada sem motivo ](images/vis-animations-image7.png)

Os programas não devem piscar o botão da barra de tarefas, a menos que os usuários devem fazer algo importante imediatamente. Nesse caso, a única coisa que o usuário precisa fazer é ativar o programa.

**Use animações e transições porque seu programa precisa delas, não simplesmente porque você pode.** E, para acessibilidade, não use animação como a única maneira de transmitir informações essenciais. Certifique-se de que os usuários possam obter informações equivalentes de uma maneira diferente.

### <a name="attributes-of-good-animations-and-transitions"></a>Atributos de boas animações e transições

As boas animações e transições atingem o equilíbrio certo entre esses atributos:

-   **São claramente proposital.** Boas animações estão lá porque precisam estar, seja para comunicar informações, fazer com que uma interação se sinta real ou chamar a atenção para algo importante. E animações propositivas são precisas; se uma animação mostra que uma tarefa está sendo feita, é porque a tarefa está sendo feita na verdade.

**Incorreto:**

![captura de tela do ícone de bateria e rótulo de carga total ](images/vis-animations-image8.png)

Neste exemplo, a animação mostra que uma bateria totalmente carregada está sendo carregada.

-   **Parece suave e contínua.** As boas animações removem suavemente as seams entre as alterações de estado da cena ou do elemento mostrando relações e fornecendo uma noção de local e contexto. A continuidade ajuda os usuários a entender como eles foram para onde estão e como voltar para o local em que eles vieram.

![captura de tela de três visualizações da janela da barra de tarefas ](images/vis-animations-image9.png)

A visualização da janela da barra de tarefas do Windows 7 se transforma para continuidade à medida que o usuário passa de um programa para outro.

-   **São realistas.** As boas animações simulam as propriedades físicas e o comportamento de um objeto do mundo real. Isso ajuda os usuários a prever e entender os resultados de suas interações. Você não precisa modelar o mundo real exatamente, mas se usar animações realistas, deverá mantê-las consistentes com o mundo real. Os usuários nunca devem se confundir ou se confundir com os resultados, especialmente com animações usadas para manipulação direta.

![figura do botão de barra de tarefas arrastado para a nova posição ](images/vis-animations-image10.png)

Neste exemplo, a animação "sair do caminho" usada pela barra de tarefas do Windows 7 parece mais realista do que um ponto de inserção estático.

-   **São autenticas.** Até mesmo objetos que não são encontrados no mundo real podem parecer naturais com base no comportamento do mundo real de um objeto diferente, mas relacionado. Essa metáfora só funcionará se a relação comunicar claramente a finalidade e o comportamento pretendido.

![captura de tela do efeito gerado por trás da janela movida ](images/vis-animations-image11.png)

Neste exemplo, a animação de "squeegee" da janela usada pelo Windows 7 parece autenticada porque é consistente com como as janelas de vidro podem se comportar no mundo real.

-   **Use o mapeamento natural.** Mapeamentos naturais são físicos ou culturais. Um mapeamento natural baseado culturalmente, por exemplo, pode começar com o fato de que, em culturas ocidental, as pessoas leem da esquerda para a direita. Consequentemente, para expressar uma sequência de tempo de objetos, o objeto do meio é atual, os objetos à esquerda são do passado e os objetos à direita estão no futuro. Avançar no tempo é indicado pelo movimento da esquerda para a direita.

![captura de tela da barra de progresso do player de mídia ](images/vis-animations-image12.png)

Neste exemplo, o controle Windows Media Player tem um mapeamento natural porque a reprodução move a posição da esquerda para a direita.

-   **Ter personalidade.** Animações bem escolhidas são ótimas maneiras de adicionar personalidade, caractere e estilo ao programa. Eles podem tornar a experiência do usuário mais imersiva e envolvente. Embora o tipo de animação determine o que ela se comunica, a maneira específica na qual a animação é executada mostra a personalidade do programa. Boas animações projetam a personalidade certa para seu programa, seja sério ou desalmado, ou em algum lugar entre eles.

![captura de tela da interface zune projetada de forma criadora ](images/vis-animations-image13.png)

Neste exemplo, o uso de Zune de texto animado e perspectiva dinâmica ajuda a moldar sua personalidade.

-   **Procure e sinta-se responsivo.** Boas animações não prejudicam a produtividade do usuário bloqueando os usuários de outras interações ou forçando os usuários a assistir. Não importa o quanto as animações do programa sejam naturais e envolvente, ninguém quer esperar por elas exclusivamente. Animações boas também parecem responsivas sem serem jarring, tendo um início rápido com uma aterrissagem suave. Animações responsivas também se beneficiam de comunicar sua finalidade rapidamente. Os usuários não devem ter que assistir a uma animação por um longo tempo apenas para descobrir o que ela está fazendo ou quando ela é feita. Para manipulação direta, animações responsivas são essenciais para manter uma sensação direta e envolvente do mundo real. Para se sentir direto, os pontos de contato de um objeto devem permanecer sob o ponteiro sem problemas durante a manipulação. Qualquer retardo, resposta mesiva ou perda de contato destrói a percepção da manipulação direta.

![figura do dedo tocando em uma tela sensível ao toque ](images/vis-animations-image14.png)

Neste exemplo, a transição de panorâmico de toque parece responsiva mantendo o ponto de contato sob o dedo do usuário durante a manipulação.

-   **Atrair o nível certo de atenção.** Animações boas geralmente são sutis e chamam apenas a atenção necessária para atender às suas finalidades. Como resultado, eles não são desalocar, entediantes, muito complexos, muito longos ou repetitivos. Elas não se tornam cansativas após exibições repetidas.

![captura de tela de realce de esbotão em nomes de arquivo ](images/vis-animations-image15.png)

Neste exemplo, a pesquisa do Windows chama temporariamente a atenção para palavras de pesquisa correspondentes e, em seguida, esmaece.

-   **Só será especial se for genuinamente especial.** A frequência aumenta a necessidade de sutileza, portanto, as interações comuns precisam de animações simples que comuniquem uma ideia simples de maneira simples. Reserve animações especiais e complexas para experiências especiais e pouco frequentes.

![captura de tela de quatro círculos se tornando logotipo do Windows ](images/vis-animations-image16.png)

Neste exemplo, o Windows usa uma animação de atenção na inicialização para fazer com que a experiência se sinta especial, mas essa animação seria inadequada em outro lugar.

Você saberá que atingiu o equilíbrio certo quando a experiência geral seria prejudicada se qualquer um desses atributos fosse removido.

### <a name="creating-an-animation-vocabulary"></a>Criando um vocabulário de animação

Boas animações são sobre comunicação visual eficaz e a consistência é crucial para sua eficácia. Se você usar uma transição específica, como efetuar o pushing de uma cena da direita para avançar para a próxima cena, essa deverá ser a única transição usada para essa finalidade e essa transição não deve ser usada para nenhuma outra finalidade. Atribuir significados diferentes à mesma animação prejudica sua capacidade de comunicação. Ao atribuir animações específicas e transições para significados específicos, você está criando um vocabulário de animação.

Esse problema se aplica a animações e transições que têm significado, não a aquelas genéricas às quais os usuários provavelmente não atribuem significado ou aquelas cuja finalidade deve ser imperceptível. Por exemplo, animações como esmaecem e efeitos especiais, como sempre, não têm nenhum significado específico, portanto, podem ser usadas livremente.

Um bom vocabulário atribui animações que modelam o comportamento físico e do mundo real de um objeto. Se você precisar atribuir uma animação a um objeto ou ação que não tenha um equivalente do mundo real, escolha uma animação que mostre como o objeto pode se comportar se ele for real.

![captura de tela de como o foco faz com que o logotipo do Windows brilhe ](images/vis-animations-image17.png)

Embora o menu Iniciar não seja um objeto do mundo real, seu efeito de foco se apaga como um objeto do mundo real quando ativado.

Cada animação em um vocabulário precisa ser claramente distinta. As animações deverão ter comportamentos semelhantes somente se suas ações associadas estão relacionadas da mesma forma. Por exemplo, as transições de movimento sugerem navegação, para que você possa usar transições de movimento de diferentes direções para indicar diferentes tipos de navegação.

Você saberá que suas animações e transições não estão se comunicando bem quando os usuários acharem os resultados confusos, surpreendentes ou inesperados. Em geral, é melhor atingir uma única finalidade bem do que várias finalidades não tão bem.

O ideal é que seu vocabulário de animação seja abrangente em todas as áreas do programa que precisam deles. Se apenas algumas interações têm animações naturais, isso chamará a atenção para aquelas que não têm.

Para saber mais sobre o vocabulário de animação do Windows, consulte a [seção Padrões de](#usage-patterns) uso deste artigo.

### <a name="designing-the-right-personality"></a>Projetando a personalidade certa

Embora o tipo de animação determine o que ela se comunica, a maneira específica na qual a animação é executada fala com a personalidade do programa e reforça sua marca.

A personalidade do programa deve refletir a natureza de suas tarefas e a personalidade de seus usuários, portanto, não é uma opção arbitrária. Em vez disso, uma personalidade bem projetada deve se sentir autenticada; nunca tente forçá-lo. A personalidade deve fazer uma conexão emocional com o usuário. Alguns fatores a considerar:

-   **Tarefas:** Sério ou divertido; opcional ou obrigatório.
-   **Consequências:** Sério ou menor.
-   **Custo:** Gratuito ou comprado; se comprado, com preços moderados ou caros.
-   **Foco do usuário:** Grupo relativamente estreito de usuários de destino ou público geral amplo.
-   **Ambiente do usuário:** Professional, casual ou home.
-   **Idade do usuário:** Mais novo ou mais antigo.
-   **Frequência de uso:** Frequente ou pouco frequente.

A combinação desses fatores ajuda a determinar uma personalidade apropriada para seu programa. Aqui estão algumas combinações adequadas para tipos comuns de programas:

**Aplicativos de produtividade**

Naturalmente, os aplicativos de produtividade devem se concentrar na produtividade. Embora algumas experiências especiais possam se destacar, a maioria das outras animações deve ter estas características:

-   Pequeno
-   Natural, realista
-   Sutil, desleixado
-   Rápido, eficiente
-   Reduzido

**Utilitários**

Os utilitários normalmente são usados brevemente, portanto, o uso da animação pode ser mais agressivo:

-   Realista, ilustrativo, autoexplicativo
-   Safe
-   Envolver

**Entretenimento, jogos**

Como o objetivo desses programas é envolver e atrair usuários, as animações e transições podem ser muito mais agressivas tendo estas características:

-   Grande (possivelmente se tornando uma parte integrante da experiência)
-   Artificial, ltda
-   Impactful, vibrante
-   Emocional, lúdico, cômico
-   Energético

Fazer uma conexão emocional é tão importante para programas de entretenimento que é aceitável distorcer algumas regras se isso ajudar a fazer com que os usuários se apantes com o programa. Por exemplo, será aceitável se uma animação ou transição se tornar cansativa após a centésimo vez se a maioria dos usuários não usar o programa com frequência.

Em geral, animações e transições pequenas, naturais, desaqueadas, eficientes, mas que são mais seguras são as mais seguras. As transições com essas características normalmente levam o caminho mais curto do início ao fim, começam rapidamente, terminam de forma suave e não se sobrecarram. Além disso, transições bem projetadas são projetadas para funcionar bem em toda a gama de distâncias em que elas serão usadas.

### <a name="animation-performance"></a>Desempenho da animação

Ao criar animações, certifique-se de que elas não afetem a capacidade dos usuários de usar seu programa com eficiência. Em geral, torne suas animações lentas o suficiente para atender às suas finalidades, mas rápido o suficiente para que elas não interfiram na capacidade de resposta, exijam muita atenção ou se tornem cansativas.

**Incorreto:**

![figura da página que se transforma da direita para a esquerda ](images/vis-animations-image18.png)

Embora essa página que ativa a animação tenha uma sensação envolvente e real, ela diminui a produtividade dos usuários, levando mais tempo para transformar páginas.

Transições breves (200 milissegundos ou menos) são um caso especial (especialmente quando geralmente funcionam com um atraso), pois os usuários estarão cientes de que precisam aguardar uma fração de segundo por eles. Os usuários estão dispostos a aguardar essas animações se:

-   A espera percebida é extremamente breve (200 milissegundos ou menos).
-   A transição faz com que a interação se sinta mais suave e natural.
-   A transição faz com que a interação se sinta mais responsiva.
-   Qualquer atraso ajuda a manter o usuário no controle da interação.

![figura de botões da barra de tarefas arrastados para a nova posição ](images/vis-animations-image19.png)

Os usuários aceitarão um breve atraso para a animação de reordenação do botão da barra de tarefas porque ela é muito breve e torna a interação mais natural.

Há três maneiras pelas quais as animações podem afetar negativamente o desempenho: velocidade, capacidade de resposta e percepção.

Para velocidade, algumas animações são veneers visuais em tarefas com uso intensivo de CPU, portanto, a última coisa que você deve fazer é tornar essas tarefas mais lentas com animações com uso intensivo de CPU. As animações com maior uso de CPU ("animações pesadas) tendem a:

-   Envolva muitos elementos que se movem independentemente.
-   Reproduzir por uma longa duração ou distância.
-   Envolva uma grande quantidade de espaço na tela.
-   São matematicamente intensivas.

Animações com menos impacto sobre o desempenho:

-   Envolver um único objeto.
-   Reproduzir por uma curta duração ou distância.
-   Envolva uma pequena quantidade de espaço na tela.
-   Não são matematicamente intensivos.

Para garantir um bom desempenho, animações pesadas devem ser usadas apenas para tarefas que não têm uso intensivo de CPU, enquanto animações leves podem ser usadas em qualquer lugar.

Para capacidade de resposta, a maioria das animações e transições deve ser projetada para que os usuários possam interagir enquanto a animação está em execução. A menos que uma animação faça parte de um processo, faça com que ela seja independente da interação principal do usuário e permita que os usuários a interrompam.

Uma animação pode não afetar negativamente o desempenho de uma tarefa na realidade, mas os usuários podem ter a percepção de que ela tem. Por exemplo, não use uma animação que pareça pesada para uma tarefa lenta e com uso intensivo de CPU, mesmo se não prejudicar o desempenho, porque os usuários podem concluir que a animação é o motivo pelo qual a tarefa está lenta. **Se algo parecer lento, será lento, portanto, é melhor usar animações que pareçam simples, leves e rápidas.** O uso de animações com inícios de snappy para tarefas com uso intensivo de CPU ajuda.

**Arriscado:**

![captura de tela da caixa de diálogo copiar com a barra de progresso ](images/vis-animations-image20.png)

Embora a animação na caixa de diálogo de cópia de arquivo do Windows não prejudicar o desempenho da cópia de arquivo, ela corre o risco de fazer os usuários pensarem que sim.

**Também arriscado:**

![captura de tela do progresso exibida na barra de endereços ](images/vis-animations-image21.png)

Neste exemplo, a animação de progresso de aparência lenta na barra Windows Explorer endereços faz com que algumas tarefas pareçam lentamente lentas.

Animações e transições não terão valor se sua qualidade for tão ruim que tornarão a experiência menos suave e menos envolvente. Para manter sua qualidade, as animações devem ser projetadas para degradar normalmente sempre que recursos suficientes do sistema não estão disponíveis. As animações podem ser degradadas com variações que exigem menos recursos (como comprimentos mais curtos ou taxas de quadros menores) ou até mesmo não em execução. Independentemente dos recursos disponíveis, certifique-se de que as animações tenham alta qualidade e se pareçam com animações em vez de bugs de software.

Por fim, se os usuários acreditarem que as animações e transições do seu programa são prejudicadas de sua produtividade, há uma boa chance de alguns usuários quererem desativar. Para dar suporte a essa capacidade, respeita a opção para **Desativar todas as animações desnecessárias encontradas** no Windows Central de Facilidade de Acesso.

### <a name="attracting-the-right-level-of-attention"></a>Atraindo o nível certo de atenção

Embora apenas alguns tipos de animações e transições sejam especificamente projetados para atrair a atenção do usuário, eles devem ser projetados para atrair o nível certo de atenção para atender bem à finalidade. Quais são as diferentes maneiras de chamar a atenção e como escolher a correta?

**Efeitos de animação**

Diferentes efeitos de animação atraindo diferentes níveis de atenção. A lista a seguir resume os métodos mais comuns, começando com a maior atenção:

-   **Piscando rapidamente.** Exige atenção imediata. Pode quebrar a concentração dos usuários, independentemente do local em que o flash está ocorrendo.
-   **Piscar moderadamente.** Mesmo, mas exige menos atenção com menor frequência.
-   **Saltando.** Perceptível na visão periférico e relativamente exigente por natureza. É provável que os usuários observem, mas podem continuar se concentrando em outro lugar somente se a duração for curta.
-   **Movimento.** Perceptível na visão periférico, mas não exigindo. No entanto, movimentos complexos ou 3D chamam mais atenção do que movimentos simples ou 2D. É provável que os usuários observem, mas podem continuar se concentrando em outro lugar.
-   **Pulsação moderada.** Perceptível, mas não desalocar a visão periférico. Os usuários podem continuar se concentrando em outro lugar. Pode pulsar brilho, cores e tamanhos.
-   **Pulsing/slow lento.** Perceptível, mas sutil. Chama mais atenção do que um efeito estático, mas os usuários podem não perceber a animação, a menos que já estão procurando.
-   **Desaparecer.** Ainda menos perceptível. Chama mais atenção do que um efeito estático, mas os usuários podem não perceber a animação, a menos que já estão procurando.
-   **Realça-se/ressaldo estático.** Perceptível se os usuários optarem por procurar, mas não exigirem atenção se ele estiver em outro lugar.
-   **Ambiente/natural.** Propositalmente não é perceptível tendo uma aparência natural e real.

Para determinar a abordagem certa para seu programa ou recurso, considere como esses fatores se relacionam com os cenários do recurso.

Por exemplo, suponha que você está projetando um programa de mensagens instantâneas e alguém acabou de enviar uma mensagem ao usuário. Esse cenário exige a atenção do usuário, ele deve ser perceptível em qualquer lugar e, geralmente, o usuário deseja responder rapidamente. Esse cenário sugere que uma animação intermitente moderada seria uma boa opção. Por outro lado, suponha que você queira informar aos usuários que um trabalho de impressão foi concluído. Os usuários devem ser capazes de continuar a se concentrar e trabalhar de maneira produtiva em outro lugar, e isso será aceitável se os usuários não perceberem. Esse cenário sugere que a pulsação moderada a lenta ou a desiluminação seria uma boa opção.

**Duration**

A duração apropriada para uma animação de atenção depende do cenário e do tipo específico de animação usado. Quanto mais atenção um efeito de animação exigir, menor será a duração. Embora efeitos muito sutis que exijam pouca atenção (como pulsões lentas) possam ser desempenhados indefinidamente, os efeitos que exigem atenção só devem ser interpretados entre 1 e 3 segundos. Qualquer coisa mais longa corre o risco de tornar a animação sobrecarregante e entediante.

![captura de tela do botão da barra de tarefas realçada ](images/vis-animations-image22.png)

No Windows 7, a barra de tarefas pisca para atenção por apenas um segundo. Por mais tempo seria entediante.

**Decaimento de efeito**

Você deve criar animações de atenção com base na suposição de que, se os usuários não responderem imediatamente, é porque eles estão ocupados fazendo outra coisa e não querem ser interrompidos. Portanto, sua meta deve ser chamar a atenção sem exigi-la.

Para obter o equilíbrio certo de chamar a atenção sem exigi-la, decaa a intensidade de um efeito ao longo do tempo. Por exemplo, para atrair a atenção, você pode tornar o efeito inicialmente forte, mas retardar o efeito rapidamente. Ao fazer isso, a potência atrativa é basicamente determinada pelo efeito inicial, mas a impressão geral do usuário é determinada principalmente pelo seu término.

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



|   Uso                                                                                                               |   Descrição                                     |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentários de foco**<br/> para mostrar onde está o ponto de interação. <br/>                                | Indica que o ponto de interação está ativo. o foco pode ser mostrado também por meio de um efeito estático.<br/> vocabulário do Windows: Exibir efeito de foco (retângulo delimitador, realce, ampliação) com um efeito de fade in/fade out para suavidade. <br/> ![captura de tela de uma das seis tampas do álbum realçadas ](images/vis-animations-image24.png)<br/> No player de mídia digital do Zune, o álbum cobre realce e adicione controles de reprodução ao focalizar.<br/>                                                                                                                                                                                                                 |
| **Clique em comentários**<br/> para mostrar que um objeto clicável é responsivo e recebeu um clique. <br/>    | Indica que um objeto foi clicado.<br/> vocabulário do Windows: plano de fundo do objeto flash no evento clique para baixo. para mostrar contato de toque, use um efeito de ondulação. <br/> ![foto do dedo na tela sensível ao toque mostrando as copiadas ](images/vis-animations-image25.png)<br/> O Touch exibe uma animação ondulada para que o usuário saiba que a interação foi reconhecida.<br/>                                                                                                                                                                                                                                                                                                         |
| **Comentários da seleção**<br/> para mostrar que um objeto está selecionado. <br/>                                | Indica que um objeto está selecionado. a seleção também pode ser mostrada por meio de um efeito estático.<br/> vocabulário do Windows: desenhar retângulo de seleção com um efeito de fade in/fade out para suavização. <br/> ![Figura de uma capa de álbum clicada e selecionada ](images/vis-animations-image26.png)<br/> No Zune, o álbum cobre piscar de clique e, em seguida, obter um retângulo de seleção na seleção.<br/>                                                                                                                                                                                                                                                                      |
| **Comentários de progresso**<br/> para mostrar que uma tarefa está sendo executada. <br/>                             | Os comentários de progresso indicam que uma tarefa está progredindo, normalmente com indicadores de atividade, barras de progresso ou animações que ilustram a tarefa. Os comentários de progresso de destérmino mostram aproximadamente quanto da tarefa foi feita e o quanto resta, enquanto o progresso indeterminado apenas indica que a tarefa está sendo feita.<br/> vocabulário do Windows: indicadores de atividade de rotação, barras de progresso, planos de fundo de progresso, animações de ilustração. <br/> ![captura de tela da caixa de diálogo com texto ' entrando ' ](images/vis-animations-image27.png)<br/> Neste exemplo, o Windows Live Messenger exibe os comentários de progresso indeterminados durante a entrada.<br/> |
| **Atraidor**<br/> para mostrar que algo precisa da atenção do usuário. <br/>                          | Atraia o nível certo de atenção quando objetos significativos são criados ou precisam de atenção (geralmente devido a alterações) ou eventos importantes ou urgentes acontecem. consulte [atraindo o nível certo de atenção](#attracting-the-right-level-of-attention) para técnicas de design.<br/> vocabulário do Windows: piscando, movendo, Pulsing, brilhando, gleam. <br/> ![captura de tela demonstrando animação de barra de ferramentas ](images/vis-animations-image28.png)<br/> A barra de ferramentas do Windows Live anima na primeira aparência para deixá-la óbvia onde está.<br/>                                                                                                                                 |
| **Relação**<br/> para mostrar a relação entre objetos ou causalidade em efeitos. <br/>        | Mostrar relações, especialmente quando a relação pode não ser compreendida ou esperada, de uma forma que não seja confuso ou confusa.<br/> vocabulário do Windows: metamorfose, transporte, alteração física, como inverter, aumentando de uma fonte de ponto, reduzindo para um destino de ponto. <br/> ![captura de tela da caixa de diálogo de calibragem de cor](images/vis-animations-image29.png)<br/> Neste exemplo, a animação mostra a relação entre a configuração gama e seu efeito na exibição.<br/>                                                                                                                                                    |
| **Ilustração/visualização**<br/> para explicar visualmente um conceito, uma tarefa ou o efeito de um comando. <br/> | Uma animação ou vídeo que explica um conceito ou como algo funciona visualmente, seja para complementar ou substituir uma explicação textual. Isso permite que os usuários executem tarefas ou escolham comandos com eficiência e confiança. <br/> ![captura de tela de erro de ortografia de correção de caneta ](images/vis-animations-image30.png)<br/> Neste exemplo, os comandos "Mostre-me" do painel de entrada do Tablet PC usam ilustrações para mostrar como corrigir, excluir, dividir e unir.<br/>                                                                                                                                                                                                        |



 

As transições têm vários padrões de uso:



|      Uso                                                                                                                                                                                                      |    Descrição                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Objeto aumentar/reduzir/aparecer**<br/> para alterar o tamanho ou o estado de um objeto sem problemas. <br/>                                                                                                         | Alterações de objeto entre os Estados, possivelmente ao mover. a transição mantém os usuários orientados durante as alterações.<br/> vocabulário do Windows: Morph, altere o tamanho, os slides de objeto para dentro ou para fora. <br/> ![captura de tela de três tamanhos de gadgets meteorológicos ](images/vis-animations-image31.png)<br/> Neste exemplo, o gadget meteorológico é metamorfose de seu estado conciso para exibir sua caixa de diálogo opções.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Mostrar/ocultar/alterar conteúdo**<br/> para mostrar, ocultar ou alterar o conteúdo sem problemas, normalmente para divulgação progressiva. <br/>                                                                       | As reformulações do interior da janela para exibir conteúdo mais, menor ou diferente. a transição mantém os usuários orientados durante as alterações.<br/> vocabulário do Windows: painel de slides para dentro ou para fora. janelas de submenu fade in e out. um conteúdo diferente desaparece ou se acumula. <br/> ![captura de tela de três tamanhos de calculadora ](images/vis-animations-image32.png)<br/> A calculadora do Windows tem uma transição suave entre modos de exibição.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Controle ou custo mostrar/ocultar**<br/> para mostrar ou ocultar de forma suave os controles ou suas capacidades na movimentação do mouse ou do rato a fim de simplificar a aparência normal do Visual. <br/>                | Exibe controles quando os usuários estão passando o ponteiro sobre uma área de comando ou exibem capacidades quando os usuários estão focalizando um controle. passar o mouse sobre essas áreas indica que o usuário pretende interagir. as acessível podem ocultar se o ponteiro se tornar estacionário. <br/> ![captura de tela de controles esbotados antes de passar o mouse ](images/vis-animations-image33.png)<br/> Neste exemplo, os controles Windows Media Player esmaecem ao passar o mouse quando estão no modo de tela inteira.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Transições de cena**<br/> para fazer uma transição de cena suave e perfeita para evitar atenção. <br/>                                                                                   | As alterações de cena abruptas podem ser um jarring, especialmente para áreas de tela grande, portanto, use transições de cena para criar suavidade e continuidade e fornecer contexto. as transições de cena são projetadas para serem naturais e com pouca chave, a fim de evitar chamar a atenção para o processo de transição em si.<br/> vocabulário do Windows: esmaecer dentro/fora; cross fade; deslizando para dentro/para a esquerda, para fora/para a direita, para cima, para baixo; pushes e covers. <br/> ![captura de tela de uma foto esbotando em outra ](images/vis-animations-image34.png)<br/> Neste exemplo, o papel de parede da área de trabalho do Windows esmaece entre imagens para fazer com que a transição se sinta suave e controlada.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Transições de cena especiais**<br/> para chamar a atenção para uma alteração de cena para torná-la especial ou refocar a atenção do usuário. <br/>                                                               | Embora a maioria das transições de cena não deva chamar a atenção para o processo de transição, algumas são projetadas para quebrar o fluxo e chamar a atenção para enfatizar que algo diferente está prestes a acontecer. para chamar a atenção, as transições de cena especiais são projetadas para serem incomuns e ter alto impacto visual. <br/> ![captura de tela do slide de transição que chama a atenção ](images/vis-animations-image35.png)<br/> Neste exemplo, o PowerPoint usa transições de atenção para desenhar o público-alvo para a alteração.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulações diretas**<br/> para mostrar o efeito de manipulações diretas (como mover, rolar/panorcar, girar e ampliar). <br/>                                                                   | A transição mostra o efeito da manipulação em tempo real. O efeito deve ser suave, contínuo e consistente com o mundo real. mover e girar pode não ser contínuo em alguns locais para indicar restrições ou opções preferenciais prováveis. O zoom torna o conteúdo maior ou menor, possivelmente alterando o nível de detalhes de acordo. <br/> ![captura de tela de três tamanhos de lupa ](images/vis-animations-image36.png)<br/> Neste exemplo, a Lupa amplia suavemente entre níveis.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipulações diretas incorretas**<br/> para indicar que uma manipulação direta (como movimentação, rolagem/panoragem) foi tentada, mas não pôde ser feita. <br/>                                           | A transição mostra a manipulação que está sendo tentada, mas reverte de volta para o estado original. geralmente, o efeito parece que a manipulação não pode ser executada devido a alguma restrição física do mundo real. essas animações são usadas em vez de mensagens de erro baseadas em texto, o que interromperia a sensação do mundo real da manipulação.<br/> vocabulário do Windows: ressalto <br/> ![figura de animação se comunicando visualmente ](images/vis-animations-image4.png)<br/> Neste exemplo, o documento é ressalto para mostrar que o usuário atingiu o final.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Classificar, filtrar, reordenar transições**<br/> para indicar que a apresentação ou o conteúdo de uma coleção de itens foi alterado. <br/>                                                            | A transição mostra (ou para alterações complexas, sugere) o efeito da alteração. <br/> ![captura de tela de câmeras de linhas com três removidos ](images/vis-animations-image37.png)<br/> ![captura de tela semelhante com câmeras diferentes removidas ](images/vis-animations-image38.png)<br/> ![captura de tela semelhante com outras câmeras removidas ](images/vis-animations-image39.png)<br/> neste exemplo, a pesquisa visual do Bing usa uma transição de filtro.<br/> ![captura de tela da capa do álbum alterando sua aparência ](images/vis-animations-image40.png)<br/> Neste exemplo, Windows Media Center uma transição de reordenar como uma experiência especial enquanto uma música está tocando.<br/>                                                                                                                                                                                                                                                                                   |
| **Transições de desempenho**<br/> para fazer com que uma ação pareça acontecer mais rapidamente. <br/>                                                                                                              | Embora qualquer transição tenha o potencial de fazer com que uma ação pareça acontecer mais rapidamente, a principal finalidade dessas transições é melhorar a percepção de desempenho e capacidade de resposta. uma boa técnica é mostrar a tarefa que está sendo executada em etapas deliberadas. Por outro lado, atrasar a ação, renderizar os resultados de maneira hafafatória ou usar um indicador de atividade será lento.<br/> vocabulário do Windows: execute a ação em estágios, com transições suaves entre os estágios. <br/> ![captura de tela da lista de saltos adicionando destinos ](images/vis-animations-image41.png)<br/> Neste exemplo, uma barra de Lista de Atalhos exibe imediatamente os itens padrão e, em seguida, desliza para exibir os destinos quando a lista estiver pronta. Fazer isso revela o tempo necessário para criar a lista. Por outro lado, atrasar a exibição inicial pareceria sem resposta e exibir uma lista incompleta ou comentários de progresso seria muito mais lento.<br/> |
| **Experiências especiais**<br/> para envolver e atrair os usuários [](glossary.md) durante experiências especiais e pouco frequentes que são importantes para seu programa e que tenham a atenção total do usuário. <br/>    | Embora qualquer transição tenha o potencial de ser uma experiência especial, essas transições são mais bem reservadas para experiências pouco frequentes que são realmente especiais para seu programa. as transições personalizadas são usadas para dar uma sensação especial. identidade visual e personalidade geralmente são elementos de design importantes. ao contrário de outros padrões, as experiências especiais podem exigir atenção, ser pesadas e exigir que os usuários aguardem um momento. consequentemente, essas transições se desessam rapidamente se superutilizadas porque a experiência não é mais especial. <br/> ![captura de tela do logotipo do Windows mudando para nova tela ](images/vis-animations-image42.png)<br/> Neste exemplo, o Windows Media Center exibe uma animação durante o carregamento para envolver imediatamente os usuários.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Diretrizes

### <a name="effective-communication"></a>Comunicação efetiva

-   **Defina e use um vocabulário de** animação para garantir que suas animações e transições tenham um significado consistente e use-o de forma consistente em todo o programa. A maioria dos vocabulários deve incluir entradas para aparência de cena e objeto, navegação, interação básica (passar o mouse, selecionar, clicar), manipulação de objetos e interação (mover, soltar, ressizing, rolar, panorâmico, ampliar, girar, filtrar) e chamar a atenção. O significado consistente é crucial para a comunicação eficaz.
-   **Sempre que for prático, use o vocabulário de animação do Windows.** Embora seu programa possa ter um público-alvo diferente e necessidades diferentes, geralmente os benefícios da consistência e da familiaridade superam os benefícios de serem diferentes. Se o vocabulário do programa deve ser diferente, use os mesmos tipos de animação básicos que o Windows, mas dê a eles a personalidade certa para seu programa.
-   **Não atribua significados específicos a animações genéricas e transições em um vocabulário de animação.** Transições genéricas, como esmaeceções e efeitos especiais, como sempre, não têm nenhum significado específico (além de aparecer ou desaparecer), para que possam ser usadas livremente.

    **Incorreto:**

    ![captura de tela de uma caixa de diálogo esbotando em outra ](images/vis-animations-image43.png)

    Neste exemplo, um esmaeçando cruzado é usado incorretamente para navegar até o próximo item. Como esmaeces cruzados não têm nenhum significado específico, essa transição não fornece contexto.

-   **Tornar as entradas de vocabulário claramente distintas.** Ações relacionadas podem ter efeitos semelhantes (por exemplo, ampliar e reduzir deve ter transições inversas), mas ações não relacionadas devem ter efeitos claramente distintos (por exemplo, o zoom nunca deve ser confundido com a rotação).
-   **Mantenha os efeitos reais realistas e consistentes.** Se você usar animações e transições realistas, mantenha a experiência consistente com o mundo real. Os usuários nunca devem se confundir, confundir ou confundir com os resultados. E, para consistência, não misture as metáforas.
-   **Dê animações inversas de ações inversas.** Isso atende às expectativas do usuário e simplifica o vocabulário. Por exemplo, se um painel aparecer deslizando, remova-o deslizando e não com algum outro efeito.
-   **Tornar animações compreensíveis.** Os usuários devem ser capazes de entender rapidamente a finalidade de uma animação. É possível tornar uma animação muito pequena, muito breve (menos de 50 milissegundos) ou tão sutil que os usuários não conseguem compreender sua finalidade. Nesses casos, reprojete para deixar o significado claro ou remova.

    **Incorreto:**

    ![captura de tela da animação na caixa de diálogo de exclusão ](images/vis-animations-image44.png)

    Neste exemplo, o efeito é tão pequeno e sutil que poucos usuários podem compreender sua finalidade. É melhor reprojetar ou remover.

### <a name="patterns"></a>Padrões

**Comentários sobre o foco**

-   **Para parecer responsivo, busque reproduzir animação em 50 milissegundos de entrada ou saída do estado de foco.**
-   **Para parecer rápido, faça com que a duração das animações de foco seja inferior a 50 milissegundos.**
-   **Use um esmaeçando dentro/esmaecer do efeito de foco.** Isso torna os efeitos de foco claramente distintos dos comentários de clique e seleção.

**Clique em comentários**

-   **Para parecer responsivo, busque reproduzir animação em até 50 milissegundos do evento de clique para baixo.** Eventos de clique para cima não precisam de clique em comentários.
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

-   **Para alterações simples, mostre a transição inteira.** Os usuários poderão seguir facilmente a transição inteira. Alterações simples envolvem quatro itens ou menos.
-   **Para alterações complexas, enfatiza o final do movimento conforme ele fica mais lento e deixe o olho preencher o restante.** Fazer isso faz com que o movimento se sinta muito mais responsivo e pedido.

**Transições de desempenho**

-   **Considere executar transições lentas em dois ou três estágios para torná-las mais rápidas e interativas imediatamente.** Use a seguinte ordem de composição quando apropriado:
    -   Quadro externo
    -   Segundo plano
    -   Conteúdo inicial (usando uma representação temporária, se necessário)
    -   Controles primários (para que os usuários possam interagir imediatamente)
    -   Controles secundários e quaisquer elementos de interface do usuário restantes
    -   Conteúdo final (se uma representação temporária tiver sido usada) Use transições como esmaece e desliza para fazer com que a composição pareça suave, ordem e refinada.

![captura de tela do mapa com foto e grade satélite ](images/vis-animations-image50.png)

Ao rolar na exibição "Olho do pássaro", os mapas do Bing exibem uma tela de fundo de grade temporária. Isso permite que os usuários continuem a rolar imediatamente, bem antes que o conteúdo final seja renderizado.

**Animações de experiência especial**

-   **Releição de telas insotivas animadas (bem como telas invasões estáticas).** Geralmente, as telas insalvas apenas chamam a atenção para quanto tempo um programa leva para carregar e desempatam suas boas-vindas rapidamente. Embora as telas invasões sejam aceitáveis se elas só são exibidas quando a interação do usuário não é possível, sempre que uma alternativa melhor é criar seu programa para que os usuários possam interagir com ele imediatamente, mesmo enquanto ele ainda estiver carregando.
-   **Forneça um comando Ignorar Introdução se uma tela inicial animada levar mais de três segundos.** Clicar em qualquer lugar na tela inicial também deve descartá-lo. Como alternativa, use uma versão curta da animação após um período inicial.

### <a name="performance"></a>Desempenho

-   **Não faça com que os usuários aguardem as animações e transições do programa.** Use animações e transições breves (menos de 200 milissegundos) sempre que for prático. Use animações mais rápidas (100 milissegundos) para operações mais frequentes. Projete animações mais longas (mais de um segundo geralmente os comentários de progresso, a ilustração e os padrões de experiência especiais) para que os usuários possam continuar a trabalhar enquanto estão em execução.
-   **Projete animações de execução longa para deixar claro aos usuários que eles podem interagir enquanto a animação está em execução.** Os usuários não tentarão continuar a trabalhar se as pistas visuais sugerirem que não podem.

    ![captura de tela de uma barra de progresso em uma barra de status ](images/vis-animations-image51.png)

    Neste exemplo do Windows Internet Explorer, a barra de progresso de baixa chave na barra de status sugere que os usuários não precisam aguardar a conclusão antes que possam interagir.

-   **Use animações leves para tarefas com uso intensivo de CPU.** Isso fornece potência total de processamento para a tarefa. Além disso, os usuários não perceberão que a animação leve é o motivo pelo qual a tarefa faz uso intensivo de CPU.
-   **Não exibir um indicador de atividade durante uma animação ou transição.** Fazer isso destrói o efeito. Projete animações e transições para que elas sejam capazes de começar imediatamente.
-   **Projete animações para degradar normalmente sempre que houver recursos insuficientes do sistema.** As animações podem ser degradadas com variações que exigem menos recursos (como comprimentos mais curtos ou taxas de quadros menores) ou até mesmo não em execução. Independentemente dos recursos disponíveis, certifique-se de que as animações tenham alta qualidade e se pareçam com animações em vez de bugs de software.

    **Incorreto:**

    ![captura de tela do quadro de programa esbotado na área de trabalho ](images/vis-animations-image52.png)

    Neste exemplo, a transição de restauração de janela é usada mesmo que não haja recursos de sistema suficientes para reproduzi-la bem. Consequentemente, o quadro congelado parece ser um bug. Se os recursos não estão disponíveis, é melhor apenas exibir a janela sem uma transição.

### <a name="animation-characteristics"></a>Características de animação

Animações e transições bem projetadas geralmente têm estas características:

-   **Breve duração.** A maioria das animações deve estar entre 100 e 300 milissegundos, preferencialmente 1/6 segundo (167 milissegundos) ou 1/4 segundo (250 milissegundos). (Experiências especiais e comentários de progresso podem ser mais longos.) Use tempos de animação mais rápidos para operações mais frequentes. Em geral, animações mais longas levam mais tempo para ser concluídas, levam mais tempo para entender e se sentir lentas.
-   **Resposta.** As animações devem começar dentro de 50 milissegundos do evento de inicialização ou da ação do usuário. Tempos de início mais longos não são responsivos.
-   **Aceleração/desaceleração.** Para parecer natural, a maioria dos efeitos de animação precisa ser acelerada ao iniciar e desacelerar ao parar. Para parecer responsivo, projete animações para ter inícios rápidos. Para parecer controlado, projete animações para ter aterrissagem suaves no final. Embora isso se aplique a efeitos de movimento, ele também se aplica a qualquer efeito que sugira movimento, como zooms e até mesmo esmaeça.

    ![figura de um grafo mostrando a velocidade reduzida ao longo do tempo ](images/vis-animations-image53.png)

    A maioria das animações deve ter inícios rápidos e terminações suaves para ter uma sensação responsiva, mas controlada.

-   **Movimento.** Animações que reagem ao movimento em particular precisam ser aceleradas e desaceleradas, portanto, não use o movimento linear, a menos que a duração da animação seja muito curta. Os movimentos devem seguir o caminho de shorts do início ao fim, sem sobrecarr. O caminho de movimento completo nem sempre é necessário. Quando apropriado, enfatizar o final do movimento conforme ele fica mais lento e deixar o olho preencher o restante. Fazer isso faz com que o movimento se sinta muito mais responsivo e pedido. Ao animar o movimento de vários objetos simultaneamente, dê a eles caminhos ligeiramente diferentes com tempos ligeiramente diferentes para se sentir mais natural.
-   **Taxa de quadros.** A maioria das animações deve usar uma taxa de quadros de 20 quadros por segundo. Se a animação for para uma experiência especial ou estiver relacionada à finalidade principal do programa, considere usar uma taxa mais alta de 24 30 quadros por segundo para melhorar a suavidade e realismo.
-   **Escala.** Projete animações para funcionar bem em toda a gama de uso pretendido. Por exemplo, as transições de página devem ser projetadas para funcionar para todos os tamanhos de página.
-   **Personalidade.** Projete animações para se sentir natural, desalocarada e eficiente em vez de artificial, elegante ou lenta.

### <a name="animated-text"></a>Texto animado

-   Embora você possa exibir texto usando uma transição, **não anima continuamente o texto.** O texto animado geralmente é uma distração e é mais difícil de ler do que o texto estático. **Exceções:**
    -   Você pode animar o texto em situações em que ele é animado tradicionalmente e fornece uma alternativa acessível.
    -   Você poderá animar o texto se a finalidade do texto for principalmente decorativa.

![captura de tela da interface zune projetada de forma criadora ](images/vis-animations-image13.png)

Neste exemplo, Zune anima o texto, mas sua finalidade é principalmente decorativa. Não haverá um problema se os usuários não lerem o texto com cuidado.

### <a name="reducing-power-consumption"></a>Reduzindo o consumo de energia

-   **Projete suas animações para reduzir o consumo de energia.** Quando projetadas corretamente, as animações não devem aumentar significativamente o consumo de energia. Para reduzir o consumo de energia:
    -   **Pare a animação quando a exibição estiver desligada.** A exibição pode estar desligada para economizar energia.
    -   **Não use animações de execução longa que não são iniciadas pelo usuário.** Animações que usam temporizadores periódicos de alta resolução reduzem a eficiência do gerenciamento de energia do processador. Além disso, desabilite todos os temporizadores periódicos de alta resolução quando as animações são concluídas.
    -   **Suspenda todas as animações quando o sistema ficar ocioso.** O período de inatividade do usuário para ficar ocioso é determinado Opções de Energia em Painel de Controle.

### <a name="accessibility"></a>Acessibilidade

-   **Não use animação como a única maneira de transmitir informações essenciais.** As animações devem comunicar informações úteis, mas não críticas, pois não podem ser acessadas por usuários com deficiências visuais.
-   **Certifique-se de que informações equivalentes estão disponíveis por outros meios,** como:

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

