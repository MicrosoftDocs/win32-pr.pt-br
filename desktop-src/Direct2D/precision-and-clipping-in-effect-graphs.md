---
title: Recorte numérico e de precisão nos grafos de efeito
description: os aplicativos que processam efeitos usando Direct2D devem tomar cuidado para alcançar o nível desejado de qualidade e previsibilidade em relação à precisão numérica.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f2af6fdee4561caa60ea22a0c700593f2333727e6c5a63c5346fdc78bbdb40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160464"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Recorte numérico e de precisão nos grafos de efeito

os aplicativos que processam efeitos usando Direct2D devem tomar cuidado para alcançar o nível desejado de qualidade e previsibilidade em relação à precisão numérica. este tópico descreve as práticas recomendadas e as configurações relevantes no Direct2D que são úteis se:

-   O grafo de efeito depende de uma precisão ou cores numéricas altas fora do \[ intervalo 0, 1 \] e você deseja garantir que eles sempre estarão disponíveis
-   Ou, o grafo de efeito depende da implementação de renderização para fixe as cores intermediárias para o \[ intervalo 0, 1 \] e você deseja garantir que esse fixação MSS sempre ocorra

geralmente, Direct2D divide um gráfico de efeito em seções e renderiza cada seção em uma etapa separada. A saída de algumas etapas pode ser armazenada em texturas de Direct3D intermediárias que, por padrão, têm uma precisão e um intervalo numérico limitados. Direct2D não faz nenhuma garantia sobre se ou onde essas texturas intermediárias são usadas. esse comportamento pode variar de acordo com os recursos de GPU, bem como entre Windows versões.

em Windows 10, Direct2D usa menos texturas intermediárias devido ao uso de vinculação de sombreador. o Direct2D pode, portanto, produzir resultados diferentes com configurações padrão do que nas versões anteriores do Windows. Isso afeta principalmente cenários em que a vinculação de sombreador é possível em um grafo de efeito, e esse grafo também contém efeitos que produzem cores de saída de intervalo estendido.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Visão geral da renderização de efeito e intermediários

para renderizar um grafo de efeito, Direct2D primeiro encontra o gráfico subjacente de "transformações", em que uma transformação é um nó de gráfico usado dentro de um efeito. há diferentes tipos de transformações, incluindo aquelas que fornecem sombreadores de Direct3D para Direct2D a serem usadas.

por exemplo, Direct2D pode renderizar um grafo de efeito da seguinte maneira:

![Grafo de efeito com texturas intermediárias](images/precision-and-clipping-1.png)

Direct2D procura oportunidades para reduzir o número de texturas intermediárias usadas para renderizar o grafo de efeito; Essa lógica é opaca para aplicativos. por exemplo, o grafo a seguir pode ser renderizado por Direct2D usando uma chamada do Direct3D draw e nenhuma textura intermediária:

![Grafo de efeito sem texturas intermediárias](images/precision-and-clipping-2.png)

antes de Windows 10, Direct2D sempre usaria texturas intermediárias se vários sombreadores de pixels fossem usados no mesmo grafo de efeito. A maioria dos efeitos internos que simplesmente ajusta os valores de cor (por exemplo, brilho ou saturação) faz isso usando sombreadores de pixel.

em Windows 10, Direct2D agora pode evitar o uso de texturas intermediárias nesses casos. Ele faz isso por meio da vinculação interna de sombreadores de pixel adjacentes. Por exemplo:

![Grafo de efeito do Windows 10 com vários sombreadores de pixel e nenhuma textura intermediária](images/precision-and-clipping-3.png)

Observe que nem todos os sombreadores de pixel adjacentes em um grafo podem ser vinculados juntos e, portanto, apenas determinados grafos produzirão uma saída diferente em Windows 10. Para obter detalhes completos, consulte [efeitos de vinculação de sombreador](effect-shader-linking.md). As principais restrições são:

-   Um efeito não será vinculado com efeitos que consomem sua saída, se o primeiro efeito estiver conectado como uma entrada para vários efeitos.
-   Um efeito não será vinculado a um conjunto de efeitos como sua entrada, se o primeiro efeito amostras de sua entrada em uma posição lógica diferente da sua saída. Por exemplo, um efeito de matriz de cor pode ser vinculado com sua entrada, mas um efeito de convolução não será.

## <a name="built-in-effect-behavior"></a>Comportamento de efeito interno

Muitos efeitos internos podem produzir cores fora do \[ intervalo de 0, 1 \] no espaço de cores unpremultiplied, mesmo quando suas cores de entrada estão dentro desse intervalo. Quando isso acontece, essas cores podem estar sujeitas ao recorte numérico. Observe que é importante considerar o intervalo de cores no espaço unpremultiplied, embora os efeitos internos normalmente produzam cores no espaço premultiplicado. Isso garante que as cores permaneçam dentro do intervalo, mesmo se outros efeitos subsequentemente unpremultiply-las.

Alguns dos efeitos que podem emitir essas cores fora do intervalo oferecem uma propriedade "ClampOutput". Elas incluem:

-   [Matriz de cores](color-matrix.md)
-   [Composto aritmético](arithmetic-composite.md)
-   [Convolve](convolve-matrix.md)
-   [Efeitos de transferência](built-in-effects.md)

Definir a propriedade ClampOutput como TRUE nesses efeitos garante que um resultado consistente será obtido, independentemente de fatores como a vinculação de sombreador. Observe que fixação MSS ocorre no espaço unpremultiplied.

Outros efeitos internos também podem produzir cores de saída além de \[ 0, 1 \] intervalo no espaço unpremultiplied, mesmo quando suas cores pixels (e propriedades de "cor", se houver) estiverem dentro desse intervalo. Elas incluem:

-   [Transformando e dimensionando efeitos](built-in-effects.md) (quando a propriedade modo de interpolação é cúbica ou cúbico de alta qualidade)
-   [Efeitos de iluminação](built-in-effects.md)
-   [Detecção de borda](edge-detection-effect.md) (quando a propriedade sobrepor bordas for verdadeira)
-   [Bem](exposure-effect.md)
-   [Composite](composite.md) (quando a propriedade Mode é mais)
-   [Temperatura e tonalidade](temperature-and-tint-effect.md)
-   [Sépia](sepia-effect.md)
-   [Saturação](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Forçando o recorte numérico dentro de um grafo de efeito

Ao usar os efeitos listados acima que não têm uma propriedade ClampOutput, os aplicativos devem considerar a possibilidade de forçar o fixação MSS numérico. Isso pode ser feito inserindo um efeito adicional no grafo que coloca seus pixels. Um efeito de matriz de cor pode ser usado, com sua propriedade ' ClampOutput ' definida como TRUE e deixando a propriedade ' ColorMatrix ' como o valor padrão (passagem).

uma segunda opção para obter resultados consistentes é solicitar que Direct2D usem texturas intermediárias que tenham maior precisão. Isso é descrito abaixo.

## <a name="controlling-precision-of-intermediate-textures"></a>Controlando a precisão das texturas intermediárias

Direct2D fornece algumas maneiras de controlar a precisão de um grafo. antes de usar formatos de alta precisão no Direct2D, os aplicativos devem garantir que eles tenham suporte suficiente pela GPU. Para verificar isso, use [**ID2D1DeviceContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).

Os aplicativos podem criar um dispositivo Direct3D usando WARP (emulação de software) para garantir que todas as precisão de buffer tenham suporte independente do hardware de GPU real no dispositivo. Isso é recomendado em cenários como aplicar efeitos a uma foto enquanto salva em disco. mesmo que Direct2D ofereça suporte a formatos de buffer de alta precisão na GPU, o uso de WARP é recomendado nesse cenário em gpus de nível de recurso 9. X, devido à precisão limitada da aritmética de sombreador e da amostragem em algumas gpus móveis de baixa energia.

em cada caso abaixo, a precisão solicitada é, na verdade, a precisão mínima Direct2D será usada. Uma precisão maior poderá ser usada se os intermediários não forem necessários. Direct2D também pode compartilhar texturas intermediárias para diferentes partes do mesmo grafo ou grafos diferentes. nesse caso Direct2D usa a precisão máxima solicitada para todas as operações envolvidas.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Seleção de precisão de ID2D1DeviceContext:: SetRenderingControls

a maneira mais simples de controlar a precisão das texturas intermediárias de Direct2D é usar [**ID2D1DeviceContext:: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)). Isso controla a precisão de todas as texturas intermediárias, contanto que uma precisão não seja também definida manualmente em efeitos ou transformações diretamente.


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  // Get the current rendering controls
  D2D1_RENDERING_CONTROLS renderingControls = {};
  Context->GetRenderingControls(&renderingControls);

  // Switch the precision within the rendering controls and set it
  renderingControls.bufferPrecision = D2D1_BUFFER_PRECISION_32BPC_FLOAT;
  Context->SetRenderingControls(&renderingControls);
}
              
```



### <a name="precision-selection-from-inputs-and-render-targets"></a>Seleção de precisão de entradas e destinos de renderização

Os aplicativos também podem contar com a precisão das entradas para um grafo de efeito controlar a precisão das texturas intermediárias. Isso é verdadeiro, desde que uma precisão de buffer não seja especificada usando [**ID2D1DeviceContext:: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)), e não seja definida manualmente em efeitos e transformação diretamente.

As precisão de entradas para efeitos são propagadas por meio do grafo para selecionar a precisão dos intermediários downstream. Onde as diferentes ramificações do grafo de efeito se encontram, a maior precisão de qualquer entrada é usada.

a precisão selecionada com base em um bitmap Direct2D é determinada em seu formato de pixel. A precisão selecionada para um [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) é determinada do formato do pixel do WIC do IWICBitmapSource subjacente usado para criar o **ID2D1ImageSource**. observe que Direct2D não permite que fontes de imagem sejam criadas com fontes de WIC usando precisão sem suporte pelo Direct2D e pela GPU.

é possível que Direct2D não possa atribuir um efeito a uma precisão com base em suas entradas. Isso acontece quando um efeito não tem entradas ou quando um [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) é usado, o que não tem precisão específica. Nesse caso, a precisão das texturas intermediárias é determinada do conjunto de bitmaps como o destino de renderização atual do contexto.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Seleção de precisão diretamente no efeito e nas transformações

A precisão mínima para texturas intermediárias também pode ser definida em locais explícitos dentro de um grafo de efeito. Isso é recomendado apenas para cenários avançados.

A precisão mínima pode ser definida usando uma propriedade em um efeito da seguinte maneira:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



Dentro de uma implementação de efeito, a precisão mínima pode ser definida usando ID2D1RenderInfo:: SetOutputPrecision da seguinte maneira:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Observe que a precisão definida em um efeito será propagada para efeitos downstream no mesmo grafo de efeito, a menos que uma precisão diferente seja definida nesses efeitos de downstream. A precisão definida em uma transformação dentro de um efeito não afeta a precisão dos nós de transformação downstream.

Abaixo está a lógica recursiva completa usada para determinar a precisão mínima para um buffer intermediário que armazena a saída de um determinado nó de transformação:

![Lógica de precisão mínima do buffer intermediário](images/precision-and-clipping-4.png)

 

 