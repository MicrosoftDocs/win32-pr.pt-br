---
title: Animação (DirectComposition)
description: Este tópico discute os conceitos básicos da animação do Microsoft DirectComposition.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7462a10fd83b45c1b90450fdde806ef306a2f6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105762059"
---
# <a name="animation-directcomposition"></a>Animação (DirectComposition)

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico discute os conceitos básicos da animação do Microsoft DirectComposition. Ela contém os seguintes tópicos:

-   [O que é uma animação?](#what-is-an-animation)
-   [Propriedades que podem ser animadas](#properties-that-can-be-animated)
-   [Funções de animação](#animation-functions)
-   [Segmentos de animação](#animation-segments)
    -   [Segmento cúbico](#cubic-segment)
    -   [Segmento sinusoidal](#sinusoidal-segment)
    -   [Repetir segmento](#repeat-segment)
    -   [Segmento final](#end-segment)
-   [Compatibilidade com o Gerenciador de animação do Windows](#compatibility-with-windows-animation-manager)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-an-animation"></a>O que é uma animação?

A *animação* é uma ilusão óptica criada com a criação rápida de alterações incrementais em um visual durante um período de tempo ao redesenhar o Visual após a realização de cada alteração. Como os reempates ocorrem rapidamente, o cérebro percebe as alterações incrementais como uma única cena de alteração, assim como em um filme ou vídeo de ação ao vivo.

A tabela a seguir descreve algumas das maneiras típicas de usar a animação.

| Animação                 | Descrição                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rolagem                 | Use a animação para adicionar recursos como a dinâmica de emulação de física a um controle de lista de rolagem.                                                                                                                                                           |
| Transições de cena         | Use a animação para criar transições de cena de navegação que fornecem continuidade entre tarefas em um fluxo de trabalho. As transições de cena de navegação fornecem contexto que mostra o usuário onde eles foram, onde eles estão e onde eles precisam ir em seguida. |
| Interações entre janelas | Anime os elementos da interface do usuário de diferentes aplicativos de forma a fornecer a percepção de continuidade direta entre eles para ajudar o usuário a concluir as tarefas que envolvem a troca de um aplicativo para outro.                                         |



 

## <a name="properties-that-can-be-animated"></a>Propriedades que podem ser animadas

No DirectComposition, você anima um Visual aplicando animação a propriedades individuais dos objetos que definem o Visual. Por exemplo, se você quiser mover um Visual horizontalmente pela tela, aplique a animação à propriedade OffsetX do Visual. Da mesma forma, se você quisesse fazer uma rotação 2D animada simples de um Visual, aplicaria a animação à propriedade Angle de um objeto de transformação 2D e, em seguida, aplicaria o objeto de transformação 2D à propriedade Transform do Visual.

DirectComposition permite aplicar animação a qualquer propriedade de objeto que usa um valor escalar. Você pode aplicar animações simultâneas a várias propriedades e a vários objetos.

DirectComposition executa animações em um thread separado. Você pode iniciar uma animação ou conjunto de animações e, em seguida, fazer outras tarefas em seus threads de aplicativo ou até mesmo colocar threads em suspensão, enquanto o mecanismo de composição executa as animações na taxa de quadros apropriada.

## <a name="animation-functions"></a>Funções de animação

O DirectComposition anima uma propriedade de objeto com base em uma função de animação que você define. Uma *função de animação* é uma construção que especifica como o valor de uma propriedade de objeto é alterado ao longo de um período de tempo. Por exemplo, você pode definir uma função de animação que altera o valor de uma propriedade de 1 para 360 ao longo de 4 segundos. Em seguida, se você aplicar a função de animação à propriedade Angle de um objeto de transformação de giro 2D e, em seguida, aplicar o objeto Transform à propriedade Transform de um Visual, a função de animação giraria o Visual em um círculo inteiro ao longo de 4 segundos.

Uma função de animação é representada por um *objeto de animação* criado por uma chamada para o método [**IDCompositionDevice:: createAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) . Você cria uma função de animação usando os métodos da interface [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) de um objeto de animação para acrescentar *segmentos de animação*, um de cada vez, à matriz que define a função de animação. Ao acrescentar um segmento, você especifica um deslocamento de base zero que marca a hora de início do segmento, em relação ao início da função de animação. Os segmentos de animação devem ser anexados em ordem crescente de tempos de início. A tentativa de acrescentar um segmento de animação cuja hora de início é anterior ou igual a um segmento anterior falhará. Uma função de animação pode ter uma hora de término especificada, indicando quando a função deve terminar.

A menos que especificado de outra forma, uma função de animação é iniciada quando o Gerenciador de Janelas da Área de Trabalho (DWM) recebe o comando para executar a animação. Cada segmento é executado até que a hora de início do próximo segmento seja atingida. Todas as alterações descontínuas que ocorrem no valor da propriedade animada entre os segmentos são consideradas alterações discretas.

Você aplica uma função de animação a uma propriedade definindo o valor da propriedade como o ponteiro [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) do objeto de animação que representa a função de animação. O mesmo objeto de animação pode ser aplicado a várias propriedades do mesmo objeto, bem como às propriedades de outros objetos criados pelo mesmo dispositivo.

## <a name="animation-segments"></a>Segmentos de animação

Os segmentos de animação são as definições de tempo fundamentais de uma função de animação; Eles são os primitivos dos quais funções de animação mais complexas e de nível mais alto são criadas. Um segmento de animação é construído a partir de uma série de parâmetros que descrevem a função e a hora em que o segmento começa, em relação ao início da função de animação. Para cada segmento, time (*t*) progride ao longo do eixo horizontal e começa em *t* = 0.

### <a name="cubic-segment"></a>Segmento cúbico

O tempo de um segmento cúbico é definido por um polinomial cúbico. Para uma determinada entrada de tempo (*t*), o valor de saída é fornecido pela seguinte equação:

*x*(*t*) = *às*³ + *BT*² + *CT*  +  *d*

O diagrama a seguir mostra uma função de animação que contém dois segmentos cúbicos. O primeiro segmento faz a transição de um valor de 0 para 16 em 4 segundos e o segundo altera o valor linearmente de 16 para 0 nos próximos 4 segundos. A primeira transição ocorre ao longo deste polinomial cúbico:

*x*(*t*) = *t*³-6 *t*² + 12 *t*

e a segunda transição ocorre ao longo deste:

*x*(*t*) =-4 *t* + 16

![diagrama de uma função de animação com dois segmentos cúbicos](images/cubicsegment.png)

Você adiciona um segmento cúbico a uma função de animação usando o método [**IDCompositionAnimation:: addcúbico**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) .

### <a name="sinusoidal-segment"></a>Segmento sinusoidal

O tempo de um segmento sinusoidal é definido pela seguinte equação:

*x*(*t*) = meio de  +  *amplitude* \* de tendência (*t* \* *frequência* \* 2 \* PI + *fase* \* PI/180,0)

Você adiciona um segmento sinusoidal a uma função de animação usando o método [**IDCompositionAnimation:: AddSinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) .

### <a name="repeat-segment"></a>Repetir segmento

Um segmento de repetição repete uma parte anterior especificada de uma função de animação. Um segmento de repetição faz com que a parte especificada da função de animação seja repetida indefinidamente até que o próximo segmento seja encontrado ou a extremidade especificada da animação seja atingida. A parte anterior de uma animação é feita de outros segmentos, incluindo outros segmentos de repetição. Um segmento de repetição não pode ser usado como o primeiro segmento em uma função de animação.

O diagrama a seguir mostra uma função de animação que consiste em dois segmentos cúbicos de duração de 4 segundos, seguidos por um segmento de repetição que dura 12 segundos. O segmento de repetição começa com 8 segundos na animação e repete os 6 segundos anteriores da animação duas vezes até que o segmento final seja atingido em 20 segundos.

![diagrama de uma função de animação que contém dois segmentos cúbicos e um segmento de repetição](images/repeatsegment.png)

Para adicionar um segmento de repetição a uma função de animação, use o método [**IDCompositionAnimation:: addrepeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) .

### <a name="end-segment"></a>Segmento final

Depois de construir uma função de animação de segmentos, você pode acrescentar um segmento final para fazer com que a função de animação termine em um momento específico. Se você não acrescentar um segmento final, o segmento final da função de animação será executado indefinidamente.

Você acrescenta um segmento final chamando o método [**IDCompositionAnimation:: End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) , especificando um deslocamento do início da função de animação que indica o ponto de extremidade da função. O deslocamento deve ser maior que o deslocamento inicial do segmento anterior. Além disso, um segmento final não pode ser usado como o primeiro primitivo em uma função de animação.

Ao chamar [**end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), você também especifica um valor final para a propriedade que está sendo animada. A propriedade é definida para o valor final especificado no momento em que o ponto final da função de animação é atingido.

Depois de acrescentar um segmento final, você não pode acrescentar outros segmentos à função de animação. Ou seja, todas as chamadas de método no objeto de animação falham, exceto [**IDCompositionAnimation:: Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset). Chamar **redefinição** retorna o objeto de animação para o estado de limpeza no qual a função de animação não contém nenhum segmento. nesse ponto, você pode adicionar novamente os segmentos.

## <a name="compatibility-with-windows-animation-manager"></a>Compatibilidade com o Gerenciador de animação do Windows

O Gerenciador de animação do Windows (animação do Windows) gera primitivos de animação em um formato compatível com a API DirectComposition. Isso significa que o DirectComposition pode criar animações com base em primitivos de animação criados pela animação do Windows.

Para obter mais informações, consulte [Gerenciador de animação do Windows](/windows/desktop/UIAnimation/-main-portal), o método [**IUIAnimationVariable2:: Getcurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) e [Gerenciando a animação DirectComposition com o Gerenciador de animação do Windows v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
