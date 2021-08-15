---
title: Windows Visão geral da animação
description: esta visão geral fornece uma introdução ao gerenciador de animação Windows e se concentra nos principais componentes e conceitos.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows animação Windows animação, visão geral
- objetos do gerenciador de animação Windows animação, descrito
- variáveis de animação Windows animação, descrita
- objetos de timer de animação Windows animação, descrita
- animação de Windows do sistema de tempo
- duração sensível ao contexto Windows animação
- Windows de animação de correspondência de velocidade
- animação de Windows de gerenciamento de contenção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc0892cffa3e79428e19cbe5b1a3c27d7abda62365c4ceb15731101aa857f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347989"
---
# <a name="windows-animation-overview"></a>Windows Visão geral da animação

esta visão geral fornece uma introdução ao gerenciador de animação Windows e se concentra nos principais componentes e conceitos. Para obter mais informações sobre storyboards e transições, consulte [visão geral do storyboard](storyboard-construction.md).

Este tópico contém as seguintes seções:

-   [Conceitos básicos](#basic-concepts)
-   [componentes da animação de Windows](#components-of-windows-animation)
-   [a API de animação de Windows](#the-windows-animation-api)
-   [Configurações](#configurations)
    -   [Animação orientada por aplicativo](#application-driven-animation)
    -   [Animação orientada por temporizador](#timer-driven-animation)
-   [Recursos avançados](#advanced-features)
    -   [Gerenciamento de contenção](#contention-management)
-   [Tópicos relacionados](#related-topics)

## <a name="basic-concepts"></a>Conceitos básicos

A *animação* é uma sequência de imagens sucessivas que produz uma ilusão de movimento ao reproduzir. O uso da animação interativa em sua interface do usuário pode dar a um aplicativo uma personalidade exclusiva, bem como melhorar a experiência do usuário. A animação pode ajudar a comunicar as principais alterações de estado na interface do usuário e a ajudar a gerenciar a complexidade da interface do usuário. A animação também pode ser adicionada à percepção do usuário da qualidade de um aplicativo.

como exemplos, Windows animação é usada na barra de tarefas para ajudá-lo a gerenciar e acessar arquivos e programas, e a lupa para ampliar partes diferentes da tela para facilitar a visualização dos usuários.

As unidades fundamentais de uma animação são a característica de um elemento visual ser animado e a descrição de como essa característica muda ao longo do tempo. Um aplicativo pode animar uma ampla variedade de características, como posição, cor, tamanho, rotação, contraste e opacidade.

na animação Windows, uma *variável de animação* representa a característica a ser animada. Uma *transição* descreve como o valor dessa variável de animação muda conforme ocorre a animação. Por exemplo, um elemento visual pode ter uma variável de animação que especifica sua opacidade e uma ação do usuário pode gerar uma transição que leva essa opacidade de um valor de 50 para 100, representando uma animação de semitransparente para totalmente opaca.

Um *storyboard* é um conjunto de transições aplicadas a uma ou mais variáveis de animação ao longo do tempo. Um aplicativo exibe animações construindo e reproduzindo storyboards e, em seguida, desenhando seqüências de quadros discretos à medida que os valores das variáveis de animação mudam com o passar do tempo.

## <a name="components-of-windows-animation"></a>componentes da animação de Windows

Windows A animação consiste nos seguintes componentes:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>Gerenciador de animação
</dt> <dd>

Os aplicativos usam um objeto do Gerenciador de animação para criar variáveis de animação e storyboards, agendar e controlar animações e atualizar informações de estado antes que o aplicativo desenhe cada quadro. Um único objeto Gerenciador de animação geralmente gerencia todas as animações em um aplicativo e, portanto, tem controle global sobre todos os storyboards agendados.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>variáveis de animação
</dt> <dd>

Antes de iniciar qualquer animação, um aplicativo precisa criar objetos de variável de animação. Uma variável de animação representa um aspecto de um elemento visual a ser animado. A variável é um valor de ponto flutuante escalar, embora o valor possa ser arredondado para um valor inteiro.

Uma variável de animação normalmente tem o mesmo tempo de vida que o elemento visual para animar. O valor inicial de uma variável de animação é especificado quando a variável é criada. Depois disso, seu valor não pode ser alterado diretamente; Ele deve ser atualizado por meio do Gerenciador de animação.

Uma variável de animação pode ser identificada por uma *marca*, que é um emparelhamento de um identificador inteiro com um ponteiro para um objeto com. Uma marca não precisa ser exclusiva, a menos que o aplicativo a use para pesquisar uma variável. Por padrão, uma variável de animação não tem uma marca e qualquer tentativa de ler sua marca falhará até que uma tenha sido definida.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>sistema de tempo
</dt> <dd>

Windows A animação inclui um sistema de tempo que ajuda a garantir que as animações sejam renderizadas em uma taxa de quadros suave e consistente, reduzindo também o uso de recursos do sistema para renderização quando o sistema estiver ocupado. Um *temporizador* ajuda a gerenciar a renderização de animação, indicando automaticamente a passagem de uma pequena unidade de tempo, chamada de *tique*. O sistema de temporização monitora o desempenho geral da renderização do sistema e *limita* as animações, aumentando ou diminuindo dinamicamente a frequência das tiques. Os aplicativos podem permitir que um temporizador conduza o Gerenciador de animação e possa registrar um manipulador para ser notificado antes e depois que o gerente é atualizado para cada tique. Os aplicativos podem especificar a taxa mínima de quadros de animação aceitável para um temporizador e ser notificado se a taxa de quadros real de uma animação cair abaixo dessa taxa.

Para conservar recursos do sistema, um temporizador pode ser configurado para se desabilitá-lo quando nenhuma animação estiver ocorrendo.

</dd> </dl>

## <a name="the-windows-animation-api"></a>a API de animação de Windows

a api de animação de Windows é uma api baseada em com de um único thread que fornece os seguintes recursos para desenvolvedores:

-   Um objeto Gerenciador de animação, [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)), para criar objetos de animação e controlar animações
-   Variáveis de animação e storyboards
-   Uma biblioteca básica, [**UIAnimationTransitionLibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85)), de transições prontas para uso
-   Um objeto de timer, [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)), para determinar a hora atual e, opcionalmente, para a direção da animação
-   Ganchos de evento para monitorar o estado e o andamento da animação

para obter a referência de API completa, consulte [referência de animação de Windows](windows-animation-reference.md). para obter um exemplo de código, consulte [Windows tarefas de animação](using-windows-animation.md) e [exemplos de animação de Windows](windows-animation-samples.md).

## <a name="configurations"></a>Configurações

Os aplicativos devem obter a hora atual antes de agendar uma nova animação. a seguir estão os mecanismos de tempo com suporte na animação Windows:

-   [Animação orientada por aplicativo](#application-driven-animation)
-   [Animação orientada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animação

Os aplicativos que usam uma API gráfica acelerada por hardware podem sincronizar com a taxa de atualização do monitor para renderizar animações suaves. Como alternativa, um aplicativo pode usar um mecanismo de tempo próprio para determinar quando desenhar cada quadro de uma animação. Em ambos os casos, o aplicativo informará ao Gerenciador de animação quando atualizar seu estado. Um temporizador de animação ainda pode ser usado para determinar a hora atual com alta precisão, nas unidades exigidas pelo Gerenciador de animação.

o diagrama a seguir mostra as interações entre um aplicativo e os componentes de animação Windows quando o aplicativo está orientando as atualizações de animação diretamente.

![diagrama que mostra as interações entre um aplicativo e os componentes de animação do Windows quando o aplicativo está orientando as atualizações de animação diretamente.](images/animationupdates.png)

Na configuração mais simples, um aplicativo redesenhará tudo sempre que a tela for atualizada, mesmo quando nenhuma animação for reproduzida. Para evitar o desperdício de trabalho, um aplicativo pode registrar um manipulador de eventos de gerente para ser notificado quando houver animações agendadas e detectar quando a agenda está vazia para que possa parar de redesenhar.

### <a name="timer-driven-animation"></a>Timer-Driven animação

Em vez de atualizar o Gerenciador de animação diretamente, os aplicativos podem deixar o temporizador de animação informar ao Gerenciador de animação quando atualizar seu estado e simplesmente ser notificado quando cada atualização ocorrer. Essa abordagem é recomendada para APIs de gráficos mais antigas. Em geral, se for possível sincronizar com a taxa de atualização do monitor, é melhor fazê-lo e usar a animação orientada por aplicativo.

o diagrama a seguir mostra as interações entre um aplicativo e os componentes de animação Windows quando o temporizador de animação está orientando as atualizações de animação.

![diagrama que mostra as interações entre um aplicativo e os componentes de animação do Windows quando o temporizador de animação está orientando atualizações de animação.](images/animationtimerupdates.png)

O temporizador pode ser configurado para ser executado somente quando as animações são agendadas; fazer isso é uma simples questão de passar um parâmetro específico quando o temporizador e o Gerenciador de animação estiverem conectados.

## <a name="advanced-features"></a>Recursos avançados

além de uma base básica para dar suporte à animação, Windows animação inclui suporte para várias técnicas de animação avançadas, incluindo:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*duração sensível ao contexto*
</dt> <dd>

A duração de uma transição não precisa ser corrigida; Ele pode ser determinado com base no valor e na velocidade da variável animada quando a transição começa.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*correspondência de velocidade*
</dt> <dd>

A movimentação é geralmente mais agradável ao olho se a posição e a velocidade de um objeto de movimentação não saltam instantaneamente entre os valores. Quando um novo storyboard interrompe um que está sendo executado no momento, a correspondência de velocidade permite que o novo storyboard apareça sem problemas onde o anterior terminou.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*gerenciamento de contenção*
</dt> <dd>

Se dois storyboards precisarem atualizar a mesma variável de animação simultaneamente, ocorrerá um conflito de agendamento. em vez de exigir uma prioridade numérica específica para cada storyboard, Windows animação permite que o aplicativo determine as prioridades relativas de quaisquer dois storyboards.

</dd> </dl>

### <a name="contention-management"></a>Gerenciamento de contenção

Os desenvolvedores podem implementar um retorno de chamada de *comparação de prioridade* para comparar a prioridade do storyboard de ser agendado e o storyboard que já está no agendamento. Um aplicativo que implementa uma comparação de prioridade pode usar qualquer lógica preferencial para determinar quando um storyboard empts o outro. para resolver o conflito de agendamento, Windows animação pergunta ao aplicativo quais dessas ações podem ser executadas, na seguinte ordem:

-   **Cancele o storyboard agendado.** Se o storyboard agendado ainda não tiver começado a ser reproduzido, ele poderá ser cancelado e removido imediatamente da agenda.
-   **Corte o storyboard agendado.** Quando um novo storyboard corta um storyboard agendado, o storyboard agendado deixa de afetar a variável assim que o novo storyboard começa a animá-la. Os velocidades são correspondidos, permitindo que o novo storyboard seja retirado suavemente onde o anterior parou.
-   **Conclua o storyboard agendado.** Um storyboard pode ser concluído somente se ele contiver um loop que se repete indefinidamente. Se o storyboard estiver em um loop desse tipo quando for concluído, a repetição atual será concluída e o restante do storyboard será reproduzido. Se o loop ainda não tiver começado quando um storyboard for concluído, o loop será ignorado inteiramente.
-   **Compacte o storyboard agendado.** Se o corte ou cancelamento do storyboard agendado não for uma opção, o storyboard poderá ser concluído. Windows A animação apresenta a possibilidade de compactar o tempo disponível para o storyboard agendado (e todos os storyboards agendados antes dele), de modo que as variáveis alcancem seu estado final mais rapidamente. Quando a compactação é aplicada, o tempo é temporariamente acelerado para storyboards afetados, para que eles joguem mais rapidamente.

Se nenhuma das ações acima for permitida pelos objetos de comparação de prioridade registrados, a tentativa de agendar o novo storyboard falhará. Por padrão, todos os storyboards podem ser cortados, concluídos ou compactados para evitar falhas, mas nenhum pode ser cancelado.

O diagrama a seguir mostra o ciclo de vida de um storyboard, usando os Estados definidos pela enumeração [**\_ status do \_ storyboard \_ da animação da interface do usuário**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) . os aplicativos usam a API de animação Windows para criar um storyboard e enviá-lo para agendamento. O Gerenciador de animação agenda o storyboard e gerencia a animação.

![diagrama que mostra como o Gerenciador de animação agenda o storyboard e gerencia a animação.](images/statediagram.png)

Para obter mais informações sobre agendamento e gerenciamento de storyboard, consulte [visão geral do storyboard](storyboard-construction.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Referência de animação](windows-animation-reference.md)
</dt> <dt>

[Windows Exemplos de animação](windows-animation-samples.md)
</dt> <dt>

[Windows Tarefas de animação](using-windows-animation.md)
</dt> </dl>

 

 