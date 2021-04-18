---
description: O codificador do Windows Media Video 9 codificará fluxos de vídeo.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Codificador do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772717"
---
# <a name="windows-media-video-9-encoder"></a>Codificador do Windows Media Video 9

O codificador do Windows Media Video 9 codificará fluxos de vídeo. O codificador dá suporte às quatro categorias de saída codificadas a seguir.

-   Perfil simples do Windows Media Video 9
-   Perfil principal do Windows Media Video 9
-   Perfil avançado do Windows Media Video 9
-   Imagem do vídeo 9,1 do Windows Media

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) para o codificador de vídeo do Windows Media é representado pela constante **CLSID \_ CWMV9EncMediaObject**. Você pode criar uma instância do codificador de vídeo chamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Um objeto de codificador de vídeo expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

Um codificador de vídeo se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada. A tabela a seguir mostra as condições sob as quais um codificador de vídeo se comporta como um DMO ou um MFT.



| Sistema operacional            | Comportamento do codificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Um codificador de vídeo do Windows Media sempre se comporta como DMO.                                                                                                                |
| Windows Vista e Windows 7 | Por padrão, um codificador de vídeo do Windows Media se comporta como DMO. Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um codificador de vídeo, ela se comporta como um MFT. |



 

## <a name="input-formats"></a>Formatos de entrada

O codificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de entrada quando ele está agindo como DMO.

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ FOTOmotion

O codificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de entrada quando ele está atuando como um MFT.

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8
-   MEDIASUBTYPE \_ FOTOmotion

## <a name="output-formats"></a>Formatos de saída

A tabela a seguir mostra os códigos de quatro caracteres (FOURCC) que correspondem às categorias de saída codificada.



| Categoria                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Perfil simples do Windows Media Video 9   | "WMV3"                                   |
| Perfil principal do Windows Media Video 9     | "WMV3"                                   |
| Perfil avançado do Windows Media Video 9 | "WVC1"                                   |
| Imagem do vídeo 9,1 do Windows Media          | "WMVP" para 9,1, "WVP2" para 9,1 versão 2 |



 

Para distinguir entre perfil simples e perfil principal, defina a propriedade [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) .

## <a name="properties"></a>Propriedades

O codificador do Windows Media Video 9 dá suporte às propriedades a seguir.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>Especifica a sobrecarga, em bytes por pacote, necessária para o contêiner usado para armazenar o conteúdo compactado.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Especifica a taxa média de quadros do conteúdo do vídeo, em quadros por segundo.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa média de bits (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Especifica o aumento Delta entre a imagem quantizador do quadro âncora e a quantizador da imagem do quadro B.<br/> <dl> Windows XP e posterior.<br />
Perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Especifica o padrão de codificação a ser usado no início de um grupo de imagens.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo codificados pelo codec.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Essa propriedade é substituída por <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Especifica a complexidade do algoritmo do codificador.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal. Perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>Especifica o tipo de otimização a ser usado para o codec de perfil avançado do Windows Media Video 9.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem na saída do codec.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>Não usado.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica o modelo de conformidade do dispositivo para o qual o conteúdo codificado está em conformidade.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Especifica o método usado para codificar as informações de vetor de movimento.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Especifica se o codec usará o filtro de ruído durante a codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Especifica o nível de qualidade desejado para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo removidos durante a codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica o fim de uma passagem de codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Especifica uma altura intermediária de quadro para vídeo codificado.<br/> <dl> Windows XP e posterior.<br />
Perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Especifica uma largura de quadro intermediária para o vídeo codificado.<br/> <dl> Windows XP e posterior.<br />
Perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Especifica se o codec deve usar a filtragem mediana durante a codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Especifica o FOURCC que identifica o codificador que você deseja usar.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Obsoleto.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Especifica se o codificador tem permissão para descartar quadros.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Especifica se a saída do codec será entrelaçada.<br/> <dl> Windows XP e posterior.<br />
Perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>Não usado.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>Especifica o número de quadros após o quadro atual que o codec avaliará antes de codificar o quadro atual.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Especifica se o codec deve usar o filtro de desbloqueio no loop durante a codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Especifica o método de custo usado pelo codec para determinar qual modo de macrobloco usar.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Especifica o método a ser usado para a correspondência de movimento.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Especifica os tipos de informações de vídeo que são usadas em operações de pesquisa de movimento.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Especifica o intervalo usado em pesquisas de movimento.<br/> <dl> Windows XP e posterior.<br />
Perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Especifica se o codec deve tentar detectar bordas de quadro ruidosas e removê-las.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Especifica o número de quadros de previsão bidirecionais (quadros B).<br/> <dl> Windows XP e posterior.<br />
Perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Especifica o número de threads que o codec usará para codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica o número máximo de passagens aceitas pelo codec.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica o número de passagens que o codec usará para codificar o conteúdo.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Especifica se o codec deve usar a otimização de perceptiva conservadora durante a codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Especifica QP.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Especifica o grau para o qual o codec deve reduzir o intervalo de cores efetivo do vídeo.<br/> <dl> Windows XP e posterior.<br />
Perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Especifica a taxa média de bits, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) de 2 passagens.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Especifica se o codificador usa a pesquisa MV de sub-pixel baseada em RD. <br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Para nova codificação de segmento, especifica o tamanho do buffer.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Para a recodificação de segmento, especifica a duração do segmento a ser codificado novamente.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Para a recodificação de segmento, especifica o quantizador do quadro antes do segmento inicial.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Para a recodificação de segmento, especifica a totalidade do buffer inicial.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Especifica a taxa de bits de pico, em bits por segundo, usada para taxa de bits variável restrita de 2 passagens (VBR).<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo passados para o codificador durante o processo de codificação.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Especifica se o codec usará a codificação de taxa de bits variável (VBR).<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Especifica se o codec usará a otimização de escala de vídeo.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Especifica a quantidade de conteúdo, em milissegundos, que pode caber no buffer de modelo.<br/> <dl> Windows XP e posterior.<br />
Perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Para a recodificação de segmento, especifica os dados privados do codec do arquivo que está sendo codificado novamente.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>Especifica o tipo de lógica que o codec usará para detectar o vídeo de origem entrelaçado.<br/> <dl> Windows XP e posterior.<br />
Perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo que foram ignorados porque eles eram duplicatas de quadros anteriores.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente leitura<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> </dl>

 

 
