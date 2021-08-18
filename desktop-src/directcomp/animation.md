---
title: Animação (DirectComposition)
description: Este tópico aborda os conceitos básicos da animação do Microsoft DirectComposition.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b1f021d5a11fac70f47d5fe87f9389d2ad3e3108d224835fb295a8c3216354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119121"
---
# <a name="animation-directcomposition"></a>Animação (DirectComposition)

> [!NOTE]
> Para aplicativos Windows 10, recomendamos o uso de APIs Windows.UI.Composition em vez de DirectComposition. Para obter mais informações, consulte [Modernizar seu aplicativo da área de trabalho usando a camada visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico aborda os conceitos básicos da animação do Microsoft DirectComposition. Ela contém os seguintes tópicos:

-   [O que é uma animação?](#what-is-an-animation)
-   [Propriedades que podem ser animadas](#properties-that-can-be-animated)
-   [Funções de animação](#animation-functions)
-   [Segmentos de animação](#animation-segments)
    -   [Segmento cúbica](#cubic-segment)
    -   [Segmento sinusoidal](#sinusoidal-segment)
    -   [Segmento de repetição](#repeat-segment)
    -   [Segmento final](#end-segment)
-   [Compatibilidade com o Windows Animation Manager](#compatibility-with-windows-animation-manager)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-an-animation"></a>O que é uma animação?

*A* animação é uma ilusão óptica criada fazendo rapidamente alterações incrementais em um visual durante um período de tempo enquanto redesenha o visual depois que cada alteração é feita. Como os redesenhados ocorrem rapidamente, o cérebro percebe as alterações incrementais como uma única cena de alteração, assim como em um filme ou vídeo de ação ao vivo.

A tabela a seguir descreve algumas das maneiras típicas de usar animação.

| Animação                 | Descrição                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rolagem                 | Use a animação para adicionar recursos como a dinâmica de emulação de física a um controle de lista de rolagem.                                                                                                                                                           |
| Transições de cena         | Use a animação para criar transições de cena de navegação que fornecem continuidade entre tarefas em um fluxo de trabalho. As transições de cena de navegação fornecem contexto que mostra ao usuário onde ele esteve, onde ele está e onde precisa ir em seguida. |
| Interações entre janelas | Animar elementos de interface do usuário de diferentes aplicativos de uma maneira que dê a percepção de continuidade perfeita entre eles para ajudar o usuário a concluir tarefas que envolvem a troca de um aplicativo para outro.                                         |



 

## <a name="properties-that-can-be-animated"></a>Propriedades que podem ser animadas

No DirectComposition, você anima um visual aplicando animação a propriedades individuais dos objetos que definem o visual. Por exemplo, se você quiser mover um visual horizontalmente pela tela, aplique animação à propriedade OffsetX do visual. Da mesma forma, se você quisesse fazer uma simples rotação animada em 2D de um visual, aplicaria animação à propriedade Angle de um objeto de transformação 2D e, em seguida, aplicaria o objeto de transformação 2D à propriedade Transformar do visual.

DirectComposition permite que você aplique animação a qualquer propriedade de objeto que aceita um valor escalar. Você pode aplicar animações simultâneas a várias propriedades e vários objetos.

DirectComposition executa animações em um thread separado. Você pode iniciar uma animação ou um conjunto de animações e, em seguida, fazer outro trabalho em seus threads de aplicativo ou até mesmo colocar threads em sleep, enquanto o mecanismo de composição executa as animações na taxa de quadros apropriada.

## <a name="animation-functions"></a>Funções de animação

DirectComposition anima uma propriedade de objeto com base em uma função de animação que você define. Uma *função de* animação é um constructo que especifica como o valor de uma propriedade de objeto muda durante um período de tempo. Por exemplo, você pode definir uma função de animação que altera o valor de uma propriedade de 1 para 360 ao longo de 4 segundos. Em seguida, se você aplicar a função de animação à propriedade Angle de um objeto de transformação de rotação 2D e, em seguida, aplicar o objeto de transformação à propriedade Transformar de um visual, a função de animação girará o visual em um círculo completo durante 4 segundos.

Uma função de animação é representada por um objeto *de animação* criado por uma chamada para o [**método IDCompositionDevice::CreateAnimation.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) Você cria uma função de animação usando os métodos da interface [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) de um objeto de animação para anexar *segmentos* de animação , um de cada vez, à matriz que define a função de animação. Ao passar um segmento, você especifica um deslocamento baseado em zero que marca a hora de início do segmento, em relação ao início da função de animação. Segmentos de animação devem ser anexados em ordem crescente de horários de início. A tentativa de anexar um segmento de animação cuja hora de início é anterior ou igual a um segmento anterior falhará. Uma função de animação pode ter uma hora de término especificada, indicando quando a função deve ser concluída.

A menos que especificado de outra forma, uma função de animação é iniciada quando o DWM (Gerenciador de Janelas da Área de Trabalho) recebe o comando para executar a animação. Cada segmento é executado até que a hora de início do próximo segmento seja atingida. Todas as alterações descontinuosas que ocorrem no valor da propriedade animada entre segmentos são consideradas alterações discretas.

Aplique uma função de animação a uma propriedade definindo o valor da propriedade como o ponteiro [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) do objeto de animação que representa a função de animação. O mesmo objeto de animação pode ser aplicado a várias propriedades do mesmo objeto, bem como às propriedades de outros objetos criados pelo mesmo dispositivo.

## <a name="animation-segments"></a>Segmentos de animação

Segmentos de animação são as definições de tempo fundamentais de uma função de animação; eles são os primitivos dos quais as funções de animação mais complexas e de nível superior são criadas. Um segmento de animação é construído de uma série de parâmetros que descrevem a função e a hora em que o segmento começa, em relação ao início da função de animação. Para cada segmento, time (*t*) progride ao longo do eixo horizontal e começa em *t* = 0.

### <a name="cubic-segment"></a>Segmento cúbica

O tempo de um segmento cúbica é definido por um polinomial cúbico. Para uma determinada entrada de tempo (*t*), o valor de saída é dado pela seguinte equação:

*x*(*t*) = *em* 2 + *bt* igual a + *ct*  +  *d*

O diagrama a seguir mostra uma função de animação que contém dois segmentos cúbicos. O primeiro segmento faz a transição de um valor de 0 para 16 durante 4 segundos e o segundo altera o valor linearmente de 16 para 0 nos próximos 4 segundos. A primeira transição ocorre ao longo deste polinomial cúbica:

*x*(*t*) = *t* polegada - 6 *t* Igual a 12 *t*

e a segunda transição ocorre ao longo desta:

*x*(*t*) = - 4 *t* + 16

![diagrama de uma função de animação com dois segmentos cúbicos](images/cubicsegment.png)

Você adiciona um segmento cúbica a uma função de animação usando o [**método IDCompositionAnimation::AddCubic.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic)

### <a name="sinusoidal-segment"></a>Segmento sinusoidal

O tempo de um segmento sinusoidal é definido pela seguinte equação:

*x*(*t*) = *Bias*  +  *Amplitude* \* sin(*t* \* *Frequency* \* 2 PI + \* *Phase* \* PI/180.0)

Você adiciona um segmento sinusoidal a uma função de animação usando o [**método IDCompositionAnimation::AddSinusoidal.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal)

### <a name="repeat-segment"></a>Segmento de repetição

Um segmento de repetição repete uma parte anterior especificada de uma função de animação. Um segmento de repetição faz com que a parte especificada da função de animação loop indefinidamente até que o próximo segmento seja encontrado ou o final especificado da animação seja atingido. A parte anterior de uma animação é feita de outros segmentos, incluindo outros segmentos de repetição. Um segmento de repetição não pode ser usado como o primeiro segmento em uma função de animação.

O diagrama a seguir mostra uma função de animação que consiste em dois segmentos cúbicos de duração de 4 segundos cada, seguido por um segmento de repetição que dura 12 segundos. O segmento de repetição começa 8 segundos na animação e repete os 6 segundos anteriores da animação duas vezes até que o segmento final seja atingido em 20 segundos.

![diagrama de uma função de animação que contém dois segmentos cúbicos e um segmento de repetição](images/repeatsegment.png)

Para adicionar um segmento de repetição a uma função de animação, use o [**método IDCompositionAnimation::AddRepeat.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat)

### <a name="end-segment"></a>Segmento final

Depois de construir uma função de animação de segmentos, você pode anexar um segmento final para fazer com que a função de animação termine em um momento específico. Se você não anexar um segmento final, o segmento final da função de animação será executado indefinidamente.

Você anexa um segmento final chamando o método [**IDCompositionAnimation::End,**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) especificando um deslocamento do início da função de animação que indica o ponto de extremidade da função. O deslocamento deve ser maior que o deslocamento inicial do segmento anterior. Além disso, um segmento final não pode ser usado como o primeiro primitivo em uma função de animação.

Ao chamar [**End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), você também especifica um valor final para a propriedade que está sendo animada. A propriedade é definida como o valor final especificado no momento em que o ponto final da função de animação é atingido.

Depois de anexar um segmento final, você não pode anexar nenhum outro segmento à função de animação. Ou seja, todas as chamadas de método no objeto de animação falham, [**exceto IDCompositionAnimation::Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset). A **chamada redefinição** retorna o objeto de animação para limpar o estado em que a função de animação não contém segmentos, momento em que você pode adicionar segmentos novamente.

## <a name="compatibility-with-windows-animation-manager"></a>Compatibilidade com o Windows Animation Manager

Windows O Gerenciador de Animação (Windows Animação) saída primitivos de animação em um formato compatível com a API directComposition. Isso significa que DirectComposition pode criar animações com base em primitivos de animação criados por Windows Animação.

Para obter mais informações, [consulte Windows Animation Manager](/windows/desktop/UIAnimation/-main-portal), o método [**IUIAnimationVariable2::GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) e Gerenciando a animação [DirectComposition com Windows Animation Manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
