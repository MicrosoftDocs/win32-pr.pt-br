---
description: 'O codificador Windows Media Audio codifica fluxos de áudio. O codificador dá suporte a três categorias de saída codificada: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Windows Codificador de Áudio de Mídia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba1a94ff5867282049521e3ac13ae28f949a7fc3ccd1855962fb9abb2217d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688180"
---
# <a name="windows-media-audio-encoder"></a>Windows Codificador de áudio de mídia

O codificador Windows Media Audio codifica fluxos de áudio. O codificador dá suporte a três categorias de saída codificada: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do codificador de áudio Windows media é representado pela constante **CLSID \_ CWMAEncMediaObject**. Você pode criar uma instância do codificador de áudio chamando **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de entrada com suporte pelo codificador Windows Media Audio. Para obter informações sobre como definir os tipos de entrada e saída para o codificador, consulte [Configuring Audio Encoding](configuringaudioencoding.md).



| Constante de marca de formato       | Valor da marca de formato | Formato de áudio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| FORMATO WAVE \_ \_ PCM         | 0x0001           | Formato do PCM                                            |
| WAVE \_ FORMAT \_ IEEE \_ FLOAT | 0x0003           | Ponto flutuante IEEE                                   |
| FORMATO \_ WAVE \_ EXTENSÍVEL  | 0xFFFE           | Formato PCM/IEEE na **estrutura WAVEFORMATEXTENSIBLE** |



 

## <a name="output-formats"></a>Formatos de saída

A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de saída com suporte pelo codificador Windows Media Audio.



| Constante de marca de formato             | Valor da marca de formato | Formato de áudio                     |
|---------------------------------|------------------|----------------------------------|
| FORMATO \_ WAVE \_ WMAUDIO2          | 0x0161           | Windows Media Audio Standard     |
| FORMATO \_ WAVE \_ WMAUDIO3          | 0x0162           | Windows Mídia audio Professional |
| FORMATO \_ WAVE \_ WMAUDIO \_ SEM PERDA | 0x0163           | Windows Sem perda de áudio de mídia     |



 

## <a name="interfaces"></a>Interfaces

Um objeto de endoder de áudio expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia directX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma transformação Media Foundation (MFT).

Um Windows de áudio de mídia se comporta como um DMO ou um MFT, dependendo de quais interfaces você obtém e qual versão do Windows está em execução. A tabela a seguir mostra as condições sob as quais um codificador de áudio se comporta como um DMO ou um MFT.



| Sistema operacional | Comportamento do codificador                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Um Windows de áudio de mídia sempre se comporta como um DMO.                                                                                                                                |
| Windows Vista    | Por padrão, um codificador Windows Media Audio se comporta como um DMO. Se você obter uma interface **IMFTransform** ou uma interface **IPropertyStore** em um codificador de áudio, ela se comportará como uma MFT. |
| Windows 7        | Por padrão, um codificador Windows Media Audio se comporta como um DMO. Se você obter uma interface **IMFTransform** em um codificador de áudio, ela se comportará como uma MFT.                                    |



 

## <a name="encoder-properties"></a>Propriedades do codificador

O codificador Windows Media Audio dá suporte às propriedades a seguir.



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
<td>Especifica se o codificador usa codificação VBR de controle médio.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Especifica a janela do buffer, em milissegundos, de um fluxo de VBR (taxa de bits variável) restrita em sua taxa de bits de pico.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Especifica se o codificador deve verificar se há consistência de dados entre passagens ao executar a codificação VBR de duas passagens. <br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Especifica se o codificador é restrito por um requisito máximo de latência do decodificador.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Especifica se a complexidade do algoritmo de codificação está restrita.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Especifica se o codificador é restrito por um requisito máximo de latência.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica se os modos enumerados pelo codificador são limitados àqueles que atendem a um requisito de qualidade.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Especifica o perfil de complexidade do conteúdo codificado.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perda.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Especifica o nível de qualidade desejado para codificação VBR.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Especifica se o codificador usa substituição de ruído.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Especifica se o codificador usa a limitação de intervalo de PCM.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Especifica a largura de banda codificada máxima permitida pelo truncamento de banda no codificador.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Especifica a largura de banda codificada mínima permitida pelo truncamento de banda no codificador.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Especifica a qualidade na qual a largura de banda codificada mínima é permitida. <br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Especifica a qualidade na qual a largura de banda codificada máxima é permitida.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Especifica se o codificador executa truncamento de banda.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Especifica se o codificador usa o estilo de computação de máscara executada pela versão 7 do codificador Windows Media Audio.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Especifica se o codificador executa o processamento de imagem estéreo. <br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação VBR de controle médio.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Especifica a taxa média de bits, em bits por segundo, para um codificador configurado para usar a codificação VBR de controle médio.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Especifica a complexidade do algoritmo de codificação.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Especifica o final de uma passagem de codificação.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Especifica se o codificador principal usa o &quot; recurso &quot; Plus.<br/> <dl> Windows Vista e posterior.<br />
Professional.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Especifica a latência máxima para o decodificador, em milissegundos.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Especifica a latência máxima para o codificador, em milissegundos.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Especifica o nível de qualidade da VBR do tipo de saída enumerado mais recentemente.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perda.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Especifica o número máximo de passagens com suporte pelo codificador.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perda.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Especifica o número de passagens que o codificador usará para codificar o conteúdo.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perda.<br />
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
<td>essa propriedade não é usada atualmente pelo Windows codec de áudio de mídia.<br/></td>
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
| Cabeçalho<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> </dl>

 

 




