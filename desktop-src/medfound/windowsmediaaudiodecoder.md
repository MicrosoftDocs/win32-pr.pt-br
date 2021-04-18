---
description: O decodificador de áudio do Windows Media decodifica os fluxos de áudio que foram codificados pelo codificador de áudio do Windows Media.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Decodificador de áudio do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781374"
---
# <a name="windows-media-audio-decoder"></a>Decodificador de áudio do Windows Media

O decodificador de áudio do Windows Media decodifica os fluxos de áudio que foram codificados pelo [**codificador de áudio do Windows Media**](windowsmediaaudioencoder.md). O codificador e o decodificador dão suporte a três categorias de áudio codificado: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) para o decodificador de áudio do Windows Media é representado pela constante **CLSID \_ CWMADecMediaObject**. Você pode criar uma instância do decodificador de áudio chamando **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de entrada com suporte pelo decodificador de áudio do Windows Media. Para obter informações sobre como definir os tipos de entrada e saída para o decodificador, consulte [Configurando a decodificação de áudio](configuringaudiodecoding.md).



| Formatar constante de marca             | Formatar valor da marca | Formato de áudio                     |
|---------------------------------|------------------|----------------------------------|
| \_WMAUDIO2 de formato Wave \_          | 0x0161           | Padrão de áudio do Windows Media     |
| \_WMAUDIO3 de formato Wave \_          | 0x0162           | Windows Media Audio Professional |
| \_formato Wave \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio sem perdas     |



 

## <a name="output-formats"></a>Formatos de saída

A tabela a seguir mostra as marcas de formato de áudio que representam os tipos de saída com suporte pelo **decodificador de áudio do Windows Media**. Para obter informações sobre como definir os tipos de entrada e saída para o decodificador, consulte [Configurando a codificação de áudio](configuringaudioencoding.md).



| Formatar constante de marca       | Formatar valor da marca | Formato de áudio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM de formato Wave \_         | 0x0001           | Formato PCM                                            |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Ponto flutuante IEEE                                   |
| \_formato Wave \_ extensível  | 0xFFFE           | Formato PCM/IEEE na estrutura **WAVEFORMATEXTENSIBLE** |



 

## <a name="interfaces"></a>Interfaces

Um objeto decodificador de áudio expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

Um decodificador de áudio do Windows Media se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está em execução. A tabela a seguir mostra as condições sob as quais um decodificador de áudio se comporta como um DMO ou um MFT.



| Sistema operacional | Comportamento do decodificador                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Um decodificador de áudio do Windows Media sempre se comporta como DMO.                                                                                                                                |
| Windows Vista    | Por padrão, um decodificador de áudio do Windows Media se comporta como DMO. Se você obter uma interface **IMFTransform** ou uma interface **IPropertyStore** em um decodificador de áudio, ela se comporta como um MFT. |
| Windows 7        | Por padrão, um decodificador de áudio do Windows Media se comporta como DMO. Se você obtiver uma interface **IMFTransform** em um decodificador de áudio, ele se comporta como um MFT.                                    |



 

## <a name="properties"></a>Propriedades

O decodificador de áudio do Windows Media dá suporte às propriedades a seguir.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></td>
<td>Especifica o número máximo de amostras de PCM adicionais que podem ser retornadas ao final da decodificação de um arquivo.<br/> <dl> Windows Vista e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></td>
<td>Especifica o modo de controle de intervalo dinâmico que o decodificador de áudio usará.<br/> <dl> Windows XP e posterior.<br />
Standard, Professional, sem perdas.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></td>
<td>Especifica os coeficientes de dobra fornecidos pelo autor para decodificação de áudio multicanal para menos canais do que o fluxo codificado contém. <br/> <dl> Windows XP e posterior.<br />
Professional<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></td>
<td>Especifica se o decodificador de áudio deve fornecer saída de alta resolução.<br/> <dl> Windows XP e posterior.<br />
Professional, sem perdas.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></td>
<td>Especifica se o decodificador de áudio deve executar Lt-Rt dobra para baixo.<br/> <dl> Windows Vista e posterior.<br />
Professional.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></td>
<td>Especifica a configuração do alto-falante no computador cliente.<br/> <dl> Windows XP e posterior.<br />
Professional.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Especifica o nível médio de volume de conteúdo de áudio.<br/> <dl> Windows XP e posterior.<br />
Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></td>
<td>Especifica o nível de volume médio desejado de conteúdo de áudio de saída.<br/> <dl> Windows XP e posterior.<br />
Professional, sem perdas.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Especifica o nível de volume mais alto que ocorre no conteúdo de áudio.<br/> <dl> Windows XP e posterior.<br />
Professional, sem perdas.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></td>
<td>Especifica o nível máximo de volume desejado de conteúdo de áudio de saída.<br/> <dl> Windows XP e posterior.<br />
Professional, sem perdas.<br />
Somente gravação.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmod.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> </dl>

 

 




