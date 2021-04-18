---
description: O codificador do Windows Media Video 7/8 implementa versões anteriores do codificador de vídeo do Windows Media.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Codificador de vídeo 7/8 do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763489"
---
# <a name="windows-media-video-78-encoder"></a>Codificador de vídeo 7/8 do Windows Media

O codificador do Windows Media Video 7/8 implementa versões anteriores do codificador de vídeo do Windows Media.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do Windows Media Video 7/8 Encoder é **CLSID \_ CWMVXEncMediaObject**. Você pode criar uma instância do codificador chamando **CoCreateInstance**.

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

A tabela a seguir mostra os códigos de quatro caracteres (FOURCC) para os tipos de saída com suporte no codificador de vídeo 7/8 do Windows Media.



| Category              | FOURCC |
|-----------------------|--------|
| Windows Media Video 7 | "WMV1" |
| Vídeo do Windows Media 8 | "WMV2" |



 

## <a name="properties"></a>Propriedades

O codificador do Windows Media Video 7/8 dá suporte às seguintes propriedades.



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
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Especifica a taxa média de quadros do conteúdo do vídeo, em quadros por segundo.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa média de bits (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo codificados pelo codec.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.<br/> <dl> Windows XP e posterior.<br />
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
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem na saída do codec.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica o modelo de conformidade do dispositivo para o qual o conteúdo codificado está em conformidade.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo removidos durante a codificação.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica o fim de uma passagem de codificação.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Especifica o FOURCC que identifica o codificador que você deseja usar.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Especifica se a saída do codec será entrelaçada.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica o número máximo de passagens aceitas pelo codec.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica o número de passagens que o codec usará para codificar o conteúdo.<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Especifica QP.<br/> <dl> Windows Vista e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Especifica a taxa média de bits, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) de 2 passagens.<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Especifica a taxa de bits de pico, em bits por segundo, usada para taxa de bits variável restrita de 2 passagens (VBR).<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo passados para o codificador durante o processo de codificação.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Especifica se o codec usará a codificação de taxa de bits variável (VBR).<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Especifica a quantidade de conteúdo, em milissegundos, que pode caber no buffer de modelo.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Especifica o número de quadros de vídeo que foram ignorados porque eles eram duplicatas de quadros anteriores.<br/> <dl> Windows XP e posterior.<br />
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
| DLL<br/>    | <dl> <dt>Wmvxencd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> <dt>

[GUIDs de subtipo de vídeo](video-subtype-guids.md)
</dt> </dl>

 

 
