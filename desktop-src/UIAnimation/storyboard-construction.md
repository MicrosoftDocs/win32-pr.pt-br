---
title: Visão geral do storyboard
description: Esta visão geral concentra-se em como as transições e os storyboards são usados na animação do Windows.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Animação Windows animação do Windows, visão geral do storyboard
- Animação de storyboards do Windows, descrita
- transição de animação do Windows, descrita
- transições de animação do Windows, personalizadas
- Animação de interpolação do Windows, descrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d8e0af3937cd31ccdc43216a9d3426bad0e7b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641300"
---
# <a name="storyboard-overview"></a>Visão geral do storyboard

Esta visão geral concentra-se em como as transições e os storyboards são usados na animação do Windows. Para obter uma visão geral dos componentes da animação do Windows, consulte [visão geral da animação do Windows](scenic-animation-api-overview.md).

Este tópico contém as seguintes seções:

-   [Transições](#custom-transitions)
    -   [Biblioteca de transição](#transition-library)
    -   [Transições personalizadas](#custom-transitions)
-   [Storyboards](#storyboards)
    -   [Criando um storyboard simples](#building-a-simple-storyboard)
    -   [Usando uma duração de Context-Sensitive](#using-a-context-sensitive-duration)
    -   [Criando um storyboard mais complexo](#building-a-more-complex-storyboard)
    -   [Usando quadros-chave](#using-keyframes)
    -   [Mantendo variáveis](#holding-variables)
    -   [Agendando um storyboard](#scheduling-a-storyboard)
-   [Tópicos relacionados](#related-topics)

## <a name="transitions"></a>Transições

Uma transição define como uma variável de animação única é alterada em um intervalo de tempo específico. A animação do Windows inclui uma biblioteca de transições comuns que os desenvolvedores podem aplicar a uma ou mais variáveis de animação. Diferentes tipos de transições têm conjuntos diferentes de parâmetros, que podem incluir o valor da variável quando a transição for concluída, a duração da transição ou as quantidades exclusivas da função matemática subjacente, como aceleração ou intervalo de oscilação.

Todas as transições compartilham dois parâmetros implícitos: o valor inicial e a velocidade inicial (inclinação) da função matemática. Eles podem ser especificados explicitamente pelo aplicativo, mas normalmente são definidos pelo Gerenciador de animação para o valor e a velocidade da variável de animação quando a transição começa.

-   [Biblioteca de transição](#transition-library)
-   [Transições personalizadas](#custom-transitions)

### <a name="transition-library"></a>Biblioteca de transição

As transições a seguir são atualmente fornecidas pela biblioteca de transição. Se um aplicativo exigir um efeito que não possa ser especificado usando a biblioteca de transição, os desenvolvedores poderão criar outros tipos de transições implementando um interpolador personalizado para o aplicativo ou usando uma biblioteca de transição de terceiros.



| Nome da transição                        | Description                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| acelerar-desacelerar<br/>       | A variável de animação acelera e diminui a velocidade de uma determinada duração.<br/>                                                                                                               |
| constante<br/>                    | A variável de animação permanece em seu valor inicial durante toda a transição.<br/>                                                                                                            |
| cúbicas<br/>                       | A variável de animação muda de seu valor inicial para um valor final especificado, com uma velocidade final especificada, em uma determinada duração.<br/>                                                 |
| própria<br/>                    | A variável de animação permanece em seu valor inicial para um tempo de atraso especificado e alterna instantaneamente para um valor final especificado e permanece nesse valor para um determinado tempo de espera.<br/> |
| instantânea<br/>               | A variável de animação é alterada instantaneamente de seu valor atual para um valor final especificado.<br/>                                                                                               |
| linear<br/>                      | A variável de animação faz a transição linearmente de seu valor inicial para um valor final especificado em uma determinada duração.<br/>                                                                      |
| linear da velocidade<br/>           | A variável de animação faz a transição linearmente de seu valor inicial para um valor final especificado com uma velocidade especificada.<br/>                                                                     |
| parabólico da aceleração<br/> | A variável de animação faz a transição de seu valor inicial para um valor final especificado, com uma velocidade final especificada, alterando sua velocidade com uma aceleração especificada.<br/>               |
| versa<br/>                    | A variável muda de direção em uma determinada duração. O valor final será o mesmo que o valor inicial e a velocidade final será o negativo da velocidade inicial.<br/>          |
| sinusoidal do intervalo<br/>       | A variável oscila dentro de um determinado intervalo de valores, com um período especificado de oscilação, para uma determinada duração.<br/>                                                                     |
| sinusoidal da velocidade<br/>    | A variável oscila com um período especificado de oscilação para uma determinada duração. A amplitude de oscilação é determinada pela velocidade inicial da variável.<br/>                      |
| interrupção suave<br/>                 | A variável de animação chega a uma parada suave em um valor final especificado, dentro de uma duração máxima de tempo.<br/>                                                                              |



 

A tabela a seguir contém ilustrações para cada uma dessas transições.



|                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![ilustração de uma transição instantânea](images/instantaneoustransition.png)  ![ilustração de uma transição constante](images/constanttransition.png)  ![ilustração de uma transição linear](images/lineartransition.png)  ![ilustração de uma transição de Lineat da velocidade](images/lineartransitionfromspeed.png)  ![ilustração de uma transição discreta](images/discretetransition.png) |
| ![ilustração de uma transição parabólico da aceleração](images/parabolictransitionfromacceleration.png)  ![ilustração de uma transição cúbica](images/cubictransition.png)  ![ilustração de uma transição de interrupção suave](images/smoothstoptransition.png)                                                                                                                                       |
| ![ilustração de uma transição de estorno](images/reversaltransition.png)  ![ilustração de uma transição de sinusoidal da velocidade](images/sinusolidaltransitionfromvelocity.png)  ![ilustração de uma transição de sinusoidal do intervalo](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![ilustração de transições de accellerate e desaceleração](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Transições personalizadas

Um *interpolador* define a função matemática que determina como uma variável de animação muda ao longo do tempo conforme progride de seu valor inicial para um valor final. Cada transição na biblioteca de transição tem um objeto interpolador associado que é fornecido pelo sistema e implementa a função interpolador. Se um aplicativo exigir um efeito que não possa ser especificado usando a biblioteca de transição, ele poderá implementar uma ou mais transições personalizadas implementando um objeto interpolador para cada nova transição. Os objetos do interpolador não podem ser usados diretamente por aplicativos e, em vez disso, devem ser encapsulados em uma transição associada. Uma *fábrica de transição* é usada para gerar transições de um objeto interpolador. Consulte [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) e [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) para obter mais detalhes.

Observe que a maioria dos aplicativos terá todas as transições de que precisam usando a biblioteca de transição e, portanto, não precisará implementar um interpolador.

## <a name="storyboards"></a>Storyboards

Um Storyboard é uma coleção de transições aplicadas a uma ou mais variáveis de animação ao longo do tempo. As transições em um storyboard têm garantia de permanecer sincronizadas em relação umas às outras, e o storyboard é agendado ou cancelado como uma unidade. Depois de criar as transições desejadas, um aplicativo cria um storyboard usando o Gerenciador de animação, adiciona as transições ao storyboard, configura o storyboard adequadamente e o agenda para reprodução assim que possível. O Gerenciador de animação determina a hora de início real do storyboard, porque pode haver contenção com outros storyboards que atualmente animam as mesmas variáveis.

A duração geral de um storyboard depende das durações das transições dentro do storyboard. A duração de uma transição não precisa ser corrigida; Ele pode ser determinado pelo valor e velocidade das variáveis animadas quando a transição começa. Portanto, a duração de um storyboard também pode depender do estado das variáveis que ele anima.

Os exemplos a seguir pressupõem que um Gerenciador de animação, uma biblioteca de transição e um temporizador foram criados. Para obter mais informações, consulte [criar os objetos de animação principal](adding-animation-to-an-application.md). Os exemplos também pressupõem que o aplicativo criou três variáveis de animação (X, Y e Z) usando o método [**IUIAnimationManager:: CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) e cinco transições (T1, T2, T3, T4 e T5) usando um dos métodos da interface [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) .

-   [Criando um storyboard simples](#building-a-simple-storyboard)
-   [Usando uma duração de Context-Sensitive](#using-a-context-sensitive-duration)
-   [Criando um storyboard mais complexo](#building-a-more-complex-storyboard)
-   [Usando quadros-chave](#using-keyframes)
-   [Mantendo variáveis](#holding-variables)
-   [Agendando um storyboard](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Criando um storyboard simples

Para criar um storyboard simples, use o método [**IUIAnimationManager:: createstoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) para criar um novo storyboard, o método [**IUIAnimationTransitionLibrary:: CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) para criar uma transição linear, T1 e o método [**IUIAnimationStoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) para aplicar a transição T1 à variável X e adicionar a transição resultante ao storyboard.

Esse processo gera um storyboard simples, conforme mostrado na figura a seguir. O storyboard contém uma transição, T1, de modo que o valor da variável X seja alterado linearmente em uma duração fixa de tempo.

![ilustração mostrando um storyboard simples com uma duração fixa](images/simplestoryboardfixedduration.png)

Observe que, para esse cenário simples, uma opção alternativa é usar o método [**IUIAnimationManager:: ScheduleTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) .

### <a name="using-a-context-sensitive-duration"></a>Usando uma duração de Context-Sensitive

Enquanto algumas transições têm uma duração fixa, a duração de outras depende do valor inicial ou da velocidade da variável animada quando a transição é iniciada. Por exemplo, o método [**IUIAnimationTransitionLibrary:: CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) cria uma transição com uma duração proporcional à diferença entre o valor inicial da variável de animação e o valor final especificado. Nesta ilustração, e as demais ilustrações, tais transições com durações arbitrárias são mostradas com um ponto de interrogação (?), e suas durações reais são determinadas quando o storyboard é reproduzido.

![ilustração mostrando um storyboard simples com duração desconhecida](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Criando um storyboard mais complexo

Depois de criar um storyboard e adicionar uma única transição, T1, você pode acrescentar uma segunda transição para a variável X chamando o método [**IUIAnimationStoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) novamente, mas com T2 em vez de T1.

Supondo que a transição T2 tenha uma duração que seja sensível ao contexto, o storyboard agora contém duas transições back-to-back de duração arbitrária que afetam a variável X.

![ilustração mostrando um Storyboard que contém duas transições na mesma variável](images/appendingwithaddtransition.png)

Chamar [**Addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) novamente com a variável Y e a transição T3 adiciona uma terceira transição no início do storyboard. Dependendo dos valores de X e Y quando o storyboard for reproduzido, T3 poderá terminar após T1 ou mesmo após T2.

![ilustração mostrando um Storyboard que contém transições entre várias variáveis](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Usando quadros-chave

Para adicionar uma transição em um deslocamento do início do storyboard, primeiro você deve adicionar um quadro-chave. Os quadros-chave representam instantâneos no tempo e, por si só, não afetam o comportamento do storyboard. Cada Storyboard tem um quadro-chave implícito que representa o início do storyboard, o [**quadro-chave do storyboard da animação da interface do usuário \_ \_ \_ \_ Iniciar**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)); você pode adicionar novos quadros chave em deslocamentos do início chamando o método [**IUIAnimationStoryboard:: AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) com o **quadro-chave da animação da interface do usuário \_ \_ \_ \_ início do storyboard**.

O deslocamento no qual você adiciona um quadro-chave é sempre relativo a outro quadro-chave. O diagrama a seguir mostra o resultado da adição de keyframe1 e de transição T4, que é aplicado à variável Z, alinhada com keyframe1 e criada com uma duração fixa. É claro que, como as durações das outras transições ainda não são conhecidas, o T4 pode não ser a última transição para concluir.

![ilustração mostrando a adição de uma transição alinhada em um quadro-chave](images/addtransitionatkeyframe.png)

Os quadros-chave também podem ser colocados nas extremidades das transições, usando o método [**IUIAnimationStoryboard:: AddKeyframeAfterTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) . O diagrama a seguir mostra o resultado da adição de keyframe2 após T1 e keyframe3 após T2.

![ilustração mostrando a adição de quadros-chave após várias transições](images/addkeyframeaftertransition.png)

Como as durações de T1 e T2 não são conhecidas até que o storyboard seja reproduzido, os deslocamentos de keyframe2 e keyframe3 também não são determinados até lá. Consequentemente, keyframe2 e até mesmo keyframe3 podem ocorrer antes de keyframe1.

Tanto o início quanto o fim de uma transição podem ser alinhados com quadros-chave usando o método [**IUIAnimationStoryboard:: AddTransitionBetweenKeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) . O diagrama a seguir mostra o resultado da adição de uma quinta transição, T5, na variável Y, entre keyframe2 e keyframe3. Isso altera a duração de T5, tornando-o mais longo ou mais curto, dependendo dos deslocamentos relativos de keyframe2 e keyframe3.

![ilustração mostrando additon de uma transição entre quadros-chave](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Mantendo variáveis

Se o T4 terminar após T2 e T5, o storyboard interromperá a animação das variáveis X e Y, tornando-as disponíveis para que outros storyboards sejam animados. No entanto, o aplicativo pode chamar o método [**IUIAnimationStoryboard:: HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) para solicitar que o storyboard Mantenha algumas ou todas as variáveis que ele anima em seus valores finais até que o storyboard seja concluído. O diagrama a seguir mostra o resultado de manter X e Z quando o T4 termina por último. Observe que o storyboard mantém X em seu valor final até que o storyboard seja concluído. A suspensão não tem nenhum efeito em Z porque o storyboard termina quando o T4 é concluído.

![ilustração mostrando a retenção de variáveis em valores finais até que o storyboard seja concluído](images/holdvariable.png)

Embora Y não seja mantido por este storyboard, seu valor não é alterado depois que T5 é concluído, a menos que outro storyboard o anime. Como Y não é mantido, qualquer outro storyboard, independentemente da prioridade, pode animar Y após a conclusão de T5. Por outro lado, como X é mantido, um storyboard de prioridade mais baixa não pode animar X até que este storyboard seja concluído.

Todas essas ilustrações assumiram um conjunto arbitrário de valores atuais para as variáveis quando o storyboard começa a ser reproduzido. Se outros valores forem encontrados, as durações das transições sensíveis ao contexto provavelmente serão diferentes, conforme mostrado na ilustração a seguir.

![ilustração mostrando o resultado da alteração das condições iniciais usadas para a ilustração anterior](images/holdvariablez.png)

Nesse cenário, T5 começa antes de concluir o T3 e, portanto, o T3 é cortado. Como o T4 termina antes de T2 e T5, o valor de Z é mantido até o final do storyboard. Em geral, os valores e velocidades de variáveis quando um storyboard começa a ser executado podem afetar a ordenação do quadro-chave e o comprimento geral e a forma do storyboard.

### <a name="scheduling-a-storyboard"></a>Agendando um storyboard

Ao agendar um storyboard, sua hora de início é determinada por sua estrutura de tópicos e os contornos dos storyboards que estão atualmente no agendamento. Especificamente, o primeiro e último instante quando o storyboard anima cada variável individual determinam se e quando dois storyboards colidem, mas os detalhes internos das transições no não são importantes.

A ilustração a seguir mostra a estrutura de um storyboard com cinco transições animando três variáveis.

![ilustração mostrando um storyboard com cinco transições animando três variáveis](images/storyboardwithoutline.png)

A base da plataforma de animação do Windows é seu suporte para permitir que uma animação seja concluída antes que outra comece, quando necessário. Embora isso elimine muitos problemas lógicos, ele também apresenta uma latência arbitrária na interface do usuário. Para resolver isso, os aplicativos podem especificar o *atraso aceitável mais longo* para que um storyboard comece, usando o método [**IUIAnimationStoryboard:: SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) e o Gerenciador de animação use essas informações para agendar o storyboard antes de o período de latência especificado expirar. Quando um Storyboard é agendado, o Gerenciador de animação determina se outros storyboards devem primeiro ser cancelados, cortados, concluídos e/ou compactados.

Um aplicativo pode registrar um manipulador que será chamado quando o status de um storyboard for alterado. Isso permite que o aplicativo responda quando o storyboard começa a ser executado, executa até a conclusão, é removido totalmente da agenda ou não é impedido de concluir devido à interrupção por um storyboard de prioridade mais alta. Para identificar os storyboards passados para manipuladores de eventos de storyboard (ou comparações de prioridade), um aplicativo pode usar o método [**IUIAnimationStoryboard:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) para aplicar marcas a storyboards, semelhante àqueles que podem ser usados para identificar variáveis. Assim como na reutilização do storyboard, os desenvolvedores devem ter cuidado ao usar marcas para identificar storyboards e garantir que as ambiguidades não surjam quando as ações do usuário resultam na fila de muitos storyboards.

Os exemplos a seguir mostram duas variações de uma tentativa de agendar o storyboard criado nas seções anteriores deste tópico.

Nesse cenário, seis storyboards, A até F, já foram agendadas para animar variáveis W, X, Y e Z, mas apenas A e B começaram A ser reproduzidos. O novo storyboard, rotulado como G, tem seu atraso aceitável mais longo definido como a duração mostrada na ilustração a seguir.

![ilustração mostrando a adição de um novo storyboard à agenda existente](images/existingschedule1withlines.png)

O aplicativo tem comparações de prioridade registradas que incluem a seguinte lógica:

-   G só pode cancelar C e E e apenas para evitar falhas.
-   G pode cortar apenas A, C, e e F e apenas para evitar falha.
-   Qualquer storyboard pode compactar qualquer outro Storyboard (a compactação é sempre feita apenas para evitar falhas).

> [!Note]  
> O qualificador "somente para evitar falhas" significa que as comparações de prioridade registradas retornam S \_ OK somente quando o parâmetro *priorityEffect* é uma **falha de efeito de prioridade de animação da interface do usuário \_ \_ \_ \_**. Consulte o método [**IUIAnimationPriorityComparison:: HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) para obter detalhes.

 

Para iniciar o G antes que o atraso aceitável mais longo tenha decorrido, o Gerenciador de animação deve fazer o seguinte:

-   Cortar F
-   Cancelar E

Quando E é cancelado, D e F são descobertos e revertidos para seus contornos originais:

![ilustração mostrando estruturas de tópicos originais](images/existingschedule1bwithlines.png)

O Gerenciador de animação não precisa cancelar ou cortar C para agendar antes que o atraso aceitável mais longo tenha decorrido, portanto, a reunião de C e G determina quando G é iniciado.

![ilustração mostrando que f é cortado para permitir que c e g atendam](images/schedule1withgwithlines.png)

Depois que o G tiver sido agendado com êxito, as durações de suas transições poderão ser determinadas e o restante de sua estrutura de tópicos será, portanto, conhecido. No entanto, a estrutura de tópicos poderá ser alterada se outro storyboard for removido posteriormente da agenda.

Como um segundo exemplo, considere um cenário como esse acima, mas com um atraso mais curto aceitável mais longo especificado para G.

![ilustração mostrando o cenário anterior, mas com um atraso mais curto aceitável mais longo para g](images/existingschedule2withlines.png)

Nesse caso, as seguintes ações são executadas:

-   Cortar F
-   Cancelar E
-   Cancelar C

Além disso, o Gerenciador de animação deve compactar D pelo valor mostrado para habilitar o G para iniciar após seu atraso aceitável mais longo e não mais tarde.

![ilustração que mostra onde d deve ser compactado para permitir que g inicie em seu atraso mais longo aceitável](images/trimmedandcancelledwithlines.png)

Para preservar o tempo relativo, A, B e F também são compactados.

![ilustração mostrando a, b, d e f compactados](images/schedule2withgwithlines.png)

No entanto, os storyboards em variáveis não relacionadas (não mostradas) não seriam compactados.

Mais uma vez, a estrutura de G agora é conhecida e é diferente do resultado no primeiro cenário, pois as variáveis têm valores diferentes quando G começa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationPriorityComparison**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[**IUIAnimationStoryboard**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

