---
description: 'O codificador de áudio do Windows Media codificará os fluxos de áudio. O codificador dá suporte a três categorias de saída codificada: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio sem perdas.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Codificador de áudio do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798048"
---
# <a name="windows-media-audio-encoder"></a>Codificador de áudio do Windows Media

O codificador de áudio do Windows Media codificará os fluxos de áudio. O codificador dá suporte a três categorias de saída codificada: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio sem perdas.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) para o codificador de áudio do Windows Media é representado pela constante **CLSID \_ CWMAEncMediaObject**. Você pode criar uma instância do codificador de áudio chamando **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de entrada com suporte pelo codificador de áudio do Windows Media. Para obter informações sobre como definir os tipos de entrada e saída para o codificador, consulte [Configurando a codificação de áudio](configuringaudioencoding.md).



| Formatar constante de marca       | Formatar valor da marca | Formato de áudio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM de formato Wave \_         | 0x0001           | Formato PCM                                            |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Ponto flutuante IEEE                                   |
| \_formato Wave \_ extensível  | 0xFFFE           | Formato PCM/IEEE na estrutura **WAVEFORMATEXTENSIBLE** |



 

## <a name="output-formats"></a>Formatos de saída

A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de saída com suporte pelo codificador de áudio do Windows Media.



| Formatar constante de marca             | Formatar valor da marca | Formato de áudio                     |
|---------------------------------|------------------|----------------------------------|
| \_WMAUDIO2 de formato Wave \_          | 0x0161           | Padrão de áudio do Windows Media     |
| \_WMAUDIO3 de formato Wave \_          | 0x0162           | Windows Media Audio Professional |
| \_formato Wave \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio sem perdas     |



 

## <a name="interfaces"></a>Interfaces

Um objeto endoder de áudio expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

Um codificador de áudio do Windows Media se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada. A tabela a seguir mostra as condições sob as quais um codificador de áudio se comporta como um DMO ou um MFT.



| Sistema operacional | Comportamento do codificador                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Um codificador de áudio do Windows Media sempre se comporta como DMO.                                                                                                                                |
| Windows Vista    | Por padrão, um codificador de áudio do Windows Media se comporta como DMO. Se você obtiver uma interface **IMFTransform** ou uma interface **IPropertyStore** em um codificador de áudio, ela se comporta como um MFT. |
| Windows 7        | Por padrão, um codificador de áudio do Windows Media se comporta como DMO. Se você obtiver uma interface **IMFTransform** em um codificador de áudio, ele se comporta como um MFT.                                    |



 

## <a name="encoder-properties"></a>Propriedades do codificador

O codificador de áudio do Windows Media dá suporte às propriedades a seguir.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>Especifica se o codificador usa a codificação de VBR média controlável.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Especifica se o codificador deve verificar a consistência dos dados entre as passagens ao executar a codificação de VBR de duas passagens. <br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Especifica se o codificador é restrito por um requisito de latência de decodificador máximo.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Especifica se a complexidade do algoritmo de codificação é restrita.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Especifica se o codificador é restrito por um requisito de latência máxima.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica se os modos enumerados pelo codificador são limitados àqueles que atendem a um requisito de qualidade.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica o perfil de complexidade do conteúdo codificado.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Especifica o nível de qualidade desejado para a codificação de VBR.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Especifica se o codificador usa substituição de ruído.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Especifica se o codificador usa a limitação de intervalo PCM.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Especifica a largura de banda máxima codificada permitida pelo truncamento de banda no codificador.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Especifica a largura de banda mínima codificada permitida pelo truncamento de banda no codificador.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Especifica a qualidade na qual a largura de banda mínima codificada é permitida. <br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Especifica a qualidade na qual a largura de banda máxima codificada é permitida.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Especifica se o codificador executa o truncamento de banda.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Especifica se o codificador usa o estilo de computação de máscara executado pela versão 7 do codificador de áudio do Windows Media.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Especifica se o codificador executa o processamento de imagens estéreo. <br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação de VBR média controlável.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Especifica a taxa média de bits, em bits por segundo, para um codificador configurado para usar a codificação de VBR média controlável.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Especifica a complexidade do algoritmo de codificação.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica o fim de uma passagem de codificação.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Especifica se o codificador principal usa &quot; o &quot; recurso Plus.<br/> <dl> Windows Vista e posterior.<br />
Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Especifica a latência máxima para o decodificador, em milissegundos.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Especifica a latência máxima para o codificador, em milissegundos.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica o nível de qualidade de VBR do tipo de saída enumerado mais recentemente.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica o número máximo de passagens aceitas pelo codificador.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica o número de passagens que o codificador usará para codificar o conteúdo.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Especifica se o codificador é restrito por uma taxa de bits de pico.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></td>
<td>Especifica o número preferencial de amostras por quadro.<br/> <dl> Windows Vista e posterior.<br />
Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></td>
<td>Especifica se o codificador deve usar um tamanho de quadro preferencial.<br/> <dl> Windows Vista e posterior.<br />
Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Especifica a taxa de bits de pico, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) restrita de 2 passagens. <br/> <dl> Windows XP e posterior.<br />
Standard, Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Especifica a janela de buffer médio, em milissegundos, de um fluxo codificado.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Especifica a janela de buffer máximo, em milissegundos, de um fluxo codificado.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Especifica a taxa média de bits, em bits por segundo, de um fluxo codificado.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Especifica a taxa de bits máxima, em bits por segundo, de um fluxo codificado.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Especifica se o codificador usa a codificação VBR.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Essa propriedade não é usada no momento pelo codec de áudio do Windows Media.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Especifica o nível médio de volume de conteúdo de áudio.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Especifica o nível de volume mais alto que ocorre no conteúdo de áudio.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Especifica a média de bytes por segundo para áudio de VBR codificado.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Especifica se o codificador deve produzir 1 pacote WMA por quadro.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Especifica se o codificador deve gerar parâmetros de controle de intervalo dinâmico.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Especifica a estrutura <strong>WAVEFORMATEX</strong> que descreve o conteúdo de áudio de entrada.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>Especifica se o codificador deve habilitar a codificação S/PDIF em tempo real.<br/> <dl> Windows Vista e posterior.<br />
Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> </dl>

 

 




