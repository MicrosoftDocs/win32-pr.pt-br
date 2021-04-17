---
title: Visão geral de realizações de geometria
description: Este tópico descreve como usar a realização de geometria de Direct2D para melhorar o desempenho de renderização de geometria do aplicativo em determinados cenários.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b903e047ee58a803a7584aaca407281fc803e30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749282"
---
# <a name="geometry-realizations-overview"></a>Visão geral de realizações de geometria

Este tópico descreve como usar a realização de geometria de [Direct2D](direct2d-portal.md) para melhorar o desempenho de renderização de geometria do aplicativo em determinados cenários.

Ele contém as seções a seguir:

-   [O que são a realização de geometria?](#what-are-geometry-realizations)
-   [Por que usar a realização de geometria?](#why-use-geometry-realizations)
-   [Quando usar a realização de geometrias](#when-to-use-geometry-realizations)
-   [Criando realizações de geometria](#creating-geometry-realizations)
-   [Desenhando a realização de geometria](#drawing-geometry-realizations)
-   [Dimensionamento de comparações de geometria](#scaling-geometry-realizations)
    -   [Usando a realização de geometria em aplicativos que não são dimensionados](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Usando a realização de geometria em aplicativos que são dimensionados por uma pequena quantidade](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Usando a realização de geometria em aplicativos que são dimensionados por uma grande quantidade](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Tópicos relacionados](#related-topics)

## <a name="what-are-geometry-realizations"></a>O que são a realização de geometria?

As realizações de geometria, introduzidas na Windows 8.1, são um novo tipo de primitivo de desenho que facilita para aplicativos [Direct2D](direct2d-portal.md) melhorar o desempenho de renderização de geometria em determinados casos. As realizações de geometria são representadas pela interface [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) .

## <a name="why-use-geometry-realizations"></a>Por que usar a realização de geometria?

Quando [Direct2D](direct2d-portal.md) renderiza um objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , ele deve converter essa geometria em um formulário que o hardware de gráficos entenda através de um processo chamado Mosaicing. Normalmente, Direct2D deve incluí Geometry a cada quadro que é desenhado, mesmo que a geometria não seja alterada. Se seu aplicativo renderizar a mesma geometria de cada quadro, a nova estrutura de remosaico representará um esforço computacional desperdiçado. É mais eficiente em cache o mosaico, ou até mesmo a rasterização completa, da geometria e para desenhar essa representação em cache em cada quadro, em vez de inclusão repetidamente.

Uma maneira comum de os desenvolvedores resolverem esse problema é armazenar em cache a rasterização completa da geometria. Em particular, é comum criar um novo bitmap, rasterizar a geometria para esse bitmap e, em seguida, desenhar esse bitmap para a cena, conforme necessário. (Essa abordagem é descrita na seção [renderização de geometria](improving-direct2d-performance.md) de aprimorar o desempenho de aplicativos Direct2D.) Embora essa abordagem seja computacionalmente eficiente, ela tem algumas desvantagens:

-   O bitmap armazenado em cache é sensível a alterações na transformação aplicada à cena. Por exemplo, dimensionar a rasterização pode resultar em um artefato de dimensionamento perceptível. A mitigação desses artefatos com algoritmos de dimensionamento de alta qualidade pode ser computacionalmente cara.
-   O bitmap em cache consome uma quantidade significativa de memória, especialmente se for rasterizado em uma resolução alta.

A realização de geometria fornece uma maneira alternativa de armazenar em cache a geometria que evita as desvantagens acima. As realizações de geometria são representadas não por pixels (como é o caso com uma rasterização completa), mas em vez de pontos em um plano matemático. Por esse motivo, eles são menos sensíveis do que rasterizações completas para dimensionar e outras manipulações e consomem significativamente menos memória.

## <a name="when-to-use-geometry-realizations"></a>Quando usar a realização de geometrias

Considere o uso de comparações de geometria quando seu aplicativo renderizar geometrias complexas cujas formas mudam com pouca frequência, mas que podem estar sujeitas a alterações de transformações.

Por exemplo, considere um aplicativo de mapeamento que mostra um mapa estático, mas que permite ao usuário ampliar e reduzir. Este aplicativo pode se beneficiar com a realização de contratações de geometria. Como as geometrias que estão sendo renderizadas permanecem estáticas, é útil armazená-las em cache para salvar o trabalho de mosaico. Mas como os mapas são dimensionados quando o usuário se aplica, o cache de uma rasterização completa não é o ideal, devido aos artefatos de dimensionamento. O cache de realizações de geometria permitiria que o aplicativo evitasse o trabalho de novo mosaico, mantendo a alta qualidade visual durante o dimensionamento.

Por outro lado, considere um aplicativo caleidoscópio com geometria animada que muda continuamente. Esse aplicativo provavelmente não se beneficiaria do uso de realizações de geometria. Como as próprias formas mudam de quadro para quadro, não é útil armazenar em cache seus mosaicos. A melhor abordagem para esse aplicativo é desenhar objetos [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) diretamente.

## <a name="creating-geometry-realizations"></a>Criando realizações de geometria

Um objeto [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) deve ser criado a partir de um objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) existente. Para criar uma realização de geometria, chame o método [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) ou o método [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) e passe o **ID2D1Geometry** para ser percebido.

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) cria uma realização do interior da forma: a região que seria desenhada chamando [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry).
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) cria uma realização do traço da forma: a região que seria desenhada chamando [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry).

Os dois tipos de realização de geometria são representados pela interface [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) .

Ao criar uma realização de geometria, [Direct2D](direct2d-portal.md) deve mesclar todas as curvas na geometria fornecida para as aproximaçãos poligonal. Você deve fornecer um parâmetro de tolerância de nivelamento para o método de criação — isso especifica a distância máxima, em pixels independentes de dispositivo (DIPs), entre a curva verdadeira da geometria e sua aproximação poligonal. Quanto menor a tolerância de nivelamento que você fornece, maior a fidelidade do objeto de realização de geometria resultante. Da mesma forma, fornecer uma tolerância de nivelamento maior produz uma realização de geometria de baixa fidelidade. Observe que as realizações de geometria de alta fidelidade são mais caras de desenhar do que as menos baratas, mas elas podem ser ampliadas ainda mais antes de introduzir artefatos visíveis. Para obter orientação sobre como usar tolerâncias de nivelamento, confira [dimensionamento](#scaling-geometry-realizations) de conversões de geometria abaixo.

> [!Note]  
> Os objetos de realização de geometria são associados a um dispositivo de gráficos específico: eles são recursos dependentes de dispositivo.

 

## <a name="drawing-geometry-realizations"></a>Desenhando a realização de geometria

O desenho de realizações de geometria é semelhante ao desenho de outros primitivos de [Direct2D](direct2d-portal.md) , como bitmaps. Para fazer isso, chame o método [**DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) e passe o objeto de realização de geometria a ser desenhado e o pincel a ser usado. Assim como ocorre com outros métodos de desenho Direct2D, você deve chamar **DrawGeometryRealization** entre chamadas para [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="scaling-geometry-realizations"></a>Dimensionamento de comparações de geometria

A realização de geometria, como outras primitivas de [Direct2D](direct2d-portal.md) , respeitam a transformação definida no contexto do dispositivo. Embora as transformações de conversão e de rotação não tenham efeito sobre a qualidade visual da realização de geometria, as transformações de escala podem produzir artefatos visuais.

Em particular, aplicar uma escala grande o suficiente a qualquer realização de geometria pode revelar a aproximação poligonal das curvas reais. A imagem aqui mostra um par de realizações de geometria elíptico (preenchimento e traço) que foram dimensionados muito longe. Os artefatos de mesclagem de curva são visíveis.

![um par de realizações de geometria elíptica (preenchimento e traço) que foram dimensionados muito longe. os artefatos de mesclagem de curva são visíveis.](images/zoomed-in.png)

Os aplicativos que são sensíveis à qualidade visual devem tomar medidas para garantir que isso não aconteça. A maneira como você lida com o dimensionamento depende das necessidades do seu aplicativo. A seguir, há várias abordagens recomendadas para vários tipos diferentes de aplicativo.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Usando a realização de geometria em aplicativos que não são dimensionados

Se seu aplicativo não executar qualquer escala na realização da geometria, será seguro criar as realizações apenas uma vez, usando uma única tolerância de nivelamento. (As transformações sem dimensionamento não afetam a qualidade visual da realização da geometria renderizada.) Use a função [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) para calcular a tolerância de nivelamento apropriada para o DPI:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Usando a realização de geometria em aplicativos que são dimensionados por uma pequena quantidade

Se seu aplicativo puder dimensionar uma realização de geometria por um valor pequeno (por exemplo, até 2x ou 3x), pode ser apropriado simplesmente criar a realização de geometria uma vez, em uma tolerância de nivelamento proporcionalmente menor do que o padrão. Isso cria uma percepção de alta fidelidade que pode ser aumentada significativamente antes de incorrer em artefatos de dimensionamento; a desvantagem é que desenhar a realização de alta fidelidade requer mais trabalho.

Por exemplo, suponha que você saiba que seu aplicativo nunca dimensionará uma realização de geometria em mais de 2x. Seu aplicativo pode criar a realização de geometria usando uma tolerância de nivelamento que é metade do valor padrão e simplesmente dimensionar a realização conforme necessário, até 2x. Use a função [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) para calcular a tolerância de nivelamento apropriada passando 2,0 como o parâmetro *maxZoomFactor* :


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);
    
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY,                           // vertical DPI
        2.0f                            // realization can be scaled by an additional 2x
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Usando a realização de geometria em aplicativos que são dimensionados por uma grande quantidade

Se seu aplicativo puder dimensionar uma realização de geometria para cima ou para baixo por grandes quantidades (por exemplo, por 10x ou mais), manipular o dimensionamento adequadamente é mais complicado.

Para a maioria desses aplicativos, a abordagem recomendada é recriar a realização de geometria em tolerâncias de nivelamento progressivamente menores conforme a cena é expandida, a fim de manter a fidelidade visual e evitar artefatos de dimensionamento. Da mesma forma, à medida que a cena é reduzida, o aplicativo deve recriar as realizações de geometria em tolerâncias de nivelamento progressivamente maiores, para evitar a renderização de detalhes que não são visíveis. O aplicativo não deve recriar a realização de geometria toda vez que a escala é alterada, pois isso anula a finalidade de armazenar em cache o trabalho de mosaico. Em vez disso, o aplicativo deve recriar a realização de geometria com menos frequência: por exemplo, após cada 2x aumento ou diminuição na escala.

Cada vez que a escala é alterada em um aplicativo em resposta à interação do usuário, o aplicativo pode comparar a nova escala em relação à escala na qual a realização da geometria foi criada pela última vez (armazenado, por exemplo, em um membro **m \_ lastScale** ). Se os dois valores estiverem próximos (nesse caso, dentro de um fator de 2), nenhuma ação adicional será executada. Mas se os dois valores não estiverem próximos, a realização da geometria será recriada. A função [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) é usada para computar uma tolerância de nivelamento apropriada para a nova escala e **m \_ lastScale** é atualizado para a nova escala.

Além disso, o aplicativo sempre cria realizações usando uma tolerância menor do que o que normalmente seria usado para a nova escala, passando um valor de 2 como o parâmetro *maxZoomFactor* para [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)). Isso permite que a nova realização de geometria seja dimensionada por um fator adicional de 2 sem incorrer em artefatos de dimensionamento.

> [!Note]  
> A abordagem descrita aqui pode não ser apropriada para todos os aplicativos. Por exemplo, se seu aplicativo permitir que a cena seja dimensionada por fatores muito grandes muito rapidamente (por exemplo, se ele contiver um controle deslizante de "zoom" que possa ser movido de 100% para 1 milhão% no intervalo de alguns quadros), essa abordagem poderá resultar em excesso de trabalho recriando a realização de geometria a cada quadro. Uma abordagem alternativa é recriar a realização de geometria somente após a conclusão de cada manipulação da escala da cena (por exemplo, depois que o usuário tiver concluído um gesto de pinçar).

 

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral de geometrias](direct2d-geometries-overview.md)

[Melhorando o desempenho de aplicativos Direct2D](improving-direct2d-performance.md)

[Diretrizes gerais para a renderização de conteúdo estático complexo](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**Função ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))