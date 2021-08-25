---
title: Usando a cor em Direct2D
description: Usando a cor em Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe6ded6d181ebcbca402161fe6af0b8fb8dd65f7d082632474136a9bd1ff551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631508"
---
# <a name="using-color-in-direct2d"></a>Usando a cor em Direct2D

Direct2D usa o modelo de cores RGB, no qual as cores são formadas combinando valores diferentes de vermelho, verde e azul. Um quarto componente, alfa, mede a transparência de um pixel. em Direct2D, cada um desses componentes é um valor de ponto flutuante com um intervalo de \[ 0,0 1,0 \] . Para os três componentes de cor, o valor mede a intensidade da cor. Para o componente alfa, 0,0 significa completamente transparente e 1,0 significa completamente opaco. A tabela a seguir mostra as cores que resultam de várias combinações de intensidade de 100%.



| Vermelho | Verde | Azul | Color   |
|-----|-------|------|---------|
| 0   | 0     | 0    | Preto   |
| 1   | 0     | 0    | Vermelho     |
| 0   | 1     | 0    | Verde   |
| 0   | 0     | 1    | Azul    |
| 0   | 1     | 1    | Cores    |
| 1   | 0     | 1    | Magenta |
| 1   | 1     | 0    | Amarelo  |
| 1   | 1     | 1    | Branca   |



 

![uma imagem que mostra as cores RGB.](images/graphics13.png)

Os valores de cor entre 0 e 1 resultam em tons diferentes dessas cores puras. Direct2D usa a [**estrutura \_ \_ F de cor D2D1**](/windows/desktop/Direct2D/d2d1-color-f) para representar as cores. Por exemplo, o código a seguir especifica magenta.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



Você também pode especificar uma cor usando a classe [**d2d1:: colorf**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) , que deriva da estrutura de [**\_ cor \_ F do d2d1**](/windows/desktop/Direct2D/d2d1-color-f) .


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Mesclagem alfa

A mistura alfa cria áreas translúcidas combinando a cor de primeiro plano com a cor do plano de fundo, usando a fórmula a seguir.

<dl> cor = AF * CF + (1-AF) * CB  
</dl>

onde *CB* é a cor do plano de fundo, *CF* é a cor do primeiro plano e *AF* é o valor alfa da cor do primeiro plano. Esta fórmula é aplicada emparelhada a cada componente de cor. Por exemplo, suponha que a cor de primeiro plano seja **(R = 1,0, G = 0,4, B = 0,0)**, com **alfa = 0,6**, e a cor do plano de fundo seja **(R = 0,0, G = 0,5, B = 1,0)**. A cor alfa misturada resultante é:

R = (1,0 * 0,6 + 0 * 0,4) =. 6   
G = (0,4 * 0,6 + 0,5 * 0,4) =. 44  
B = (0 * 0,6 + 1,0 * 0,4) =. 40  

A imagem a seguir mostra o resultado dessa operação de mesclagem.

![uma imagem que mostra a mistura alfa.](images/graphics15.png)

## <a name="pixel-formats"></a>Formatos de pixel

A [**estrutura \_ \_ F de cor d2d1**](/windows/desktop/Direct2D/d2d1-color-f) não descreve como um pixel é representado na memória. Na maioria dos casos, isso não importa. Direct2D lida com todos os detalhes internos da tradução de informações de cores em pixels. mas talvez você precise saber o formato de pixel se estiver trabalhando diretamente com um bitmap na memória ou se combinar Direct2D com Direct3D ou GDI.

A enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) define uma lista de formatos de pixel. A lista é razoavelmente longa, mas apenas algumas delas são relevantes para Direct2D. (Os outros são usados pelo Direct3D).



| Formato de pixel                                                                                                                           | Descrição                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**\_Formato dxgi \_ B8G8R8A8 \_ UNORM**<br/> | Esse é o formato de pixel mais comum. Todos os componentes de pixel (vermelho, verde, azul e alfa) são inteiros sem sinal de 8 bits. Os componentes são organizados em ordem de *BGRA* na memória. (Veja a ilustração a seguir.)<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**\_Formato dxgi \_ R8G8B8A8 \_ UNORM**<br/> | Os componentes de pixel são inteiros sem sinal de 8 bits, em ordem *RGBA* . Em outras palavras, os componentes vermelho e azul são trocados em relação ao **\_ formato dxgi \_ B8G8R8A8 \_ UNORM**. Esse formato tem suporte apenas para dispositivos de hardware.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**\_Formato dxgi \_ a8 \_ UNORM**<br/>                   | Este formato contém um componente alfa de 8 bits, sem componentes RGB. É útil para criar máscaras de opacidade. para ler mais sobre como usar máscaras de opacidade em Direct2D, consulte [visão geral de destinos de renderização A8 compatíveis](/windows/desktop/Direct2D/compatible-a8-rendertargets).<br/> |



 

A ilustração a seguir mostra o layout de pixel BGRA.

![um diagrama que mostra o layout de pixel BGRA.](images/graphics14.png)

Para obter o formato de pixel de um destino de renderização, chame [**ID2D1RenderTarget:: GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat). O formato de pixel pode não corresponder à resolução de vídeo. Por exemplo, a exibição pode ser definida como cor de 16 bits, embora o destino de renderização use a cor de 32 bits.

### <a name="alpha-mode"></a>Modo alfa

Um destino de renderização também tem um modo alfa, que define como os valores Alfa são tratados.



| Modo alfa                           | Descrição                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ Ignorar modo alfa \_ d2d1**        | Nenhuma mistura alfa é executada. Os valores Alfa são ignorados.                                                                                                                                                                                                                                                                          |
| **\_Modo alfa \_ d2d1 \_ reto**      | Direto alfa. Os componentes de cor do pixel representam a intensidade de cor antes da mesclagem alfa.                                                                                                                                                                                                                           |
| **Modo alfa D2D1 pré- \_ \_ \_ multiplicado** | Alfa precalculado. Os componentes de cor do pixel representam a intensidade da cor multiplicada pelo valor alfa. Esse formato é mais eficiente para renderizar do que o Straight Alpha, pois o termo (AF CF) da fórmula de mesclagem alfa é previamente computado. No entanto, esse formato não é apropriado para armazenar em um arquivo de imagem. |



 

Aqui está um exemplo da diferença entre alfa linear e semimultiplicado alfa. Suponha que a cor desejada seja vermelha pura (intensidade de 100%) com 50% alfa. como um tipo de Direct2D, essa cor seria representada como (1, 0, 0, 0,5). Usando o Straight Alpha e supondo componentes de cor de 8 bits, o componente vermelho do pixel é 0xFF. Usando alfa precalculado, o componente vermelho é dimensionado por 50% para 0x80 igual a.

O tipo de dados [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) sempre representa as cores usando alfa linear. Direct2D converte pixels em formato alfa premultiplicado, se necessário.

Se você souber que seu programa não executará nenhuma mistura alfa, crie o destino de renderização com o **modo \_ alfa \_ d2d1 \_ ignore** o modo alfa. esse modo pode melhorar o desempenho, pois Direct2D pode ignorar os cálculos alfa. para obter mais informações, consulte [melhorando o desempenho de aplicativos de Direct2D](/windows/desktop/Direct2D/improving-direct2d-performance).

## <a name="next"></a>Avançar

[Aplicar transformações em Direct2D](applying-transforms-in-direct2d.md)

 

