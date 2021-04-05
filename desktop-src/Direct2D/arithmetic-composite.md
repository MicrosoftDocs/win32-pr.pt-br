---
title: Efeito composto aritmético
description: Use o efeito de composição aritmética para combinar 2 imagens usando uma soma ponderada de pixels das imagens de entrada.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- efeito composto aritmético
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918919"
---
# <a name="arithmetic-composite-effect"></a>Efeito composto aritmético

Use o efeito de composição aritmética para combinar 2 imagens usando uma soma ponderada de pixels das imagens de entrada.

O CLSID para esse efeito é CLSID \_ D2D1ArithmeticComposite.

-   [Fórmula](#formula)
-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="formula"></a>Fórmula

A fórmula aqui é usada para computar esse efeito.

Saída<sub>RGBA</sub> = destino \* de<sub>RGBA</sub> de origem de fonte de software \* <sub>RGBA</sub> + C2 \* origem<sub>RGBA</sub> + C3 \* Destination<sub>RGBA</sub> + C4

Onde C1, C2, C3, C4 são os coeficientes que você define.

Os coeficientes mapeiam os valores em um \_ vetor d2d1 \_ 4F (x, y, z, w):

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Imagem de exemplo

Um exemplo simples é adicionar os pixels de origem e de destino. No exemplo, 2 retângulos arredondados são compostos juntos. O retângulo de origem é azul e o destino é vermelho.

A imagem aqui é a saída do efeito composto aritmético com os coeficientes da equação definida com os valores aqui.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![uma imagem de exemplo mostrando dois retângulos arredondados do mesmo tamanho que se sobrepõem usando o efeito composto aritmético.](images/arithmetic-50-percent.png)

O resultado é que os valores de pixel para a origem e o destino são adicionados. As regiões onde os retângulos não se sobrepõem aos valores RGBA são todos 0. O local em que os retângulos se sobrepõem a cor é magenta porque os valores R e B estão no máximo.

Aqui está outra imagem de exemplo com código.



| Antes da imagem 1                                                             |
|----------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg)    |
| Antes da imagem 2                                                             |
| ![a segunda imagem antes do efeito.](images/4-arthimetic-composite2.jpg) |
| After (após)                                                                      |
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



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coeficientes<br/> Coeficientes de prop D2D1 \_ ARITHMETICCOMPOSITE \_ \_<br/> | Os coeficientes da equação usados para compor as duas imagens de entrada. Os coeficientes são sem limite e sem limites. Type é D2D1 \_ vector \_ 4F.<br/> O valor padrão é {1,0 f, 0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> \_Saída d2d1 ARITHMETICCOMPOSITE \_ prop \_ fixe \_<br/> | O efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. <br/> Se você definir isso como verdadeiro, o efeito irá fixe os valores. Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

O bitmap de saída depende dos valores de coeficiente. Esses são os tamanhos de bitmap de saída possíveis.

-   Se C1 for o único coeficiente diferente de zero, o tamanho de saída será a interseção dos retângulos de entrada.
-   Se C2 for o único coeficiente diferente de zero, o tamanho de saída será o tamanho do retângulo de origem.
-   Se C3 for o único coeficiente diferente de zero, o tamanho de saída será o tamanho do retângulo de destino.
-   Se todos os coeficientes forem zero, o tamanho de saída será um retângulo vazio.
-   Para todos os outros valores de coeficiente, o tamanho de saída é a União dos retângulos de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

