---
description: O codec JPEG XR nativo está disponível por meio do Windows Imaging Component (WIC). O formato JPEG XR, ao qual o codec dá suporte, foi projetado para fotografias digitais de consumidores e profissionais.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Visão geral do codec do JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784664"
---
# <a name="jpeg-xr-codec-overview"></a>Visão geral do codec do JPEG XR

O codec JPEG XR nativo está disponível por meio do Windows Imaging Component (WIC). O formato JPEG XR, ao qual o codec dá suporte, foi projetado para fotografias digitais de consumidores e profissionais.

O formato JPEG XR pode atingir até duas vezes a eficiência da compactação do formato JPEG original, com artefatos de compactação menos perceptíveis. Os recursos do JPEG XR incluem:

-   Suporte para imagens monocromáticas, RGB, CMYK e n-Channel
-   formatos de inteiro de 8, 16 e 32 bits
-   Alto intervalo dinâmico, formatos de ampla gama, usando valores de cores de ponto fixo ou ponto flutuante
-   Decodificação progressiva
-   Codificação com perdas ou sem perdas usando o mesmo algoritmo de compactação
-   Suporte para decodificação de regiões de interesse em imagens grandes

O formato JPEG XR é definido nos seguintes documentos de padrões:

-   ITU-T T. 832: *tecnologia da informação – sistema de codificação de imagem JPEG XR – especificação de codificação de imagem*
-   ISO/IEC 29199-2:2010: *tecnologia da informação – sistema de codificação de imagem JPEG XR – parte 2: especificação de codificação de imagem*

O JPEG XR Standard é amplamente baseado no formato [HD Photo](hdphoto-format-overview.md) , mas há algumas diferenças entre os dois formatos. No Windows 8, o HD Photo codec foi atualizado para dar suporte a JPEG XR. O codificador agora sempre gera um fluxo de bits compatível com o JPEG XR. O decodificador pode decodificar imagens JPEG XR e HD Photo.

Melhorias de desempenho substanciais, em relação ao codec HD Photo, foram feitas no codec JPEG XR. Por exemplo, a decodificação de imagem de subresolução, como geração de miniaturas, foi aprimorada, bem como decodificação de imagem de baixa resolução. É recomendável que você use o formato JPEG XR em vez do formato HD Photo.

## <a name="codec-information"></a>Informações do codec



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| Extensão de nome de arquivo | "jxr" e "WDP"                                                         |
| GUID do contêiner      | **\_CONTAINERFORMATWMP GUID**                                            |
| GUID do decodificador        | **\_WICWMPDECODER CLSID**                                                |
| GUID do codificador        | **\_WICWMPENCODER CLSID**                                                |
| Suporte a perfil     | O codificador e o decodificador suportam até o perfil principal e até o nível 128. |



 

## <a name="codec-features"></a>Recursos do codec

### <a name="high-dynamic-range"></a>Intervalo dinâmico alto

O JPEG XR dá suporte a imagens de intervalo alto-dinâmicas, usando cores de ponto ou de ponto flutuante. Nesses formatos de cor, o intervalo numérico de um pixel é maior do que o intervalo visível, de modo que você pode ajustar as cores acima ou abaixo do intervalo visível durante os estágios de processamento intermediário.

-   Ponto fixo: em uma representação de ponto fixo, 0 representa preto e 1,0 representa a saturação máxima. O codec do JPEG XR dá suporte a formatos de ponto fixo de 16 bits e 32 bits. Para 16 bits, 1,0 = 0x2000h, que fornece 13 bits para o intervalo visível \[ 0... 1 \] . O intervalo total é de – 4,0 a + 3,999 e é mapeado linearmente. Para 32 bits, 1,0 = 0x01000000h, o intervalo visível é de 24 bits e o intervalo total é de – 128 a + 127,999.
-   Ponto flutuante: em uma representação de ponto flutuante, 0 representa preto e 1,0 representa a saturação máxima. O codec do JPEG XR dá suporte a formatos de ponto flutuante de 16 bits e 32 bits.

### <a name="tiles"></a>Blocos

Um quadro pode ser particionado em subregiãos retangulares chamadas *blocos*. Um bloco é uma área de uma imagem que contém matrizes retangulares de macroblocos. Os blocos permitem que regiões da imagem sejam decodificadas sem processar a imagem inteira.

Durante a codificação, selecione o número de blocos definindo as propriedades **HorizontalTileSlices** e **VerticalTileSlices** . O tamanho mínimo do bloco é 16 × 16 pixels. O codificador ajusta o número de blocos para manter essa restrição. Há sobrecarga de armazenamento e processamento associada a cada bloco, portanto, você deve considerar o número de blocos necessários para cenários específicos.

### <a name="image-stream-output"></a>Saída de fluxo de imagem

O padrão JPEG-XR define duas partes de um arquivo JPEG-XR:

-   O fluxo de bits de imagem, definido no corpo do padrão.
-   O contêiner da imagem. O arquivo contém metadados EXIF e XMP e é definido no anexo A do padrão.

Ele é possível e permitido pelo padrão, para inserir o fluxo de imagem dentro de outro tipo de contêiner de arquivo. O codificador dá suporte a um modo somente de fluxo, que gera o fluxo de bits de imagem bruto sem contêiner de imagem. Um aplicativo pode armazenar o fluxo de bits em algum outro formato de contêiner.

Para habilitar o modo somente fluxo, defina a propriedade **StreamOnly** .

### <a name="image-quality-settings"></a>Configurações de qualidade da imagem

Várias propriedades de codec controlam a qualidade da imagem de saída do codificador.

-   [ImageQuality](#imagequality) é uma propriedade comum entre os codecs do WIC. Ele especifica a qualidade da imagem como um único valor de ponto flutuante de 0,0 a 1,0,
-   As propriedades [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostragem](#subsampling) fornecem mais controle sobre as configurações de qualidade.

Para usar as propriedades [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostrar](#subsampling) , defina a propriedade [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.

Se [UseCodecOptions](#usecodecoptions) for **Variant \_ false** (**Variant \_ false** é o padrão), o codificador usará a propriedade [ImageQuality](#imagequality) . O codificador mapeia o valor de ImageQuality para [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostrar](#subsampling) por meio de uma tabela de pesquisa.

O codificador não oferece suporte à propriedade **CompressionQuality** .

### <a name="compressed-domain-transcode"></a>Transcodificação de domínio compactado

O codec do JPEG XR pode executar determinadas transformações de imagem sem, na verdade, decodificar os dados compactados e codificá-los novamente. As operações de domínio compactadas são muito eficientes e evitam qualquer perda de qualidade adicional que seja típica quando você decodifica e codifica novamente uma imagem compactada com perdas.

Há suporte para as seguintes operações de domínio compactado:

-   Corte uma região da imagem.
-   Girar ou inverter a imagem.
-   Descartar dados de frequência para criar um arquivo de imagem menor.
-   Reorganizar a imagem entre a ordem espacial e de frequência.

O codificador do JPEG XR usa transcodificação de domínio compactado, se possível, quando a imagem de origem é uma imagem JPEG XR. Quando o codificador executa uma operação de domínio compactado, ele ignora as seguintes propriedades de codec: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha),[sobreposição](#overlap) [sem perdas](#lossless)e [qualidade](#image-quality-settings). Se as propriedades [HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) estiverem presentes, você deverá defini-las como zero. Você não pode alterar o tamanho de bloco de uma imagem como parte de uma transcodificação de domínio compactado.

A lista a seguir descreve como executar as transformações de imagem.

-   Para cortar a imagem, defina a região desejada no parâmetro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) do método **WriteState** .
-   Para girar ou inverter a imagem, defina a propriedade [BitmapTransform](#bitmaptransform) .
-   Para descartar dados de frequência na imagem, defina a propriedade [ImageDataDiscard](#imagedatadiscard) . Para descartar dados de frequência no canal alfa, defina a propriedade [AlphaDataDiscard](#alphadatadiscard) . A descartação de dados de frequência reduz o tamanho do arquivo codificado e pode reduzir a resolução.
-   Para alterar a organização da imagem entre frequência e ordenação espacial, defina a propriedade [FrequencyOrdering](/windows) .

Para desabilitar a transcodificação de domínio compactado e forçar o codificador a codificar novamente a imagem, defina [UseCodecOptions](#usecodecoptions) como **Variant \_ true** e defina [CompressedDomainTranscode](#compresseddomaintranscode) como **Variant \_ false**.

## <a name="encoder-options"></a>Opções de codificador

Para definir as propriedades de codificação, use a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações, consulte [visão geral da codificação](-wic-creating-encoder.md).

A lista a seguir especifica as opções de codificador.

-   [AlphaDataDiscard](#alphadatadiscard)
-   [AlphaQuality](#alphaquality)
-   [BitmapTransform](#bitmaptransform)
-   [CompressedDomainTranscode](#compresseddomaintranscode)
-   [FrequencyOrder](#frequencyorder)
-   [HorizontalTileSlices](#horizontaltileslices)
-   [IgnoreOverlap](#ignoreoverlap)
-   [ImageDataDiscard](#imagedatadiscard)
-   [ImageQuality](#imagequality)
-   [InterleavedAlpha](#interleavedalpha)
-   [Lossless](#lossless)
-   [Post](#overlap)
-   [Progressivmode](#progressivemode)
-   [Qualidade](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [Subamostragens](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

Define a quantidade de dados de frequência Alfa a serem descartados durante uma transcodificação de domínio compactado.



| Tipo de dados | VARTYPE     | Intervalo | Padrão |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 0 a 4   | Nenhum    |



 

Essa propriedade só se aplicará se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true** e a imagem contiver um canal planar ou um canal alfa intercalado. caso contrário, será ignorado.

Para imagens que contêm um canal do planar, os valores a seguir são válidos.



| Valor | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nenhum dado de frequência de imagem é Descartado.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | Os FlexBits são descartados. Isso reduz arbitrariamente a qualidade do canal do planar alfa para a imagem transcodificada. , sem uma alteração na resolução efetiva. A redução exata no tamanho do arquivo e na qualidade depende de vários fatores e não pode ser especificada com exatidão.                                                                                                                                                                                           |
| 2     | A banda de dados de frequência de passagem alta é descartada, incluindo o FlexBits. Isso reduz efetivamente a resolução do canal do planar alfa por um fator de 4 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada bloco 4x4 de pixels de canal alfa. Normalmente, você deve definir esse valor somente quando a propriedade [ImageDataDiscard](#imagedatadiscard) tiver o mesmo valor.                            |
| 3     | As faixas de dados de frequência de passagem alta e baixa são descartadas, incluindo o FlexBits. Esse ffectively reduz a resolução do canal do planar alfa por um fator de 16 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada 16x16 macrobloco de pixels de canal alfa. Normalmente, você deve definir esse valor somente quando a propriedade [ImageDataDiscard](#imagedatadiscard) tiver o mesmo valor. |
| 4     | O canal alfa é completamente Descartado. O formato de pixel da imagem transcodificada é alterado para refletir a remoção do canal alfa.                                                                                                                                                                                                                                                                                                                                |



 

Para imagens que contêm um canal alfa intercalado, o valor a seguir é válido.



| Valor | Descrição                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | O canal alfa é completamente Descartado. O formato de pixel da imagem transcodificada é alterado para refletir a remoção do canal alfa. |



 

Para alfa intercalado, a menos que essa propriedade seja definida como 4, o canal alfa é processado da mesma forma que os dados da imagem, de acordo com o valor da propriedade [ImageDataDiscard](#imagedatadiscard) .

### <a name="alphaquality"></a>AlphaQuality

Define a qualidade de compactação para a imagem do canal alfa do planar.



| Tipo de dados | VARTYPE     | Intervalo | Padrão |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 1 a 255 | 1       |



 

Essa propriedade se aplica quando a imagem tem um canal alfa e a propriedade [InterleavedAlpha](#interleavedalpha) é **Variant \_ false**. O valor 1 indica o modo sem perdas. Os valores crescentes resultam em taxas de compactação mais altas e qualidade de imagem inferior.

### <a name="bitmaptransform"></a>BitmapTransform

Especifica se a imagem é girada ou invertida quando decodificada.



| Tipo de dados | VARTYPE     | Intervalo                                                                     | Padrão                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **\_UI1 VT** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

Habilita ou desabilita a transcodificação de domínio compactado.



| Tipo de dados         | VARTYPE      | Padrão           |
|-------------------|--------------|-------------------|
| **BOOL de variante \_** | **BOOL do VT \_** | **VARIANTE \_ true** |



 

Para desabilitar operações de domínio compactado, defina essa propriedade como **Variant \_ false**.

### <a name="frequencyorder"></a>FrequencyOrder

Habilita a codificação na ordem de frequência. Implementações de dispositivo de codificadores JPEG XR podem organizar um arquivo em ordem espacial para reduzir a memória necessária durante a codificação.



| Tipo de dados         | VARTYPE      | Padrão           |
|-------------------|--------------|-------------------|
| **BOOL de variante \_** | **BOOL do VT \_** | **VARIANTE \_ true** |



 

-   **Variante \_ TRUE**: ordem de frequência. Os dados de frequência mais baixos aparecem primeiro no arquivo, e o conteúdo da imagem é agrupado por sua frequência, em vez de sua orientação espacial. Organizar um arquivo por ordem de frequência fornece o melhor desempenho para qualquer decodificação baseada em frequência.
-   **Variante \_ FALSE**: ordem espacial. A ordem espacial reduz a memória necessária durante a codificação

A ordem de frequência é recomendada, a menos que você tenha motivos específicos de desempenho ou de aplicativo para usar a ordem espacial.

### <a name="horizontaltileslices"></a>HorizontalTileSlices

Define o número de blocos horizontais.



| Tipo de dados  | VARTYPE     | Intervalo  | Padrão                      |
|------------|-------------|--------|------------------------------|
| **NUM** | **\_UI2 VT** | 0 – 4095 | (largura da imagem – 1)  >> 8 |



 

O valor é o número de subdivisões horizontais; ou seja, o número de blocos horizontais – 1.

### <a name="ignoreoverlap"></a>IgnoreOverlap

Especifica como o codificador trata os limites de bloco durante uma transcodificação de domínio compactado.



| Tipo de dados         | VARTYPE      | Padrão            |
|-------------------|--------------|--------------------|
| **BOOL de variante \_** | **BOOL do VT \_** | **VARIANTE \_ falso** |



 

Essa propriedade será aplicada somente se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true** e uma transcodificação de sub-região de exatamente um ou mais blocos for executada.

A operação padrão para uma transcodificação de região é expandir a região solicitada para incluir os pixels adjacentes que são necessários para sobrepor a decodificação das bordas da região. Se essa propriedade for definida como **Variant \_ true**, o codec ignorará os pixels adjacentes e apenas o bloco ou blocos selecionados serão extraídos. Se a imagem de origem não for um lado ou se a região solicitada incluir blocos parciais, esse parâmetro será ignorado.

### <a name="imagedatadiscard"></a>ImageDataDiscard

Define a quantidade de dados de frequência de imagem a serem descartados durante uma transcodificação de domínio compactado.



| Tipo de dados | VARTYPE     | Intervalo | Padrão |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 0 a 3   | 0       |



 

Essa propriedade só se aplicará se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true**; caso contrário, será ignorada.



| Valor | Descrição                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nenhum dado de frequência de imagem é Descartado.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | Os FlexBits são descartados. Isso reduz arbitrariamente a qualidade da imagem transcodificada sem alterar a resolução efetiva da imagem. A redução exata no tamanho do arquivo e na qualidade depende de vários fatores e não pode ser especificada com exatidão. Esse valor retorna um erro especificado para um canal alfa intercalado.                                                                                |
| 2     | A banda de dados de frequência de passagem alta é descartada, incluindo o FlexBits. Isso reduz a resolução da imagem transcodificada por um fator de 4 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada bloco de pixels 4x4. Portanto, a imagem transcodificada deve ser downsampledda adequadamente sempre que for decodificada.                             |
| 3     | As faixas de dados de frequência de passagem alta e baixa são descartadas, incluindo o FlexBits. Isso reduz a resolução da imagem transcodificada por um fator de 16 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada 16x16 macrobloco de pixels. Portanto, a imagem transcodificada deve ser downsampledda adequadamente sempre que for decodificada. |



 

Se a imagem contiver um canal alfa intercalado, o valor de [ImageDataDiscard](#imagedatadiscard) será aplicado ao canal alfa, a menos que a propriedade [AlphaDataDiscard](#alphadatadiscard) esteja definida como 4; nesse caso, o canal alfa será Descartado.

Para o planar alfa, os dados de frequência descartados são controlados pela propriedade [AlphaDataDiscard](#alphadatadiscard) .

### <a name="imagequality"></a>ImageQuality

Define a qualidade da imagem.



| Tipo de dados | VARTYPE    | Intervalo | Padrão |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0 a 1,0 | 0,9     |



 

O nível 1,0 oferece uma compactação matematicamente sem perdas.

O nível 0,0 é a configuração de qualidade mais baixa.

### <a name="interleavedalpha"></a>InterleavedAlpha

Especifica se deve codificar alfa ou planar intercalado.



| Tipo de dados         | VARTYPE      | Padrão            |
|-------------------|--------------|--------------------|
| **BOOL de variante \_** | **BOOL do VT \_** | **VARIANTE \_ falso** |



 

-   **Variante \_ TRUE**: Alpha intercalado. As informações do canal alfa são codificadas como um canal intercalado adicional, sem correlação com os canais de conteúdo da imagem. Esse modo é útil para decodificar alfa simultaneamente com a imagem quando a imagem é transmitida.
-   VARIANTE \_ false: planar alfanumérico. Um canal alfanumérico planar é codificado como uma imagem separada. Os dados da imagem e o canal alfa são decodificados de forma independente. Opcionalmente, você pode definir o nível de qualidade do canal alfa definindo a propriedade [AlphaQuality](#alphaquality) .

Há suporte para alfa intercalado apenas para determinados formatos de pixel RGB. O planar alfanumérico tem suporte para qualquer formato de imagem que define um canal alfa.

### <a name="lossless"></a>Lossless

Habilita a compactação de perdas.



| Tipo de dados         | VARTYPE      | Padrão        |
|-------------------|--------------|----------------|
| **BOOL de variante \_** | **BOOL do VT \_** | VARIANTE \_ falso |



 

Se o valor for **Variant \_ true**, o codificador usará a compactação sem perdas. Quando definido como **Variant \_ true**, essa propriedade substitui a propriedade [ImageQuality](#imagequality) .

### <a name="overlap"></a>Post

Define o nível de filtragem de sobreposição. Com a filtragem de sobreposição, os coeficientes de transformação são aplicados entre limites de bloco e macrobloco. Isso pode reduzir os artefatos de bloqueio.



| Tipo de dados | VARTYPE     | Intervalo | Padrão |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 0 a 4   | 1       |



 



| Valor | Descrição                                   |
|-------|-----------------------------------------------|
| 0     | Sem sobreposição.                                   |
| 1     | Um nível de sobreposição, divisão suave. (Padrão.) |
| 2     | Dois níveis de sobreposição, divisão suave.           |
| 3     | Um nível de sobreposição, divisão fixa             |
| 4     | Dois níveis de sobreposição, divisão fixa.           |



 

Definições:

-   Um nível de sobreposição: os valores codificados dos blocos 4x4 são modificados com base em blocos vizinhos.
-   Dois níveis de sobreposição: o primeiro nível de sobreposição é aplicado. Além disso, os valores codificados de 16x16 macroblocos são modificados com base no macroblocos vizinho.
-   Divisão suave: a filtragem de sobreposição é aplicada entre limites de bloco.
-   Divisão fixa: a filtragem de sobreposição não é aplicada entre limites de bloco. Blocos físicos podem introduzir alguns artefatos visuais ao longo dos limites de bloco.

Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.

### <a name="progressivemode"></a>Progressivmode

Habilita ou desabilita a codificação progressiva.



| Tipo de dados         | VARTYPE      | Padrão            |
|-------------------|--------------|--------------------|
| **BOOL de variante \_** | **BOOL do VT \_** | **VARIANTE \_ falso** |



 



| Valor              | Descrição                |
|--------------------|----------------------------|
| **VARIANTE \_ true**  | Modo sequencial (padrão). |
| **VARIANTE \_ falso** | Modo progressivo.          |



 

### <a name="quality"></a>Qualidade

Define a qualidade da compactação.



| Tipo de dados | VARTYPE     | Intervalo | Padrão |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 1 a 255 | 1       |



 

O valor 1 indica o modo sem perdas. Os valores crescentes resultam em taxas de compactação mais altas e qualidade de imagem inferior.

Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.

### <a name="streamonly"></a>StreamOnly

Habilita ou desabilita o modo somente fluxo.



| Tipo de dados         | VARTYPE      | Padrão            |
|-------------------|--------------|--------------------|
| **BOOL de variante \_** | **BOOL do VT \_** | **VARIANTE \_ falso** |



 



| Valor              | Descrição                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANTE \_ true**  | O codificador gera o fluxo de imagem bruta sem metadados.             |
| **VARIANTE \_ falso** | O codificador gera o formato de contêiner (fluxo de imagem mais metadados). |



 

### <a name="subsampling"></a>Subamostragens

Define a subamostra de croma. Essa propriedade só se aplica a imagens RGB.



| Tipo de dados | VARTYPE     | Intervalo | Padrão                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **\_UI1 VT** | 0 a 3   | 3 se [ImageQuality](#imagequality) > 0,8; caso contrário, 1 |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3</td>
<td>codificação 4:4:4. Preserva a resolução de croma completa.</td>
</tr>
<tr class="even">
<td>2</td>
<td>codificação 4:2:2. A resolução de croma é 1/2 de resolução de luminância.</td>
</tr>
<tr class="odd">
<td>1</td>
<td>codificação 4:2:0. A resolução de croma é 1/4 de resolução de luminância.</td>
</tr>
<tr class="even">
<td>0</td>
<td>codificação 4:0:0. Descarta todos os valores de croma e preserva apenas a luminância.
<blockquote>
[!Note]<br />
Esse modo não é recomendado, pois o codec usa uma definição ligeiramente modificada de luminância para melhorar o desempenho. Em vez disso, é melhor converter a imagem em monocromático antes da codificação.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 e 4:2:0 preservam os detalhes de luminância às custas dos detalhes da cor.

Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.

### <a name="usecodecoptions"></a>UseCodecOptions

Especifica se as propriedades de [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostragem](#subsampling) devem ser usadas em vez da propriedade [ImageQuality](#imagequality) genérica.



| Tipo de dados         | VARTYPE      | Padrão            |
|-------------------|--------------|--------------------|
| **BOOL de variante \_** | **BOOL do VT \_** | **VARIANTE \_ falso** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

Define o número de blocos horizontais.



| Tipo de dados  | VARTYPE     | Intervalo  | Padrão                       |
|------------|-------------|--------|-------------------------------|
| **NUM** | **\_UI2 VT** | 0 – 4095 | (altura da imagem – 1)  >> 8 |



 

O valor é o número de subdivisões verticais; ou seja, o número de blocos verticais – 1.

## <a name="supported-color-formats"></a>Formatos de cor com suporte

Para obter mais informações sobre esses formatos, consulte [formatos de pixel nativos](-wic-codec-native-pixel-formats.md).

-   **Formatos de inteiros RGB**
    -   \_WICPIXELFORMAT24BPPRGB GUID
    -   \_WICPIXELFORMAT24BPPBGR GUID
    -   \_WICPIXELFORMAT32BPPBGR GUID
    -   \_WICPIXELFORMAT48BPPRGB GUID
    -   \_WICPIXELFORMAT32BPPBGRA GUID
    -   \_WICPIXELFORMAT64BPPRGBA GUID
    -   \_WICPIXELFORMAT32BPPPBGRA GUID
    -   \_WICPIXELFORMAT64BPPPRGBA GUID
-   **Formatos RGB de ponto fixo**
    -   \_WICPIXELFORMAT48BPPRGBFIXEDPOINT GUID
    -   \_WICPIXELFORMAT64BPPRGBFIXEDPOINT GUID
    -   \_WICPIXELFORMAT96BPPRGBFIXEDPOINT GUID
    -   \_WICPIXELFORMAT128BPPRGBFIXEDPOINT GUID
    -   \_WICPIXELFORMAT128BPPRGBAFIXEDPOINT GUID
-   **Formatos RGB de ponto flutuante**
    -   \_WICPIXELFORMAT48BPPRGBHALF GUID
    -   \_WICPIXELFORMAT64BPPRGBHALF GUID
    -   \_WICPIXELFORMAT128BPPRGBFLOAT GUID
    -   \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID
    -   \_WICPIXELFORMAT64BPPRGBAHALF GUID
    -   \_WICPIXELFORMAT128BPPRGBAFLOAT GUID
    -   \_WICPIXELFORMAT128BPPPRGBAFLOAT GUID
-   **Formatos em escala de cinza**
    -   \_WICPIXELFORMAT8BPPGRAY GUID
    -   \_WICPIXELFORMAT16BPPGRAY GUID
    -   \_WICPIXELFORMAT16BPPGRAYFIXEDPOINT GUID
    -   \_WICPIXELFORMAT16BPPGRAYHALF GUID
    -   \_WICPIXELFORMAT32BPPGRAYFIXEDPOINT GUID
    -   \_WICPIXELFORMAT32BPPGRAYFLOAT GUID
-   **Formatos empacotados**
    -   \_WICPIXELFORMAT16BPPBGR555 GUID
    -   \_WICPIXELFORMAT16BPPBGR565 GUID
    -   \_WICPIXELFORMAT32BPPBGR101010 GUID
    -   \_WICPIXELFORMAT32BPPRGBE GUID
-   **Formatos CMYK**
    -   \_WICPIXELFORMAT40BPPCMYKALPHA GUID
    -   \_WICPIXELFORMAT64BPPCMYK GUID
    -   \_WICPIXELFORMAT80BPPCMYKALPHA GUID
-   **Formatos de N canais**
    -   \_WICPIXELFORMAT32BPP4CHANNELS GUID
    -   \_WICPIXELFORMAT40BPP5CHANNELS GUID
    -   \_WICPIXELFORMAT48BPP6CHANNELS GUID
    -   \_WICPIXELFORMAT56BPP7CHANNELS GUID
    -   \_WICPIXELFORMAT64BPP8CHANNELS GUID
    -   \_WICPIXELFORMAT32BPP3CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT40BPP4CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT48BPP5CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT56BPP6CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT64BPP7CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT72BPP8CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT48BPP3CHANNELS GUID
    -   \_WICPIXELFORMAT64BPP4CHANNELS GUID
    -   \_WICPIXELFORMAT80BPP5CHANNELS GUID
    -   \_WICPIXELFORMAT96BPP6CHANNELS GUID
    -   \_WICPIXELFORMAT128BPP8CHANNELS GUID
    -   \_WICPIXELFORMAT64BPP3CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT80BPP4CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT96BPP5CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT112BPP6CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT128BPP7CHANNELSALPHA GUID
    -   \_WICPIXELFORMAT144BPP8CHANNELSALPHA GUID

 

 
