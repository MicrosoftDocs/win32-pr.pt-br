---
title: Windows Visão geral da animação
description: Esta visão geral fornece uma introdução ao Windows Animation Manager e se concentra nos principais componentes e conceitos.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows Animação Windows animação , visão geral
- objetos do gerenciador de animação Windows Animação , descrito
- variáveis de animação Windows Animação , descritas
- objetos de temporizador de animação Windows Animação , descrito
- animação de Windows de tempo
- duração contextitivo Windows Animação
- velocidade correspondente Windows Animação
- animação de gerenciamento Windows contenção
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

Esta visão geral fornece uma introdução ao Windows Animation Manager e se concentra nos principais componentes e conceitos. Para obter mais informações sobre storyboards e transições, consulte Visão [geral do storyboard.](storyboard-construction.md)

Este tópico contém as seguintes seções:

-   [Conceitos básicos](#basic-concepts)
-   [Componentes da Windows animação](#components-of-windows-animation)
-   [A API Windows de Animação do Windows](#the-windows-animation-api)
-   [Configurações](#configurations)
    -   [Animação controlada por aplicativo](#application-driven-animation)
    -   [Animação controlada por temporizador](#timer-driven-animation)
-   [Recursos avançados](#advanced-features)
    -   [Gerenciamento de contenção](#contention-management)
-   [Tópicos relacionados](#related-topics)

## <a name="basic-concepts"></a>Conceitos básicos

*A* animação é uma sequência de imagens ainda sucessivas que produz uma ilusão de movimento quando tocada novamente. O uso da animação interativa em sua interface do usuário pode dar a um aplicativo uma personalidade exclusiva, bem como melhorar a experiência do usuário. A animação pode ajudar a comunicar as principais alterações de estado na interface do usuário e ajudar a gerenciar a complexidade da interface do usuário. A animação também pode adicionar à percepção do usuário sobre a qualidade de um aplicativo.

Como exemplos, Windows Animação é usada na barra de tarefas para ajudá-lo a gerenciar e acessar arquivos e programas e a Lupa para ampliar diferentes partes da tela para torná-las mais fáceis de ver.

As unidades fundamentais de uma animação são a característica de um elemento visual a ser animado e a descrição de como essa característica muda ao longo do tempo. Um aplicativo pode animar uma ampla variedade de características, como posição, cor, tamanho, rotação, contraste e opacidade.

Na Windows Animação, uma *variável de animação* representa a característica a ser animada. Uma *transição* descreve como o valor dessa variável de animação muda conforme a animação ocorre. Por exemplo, um elemento visual pode ter uma variável de animação que especifica sua opacidade e uma ação do usuário pode gerar uma transição que leva essa opacidade de um valor de 50 a 100, representando uma animação de semi transparente para totalmente opaco.

Um *storyboard* é um conjunto de transições aplicadas a uma ou mais variáveis de animação ao longo do tempo. Um aplicativo exibe animações construindo e tocando storyboards e, em seguida, desenhando sequências de quadros discretos à medida que os valores das variáveis de animação mudam ao longo do tempo.

## <a name="components-of-windows-animation"></a>Componentes da Windows animação

Windows A animação consiste nos seguintes componentes:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>gerenciador de animação
</dt> <dd>

Os aplicativos usam um objeto de gerenciador de animação para criar variáveis de animação e storyboards, agendar e controlar animações e atualizar informações de estado antes que o aplicativo desenhe cada quadro. Um único objeto de gerenciador de animação normalmente gerencia todas as animações em um aplicativo e, portanto, tem controle global sobre todos os storyboards agendados.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>variáveis de animação
</dt> <dd>

Antes de iniciar qualquer animação, um aplicativo precisa criar objetos de variável de animação. Uma variável de animação representa um aspecto de um elemento visual a ser animado. A variável é um valor de ponto flutuante escalar, embora o valor possa ser arredondado para um valor inteiro.

Uma variável de animação normalmente tem o mesmo tempo de vida que o elemento visual a ser animado. O valor inicial de uma variável de animação é especificado quando a variável é criada. Depois disso, seu valor não pode ser alterado diretamente; ele deve ser atualizado por meio do gerenciador de animação.

Uma variável de animação pode ser identificada por uma *marca*, que é um emparelhamento de um identificador inteiro com um ponteiro para um objeto COM. Uma marca não precisa ser exclusiva, a menos que o aplicativo a use para pesquisar uma variável. Por padrão, uma variável de animação não tem uma marca e as tentativas de ler sua marca falharão até que uma seja definida.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>sistema de tempo
</dt> <dd>

Windows A animação inclui um sistema de temporização que ajuda a garantir que as animações sejam renderizadas a uma taxa de quadros suave e consistente, além de reduzir o uso de recursos do sistema para renderização quando o sistema estiver ocupado. Um *temporizador* ajuda a gerenciar a renderização de animação indicando automaticamente a passagem de uma pequena unidade de tempo, chamada de *tique*. O sistema de temporização  monitora o desempenho geral da renderização do sistema e acelera as animações aumentando ou diminuindo dinamicamente a frequência de tiques. Os aplicativos podem permitir que um temporizador conduza o gerenciador de animação e registre um manipulador para ser notificado antes e depois que o gerenciador for atualizado para cada tique. Os aplicativos podem especificar a taxa mínima de quadros de animação aceitável para um temporizador e ser notificados se a taxa de quadros real de uma animação ficar abaixo dessa taxa.

Para conservar recursos do sistema, um temporizador pode ser configurado para desabilitar a si mesmo quando nenhuma animação está ocorrendo.

</dd> </dl>

## <a name="the-windows-animation-api"></a>A API Windows de Animação do Windows

A WINDOWS de Animação é uma API baseada em COM de thread único que fornece os seguintes recursos para desenvolvedores:

-   Um objeto do gerenciador de animação, [**UIAnimationManager,**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))para criar objetos de animação e controlar animações
-   Variáveis de animação e storyboards
-   Uma biblioteca fundamental, [**UIAnimationTransitionLibrary,**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85))de transições prontas para uso
-   Um objeto de temporizador, [**UIAnimationTimer,**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))para determinar a hora atual e, opcionalmente, para a animação de condução
-   Ganchos de evento para monitorar o estado e o progresso da animação

Para ver a referência completa da API, [consulte Referência Windows animação.](windows-animation-reference.md) Para exemplo de código, [consulte Tarefas Windows animação](using-windows-animation.md) e [exemplos Windows animação.](windows-animation-samples.md)

## <a name="configurations"></a>Configurações

Os aplicativos devem obter a hora atual antes de agendar uma nova animação. A seguir estão os mecanismos de tempo com suporte Windows Animação:

-   [Animação controlada por aplicativo](#application-driven-animation)
-   [Animação controlada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animação

Aplicativos que usam uma API gráfica acelerada por hardware podem sincronizar com a taxa de atualização do monitor para renderizar animações suaves. Como alternativa, um aplicativo pode usar um mecanismo de tempo próprio para determinar quando desenhar cada quadro de uma animação. Em ambos os casos, o aplicativo dirá ao gerenciador de animação quando atualizar seu estado. Um temporizador de animação ainda pode ser usado para determinar a hora atual com alta precisão, nas unidades exigidas pelo gerenciador de animação.

O diagrama a seguir mostra as interações entre um aplicativo e os componentes Windows Animação quando o aplicativo está impulsionando atualizações de animação diretamente.

![diagrama que mostra as interações entre um aplicativo e os componentes de animação do Windows quando o aplicativo está impulsionando atualizações de animação diretamente.](images/animationupdates.png)

Na configuração mais simples, um aplicativo redesenhará tudo sempre que a tela for atualizada, mesmo quando nenhuma animação estiver sendo reprodução. Para evitar o desperdício de trabalho, um aplicativo pode registrar um manipulador de eventos do gerenciador para ser notificado quando há animações agendadas e pode detectar quando o agendamento está vazio para que ele possa parar de redesenhar.

### <a name="timer-driven-animation"></a>Timer-Driven animação

Em vez de atualizar o gerenciador de animação diretamente, os aplicativos podem permitir que o temporizador de animação diga ao gerenciador de animação quando atualizar seu estado e simplesmente será notificado quando cada atualização tiver sido realizada. Essa abordagem é recomendada para APIs gráficas mais antigas. Em geral, se for possível sincronizar com a taxa de atualização do monitor, é melhor fazer isso e usar a animação controlada pelo aplicativo.

O diagrama a seguir mostra as interações entre um aplicativo e os componentes Windows animação quando o temporizador de animação está impulsionando atualizações de animação.

![diagrama que mostra as interações entre um aplicativo e os componentes de animação do Windows quando o temporizador de animação está impulsionando atualizações de animação.](images/animationtimerupdates.png)

O temporizador pode ser configurado para ser executado somente quando as animações são agendadas; fazer isso é uma questão simples de passar um parâmetro específico quando o temporizador e o gerenciador de animação estão conectados.

## <a name="advanced-features"></a>Recursos avançados

Além de uma base básica para dar suporte à animação, Windows animação inclui suporte para várias técnicas avançadas de animação, incluindo:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*duração contextitivo*
</dt> <dd>

A duração de uma transição não precisa ser corrigida; ele pode ser determinado com base no valor e na velocidade da variável animada quando a transição é iniciada.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*correspondência de velocidade*
</dt> <dd>

O movimento geralmente é mais fácil para o olho se a posição e a velocidade de um objeto móvel não se movem instantaneamente entre valores. Quando um novo storyboard interrompe um que está em reprodução no momento, a correspondência de velocidade permite que o novo storyboard seja interrompido sem problemas no local em que o anterior foi encerrado.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*gerenciamento de contenção*
</dt> <dd>

Se dois storyboards precisam atualizar a mesma variável de animação simultaneamente, ocorrerá um conflito de agendamento. Em vez de exigir uma prioridade numérica específica para cada storyboard, Windows Animation permite que o aplicativo determine as prioridades relativas de qualquer dois storyboards.

</dd> </dl>

### <a name="contention-management"></a>Gerenciamento de contenção

Os desenvolvedores podem implementar *um* retorno de chamada de comparação de prioridade para comparar a prioridade do storyboard de ser agendado e o storyboard que já está na agenda. Um aplicativo que implementa uma comparação de prioridade pode usar qualquer lógica preferencial para determinar quando um storyboard pré-emptsa outro. Para resolver o conflito de agendamento, Windows Animation solicita ao aplicativo qual dessas ações pode ser tomada, na seguinte ordem:

-   **Cancele o storyboard agendado.** Se o storyboard agendado ainda não tiver iniciado a reprodução, ele poderá ser cancelado e removido imediatamente da agenda.
-   **Corte o storyboard agendado.** Quando um novo storyboard corta um storyboard agendado, o storyboard agendado deixa de afetar a variável assim que o novo storyboard começa a anima-la. As velocidades são combinadas, permitindo que o novo storyboard seja bem-se de onde o anterior foi deixado.
-   **Conclua o storyboard agendado.** Um storyboard poderá ser concluído somente se contiver um loop que se repita indefinidamente. Se o storyboard estiver em tal loop quando concluído, a repetição atual será concluída e o restante do storyboard será reproduzindo. Se o loop ainda não tiver começado quando um storyboard for concluído, o loop será totalmente ignorado.
-   **Compactar o storyboard agendado.** Se cortar ou cancelar o storyboard agendado não for uma opção, o storyboard poderá ser concluído. Windows A animação apresenta a possibilidade de compactar o tempo disponível para o storyboard agendado (e todos os storyboards agendados antes dele), para que as variáveis atinjam seu estado final mais rapidamente. Quando a compactação é aplicada, o tempo é temporariamente acelerado para storyboards afetados, para que eles reproduzam mais rapidamente.

Se nenhuma das ações acima for permitida pelos objetos de comparação de prioridade registrada, a tentativa de agendar o novo storyboard falhará. Por padrão, todos os storyboards podem ser cortados, concluídos ou compactados para evitar falhas, mas nenhum pode ser cancelado.

O diagrama a seguir mostra o ciclo de vida de um storyboard, usando os estados definidos pela [**enumeração \_ STATUS STORYBOARD ANIMAÇÃO \_ \_**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) da interface do usuário. Os aplicativos usam a API Windows animação para criar um storyboard e enviar para agendamento. O gerenciador de animação agenda o storyboard e gerencia a animação.

![diagrama que mostra como o gerenciador de animação agenda o storyboard e gerencia a animação.](images/statediagram.png)

Para obter mais informações sobre gerenciamento e agendamento de storyboard, consulte Visão [geral do storyboard.](storyboard-construction.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Referência de animação](windows-animation-reference.md)
</dt> <dt>

[Windows Exemplos de animação](windows-animation-samples.md)
</dt> <dt>

[Windows Tarefas de animação](using-windows-animation.md)
</dt> </dl>

 

 