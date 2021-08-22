---
title: Efeito composto aritmético
description: Use o efeito composto aritmético para combinar duas imagens usando uma soma ponderada de pixels das imagens de entrada.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- efeito composto aritmético
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45976d577299bda7dfcef9bf20eff4980cc67ac105cb14fa793065d7ce1857f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641947"
---
# <a name="arithmetic-composite-effect"></a>Efeito composto aritmético

Use o efeito composto aritmético para combinar duas imagens usando uma soma ponderada de pixels das imagens de entrada.

O CLSID para esse efeito é CLSID \_ D2D1ArithmeticComposite.

-   [Fórmula](#formula)
-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="formula"></a>Fórmula

A fórmula aqui é usada para calcular esse efeito.

Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4

Em que C1, C2, C3, C4 são coeficientes definidos.

Os coeficientes são mapeados para os valores em um VECTOR 4F D2D1 \_ \_ (x, y, z, w):

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Imagem de exemplo

Um exemplo simples é adicionar os pixels de origem e de destino. No exemplo, dois retângulos arredondados são compostos juntos. O retângulo de origem é azul e o destino é vermelho.

A imagem aqui é a saída do efeito Composição Aritmética com os coeficientes da equação definidos para os valores aqui.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![uma imagem de exemplo mostrando dois retângulos arredondados do mesmo tamanho que se sobrepõem usando o efeito composto aritmético.](images/arithmetic-50-percent.png)

O resultado é que os valores de pixel para a origem e o destino são adicionados. As regiões em que os retângulos não se sobrepõem aos valores RGBA são todas 0. Em que os retângulos sobrepõem a cor é magenta porque os valores de R e B estão no máximo.

Aqui está outro exemplo de imagem com código.



| Antes da imagem 1                                                             |
|----------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg)    |
| Antes da imagem 2                                                             |
| ![a segunda imagem antes do efeito.](images/4-arthimetic-composite2.jpg) |
| Depois                                                                      |
| ![a imagem após a transformação.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coeficientes<br/> D2D1 \_ ARITHMETICCOMPOSITE \_ PROP \_ COEFFICIENTS<br/> | Os coeficientes da equação usada para compor as duas imagens de entrada. Os coeficientes são sem unidade e sem limites. O tipo é D2D1 \_ VECTOR \_ 4F.<br/> O valor padrão é {1.0f, 0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> D2D1 \_ ARITHMETICCOMPOSITE \_ PROP FIX \_ \_ OUTPUT<br/> | O efeito fixa valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. <br/> Se você definir isso como TRUE, o efeito fixará os valores. Se você definir isso como FALSE, o efeito não fixará os valores de cor, mas outros efeitos e a superfície de saída poderão fixar os valores se eles não são de precisão suficiente.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

O bitmap de saída depende dos valores de coeficiente. Esses são os tamanhos de bitmap de saída possíveis.

-   Se C1 for o único coeficiente não zero, o tamanho da saída será a interseção dos retângulos de entrada.
-   Se C2 for o único coeficiente não zero, o tamanho da saída será o tamanho do retângulo De origem.
-   Se C3 for o único coeficiente não zero, o tamanho da saída será o tamanho do retângulo Destino..
-   Se todos os coeficientes são zero, o tamanho da saída é um retângulo vazio.
-   Para todos os outros valores de coeficiente, o tamanho da saída é a união dos retângulos de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

