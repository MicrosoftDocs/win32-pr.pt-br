---
title: Precisão e recorte numérico em grafos de efeito
description: Os aplicativos que renderizam efeitos usando Direct2D devem tomar cuidado para atingir o nível desejado de qualidade e previsibilidade em relação à precisão numérica.
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
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Precisão e recorte numérico em grafos de efeito

Os aplicativos que renderizam efeitos usando Direct2D devem tomar cuidado para atingir o nível desejado de qualidade e previsibilidade em relação à precisão numérica. Este tópico descreve as práticas recomendadas e as configurações relevantes Direct2D que serão úteis se:

-   O grafo de efeito se baseia em alta precisão numérica ou cores fora do intervalo \[ 0, 1 e você deseja garantir que elas sempre \] estarão disponíveis
-   Ou, o grafo de efeito depende da implementação de renderização para fixar cores intermediárias ao intervalo 0, 1 e você deseja garantir que essa fixação \[ \] sempre ocorra

Direct2D geralmente divide um grafo de efeito em seções e renderiza cada seção em uma etapa separada. A saída de algumas etapas pode ser armazenada em texturas direct3D intermediárias que, por padrão, têm intervalo numérico e precisão limitados. Direct2D não garante se ou onde essas texturas intermediárias são usadas. Esse comportamento pode variar de acordo com as funcionalidades de GPU, bem como entre Windows versões.

No Windows 10, Direct2D menos texturas intermediárias devido ao uso da vinculação do sombreador. Direct2D pode, portanto, produzir resultados diferentes com configurações padrão do que nas versões Windows anteriores. Isso afeta principalmente cenários em que a vinculação do sombreador é possível em um grafo de efeito e esse grafo também contém efeitos que produzem cores de saída de intervalo estendido.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Visão geral da renderização de efeito e intermediários

Para renderizar um grafo de efeito, Direct2D primeiro encontra o grafo subjacente de "transforms", em que uma transformação é um nó de grafo usado dentro de um efeito. Há diferentes tipos de transformação, incluindo aqueles que fornecem sombreadores Direct3D para Direct2D usar.

Por exemplo, Direct2D pode renderizar um grafo de efeito da seguinte forma:

![grafo de efeito com texturas intermediárias](images/precision-and-clipping-1.png)

Direct2D procura oportunidades para reduzir o número de texturas intermediárias usadas para renderizar o grafo de efeito; essa lógica é opaca para aplicativos. Por exemplo, o grafo a seguir pode ser renderizado Direct2D uma chamada de desenho direct3D e nenhuma textura intermediária:

![grafo de efeito sem texturas intermediárias](images/precision-and-clipping-2.png)

Antes de Windows 10, Direct2D sempre usaria texturas intermediárias se vários sombreadores de pixels fossem usados no mesmo grafo de efeito. A maioria dos efeitos integrados que simplesmente ajustam valores de cor (por exemplo, Brilho ou Saturação) faz isso usando sombreadores de pixel.

No Windows 10, Direct2D agora pode evitar o uso de texturas intermediárias nesses casos. Ele faz isso vinculando internamente sombreadores de pixel adjacentes. Por exemplo:

![grafo de efeito do Windows 10 com vários sombreadores de pixel e sem texturas intermediárias](images/precision-and-clipping-3.png)

Observe que nem todos os sombreadores de pixel adjacentes em um grafo podem ser vinculados e, portanto, apenas determinados grafos produzirão uma saída diferente Windows 10. Para obter detalhes completos, [consulte Vinculação do sombreador de efeito](effect-shader-linking.md). As principais restrições são:

-   Um efeito não será vinculado a efeitos que consomem sua saída, se o primeiro efeito estiver conectado como uma entrada a vários efeitos.
-   Um efeito não será vinculado a um efeito definido como sua entrada, se o primeiro efeito amostrar sua entrada em uma posição lógica diferente da saída. Por exemplo, um efeito matriz de cores pode ser vinculado com sua entrada, mas um efeito convolução não será.

## <a name="built-in-effect-behavior"></a>Comportamento de efeito integrado

Muitos efeitos integrados podem produzir cores fora do intervalo 0, 1 no espaço de cores não aplicado, mesmo quando suas cores de entrada estão dentro \[ \] desse intervalo. Quando isso acontece, essas cores podem estar sujeitas a recorte numérico. Observe que é importante considerar o intervalo de cores em espaço não pré-aplicado, embora os efeitos interno normalmente produzam cores no espaço pré-aplicado. Isso garante que as cores permaneçam dentro do intervalo, mesmo se outros efeitos subsequentemente as desempreprecarem.

Alguns dos efeitos que podem emitir essas cores fora do intervalo oferecem uma propriedade "ClampOutput". Elas incluem:

-   [Matriz de cores](color-matrix.md)
-   [Composição aritmética](arithmetic-composite.md)
-   [Convolve](convolve-matrix.md)
-   [Efeitos de transferência](built-in-effects.md)

Definir a propriedade ClampOutput como TRUE nesses efeitos garante que um resultado consistente seja obtido, independentemente dos fatores, como a vinculação do sombreador. Observe que o fixador ocorre em espaço não aplicado.

Outros efeitos integrados também podem produzir cores de saída além do intervalo 0, 1 em espaço não pré-aplicado, mesmo quando suas cores \[ \] pixels (e propriedades "Color", se alguma) estão dentro desse intervalo. Elas incluem:

-   [Transformação e dimensionamento de efeitos](built-in-effects.md) (quando a propriedade Modo de Interpolação é Cúbica ou Cúbica de Alta Qualidade)
-   [Efeitos de iluminação](built-in-effects.md)
-   [Detecção de borda](edge-detection-effect.md) (quando a propriedade Bordas de Sobreposição é TRUE)
-   [Exposição](exposure-effect.md)
-   [Composto](composite.md) (quando a propriedade Mode é Plus)
-   [Temperatura e tonalidade](temperature-and-tint-effect.md)
-   [Sépia](sepia-effect.md)
-   [Saturação](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Forçando o recorte numérico dentro de um grafo de efeito

Ao usar efeitos listados acima que não têm uma propriedade Desprodutor, os aplicativos devem considerar forçar a fixação numérica. Isso pode ser feito inserindo um efeito adicional no grafo que fixa seus pixels. Um efeito matriz de cores pode ser usado, com sua propriedade 'ClampOutput' definida como TRUE e deixando a propriedade 'ColorMatrix' como o valor padrão (passagem).

Uma segunda opção para obter resultados consistentes é solicitar que Direct2D use texturas intermediárias que têm maior precisão. Isso é descrito abaixo.

## <a name="controlling-precision-of-intermediate-textures"></a>Controlando a precisão de texturas intermediárias

Direct2D fornece algumas maneiras de controlar a precisão de um grafo. Antes de usar formatos de alta precisão Direct2D, os aplicativos devem garantir que eles têm suporte suficiente pela GPU. Para verificar isso, use [**ID2D1DeviceContext::IsBufferPrecisionSupported.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported)

Os aplicativos podem criar um dispositivo Direct3D usando o WARP (emulação de software) para garantir que todas as precisões de buffer sejam suportadas independentemente do hardware de GPU real no dispositivo. Isso é recomendado em cenários como aplicar efeitos a uma foto ao salvar em disco. Mesmo que Direct2D suporte a formatos de buffer de alta precisão na GPU, o uso de WARP é recomendado neste cenário em GPUs de nível de recurso 9.X, devido à precisão limitada da aritmética e da amostragem do sombreador em algumas GPUs móveis de baixa potência.

Em cada caso abaixo, a precisão solicitada é, na verdade, a precisão mínima Direct2D será usada. Uma precisão mais alta poderá ser usada se intermediários não são necessários. Direct2D também pode compartilhar texturas intermediárias para diferentes partes do mesmo grafo ou grafos totalmente diferentes. Nesse caso, Direct2D a precisão máxima solicitada para todas as operações envolvidas.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Seleção de precisão de ID2D1DeviceContext::SetRenderingControls

A maneira mais simples de controlar a precisão das texturas intermediárias do Direct2D é usar [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)). Isso controla a precisão de todas as texturas intermediárias, desde que uma precisão também não seja definida manualmente sobre efeitos ou transformação diretamente.


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

Os aplicativos também podem depender da precisão das entradas para um grafo de efeito para controlar a precisão de texturas intermediárias. Isso é verdadeiro, desde que uma precisão de buffer não seja especificada usando [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))e não seja definida manualmente em efeitos e transformação diretamente.

As precisões de entradas para efeitos são propagadas por meio do grafo para selecionar a precisão de intermediários downstream. Quando diferentes branches no grafo de efeito se encontram, a maior precisão de qualquer entrada é usada.

A precisão selecionada com base em um Direct2D bitmap é determinada no formato de pixel. A precisão selecionada para [**um ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) é determinada no formato de pixel WIC do IWICBitmapSource subjacente usado para criar **o ID2D1ImageSource**. Observe que Direct2D permite que as fontes de imagem sejam criadas com fontes WIC usando precisões sem suporte Direct2D e GPU.

É possível que Direct2D possa atribuir um efeito uma precisão com base em suas entradas. Isso acontece quando um efeito não tem entradas ou quando [**um ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) é usado, que não tem precisão específica. Nesse caso, a precisão das texturas intermediárias é determinada no bitmap definido como o destino de renderização atual do contexto.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Seleção de precisão diretamente sobre o efeito e as transformaçãos

A precisão mínima para texturas intermediárias também pode ser definida em locais explícitos dentro de um grafo de efeito. Isso só é recomendado para cenários avançados.

A precisão mínima pode ser definida usando uma propriedade em um efeito da seguinte forma:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



Dentro de uma implementação de efeito, a precisão mínima pode ser definida usando ID2D1RenderInfo::SetOutputPrecision da seguinte forma:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Observe que a precisão definida em um efeito será propagada para efeitos downstream no mesmo grafo de efeito, a menos que uma precisão diferente seja definida nesses efeitos downstream. A precisão definida em uma transformação dentro de um efeito não afeta a precisão dos nós de transformação downstream.

Abaixo está a lógica recursiva completa usada para determinar a precisão mínima para um buffer intermediário que armazenar a saída de um determinado nó de transformação:

![Lógica de precisão mínima do buffer intermediário](images/precision-and-clipping-4.png)

 

 