---
title: Visão geral de transformações
description: Apresenta a API de transformação do Microsoft Direct2D para Windows 7. O Direct2D permite que os desenvolvedores do Win32 executem transformações de gráficos 2D.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Visão geral do Direct2D, transformações
- Direct2D, sistemas de coordenadas
- Direct2D, destinos de renderização
- Direct2D, transformações 2D
- transformações 2D
- transformações, sobre
- transformações, destinos de renderização
- transformações, objetos
- renderizar destinos, transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b924c51d73e71f206fbb250f4a7dd50ca71db2a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549141"
---
# <a name="transforms-overview"></a>Visão geral de transformações

Este tópico discute os conceitos básicos de transformações do Direct2D e inclui exemplos de várias transformações. Ele contém as seguintes partes:

-   [O que é uma transformação Direct2D?](#what-is-a-direct2d-transform)
-   [O espaço de coordenadas Direct2D](#the-direct2d-coordinate-space)
-   [Criando matrizes de transformação](#creating-transformation-matrices)
-   [Renderizando transformações de destino](#rendering-target-transforms)
-   [Transformações de pincel](#brush-transforms)
-   [Transformações de geometria](#geometry-transforms)
-   [Como uma transformação de destino de renderização afeta os clipes](#how-a-render-target-transform-affects-clips)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>O que é uma transformação Direct2D?

Uma transformação especifica como mapear os pontos de um objeto de um espaço de coordenadas para outro ou de uma posição para outra dentro do mesmo espaço de coordenadas. Esse mapeamento é descrito por uma matriz de transformação, definida como uma coleção de três linhas com três colunas de valores FLOAT, conforme mostrado na tabela a seguir.



|    &nbsp;       |       &nbsp;    |  &nbsp; |
|-----------------|-----------------|-----|
| M11Default: 1.0 | M12Default: 0.0 | 0.0 |
| M21Default: 0.0 | M22Default: 1.0 | 0.0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 | 1.0 |



 

Nessa matriz, os membros M11, M12, M21 e M22 definem uma transformação linear que pode dimensionar, girar ou distorcer um objeto; os membros OffsetX e OffsetY definem a conversão a ser aplicada após a transformação linear ter sido feita. Para transformações de afinidade, os valores na terceira coluna são sempre 0,0, 0,0 e 1,0.

Como o Direct2D dá suporte apenas a transformações de afinidade (linear), sua matriz de transformação é definida como uma matriz 3 por 2, omitindo a terceira coluna da matriz de transformação anterior. A tabela a seguir mostra o layout da matriz de transformação Direct2D.



|    &nbsp;       |       &nbsp;    | 
|-----------------|-----------------|
| M11Default: 1.0 | M12Default: 0.0 |
| M21Default: 0.0 | M22Default: 1.0 |
| M31OffsetX: 0.0 | M32OffsetY: 0.0 |



 

No Direct2D, essa matriz 3 por 2 é representada pela estrutura [**D2D1 \_ MATRIX \_ 3X2.**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Para simplificar as operações comuns de matriz, o Direct2D também fornece uma classe chamada [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), que é derivada da estrutura **d2d1 \_ matriz \_ 3x2** .

O construtor padrão para [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) deixa o objeto não inicializado. Para recuperar uma matriz de identidade, use [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).

Quando uma transformação de identidade é aplicada a um objeto, ela não altera a posição, a forma ou o tamanho do objeto. É semelhante à forma como multiplicar um número em 1 não altera o número. Em outras palavras, a transformação de identidade deixa as coordenadas de pontos sozinhos e não desloca os pontos para uma nova posição. Qualquer transformação que não seja a transformação de identidade modificará a posição, a forma e/ou o tamanho dos objetos.

As transformações são todas as coordenadas, e entender o espaço de coordenadas Direct2D é importante para entender o uso de transformações.

## <a name="the-direct2d-coordinate-space"></a>O espaço de coordenadas Direct2D

Direct2D usa um espaço de coordenadas da mão esquerda; ou seja, os valores positivos do eixo x aumentam para a direita e os valores positivos do eixo y aumentam para baixo. Tudo na tela é posicionado em relação à origem, que é o ponto em que o eixo x e o eixo y interseccionam (0, 0), conforme mostrado na ilustração a seguir. Os destinos de renderização Direct2D usam esse espaço de coordenadas.

![ilustração do eixo x e eixo y de um espaço de coordenadas da mão esquerda](images/coordinatespace.png)

Ao manipular valores em uma matriz de transformação, você pode girar, dimensionar, inclinar e mover (traduzir) um objeto. Por exemplo, se você definir OffsetX como 100 e OffsetY como 200, moverá o objeto para a direita de 100 pixels e para baixo em 200 pixels.

Para mostrar o efeito da movimentação do objeto, você precisa aplicar a transformação translação para renderizar destinos, pincéis ou geometrias. Aplicar uma transformação aos destinos de renderização afeta a tela inteira, ao mesmo tempo em que aplicar uma transformação a um pincel ou uma geometria afeta apenas o pincel ou a geometria específica. Para criar uma matriz de transformação, use a classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .

## <a name="creating-transformation-matrices"></a>Criando matrizes de transformação

Para criar transformações de rotação, escala, distorção e tradução, a classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornece os métodos estáticos mostrados na tabela a seguir. A coluna Exemplo da tabela contém links para os tópicos de ida e voltar que demonstram como usar cada método de transformação.



| Método                                                                   | Descrição                                                                                                     | Exemplo                                            | Ilustração                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f::rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | cria uma transformação de rotação que tem o ângulo e o ponto central especificados.                                | [como girar um objeto](how-to-rotate.md)       | ![ilustração de um quadrado girado 45 graus no sentido horário sobre o centro do quadrado original](images/rotate-ovw.png)                 |
| [**matrix3x2f::scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | cria uma transformação de escala que tem os fatores de escala e o ponto central especificados.                           | [como dimensionar um objeto](how-to-scale.md)         | ![ilustração de um quadrado dimensionado em 130%](images/scale-ovw.png)                                                                           |
| [**matrix3x2f::skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | cria uma transformação de distorção que tem os valores de eixo x e eixo y especificados e o ponto central.                 | [como distorcer um objeto](how-to-skew.md)           | ![ilustração de um quadrado distorceu 30 graus no sentido anti-horário do eixo y](images/skew-ovw.png)                                     |
| [**matrix3x2f::translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | cria uma transformação de tradução e especifica os deslocamentos na direção do eixo x e eixo y. | [como converter um objeto](how-to-translate.md) | ![ilustração de um quadrado movido 20 unidades ao longo do eixo x positivo e 10 unidades ao longo do eixo y positivo](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Renderização de transformaçãos de destino

Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Ele cria recursos para desenhar e executa operações reais de desenho. Ele também fornece métodos para transformar o espaço de coordenadas. Você pode chamar o método [**ID2D1RenderTarget:: SetTransform**](id2d1rendertarget-settransform.md) para aplicar a transformação especificada ao destino de renderização. Todas as operações de desenho subsequentes ocorrem no espaço transformado.

Para renderizar o conteúdo, use os métodos de desenho do destino de renderização. Antes de começar a desenhar, chame o método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Para concluir a renderização de conteúdo, chame o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Para obter um exemplo, consulte [como aplicar várias transformações a um objeto](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Transformações de pincel

Você pode ajustar a transformação no pincel chamando [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)). Para essa transformação, você pode considerar o pincel como uma grande parte do papel e dos primitivos de renderização diferentes (texto, geometria, retângulo e assim por diante) como estênceis. Quando você ajusta a transformação do pincel, é como se estivesse deslizando a grande parte do papel embaixo do estêncil, sem alterar a posição do próprio estêncil. Você pode usar essa técnica para deixar o texto desaparecer de amarelo para preto no espaço 3D.

Quando a transformação do pincel é a transformação de identidade, os pincéis aparecem no mesmo espaço de coordenadas que o destino de renderização no qual eles são desenhados. A transformação pincel permite que um chamador altere o modo como as coordenadas do pincel são mapeadas para esse espaço.

O espaço do pincel é especificado de forma diferente em Direct2D do que no Windows Presentation Foundation (WPF). No Direct2D, o espaço do pincel não é relativo ao objeto que está sendo desenhado, mas sim ao sistema de coordenadas atual do destino de renderização, transformado pela transformação do pincel, se houver. Para que o pincel preencha um objeto como foi feito no WPF, você deve converter a origem do espaço do pincel no canto superior esquerdo da caixa delimitadora do objeto e, em seguida, dimensionar o espaço do pincel para que o bloco de base preencha a caixa delimitadora do objeto.

Para obter mais informações sobre as transformação de pincel, consulte [Visão geral de pincéis Direct2D](direct2d-brushes-overview.md).

## <a name="geometry-transforms"></a>Transformações de geometria

Ao dimensionar, mover, converter ou distorcer geometrias, você pode aplicar diretamente uma transformação a uma geometria específica, não a uma transformação de destino de renderização que afetaria toda a tela. Uma transformação de destino de renderização geralmente afeta o traço e o preenchimento de uma geometria. Por outro lado, uma transformação de geometria afeta apenas o preenchimento de uma geometria, porque a transformação é aplicada a uma geometria antes de ser traço.

> [!Note]  
> Começando com Windows 8, a transformação de mundo não afetará o traço se você definir o tipo de traço como [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) ou [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).

 

Você pode ajustar a transformação em uma geometria chamando [**ID2D1Factory::CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) para criar um [**objeto ID2D1TransformedGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) Para obter mais informações sobre as transformação de geometria, consulte [Visão geral de geometrias Direct2D.](direct2d-geometries-overview.md)

## <a name="how-a-render-target-transform-affects-clips"></a>Como uma transformação de destino de renderização afeta clipes

A transformação em um destino de renderização afeta como a caixa delimitada de um clipe alinhado ao eixo é computada. Quando [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) é chamado, o parâmetro *clipRect* é transformado pela transformação do mundo atual que é definida no destino de renderização. Depois que a transformação é aplicada ao *clipRect*, a caixa delimitador alinhada ao eixo para *o clipRect* é computada. Para eficiência, o conteúdo é recortado para essa caixa delimitador alinhada ao eixo e não para o *clipRect* original que é passado. Os diagramas a seguir mostram como uma transformação de rotação é aplicada ao destino de renderização, ao *clipRect* resultante e a uma caixa delimitador alinhada ao eixo calculada.

1.  Suponha que o retângulo na ilustração a seguir seja um destino de renderização alinhado aos pixels da tela.

    ![ilustração de um retângulo (destino de renderização)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Aplique uma transformação de rotação ao destino de renderização. Na ilustração a seguir, o retângulo preto representa o destino de renderização original e o retângulo tracejado vermelho representa o destino de renderização transformado.

    ![ilustração do retângulo original e um retângulo girado (destino de renderização transformado)](images/pushaxisalignedclip-step2-transformed.png)

3.  Depois que [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) é chamado, a transformação de rotação é aplicada ao *clipRect*. Na ilustração a seguir, o retângulo azul representa o *clipRect* transformado.

    ![ilustração de um retângulo azul menor (ClipRect) dentro do retângulo girado (destino de renderização transformado)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  A caixa delimitadora alinhada ao eixo é calculada. Na ilustração a seguir, o retângulo tracejado verde representa a caixa delimitadora. Todo o conteúdo é recortado nesta caixa delimitadora alinhada ao eixo.

    ![ilustração de uma caixa delimitadora verde no pequeno retângulo azul (ClipRect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Resumo

O Direct2D torna mais fácil transformar objetos bidimensionais com espaços de coordenadas simplificados e classes relacionadas. Usando vários tipos de transformações, você pode traduzir, girar, distorcer e dimensionar seus objetos para obter muitos efeitos visuais impressionantes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Direct2D](reference.md)
</dt> </dl>

 

 