---
title: Visão geral de transformações
description: Apresenta a API de transformação Direct2D Microsoft para Windows 7. Direct2D permite que os desenvolvedores do Win32 executem transformações gráficas 2D.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D,visão geral das transformaçãos
- Direct2D, sistemas de coordenadas
- Direct2D, renderizar destinos
- Direct2D,2D transforma
- Transformaçãos 2D
- transforms,about
- transforms, renderizar destinos
- transforms,objects
- renderizar destinos, transformar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80f2fad970af1d231adab691ad9345377c585b839053625ad49b3d8f7a9e203a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833086"
---
# <a name="transforms-overview"></a>Visão geral de transformações

Este tópico aborda os conceitos básicos Direct2D transforma e inclui exemplos de várias transformaçãos. Ele contém as seguintes partes:

-   [O que é uma Direct2D transformação?](#what-is-a-direct2d-transform)
-   [O espaço Direct2D coordenadas](#the-direct2d-coordinate-space)
-   [Criando matrizes de transformação](#creating-transformation-matrices)
-   [Renderização de transformaçãos de destino](#rendering-target-transforms)
-   [Transformar pincel](#brush-transforms)
-   [Transformações de geometria](#geometry-transforms)
-   [Como uma transformação de destino de renderização afeta clipes](#how-a-render-target-transform-affects-clips)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>O que é uma Direct2D transformação?

Uma transformação especifica como mapear os pontos de um objeto de um espaço de coordenadas para outro ou de uma posição para outra dentro do mesmo espaço de coordenadas. Esse mapeamento é descrito por uma matriz de transformação, definida como uma coleção de três linhas com três colunas de valores FLOAT, conforme mostrado na tabela a seguir.



|    &nbsp;       |       &nbsp;    |  &nbsp; |
|-----------------|-----------------|-----|
| M11Default: 1.0 | M12Default: 0.0 | 0,0 |
| M21Default: 0.0 | M22Default: 1.0 | 0,0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 | 1.0 |



 

Nessa matriz, os membros M11, M12, M21 e M22 definem uma transformação linear que pode dimensionar, girar ou distorcer um objeto; os membros OffsetX e OffsetY definem a conversão a ser aplicada após a transformação linear ter sido feita. Para transformações de afinidade, os valores na terceira coluna são sempre 0,0, 0,0 e 1,0.

Como Direct2D dá suporte apenas a transformações de afinidade (linear), sua matriz de transformação é definida como uma matriz 3 por 2, omitindo a terceira coluna da matriz de transformação anterior. A tabela a seguir mostra o layout da matriz Direct2D transformação.



|    &nbsp;       |       &nbsp;    | 
|-----------------|-----------------|
| M11Default: 1.0 | M12Default: 0.0 |
| M21Default: 0.0 | M22Default: 1.0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 |



 

Em Direct2D, essa matriz 3 por 2 é representada pela estrutura [**D2D1 \_ MATRIX \_ 3X2.**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Para simplificar as operações comuns de matriz, Direct2D também fornece uma classe chamada [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), que é derivada da estrutura **D2D1 \_ MATRIX \_ 3X2.**

O construtor padrão para [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) deixa o objeto não reinicializado. Para recuperar uma matriz de identidade, use [**Matrix3x2F::Identity.**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix)

Quando uma transformação de identidade é aplicada a um objeto, ela não altera a posição, a forma ou o tamanho do objeto. É semelhante à maneira como a multiplicação de um número por 1 não altera o número. Em outras palavras, a transformação de identidade deixa as coordenadas de pontos sozinhas e não desloca os pontos para uma nova posição. Qualquer transformação diferente da transformação de identidade modificará a posição, a forma e/ou o tamanho dos objetos.

As transformações se trata de coordenadas e entender Direct2D espaço de coordenadas é importante para entender o uso de transformações.

## <a name="the-direct2d-coordinate-space"></a>O espaço Direct2D coordenadas

Direct2D usa um espaço de coordenadas à esquerda; ou seja, os valores positivos do eixo x aumentam para a direita e os valores positivos do eixo y aumentam para baixo. Tudo na tela é posicionado em relação à origem, que é o ponto em que o eixo x e o eixo y interseccionam (0, 0), conforme mostrado na ilustração a seguir. Direct2D destinos de renderização usam esse espaço de coordenadas.

![ilustração do eixo x e eixo y de um espaço de coordenadas à esquerda](images/coordinatespace.png)

Manipulando valores em uma matriz de transformação, você pode girar, dimensionar, distorcer e mover (traduzir) um objeto. Por exemplo, se você definir OffsetX como 100 e OffsetY como 200, mova o objeto para a direita 100 pixels e 200 pixels para baixo.

Para mostrar o efeito da movimentação do objeto, você precisa aplicar a transformação de tradução para renderizar destinos, pincéis ou geometrias. A aplicação de uma transformação para renderizar destinos afeta toda a tela, ao aplicar uma transformação a um pincel ou uma geometria afeta apenas esse pincel ou geometria específico. Para criar uma matriz de transformação, use a [**classe Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f)

## <a name="creating-transformation-matrices"></a>Criando matrizes de transformação

Para criar transformações de rotação, escala, distorção e tradução, a classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornece os métodos estáticos mostrados na tabela a seguir. A coluna Exemplo da tabela contém links para os tópicos de ida e voltar que demonstram como usar cada método de transformação.



| Método                                                                   | Descrição                                                                                                     | Exemplo                                            | Ilustração                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f::rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | cria uma transformação de rotação que tem o ângulo e o ponto central especificados.                                | [como girar um objeto](how-to-rotate.md)       | ![ilustração de um quadrado girado 45 graus no sentido horário sobre o centro do quadrado original](images/rotate-ovw.png)                 |
| [**matrix3x2f::scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | cria uma transformação de escala que tem os fatores de escala e o ponto central especificados.                           | [como dimensionar um objeto](how-to-scale.md)         | ![ilustração de um quadrado dimensionado em 130%](images/scale-ovw.png)                                                                           |
| [**matrix3x2f::skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | cria uma transformação de distorção que tem os valores de eixo x e eixo y especificados e o ponto central.                 | [como distorcer um objeto](how-to-skew.md)           | ![ilustração de um quadrado distorceu 30 graus no sentido anti-horário do eixo y](images/skew-ovw.png)                                     |
| [**matrix3x2f::translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | cria uma transformação de tradução e especifica os deslocamentos na direção do eixo x e eixo y. | [como converter um objeto](how-to-translate.md) | ![ilustração de um quadrado movido 20 unidades ao longo do eixo x positivo e 10 unidades ao longo do eixo y positivo](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Renderização de transformaçãos de destino

Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Ele cria recursos para desenho e executa operações de desenho reais. Ele também fornece métodos para transformar o espaço de coordenadas. Você pode chamar o [**método ID2D1RenderTarget::SetTransform**](id2d1rendertarget-settransform.md) para aplicar a transformação especificada ao destino de renderização. Todas as operações de desenho subsequentes ocorrem no espaço transformado.

Para renderizar o conteúdo, use os métodos de desenho do destino de renderização. Antes de começar a desenhar, chame o [**método BeginDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) Para concluir a renderização de conteúdo, chame o [**método EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Para ver um exemplo, [consulte How to Apply Multiple Transforms to an Object](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Transformar pincel

Você pode ajustar a transformação no pincel chamando [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)). Para essa transformação, você pode considerar o pincel como uma grande parte do papel e dos primitivos de renderização diferentes (texto, geometria, retângulo e assim por diante) como estênceis. Quando você ajusta a transformação do pincel, é como se estivesse deslizando a grande parte do papel embaixo do estêncil, sem alterar a posição do próprio estêncil. Você pode usar essa técnica para deixar o texto desaparecer de amarelo para preto no espaço 3D.

Quando a transformação do pincel é a transformação de identidade, os pincéis aparecem no mesmo espaço de coordenadas que o destino de renderização no qual eles são desenhados. A transformação pincel permite que um chamador altere o modo como as coordenadas do pincel são mapeadas para esse espaço.

o espaço do pincel é especificado de forma diferente em Direct2D do que no Windows Presentation Foundation (WPF). no Direct2D, o espaço do pincel não é relativo ao objeto que está sendo desenhado, mas sim ao sistema de coordenadas atual do destino de renderização, transformado pela transformação do pincel, se houver. Para que o pincel preencha um objeto como foi feito no WPF, você deve converter a origem do espaço do pincel no canto superior esquerdo da caixa delimitadora do objeto e, em seguida, dimensionar o espaço do pincel para que o bloco de base preencha a caixa delimitadora do objeto.

para obter mais informações sobre transformações de pincel, consulte [visão geral de pincéis de Direct2D](direct2d-brushes-overview.md).

## <a name="geometry-transforms"></a>Transformações de geometria

Ao dimensionar, mover, traduzir ou distorcer geometrias, você pode aplicar diretamente uma transformação a uma geometria específica, não a uma transformação de destino de renderização que afetaria toda a tela. Uma transformação de destino de renderização geralmente afeta o traço e o preenchimento de uma geometria. Por outro lado, uma transformação Geometry só afeta o preenchimento de uma geometria, pois a transformação é aplicada a uma geometria antes de ser traçada.

> [!Note]  
> a partir do Windows 8, a transformação do mundo não afeta o traço se você definir o tipo de traço como [**D2D1 \_ stroke \_ tipo de transformação \_ \_ fixo**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) ou [**D2D1 \_ \_ tipo de transformação \_ \_ traço**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).

 

Você pode ajustar a transformação em uma geometria chamando [**ID2D1Factory:: CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) para criar um objeto [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) . para obter mais informações sobre transformações de geometria, consulte [visão geral de geometrias de Direct2D](direct2d-geometries-overview.md).

## <a name="how-a-render-target-transform-affects-clips"></a>Como uma transformação de destino de renderização afeta os clipes

A transformação em um destino de renderização afeta como a caixa delimitadora de um clipe alinhado por eixo é computada. Quando o [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) é chamado, o parâmetro *clipRect* é transformado pela transformação do mundo atual que é definida no destino de renderização. Depois que a transformação for aplicada ao *clipRect*, a caixa delimitadora alinhada ao eixo para o *clipRect* será computada. Para eficiência, o conteúdo é recortado para essa caixa delimitadora alinhada ao eixo e não para o *clipRect* original que é passado. Os diagramas a seguir mostram como uma transformação de rotação é aplicada ao destino de renderização, o *clipRect* resultante e uma caixa delimitadora com alinhamento de eixo calculado.

1.  Suponha que o retângulo na ilustração a seguir seja um destino de renderização alinhado com os pixels da tela.

    ![ilustração de um retângulo (destino de renderização)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Aplicar uma transformação de rotação ao destino de renderização. Na ilustração a seguir, o retângulo preto representa o destino de renderização original e o retângulo tracejado vermelho representa o destino de renderização transformado.

    ![ilustração do retângulo original e um retângulo girado (destino de renderização transformado)](images/pushaxisalignedclip-step2-transformed.png)

3.  Depois que [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) é chamado, a transformação de rotação é aplicada ao *clipRect*. Na ilustração a seguir, o retângulo azul representa o *clipRect* transformado.

    ![ilustração de um retângulo azul menor (ClipRect) dentro do retângulo girado (destino de renderização transformado)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  A caixa delimitadora alinhada ao eixo é calculada. Na ilustração a seguir, o retângulo tracejado verde representa a caixa delimitadora. Todo o conteúdo é recortado nesta caixa delimitadora alinhada ao eixo.

    ![ilustração de uma caixa delimitadora verde no pequeno retângulo azul (ClipRect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Resumo

Direct2D torna fácil transformar objetos bidimensionais com espaços de coordenadas simplificados e classes relacionadas. Usando vários tipos de transformações, você pode traduzir, girar, distorcer e dimensionar seus objetos para obter muitos efeitos visuais impressionantes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> </dl>

 

 