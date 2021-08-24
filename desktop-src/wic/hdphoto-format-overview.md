---
description: este tópico fornece informações sobre o codec de foto HD nativo disponível por meio do Windows o componente de geração de imagens (WIC).
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Visão geral do formato de foto HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 772c295051186069dd7be1a3efa3bfbb4e6ea919b2ab9fbe77ffd52cad1676a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881946"
---
# <a name="hd-photo-format-overview"></a>Visão geral do formato de foto HD

este tópico fornece informações sobre o codec de foto HD nativo disponível por meio do Windows o componente de geração de imagens (WIC).

> [!IMPORTANT]
>
> O formato HD Photo é uma implementação predefinida do formato JPEG XR. O formato JPEG XR foi totalmente implementado em Windows 8. Consulte a [visão geral do codec do JPEG XR](jpeg-xr-codec.md) para obter mais informações.

 

Este tópico inclui as seções a seguir.

-   [Identidade do codec](#codec-identity)
-   [Codificação](#encoding)
    -   [Opções de codificador](#encoder-options)
-   [Decodificação](#decoding)
    -   [Suporte do IWICBitmapSourceTransform](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|   Componente            | Descrição                                                                     |
|------------------------|---------------------------------------------------------------------------------|
| Nome (s) formal (es)         | foto de HD, Windows foto de mídia                                                   |
| Extensão (s) de nome de arquivo | wdp                                                                             |
| tipo MIME              | Image/vnd. ms-Photo                                                              |
| Assinatura (s) de arquivo      | Primeiros quatro bytes: 0x4949bc00 (versão 0; pré-lançamento), 0x4949bc01 (versão 1,0) |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do HD Photo codec.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATWMP GUID | 57a37caa-367a-4540-916bf183c5093a4b |
| Decodificador          | \_WICWMPDECODER CLSID     | a26cec36-234C-4950-ae16e34aace71d0d |
| Codificador          | \_WICWMPENCODER CLSID     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Codificação

A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções de codificador

Os codecs habilitados para WIC diferem no nível de opção de codificação. As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

O HD Photo codec usa ambas as opções básicas de WIC e fornece várias opções de codificação de alta definição específicas de foto. A tabela a seguir lista as opções de codificador com suporte no codec de foto HD nativo.

Opções básicas do codificador do WIC

| Nome da Propriedade | VARTYPE | Intervalo de valores | Valor padrão |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0-1,0 | 0,9 |
| [Lossless](#lossless-option) | BOOL do VT \_ | **verdadeiro**, **falso** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | \_UI1 VT | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

Opções de codificador de HD específico

| Nome da Propriedade | VARTYPE | Intervalo de valores | Valor padrão |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | BOOL do VT \_ | **verdadeiro**, **falso** | **FALSE** |
| [Qualidade](#quality-option) | \_UI1 VT | 1 - 255 | 10 |
| [Post](#overlap-option) | \_UI1 VT | 0 - 2 | 1 |
| [Subamostragens](#subsampling-option) | \_UI1 VT | 0 a 3 | 3 se ImageQuality > 0,8; caso contrário, 1; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | \_UI2 VT | 0 - 4095 | (largura da imagem – 1)  >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | \_UI2 VT | 0 - 4095 | (altura da imagem – 1)  >> 8 |
| [FrequencyOrder](#frequencyorder-option) | BOOL do VT \_ | **verdadeiro**, **falso** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | BOOL do VT \_ | **verdadeiro**, **falso** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | \_UI1 VT | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | BOOL do VT \_ | **verdadeiro**, **falso** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | \_UI1 VT | 0 a 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | \_UI1 VT | 0 - 4 | não usado. |
| [IgnoreOverlap](#ignoreoverlap-option) | BOOL do VT \_ | **verdadeiro**, **falso** | **FALSE** |


Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.

### <a name="imagequality-option"></a>Opção ImageQuality

Especifica a fidelidade da imagem desejada. 0,0 indica a menor fidelidade possível e 1,0 especifica a fidelidade mais alta. Para o formato HD Photo Image, um valor 1,0 resulta em uma compactação matematicamente sem perdas.

O valor padrão é 0,9.

### <a name="compressionquality-option"></a>Opção CompressionQuality

Especifica a qualidade de compactação desejada. 0,0 indica o esquema de compactação eficiente disponível. Normalmente, esse esquema produz uma codificação mais rápida, mas uma saída maior. Um valor de 1,0 especifica o esquema de compactação mais eficiente disponível, que normalmente produz uma codificação mais longa, mas uma saída menor.

A foto de HD não dá suporte a essa opção de codificador. Esse valor será ignorado se estiver presente na lista de parâmetros [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .

### <a name="lossless-option"></a>Opção sem perdas

Especifica se o modo de compactação de perdas deve ser usado. Para o formato de imagem de HD Photo, esse valor substitui o valor da opção [ImageQuality](#imagequality-option) .

O valor padrão é **FALSE**.

### <a name="bitmaptransform-option"></a>Opção BitmapTransform

Especifica como a imagem é transformada durante a decodificação de imagem. Você deve definir essa opção como um dos valores de enumeração [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

O valor padrão é [**WICBitmapTransformOptions:: WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="usecodecoptions-option"></a>Opção UseCodecOptions

Se o valor for VARIANT \_ true, as opções de [qualidade](#quality-option), [sobreposição](#overlap-option)e [subamostragem](#subsampling-option) , em vez do valor da opção.

O valor padrão é **FALSE**.

### <a name="quality-option"></a>Opção de qualidade

Especifica a qualidade de compactação para a imagem. Um valor de 1 indica o modo sem perdas. Os valores crescentes resultam em taxas de compactação mais altas e qualidade de imagem inferior.

O valor padrão é 10.

### <a name="overlap-option"></a>Opção de sobreposição

Especifica o nível de processamento de sobreposição.

A tabela a seguir lista os níveis de processamento de sobreposição disponíveis.



| Valor | Descrição                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nenhum processamento de sobreposição está habilitado.                                                                                                                                                           |
| 1     | Um nível de processamento de sobreposição está habilitado, modificando valores codificados em bloco 4x4 com base nos valores de blocos vizinhos.                                                                       |
| 2     | Dois níveis de processamento de sobreposição estão habilitados. Além do processamento de primeiro nível, os valores codificados dos blocos de macro 16x16 são modificados com base nos valores de blocos de macro vizinhos. |



 

O valor padrão é 1.

### <a name="subsampling-option"></a>Opção de subamostragem

Especifica a compactação adicional no espaço croma. Dessa forma, você pode preservar os detalhes de luminância às custas dos detalhes da cor. Essa opção se aplica somente a imagens RGB.

A tabela a seguir lista as opções de subamostras disponíveis.



| Valor | Descrição                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | a codificação 4:4:4 preserva a resolução de croma completa.                                                                                                                                                                                                                                            |
| 2     | a codificação 4:2:2 reduz a resolução de croma para 1/2 da resolução de luminância.                                                                                                                                                                                                                      |
| 1     | a codificação 4:2:0 reduz a resolução de croma para 1/4 da resolução de luminância.                                                                                                                                                                                                                      |
| 0     | a codificação 4:0:0 descarta todo o conteúdo do Croma e preserva apenas a luminância. Como o codec usa uma definição ligeiramente modificada de luminância para melhorar o desempenho, é recomendável que você converta uma imagem RGB em monocromático antes da codificação, em vez de usar esse modo de subamostragem croma. |



 

O valor padrão é 3 se [ImageQuality](#imagequality-option) > 0,8; caso contrário, 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>HorizontalTileSlices, opções de VerticalTileSlices

Especifique os blocos gráficos horizontais e verticais da imagem antes de executar a codificação de compactação para o desempenho ideal da decodificação de região. Dividindo a imagem em blocos retangulares durante a codificação, você pode decodificar regiões da imagem sem processar todo o fluxo de dados compactado. O valor padrão 0 não especifica nenhuma subdivisão, portanto, a imagem inteira é tratada como um único bloco. Um valor de 1 para cada parâmetro cria uma única divisão vertical e horizontal única, dividindo efetivamente a imagem em quatro blocos igualmente dimensionados. O valor máximo de 4095 para cada parâmetro divide a imagem em 4096 linhas de bloco com 4096 blocos por linha. Em outras palavras, os valores de parâmetro são iguais ao número de blocos horizontais e verticais (respectivamente) menos 1. Um bloco nunca pode ter menos de 16 pixels de largura ou altura, portanto, o codificador de fotos de alta definição pode ajustar esse parâmetro para manter o tamanho mínimo necessário do bloco. Como há sobrecarga de armazenamento e processamento associada a cada bloco, você deve escolher esses valores cuidadosamente para atender ao cenário específico.

[HorizontalTileSlices](/windows): o valor padrão é (largura da imagem – 1)  >> 8.

[VerticalTileSlices](/windows): o valor padrão é (altura da imagem – 1)  >> 8.

### <a name="frequencyorder-option"></a>Opção FrequencyOrder

Especifica que a imagem deve ser codificada em ordem de frequência. Os dados de frequência mais baixos aparecem primeiro no arquivo, e o conteúdo da imagem é agrupado por sua frequência, em vez de sua orientação espacial. Organizar um arquivo por ordem de frequência fornece o melhor desempenho para qualquer decodificação baseada em frequência e, portanto, é recomendável. Implementações de dispositivo de codificadores de fotos de HD podem organizar um arquivo em ordem espacial para reduzir a superfície de memória necessária durante a codificação.

O valor padrão é **true** e recomendamos que aplicativos e dispositivos sempre usem a ordem de frequência, a menos que você tenha motivos específicos de desempenho ou de aplicativo para usar a ordem espacial.

### <a name="interleavedalpha-option"></a>Opção InterleavedAlpha

Definir essa opção como **TRUE** instrui o codec a codificar as informações de canal alfa como um canal intercalado adicional, sem correlação com os canais de conteúdo da imagem. Esse modo é útil quando você precisa decodificar alfa simultaneamente com a imagem em um cenário de streaming.

Definir esse parâmetro como **FALSE** resulta em um canal alfa planar, codificado como uma imagem separada com seu próprio valor de Qualidade opcional. Usando um canal alfa planar, você pode decodificar os dados da imagem e o canal alfa de forma independente. Canais alfa intercalados têm suporte apenas para determinados formatos de pixel RGB. Você pode associar um canal alfa planar a qualquer formato de imagem que define um canal alfa.

O valor padrão é **FALSE**.

### <a name="alphaquality-option"></a>Opção AlphaQuality

Especifica a qualidade da compactação para a imagem de canal alfa planar. Um valor de 1 define o modo sem perda. O aumento de valores resulta em taxas de compactação mais altas e menor qualidade da imagem.

O valor padrão é 1.

### <a name="compresseddomaintranscode-option"></a>Opção CompressedDomainTranscode

Usando o HD Photo, você pode executar várias operações de transformação de arquivo sem realmente decodificar os dados compactados e recodificá-los para o arquivo de destino. As operações de domínio compactado são muito eficientes e evitam qualquer perda de qualidade adicional que seja típica quando você decodifica e codifica uma imagem compactada com perda.

Há suporte para as seguintes operações de domínio compactado:

-   Recorte uma região da imagem.
-   Executar uma transformação de rotação/in flip.
-   Descartar dados de frequência (possibilitando a criação de um arquivo de imagem menor).)
-   Reorganize a imagem entre a ordem sequencial espacial e a frequência.

O codificador do HD Photo executa uma operação de transcodificador de domínio compactado ao codificar uma imagem do HD Photo usando um decodificador hd photo como a origem da imagem. Dependendo das opções de codificação selecionadas, o codec usará uma operação de domínio compactada, se possível. Se um aplicativo optar por inibir explicitamente qualquer operação de transcódigo de domínio compactado, você deverá definir a *opção UseCodecOptions* como **TRUE** e a *opção CompressedDomainTranscode* como **FALSE.**

Quando o codec executa uma operação de domínio compactada, apenas determinadas configurações de propriedade e parâmetro de codificador são permitidas.

-   As opções básicas do codificador [ImageQuality,](#imagequality-option) [CompressionQuality](/windows) e [Lossless](#lossless-option) são ignoradas.
-   As opções do codificador específico do HD [Photo Quality](#quality-option), [Overlap](#overlap-option), [InterleavedAlpha](#interleavedalpha-option) e [AlphaQuality](#alphaquality-option) são ignoradas.
-   Se estiver presente, [as opções HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) deverão ser definidas como zero. O tamanho do peça de uma imagem não pode ser alterado como parte de um transcódigo de domínio compactado.
-   Você pode alterar a organização da imagem entre a frequência e a ordenação espacial especificando o valor apropriado das [opções FrequencyOrdering.](/windows)
-   Uma rotação cardinal e/ou operação de invasão horizontal/vertical pode ser executada com base no valor especificado na opção do codificador [BitmapTransform.](#bitmaptransform-option)
-   A imagem pode ser cortada especificando a região desejada usando o [**parâmetro WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) do método **codificador WriteSource.**
-   Os dados de imagem e/ou alfa podem ser descartados especificando os valores apropriados nas opções [ImageDataDiscard](#imagedatadiscard-option) e/ou [AlphaDataDiscard,](#alphadatadiscard-option) reduzindo o tamanho do arquivo codificado e reduzindo efetivamente a resolução da nova imagem.

O valor padrão é **TRUE** e recomendamos que os aplicativos e dispositivos sempre usem a ordem de frequência, a menos que você tenha motivos específicos de desempenho ou aplicativo para usar a ordem espacial.

### <a name="imagedatadiscard-option"></a>Opção ImageDataDiscard

Esse parâmetro só será válido se a [opção CompressedDomainTranscode](#compresseddomaintranscode-option) for **TRUE;** caso contrário, ele será ignorado. [ImageDataDiscard](#imagedatadiscard-option) especifica a quantidade de dados de imagem a ser descartada durante um transcódigo de domínio compactado. Se a imagem contiver um canal alfa intercalado, esse descarte de dados também se aplicará ao canal alfa, com as exceções, conforme descrito posteriormente nesta seção.

Os valores a seguir são permitidos.



| Valor | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nenhum dado de frequência de imagem é descartado.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | Os FlexBits são descartados, fazendo uma redução arbitrária da qualidade da imagem transcodificada sem alterar a resolução efetiva da imagem. A redução exata do tamanho do arquivo ou a redução de qualidade específica depende de vários fatores e não pode ser especificada ou prevista. Esse valor retorna um erro se você especificá-lo para um canal alfa intercalado.                                                    |
| 2     | A faixa de dados de frequência HighPass é descartada (que também inclui o FlexBits), reduzindo efetivamente a resolução da imagem transcodificada por um fator de 4 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas ela perde todos os detalhes em cada bloco 4x4 de pixels. Portanto, você deve fazer o down-sample da imagem transcodificada de acordo sempre que decodificá-la.                            |
| 3     | As faixas de dados de frequência HighPass e LowPass são descartadas (que também inclui Os FlexBits), reduzindo efetivamente a resolução da imagem transcodificada por um fator de 16 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas ela perde todos os detalhes em cada macroblock 16x16 de pixels. Portanto, você deve fazer o down-sample da imagem transcodificada de acordo sempre que decodificá-la. |



 

O valor padrão é 0.

### <a name="alphadatadiscard-option"></a>Opção AlphaDataDiscard

Essa opção só será válida se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode-option) for **TRUE** e a imagem contiver um canal alfa planar ou intercalado; caso contrário, ele será ignorado. Especifica a quantidade de dados de frequência alfa a ser descartada durante um transcódigo de domínio compactado. Os valores a seguir são permitidos para um canal alfa planar.



| Valor | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nenhum dado de frequência de imagem é descartado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | Os FlexBits são descartados, fazendo uma redução arbitrária da qualidade do canal alfa planar para a imagem transcodificada sem alterar a resolução efetiva. A redução exata do tamanho do arquivo ou a redução de qualidade específica depende de vários fatores e não pode ser especificada ou prevista.                                                                                                                                                                                                                                                |
| 2     | A faixa de dados de frequência HighPass é descartada (que também inclui Os FlexBits), reduzindo efetivamente a resolução do canal alfa planar de imagem transcodificada por um fator de 4 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes do canal alfa planar em cada bloco 4x4 de pixels. Portanto, a imagem transcodificada deve ser amostrada de acordo sempre que for decodificada. Normalmente, você deve definir esse valor somente quando definir a propriedade ImageDataDiscard como o mesmo valor. |
| 3     | As faixas de dados de frequência HighPass e LowPass são descartadas (que também inclui Os FlexBits), reduzindo efetivamente a resolução da imagem transcodificada por um fator de 16 em ambas as dimensões. As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada macroblock 16x16 de pixels. Portanto, a imagem transcodificada deve ser amostrada de acordo sempre que for decodificada. Normalmente, você deve definir esse valor somente quando definir a propriedade ImageDataDiscard com o mesmo valor.               |
| 4     | O canal Alfa é completamente descartado. O formato de pixel da imagem transcodificada é alterado para refletir a remoção do canal alfa.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Para imagens que contêm canais alfa intercalados, a menos que essa propriedade seja definida como 4, o canal alfa é processado da mesma forma que os dados da imagem, de acordo com o valor da propriedade ImageDataDiscard. Se essa propriedade for definida como 4, o canal alfa intercalado será completamente descartado e o formato de pixel da imagem transcodificada será alterado de acordo.

Sem valor padrão.

### <a name="ignoreoverlap-option"></a>Opção IgnoreOverlap

Essa opção só será válida se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode-option) for **TRUE** e um transcodificado de sub-região de exatamente um ou mais blocos for solicitado. A operação padrão para uma transcodificação de região (ou decodificação) é expandir a região solicitada para incluir os pixels ao redor que são necessários para sobrepor a decodificação das bordas da região. Quando esse parâmetro é definido como **TRUE,** os pixels ao redor são ignorados e apenas os blocos selecionados são extraídos. Novamente, isso requer que a região solicitada corresponder exatamente às coordenadas de um ou mais blocos. Se a imagem de origem não estiver lado a lado ou se a região solicitada especificar blocos parciais, esse parâmetro será ignorado.

O valor padrão é **FALSE**.

## <a name="decoding"></a>Decodificação

A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

### <a name="iwicbitmapsourcetransform-support"></a>Suporte a IWICBitmapSourceTransform

Além das interfaces necessárias para serem um codec habilitado para WIC, o decodificador nativo do HD Photo também dá suporte ao [**IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) A interface **IWICBitmapSourceTransform** fornece uma opção avançada para decodificar um fluxo de bits de imagem. Em vez de apenas retornar uma imagem completa usando [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)a interface **IWICBitmapSourceTransform** habilita as opções de decodificador a seguir.

-   Decodificar uma sub-região retangular da imagem.
-   Decodificar para uma resolução mais baixa
-   Decodificar para um formato de pixel diferente
-   Executar uma transformação (rotação/inverter) durante a decodificação

O HD Photo codec nativo fornece o seguinte nível de suporte para a interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="doessupporttransform"></a>DoesSupportTransform

A implementação nativa dá suporte a todas as transformações de [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

### <a name="getclosestsize"></a>GetClosestSize

Para solicitações que são menores que 1/2 a dimensão da imagem de origem em ambas as dimensões, o HD Photo retorna o próximo tamanho de imagem de inteiro maior que é igualmente divisível por um fator de dois. Para todos os outros tamanhos solicitados, o HD Photo retorna as dimensões da imagem original.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

HD Photo retorna o formato de pixel da imagem codificada.

### <a name="copypixels"></a>CopyPixels

A foto de HD aceita qualquer região solicitada especificada pelo parâmetro [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) e retorna essa parte da imagem.

Os parâmetros *uiWidth* e *uiHeight* devem especificar dimensões, conforme retornado pela função [**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) . Quaisquer outros valores retornam um erro.

O parâmetro *pguidDstFormat* deve especificar o formato de pixel retornado pela função [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) . Qualquer outro valor retorna um erro.

A foto de HD aceita qualquer valor permitido para o parâmetro *dstTransform* . Observe que os valores permitidos pelo WIC para esse parâmetro são diferentes dos valores usados pela foto de HD para a marca de metadados de transformação.

 

 
