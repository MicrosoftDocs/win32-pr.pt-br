---
description: Formatos de YUV de 8 bits recomendados para renderização de vídeo
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formatos de YUV de 8 bits recomendados para renderização de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6e30f33c59bedf9a2e842d2d33328bd97d8078d21bda90ae84af9af00ec113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722043"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Formatos de YUV de 8 bits recomendados para renderização de vídeo

Carlos Sullivan e Stephen Estrop

Microsoft Corporation

Abril de 2002, atualizado em novembro de 2008

este tópico descreve os formatos de cores YUV de 8 bits que são recomendados para a renderização de vídeo no sistema operacional Windows. Este artigo apresenta técnicas para converter entre os formatos YUV e RGB, além de fornecer técnicas para formatos YUV de upamostragem. Este artigo destina-se a qualquer pessoa que trabalhe com decodificação de vídeo YUV ou renderização em Windows.

## <a name="introduction"></a>Introdução

Vários formatos YUV são definidos em todo o setor de vídeo. Este artigo identifica os formatos YUV de 8 bits recomendados para a renderização de vídeo no Windows. Os fornecedores de decodificadores e os fornecedores de exibição são incentivados a dar suporte aos formatos descritos neste artigo. Este artigo não aborda outros usos da cor YUV, como ainda fotografia.

Os formatos descritos neste artigo usam 8 bits por local de pixel para codificar o canal Y (também chamado de canal Luma) e usam 8 bits por amostra para codificar cada exemplo de croma U ou V. No entanto, a maioria dos formatos YUV usa menos de 24 bits por pixel em média, pois eles contêm menos amostras de você e V que de Y. Este artigo não aborda os formatos YUV com canais Y de 10 ou mais.

> [!Note]  
> Para os fins deste artigo, o termo U é equivalente a CB e o termo V é equivalente a CR.

 

Este artigo aborda os seguintes tópicos:

-   [Amostragem de YUV](#yuv-sampling). Descreve as técnicas de amostragem de YUV mais comuns.
-   [Definições de superfície](#surface-definitions). Descreve os formatos YUV recomendados.
-   O [espaço de cores e as conversões de taxa de amostragem croma](#color-space-and-chroma-sampling-rate-conversions). Fornece algumas diretrizes para converter entre os formatos YUV e RGB e para converter entre diferentes formatos YUV.
-   [Identificação dos formatos YUV no Media Foundation](#identifying-yuv-formats-in-media-foundation). Explica como descrever tipos de formato YUV no Media Foundation.

## <a name="yuv-sampling"></a>Amostragem de YUV

Os canais croma podem ter uma taxa de amostragem menor do que o canal do Luma, sem perda dramática de qualidade de perceptiva. Uma notação chamada de notação "A:B: C" é usada para descrever a frequência com que você e V são amostrados em relação a Y:

-   4:4:4 significa nenhuma diminuição dos canais de croma.
-   4:2:2 significa redução horizontal de 2:1, sem redução vertical. Cada linha de exame contém quatro exemplos de Y para cada dois exemplos de U ou V.
-   4:2:0 significa redução horizontal de 2:1, com resolução vertical de 2:1.
-   4:1:1 significa redução horizontal de 4:1, sem redução vertical. Cada linha de exame contém quatro exemplos de Y para cada exemplo de você e de V. 4:1:1 a amostragem é menos comum do que outros formatos e não é discutida detalhadamente neste artigo.

Os diagramas a seguir mostram como o croma é amostrado para cada uma das taxas de redução da resolução. Os exemplos de Luma são representados por uma cruz e os exemplos de croma são representados por um círculo.

![Figura 1. amostragem de croma](images/yuv-sampling-grids.png)

A forma dominante de 4:2:2 amostragem é definida no ITU-R recomendação BT. 601. Há duas variantes comuns de 4:2:0 amostragem. um deles é usado no vídeo mpeg-2 e o outro é usado em mpeg-1 e no ITU-T Recomendações H. 261 e h. 263.

Em comparação com o esquema MPEG-1, é mais simples converter entre o esquema MPEG-2 e as grades de amostragem definidas para os formatos 4:2:2 e 4:4:4. por esse motivo, o esquema MPEG-2 é preferencial em Windows e deve ser considerado a interpretação padrão dos formatos 4:2:0.

## <a name="surface-definitions"></a>Definições de superfície

Esta seção descreve os formatos YUV de 8 bits recomendados para a renderização de vídeo. Eles se enquadram em várias categorias:

-   [4:4:4 formatos, 32 bits por pixel](#444-formats-32-bits-per-pixel)
-   [4:2:2 formatos, 16 bits por pixel](#422-formats-16-bits-per-pixel)
-   [4:2:0 formatos, 16 bits por pixel](#420-formats-16-bits-per-pixel)
-   [4:2:0 formatos, 12 bits por pixel](#420-formats-12-bits-per-pixel)

Primeiro, você deve estar ciente dos seguintes conceitos para entender o que segue:

-   *Origem da superfície*. Para os formatos YUV descritos neste artigo, a origem (0, 0) é sempre o canto superior esquerdo da superfície.
-   *Stride*. O stride de uma superfície, às vezes chamada de pitch, é a largura da superfície em bytes. Dada uma origem da superfície no canto superior esquerdo, o stride é sempre positivo.
-   *Alinhamento*. O alinhamento de uma superfície é a critério do driver de vídeo de gráficos. A superfície sempre deve ser alinhada em DWORD; ou seja, as linhas individuais dentro da superfície têm a garantia de serem originadas em um limite de 32 bits (DWORD). No entanto, o alinhamento pode ser maior que 32 bits, dependendo das necessidades do hardware.
-   Formato embalado versus formato planar. Os formatos YUV são divididos em formatos *compactados* e formatos de *planar* . Em um formato empacotado, os componentes Y, U e V são armazenados em uma única matriz. Os pixels são organizados em grupos de macropixels, cujo layout depende do formato. Em um formato planar, os componentes Y, U e V são armazenados como três planos separados.

Cada um dos formatos YUV descritos neste artigo tem um código FOURCC atribuído. Um código FOURCC é um inteiro sem sinal de 32 bits que é criado pela concatenação de quatro caracteres ASCII.

-   4:4:4 (32 bpp)
    -   [AYUV](#ayuv)
-   4:2:2 (16 BPP)
    -   [YUY2](#yuy2)
    -   [UYVY](#uyvy)
-   4:2:0 (16 BPP)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 BPP)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>4:4:4 formatos, 32 bits por pixel

### <a name="ayuv"></a>AYUV

Um único formato 4:4:4 é recomendado, com o código FOURCC AYUV. Esse é um formato empacotado, em que cada pixel é codificado como quatro bytes consecutivos, organizados na sequência mostrada na ilustração a seguir.

![Figura 2. layout de memória ayuv](images/yuvformats01.gif)

Os bytes marcados como um contêm valores para alfa.

## <a name="422-formats-16-bits-per-pixel"></a>4:2:2 formatos, 16 bits por pixel

São recomendados dois formatos 4:2:2, com os seguintes códigos FOURCC:

-   YUY2
-   UYVY

Ambos são formatos compactados, em que cada macropixel é dois pixels codificados como quatro bytes consecutivos. Isso resulta em redução horizontal do Croma por um fator de dois.

### <a name="yuy2"></a>YUY2

No formato YUY2, os dados podem ser tratados como uma matriz de valores de **caracteres** não assinados, onde o primeiro byte contém o primeiro exemplo y, o segundo byte contém o primeiro exemplo U (CB), o terceiro byte contém o segundo exemplo de y e o quarto byte contém o primeiro exemplo V (CR), como mostrado no diagrama a seguir.

![Figura 3. layout de memória YUY2](images/yuvformats02.gif)

Se a imagem for endereçada como uma matriz de valores de **palavras** little-endian, a primeira **palavra** conterá a primeira amostra Y do bits menos significativo (LSBs) e o primeiro exemplo U (CB) nos bits mais significativos (MSBs). A segunda **palavra** contém o segundo exemplo de Y no LSBs e o primeiro exemplo de V (CR) no MSBs.

YUY2 é o formato de pixel preferido de 4:2:2 para aceleração de vídeo do Microsoft DirectX (DirectX VA). Espera-se que seja um requisito de termo intermediário para o DirectX VA Accelerators com suporte para vídeo 4:2:2.

### <a name="uyvy"></a>UYVY

Esse formato é o mesmo que o formato YUY2, exceto que a ordem de bytes é invertida, ou seja, os bytes croma e Luma são invertidos (Figura 4). Se a imagem for endereçada como uma matriz de dois valores de **palavra** little-endian, a primeira **palavra** conterá U no LSBs e y0 no MSBs, e a segunda **palavra** conterá V no LSBs e Y1 no MSBs.

![Figura 4. layout de memória UYVY](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>4:2:0 formatos, 16 bits por pixel

Dois formatos de 4:2:0 16 bits por pixel (BPP) são recomendados, com os seguintes códigos FOURCC:

-   IMC1
-   IMC3

Ambos os formatos YUV são formatos de planar. Os canais croma são subamostrados por um fator de dois nas dimensões horizontal e vertical.

### <a name="imc1"></a>IMC1

Todos os exemplos de Y aparecem primeiro na memória como uma matriz de valores de **caracteres** não assinados. Isso é seguido de todos os exemplos de V (CR) e, em seguida, de todos os exemplos de U (CB). Os planos V e U têm o mesmo Stride que o plano Y, resultando em áreas não usadas de memória, como mostra a Figura 5. Os planos de você e V devem começar nos limites de memória que são um múltiplo de 16 linhas. A Figura 5 mostra a origem de você e V para um quadro de vídeo 352 x 240. O endereço inicial dos planos você e V são calculados da seguinte maneira:

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

em que *pY* é um ponteiro de byte para o início da matriz de memória, conforme mostrado no diagrama a seguir.

![Figura 5. layout de memória imc1 (exemplo)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Esse formato é idêntico a IMC1, exceto que os planos de você e V são trocados, conforme mostrado no diagrama a seguir.

![Figura 6. layout de memória imc3](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>4:2:0 formatos, 12 bits por pixel

São recomendados quatro formatos 4:2:0 12-BPP, com os seguintes códigos FOURCC:

-   IMC2
-   IMC4
-   YV12
-   NV12

Em todos esses formatos, os canais croma são subamostrados por um fator de dois nas dimensões horizontal e vertical.

### <a name="imc2"></a>IMC2

Esse formato é o mesmo que IMC1, exceto pelas seguintes diferenças: as linhas V (CR) e U (CB) são intercaladas em limites de meia distância. Em outras palavras, cada linha de avanço na área croma começa com uma linha de exemplos de V, seguida por uma linha de exemplos de U que começa no próximo limite de meio-Stride (Figura 7). Esse layout faz uso mais eficiente do espaço de endereço do que IMC1. Ele corta o espaço de endereço croma pela metade e, portanto, o espaço de endereço total em 25%. Entre os formatos 4:2:0, IMC2 é o segundo formato preferencial, após NV12. A imagem a seguir ilustra esse processo.

![Figura 7. layout de memória imc2](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Esse formato é idêntico a IMC2, exceto que as linhas U (CB) e V (CR) são trocadas, conforme mostrado na ilustração a seguir.

![Figura 8. layout de memória imc4](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Todos os exemplos de Y aparecem primeiro na memória como uma matriz de valores de **caracteres** não assinados. Essa matriz é seguida imediatamente por todos os exemplos de V (CR). O stride do plano V é metade do Stride do plano Y; e o plano V contém metade do número de linhas que o plano Y. O plano V é seguido imediatamente por todos os exemplos de U (CB), com o mesmo Stride e número de linhas que o plano V, conforme mostrado na ilustração a seguir.

![Figura 9. layout de memória YV12](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Todos os exemplos de Y aparecem primeiro na memória como uma matriz de valores de **caracteres** não assinados com um número par de linhas. O plano Y é seguido imediatamente por uma matriz de valores de **caracteres** não assinados que contém exemplos de U (CB) e V (CR) empacotados. Quando a matriz de U-V combinada é endereçada como uma matriz de valores de **palavra** little-endian, o LSBs contém os valores U e MSBs contém os valores de V. NV12 é o formato de pixel preferencial de 4:2:0 para DirectX VA. Espera-se que seja um requisito de termo intermediário para o DirectX VA Accelerators com suporte para vídeo 4:2:0. A ilustração a seguir mostra o plano Y e a matriz que contém exemplos de você e V compactados.

![Figura 10. layout de memória NV12](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Conversões de taxa de amostragem de croma e de espaço de cor

Esta seção fornece diretrizes para a conversão entre YUV e RGB e para a conversão entre alguns formatos YUV diferentes. Consideramos dois esquemas de codificação RGB nesta seção: *computador de 8 bits RGB*, também conhecido como sRGB ou "Full-Scale" RGB, e *Studio Video RGB*, ou "RGB com sala de cabeça e Toe-Room". Eles são definidos da seguinte maneira:

-   O computador RGB usa 8 bits para cada amostra de vermelho, verde e azul. O preto é representado por R = G = B = 0 e o branco é representado por R = G = B = 255.
-   O vídeo RGB do estúdio usa um número de bits N para cada amostra de vermelho, verde e azul, em que N é 8 ou mais. O vídeo RGB do estúdio usa um fator de dimensionamento diferente do computador RGB e tem um deslocamento. O preto é representado por R = G = B = 16 \* 2 ^ (n-8) e o branco é representado por r = g = b = 235 \* 2 ^ (n-8). No entanto, os valores reais podem ficar fora desse intervalo.

o vídeo rgb do estúdio é a definição rgb preferida para vídeo em Windows, enquanto o computador RGB é a definição rgb preferida para aplicativos que não são de vídeo. Em qualquer forma de RGB, as coordenadas de desvio são conforme especificado em ITU-R BT. 709 para a definição dos primários de cor RGB. As coordenadas (x, y) de R, G e B são (0,64, 0,33), (0,30, 0,60) e (0,15, 0, 6), respectivamente. O branco de referência é D65 com coordenadas (0,3127, 0,3290). O gama nominal é 1/0.45 (aproximadamente 2,2), com gama preciso definido em detalhes em ITU-R BT. 709.

**Conversão entre RGB e 4:4:4 YUV**

Primeiro descrevemos a conversão entre RGB e 4:4:4 YUV. Para converter 4:2:0 ou 4:2:2 YUV em RGB, é recomendável converter os dados YUV para 4:4:4 YUV e, em seguida, converter de 4:4:4 YUV para RGB. O formato AYUV, que é um formato 4:4:4, usa 8 bits cada para os exemplos Y, U e V. O YUV também pode ser definido usando mais de 8 bits por amostra para alguns aplicativos.

Duas conversões de YUV dominantes de RGB foram definidas para vídeo digital. Ambos se baseiam na especificação conhecida como ITU-R recomendação BT. 709. A primeira conversão é o formulário YUV mais antigo definido para o uso de 50-Hz em BT. 709. É o mesmo que a relação especificada no ITU-R recomendação BT. 601, também conhecida por seu nome mais antigo, CCIR 601. Ele deve ser considerado o formato YUV preferencial para resolução de TV de definição padrão (720 x 576) e vídeo de resolução inferior. Ele é caracterizado pelos valores de duas constantes *Kr* e *KB*:

``` syntax
Kr = 0.299
Kb = 0.114
```

A segunda conversão é o formulário YUV mais recente definido para o uso de 60-Hz em BT. 709 e deve ser considerado o formato preferencial para resoluções de vídeo acima de SDTV. Ele é caracterizado por valores diferentes para essas duas constantes:

``` syntax
Kr = 0.2126
Kb = 0.0722
```

A conversão de RGB em YUV é definida começando com o seguinte:

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

Os valores YUV são obtidos da seguinte maneira:

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

onde

-   M é o número de bits por exemplo de YUV (M >= 8).
-   Z é a variável de nível preto. Para o computador RGB, Z é igual a 0. Para vídeo RGB do estúdio, Z é igual \* a 16 2 ^ (n-8), em que N é o número de bits por amostra RGB (N >= 8).
-   S é a variável de dimensionamento. Para o computador RGB, S é igual a 255. Para o vídeo do estúdio RGB, S é igual a 219 \* 2^(N-8).

O floor(x) da função retorna o maior inteiro menor ou igual a x. A função clip3(x, y, z) é definida da seguinte forma:

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> Clip3 deve ser implementado como uma função em vez de uma macro de pré-processador; caso contrário, várias avaliações dos argumentos ocorrerão.

 

O exemplo Y representa brilho e as amostras de você e V representam os desvios de cor para azul e vermelho, respectivamente. O intervalo nominal para Y é de 16 \* 2^(M-8) a 235 \* 2^(M-8). Preto é representado como 16 2^(M-8) e branco é representado como \* 235 \* 2^(M-8). O intervalo nominal para você e V é de 16 \* 2^(M-8) a 240 \* 2^(M-8), com o valor 128 \* 2^(M-8) representando a chroma neutra. No entanto, os valores reais podem ficar fora desses intervalos.

Para dados de entrada na forma de vídeo de estúdio RGB, a operação de clipe é necessária para manter os valores de V e você dentro do intervalo de 0 a (2^M)-1. Se a entrada for RGB do computador, a operação de clipe não será necessária, pois a fórmula de conversão não pode produzir valores fora desse intervalo.

Essas são as fórmulas exatas sem aproximação. Tudo o que segue neste documento é derivado dessas fórmulas. Esta seção descreve as seguintes conversões:

-   [Convertendo RGB888 em YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Convertendo YUV de 8 bits em RGB888](#converting-8-bit-yuv-to-rgb888)
-   [Convertendo 4:2:0 YUV em 4:2:2 YUV](#converting-420-yuv-to-422-yuv)
-   [Convertendo 4:2:2 YUV em 4:4:4 YUV](#converting-422-yuv-to-444-yuv)
-   [Convertendo 4:2:0 YUV em 4:4:4 YUV](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Convertendo RGB888 em YUV 4:4:4

No caso de entrada RGB do computador e saída BT.601 YUV de 8 bits, acreditamos que as fórmulas fornecidas na seção anterior podem ser razoavelmente aproximadas pelo seguinte:

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Essas fórmulas produzem resultados de 8 bits usando coeficientes que exigem no mínimo 8 bits de precisão (sem assinatura). Os resultados intermediários exigirão até 16 bits de precisão.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Convertendo YUV de 8 bits em RGB888

Das fórmulas RGB para YUV originais, é possível derivar as relações a seguir para BT.601.

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

Portanto, considerando:

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

as fórmulas para converter YUV em RGB podem ser derivadas da seguinte forma:

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

em `clip()` que indica o recorte para um intervalo de \[ 0,255 \] . Acreditamos que essas fórmulas podem ser razoavelmente aproximadas pelo seguinte:

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Essas fórmulas usam alguns coeficientes que exigem mais de 8 bits de precisão para produzir cada resultado de 8 bits, e os resultados intermediários exigirão mais de 16 bits de precisão.

Para converter 4:2:0 ou 4:2:2 YUV em RGB, é recomendável converter os dados YUV em 4:4:4 YUV e, em seguida, converter de 4:4:4 YUV para RGB. As seções a seguir apresentam alguns métodos para converter os formatos 4:2:0 e 4:2:2 em 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>Convertendo 4:2:0 YUV em 4:2:2 YUV

Converter 4:2:0 YUV em 4:2:2 YUV requer upconversion vertical por um fator de dois. Esta seção descreve um método de exemplo para executar a upconversion. O método presume que as imagens de vídeo são uma verificação progressiva.

> [!Note]  
> O processo de conversão de verificação entrelaçados de 4:2:0 a 4:2 apresenta problemas atípicos e é difícil de implementar. Este artigo não aborda o problema de conversão de verificação entrelaçada de 4:2:0 para 4:2:2.

 

Permitir que cada linha vertical de exemplos de chroma de entrada seja uma matriz que `Cin[]` varia de 0 a N a 1. A linha vertical correspondente na imagem de saída será uma matriz que varia de `Cout[]` 0 a 2N a 1. Para converter cada linha vertical, execute o seguinte processo:

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

em que clip() indica recorte para um intervalo \[ de 0,255 \] .

> [!Note]  
> As equações para lidar com as bordas podem ser simplificadas matematicamente. Eles são mostrados neste formulário para ilustrar o efeito de fixação nas bordas da imagem.

 

Na verdade, esse método calcula cada valor ausente interpolando a curva sobre os quatro pixels adjacentes, ponderados em direção aos valores dos dois pixels mais próximos (Figura 11). O método de interpolação específico usado neste exemplo gera amostras ausentes em posições de meio inteiro usando um método conhecido chamado interpolação Catmull-Rom, também conhecido como interpolação de convolução cúbica.

![Figura 11. diagrama mostrando 4:2:0 a 4:2:2 upsampling](images/yuvformats14.gif)

Em termos de processamento de sinal, o ideal é que a upconversion vertical inclua uma compensação de deslocamento de fase para levar em conta o deslocamento vertical de meio pixel (em relação à grade de amostragem de saída 4:2:2) entre os locais das linhas de exemplo 4:2:0 e o local de cada outra linha de exemplo 4:2:2. No entanto, introduzir esse deslocamento aumentaria a quantidade de processamento necessária para gerar as amostras e torna impossível reconstruir as amostras originais 4:2:0 da imagem 4:2:2 com upsampled. Isso também torna impossível decodificar o vídeo diretamente em superfícies 4:2:2 e, em seguida, usar essas superfícies como imagens de referência para decodificar imagens subsequentes no fluxo. Portanto, o método fornecido aqui não leva em conta o alinhamento vertical preciso das amostras. Isso provavelmente não é visualmente prejudicial em resoluções de imagem razoavelmente altas.

Se você começar com o vídeo 4:2:0 que usa a grade de amostragem definida em H.261, H.263 ou vídeo MPEG-1, a fase das amostras de chroma de saída 4:2:2 também será deslocada por um deslocamento horizontal de meio pixel em relação ao espaçamento na grade de amostragem luma (um deslocamento de trimestre de pixel relativo ao espaçamento da grade de amostragem de 4:2:2 chroma). No entanto, a forma MPEG-2 de vídeo 4:2:0 é provavelmente mais usada em PCs e não é vítima desse problema. Além disso, a distinção provavelmente não é visualmente prejudicial em resoluções de imagem razoavelmente altas. Tentar corrigir esse problema criaria o mesmo tipo de problema discutido para o deslocamento de fase vertical.

## <a name="converting-422-yuv-to-444-yuv"></a>Convertendo 4:2:2 YUV em 4:4:4 YUV

Converter 4:2:2 YUV em 4:4:4 YUV requer upconversion horizontal por um fator de dois. O método descrito anteriormente para upconversion vertical também pode ser aplicado à upconversion horizontal. Para o vídeo MPEG-2 e ITU-R BT.601, esse método produzirá amostras com o alinhamento de fase correto.

## <a name="converting-420-yuv-to-444-yuv"></a>Convertendo 4:2:0 YUV em 4:4:4 YUV

Para converter 4:2:0 YUV em 4:4:4 YUV, basta seguir os dois métodos descritos anteriormente. Converta a imagem 4:2:0 em 4:2:2 e converta a imagem 4:2:2 em 4:4:4. Você também pode alternar a ordem dos dois processos upconversion, pois a ordem da operação não importa para a qualidade visual do resultado.

## <a name="other-yuv-formats"></a>Outros formatos YUV

Alguns outros formatos YUV menos comuns incluem o seguinte:

-   AI44 é um formato YUV palettizado com 8 bits por exemplo. Cada amostra contém um índice nos 4 bits mais significativos (MSBs) e um valor alfa nos 4 LSBs (bits menos significativos). O índice refere-se a uma matriz de entradas de paleta YUV, que devem ser definidas no tipo de mídia para o formato. Esse formato é usado principalmente para imagens de subpicture.
-   NV11 é um formato planar 4:1:1 com 12 bits por pixel. Os exemplos Y aparecem primeiro na memória. O plano Y é seguido por uma matriz de amostras U (Cb) e V (Cr) empacotadas. Quando a matriz U-V combinada é tratada como  uma matriz de valores word little-endian, os exemplos de U estão contidos nos LSBs de cada **WORD** e os exemplos de V estão contidos nos MSBs. (Esse layout de memória é semelhante ao NV12, embora a amostragem de chroma seja diferente.)
-   Y41P é um formato empacotado 4:1:1, com você e V amostrados a cada quarto pixel horizontalmente. Cada macropixel contém 8 pixels em três bytes, com o seguinte layout de bytes: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T é idêntico a Y41P, exceto que o bit menos significativo de cada amostra Y especifica a chave de chroma (0 = transparente, 1 = opaco).
-   Y42T é idêntico ao UYVY, exceto que o bit menos significativo de cada amostra Y especifica a chave de chroma (0 = transparente, 1 = opaco).
-   YVYU é equivalente a YUYV, exceto que os exemplos de você e V são trocados.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Identificando formatos YUV Media Foundation

Cada um dos formatos YUV descritos neste artigo tem um código FOURCC atribuído. Um código FOURCC é um inteiro sem sinal de 32 bits que é criado concatenando quatro caracteres ASCII.

Há várias macros C/C++ que facilitam declarar valores FOURCC no código-fonte. Por exemplo, a macro **MAKEMINALCC** é declarada em Mmsystem.h e a macro **DECOD** é declarada em Aviriff.h. Use-os da seguinte forma:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

Você também pode declarar um código FOURCC diretamente como um literal de cadeia de caracteres simplesmente revertendo a ordem dos caracteres. Por exemplo:

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

A reversão da ordem é necessária porque Windows sistema operacional usa uma arquitetura little-endian. 'Y' = 0x59, 'U' = 0x55 e '2' = 0x32, então '2YUY' é 0x32595559.

No Media Foundation, os formatos são identificados por um GUID de tipo principal e um GUID de subtipo. O tipo principal para formatos de vídeo de computador é sempre MFMediaType \_ Video . O subtipo pode ser construído mapeando o código FOURCC para um GUID, da seguinte forma:

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

em `XXXXXXXX` que é o código FOURCC. Portanto, o SUBtipo GUID para YUY2 é:

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

As constantes para os GUIDs de formato YUV mais comuns são definidas no arquivo de header mfapi.h. Para ver uma lista dessas constantes, consulte [GUIDs de subtipo de vídeo.](video-subtype-guids.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o vídeo yuv](about-yuv-video.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 



