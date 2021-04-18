---
description: O codificador de tela do Windows Media Video 9 é otimizado para codificar capturas de tela sequenciais de monitores de computador.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Codificador de tela do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771266"
---
# <a name="windows-media-video-9-screen-encoder"></a>Codificador de tela do Windows Media Video 9

O codificador de tela do Windows Media Video 9 é otimizado para codificar capturas de tela sequenciais de monitores de computador.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do codificador de tela do Windows Media Video 9 é representado pela constante **CLSID \_ CMSSCEncMediaObject2**. Você pode criar uma instância do codificador chamando **CoCreateInstance**.

## <a name="input-types"></a>Tipos de entrada

Os seguintes tipos de entrada são suportados pelo codificador de tela da versão 9 quando ele está sendo usado como um objeto de mídia do DirectX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Os seguintes tipos de entrada são suportados pelo codificador de tela da versão 9 quando ele está sendo usado como uma Media Foundation transformação (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="output-types"></a>Tipos de saída

O FOURCC (código de quatro caracteres) para o conteúdo codificado da tela de vídeo do Windows Media versão 9 é "MSS2".

Os tipos de saída a seguir têm suporte no codificador de tela da versão 9.

-   MEDIASUBTYPE \_ MSS2

## <a name="encoder-properties"></a>Propriedades do codificador

O codificador de tela do Windows Media Video 9 dá suporte às propriedades a seguir.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></td>
<td>Especifica a sobrecarga, em bytes por pacote, necessária para o contêiner que é usado para armazenar o conteúdo compactado.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa média de bits (especificada por <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>Especifica o número de quadros de vídeo codificados pelo codec.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>Essa propriedade é substituída por <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>Especifica a complexidade do algoritmo do codificador.<br/> <dl> Windows Vista e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem na saída do codec.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>Especifica o número de quadros de vídeo removidos durante a codificação.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>Especifica o fim de uma passagem de codificação.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>Especifica o FOURCC que identifica o codificador que você deseja usar.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>Obsoleto.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>Especifica o número máximo de passagens aceitas pelo codec.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP e posterior. Leitura/gravação.<br/> Especifica o número de passagens que o codec usará para codificar o conteúdo.<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>Especifica QP. Os valores possíveis são 1,0 a 31,0.<br/> <dl> Windows Vista e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>Especifica a taxa média de bits, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) de 2 passagens.<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Especifica a taxa de bits de pico, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) restrita de 2 passagens.<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>Especifica o número de quadros de vídeo passados para o codificador durante o processo de codificação.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>Especifica se o codec usará a codificação de taxa de bits variável (VBR).<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>A quantidade de conteúdo, em milissegundos, que pode caber no buffer de modelo.<br/> <dl> Windows XP e posterior,<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>Especifica o número de quadros de vídeo que foram ignorados porque eles eram duplicatas de quadros anteriores.<br/> <dl> Windows XP e posterior.<br />
Somente leitura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Um objeto de codificador de tela expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

Um codificador de tela se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada. A tabela a seguir mostra as condições sob as quais um codificador de tela se comporta como um DMO ou uma MFT.



| Sistema operacional            | Comportamento do codificador                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Um codificador de tela do Windows Media sempre se comporta como DMO.                                                                                             |
| Windows Vista e Windows 7 | Por padrão, um codificador de tela do Windows Media se comporta como DMO. Se você obtiver uma interface **IMFTransform** em um codificador de tela, ela se comporta como um MFT. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> <dt>

[Usando o codec de tela do Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Decodificador de tela do Windows Media Video 9](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




