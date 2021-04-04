---
description: O decodificador Dolby Audio é um MFT que decodifica Dolby Digital (AC-3) e Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Decodificador de áudio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646590"
---
# <a name="dolby-audio-decoder"></a>Decodificador de áudio Dolby

O decodificador Dolby Audio é uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) que decodifica os seguintes tipos de fluxo:

-   Dolby Digital, também chamado Dolby AC-3
-   Dolby Digital Plus, também chamado de AC reforçada 3 (E-AC-3)

> [!IMPORTANT]
> Para versões do Windows anteriores ao Windows 8, a implementação da Microsoft da tecnologia Dolby Digital é restrita em termos do programa Dolby Digital Licensing para uso pelos aplicativos da Microsoft.

 

Para obter mais informações sobre esses formatos, consulte a documentação do ATSC (Comitê de sistemas de televisão avançada) *padrão de compactação de áudio digital (AC-3, E-AC-3) revisão B*.

O decodificador também pode converter um fluxo Dolby Digital Plus para o formato Dolby Digital para saída AC-3 S/PIDF ou formatar um fluxo Dolby Digital Plus para saída digital HDMI.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do decodificador de áudio Dolby é **CLSID \_ CMSDDPlusDecMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.

## <a name="input-types"></a>Tipos de entrada

O decodificador de áudio Dolby dá suporte aos seguintes subtipos de entrada.



| Subtype                                 | Descrição                                                                                                                                                 | Cabeçalho       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MEDIASUBTYPE \_ Dolby \_ AC3**            | Áudio Dolby Digital.                                                                                                                                        | mfapi. h      |
| **MEDIASUBTYPE \_ DVM**                   | Áudio Dolby Digital; consulte [**subtipos de áudio**](../directshow/audio-subtypes.md). Esse subtipo pode ser usado de forma intercambiável com **MEDIASUBTYPE \_ Dolby \_ AC3**.<br/> | wmcodecdsp. h |
| **MFAudioFormat \_ Dolby \_ digital \_ Plus** | Áudio Dolby Digital Plus.                                                                                                                                   | mfapi. h      |



 

A tabela a seguir lista os atributos requires e optional para o tipo de mídia de entrada.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
<th>Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obrigatórios. Deve ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de áudio.</td>
<td>Obrigatórios. Consulte a tabela anterior para obter detalhes.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Taxa de amostragem, em amostras por segundo.</td>
<td>Opcional. Os valores válidos são: 48000, 44100, 32000, 24000, 22050 e 16000. Se esse atributo não for definido, o valor padrão será 48000. <br/>
<blockquote>
[!Note]<br />
Os fluxos Dolby AC-3 são limitados às três taxas mais altas nessa lista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canais, incluindo o canal de baixa frequência (LFE), se presente.</td>
<td>Opcional. Os valores válidos estão no intervalo 1 (mono) a 8 (configuração de canal de 7,1). Se esse atributo não estiver definido, o valor padrão será 2 (estéreo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica a atribuição de canais de áudio a posições do orador.</td>
<td>Opcional. Se especificado, o valor deve ser consistente com o número de canais de áudio. Se o atributo não estiver definido, o decodificador usará uma máscara de canal padrão, com base no número de canais.</td>
</tr>
</tbody>
</table>



 

A tabela a seguir lista as configurações de canal Dolby com suporte.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Configuração de canal</th>
<th>Número de canais</th>
<th>Máscaras de canal</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1/0 (mono)</td>
<td>1</td>
<td>0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/0 (estéreo) ou 1 + 1 (mono duplo)</td>
<td>2</td>
<td>0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</td>
</tr>
<tr class="odd">
<td>3/0</td>
<td>3</td>
<td>0x7 (<strong></strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> de SPEAKER_FRONT_LEFT | SPEAKER_FRONT_CENTER)</td>
</tr>
<tr class="even">
<td>2/1</td>
<td>3</td>
<td>0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="odd">
<td>3/1</td>
<td>4</td>
<td>0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/2</td>
<td>4</td>
<td>0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> ou<br/> 0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="odd">
<td>3/2</td>
<td>5</td>
<td>0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> ou<br/> 0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="even">
<td>3/2 + LFE</td>
<td>6</td>
<td>0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> ou<br/> 0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)<br/></td>
</tr>
<tr class="odd">
<td>3/2/2 + LFE
<blockquote>
[!Note]<br />
Somente Dolby Digital Plus.
</blockquote>
<br/> <br/></td>
<td>8</td>
<td>0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</td>
</tr>
</tbody>
</table>



 

Além disso, as configurações de canal 1/0, 2/0, 3/0, 2/1, 3/1 e 2/2 também podem aparecer com um canal de LFE.

## <a name="output-types"></a>Tipos de saída

O decodificador de áudio Dolby dá suporte aos seguintes subtipos de saída.



| Subtype                                                   | Descrição                                                                                                                               | Cabeçalho    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**                      | Áudio Dolby AC-3 formatado para saída digital S/PDIF.                                                                                     | mfapi. h   |
| **KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital \_ Plus** | Áudio Dolby Digital Plus formatado para saída digital HDMI.                                                                               | ksmedia. h |
| **MFAudioFormat \_ float**                                  | Áudio PCM de ponto flutuante do IEEE 32-bit<br/> **Windows 10**: estéreo, 5,1, 7,1<br/> **Versões anteriores**: estéreo, 5,1<br/> | mfapi. h   |
| **\_PCM MFAudioFormat**                                    | áudio PCM de 16 bits<br/> **Windows 10**: estéreo, 5,1, 7,1<br/> **Versões anteriores**: estéreo, 5,1<br/>                     | mfapi. h   |



 

A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de saída.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
<th>Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obrigatórios. Deve ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de áudio.</td>
<td>Obrigatórios. Consulte a tabela anterior para obter detalhes.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Taxa de amostragem, em amostras por segundo.</td>
<td>Obrigatórios. Os valores válidos são: 48000, 44100, 32000, 24000, 22050 e 16000. A taxa de amostra de saída deve ser idêntica à taxa de amostra de entrada. O decodificador não pode alterar a taxa de amostragem do fluxo.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canais, incluindo o canal de baixa frequência (LFE), se presente.</td>
<td>Necessário para a saída do PCM. <br/> Não é necessário para a saída digital. <br/> Se o tipo de entrada for mono, estéreo ou dual-mono (tudo sem canal de LFE), o único valor válido será 2, para saída de estéreo. Caso contrário, o valor pode ser: <br/>
<ul>
<li>2 para downmix estéreo</li>
<li>6 para configurações de canal de 5,1</li>
<li>8 para configurações de canal de 7,1</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica a atribuição de canais de áudio a posições do orador.</td>
<td>Necessário para a saída do PCM se o número de canais for maior que 2. O valor deve ser:<br/>
<ul>
<li>0x3 para saída de estéreo</li>
<li>0x3F para saída de canal de 5,1</li>
<li>0x63F para saída de canal de 7,1</li>
</ul>
Não é necessário para a saída digital. <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Número de bits por amostra de áudio.</td>
<td>Necessário para a saída do PCM. O valor deve ser 32 para <strong>MFAudioFormat_Float</strong>e 16 para <strong>MFAudioFormat_PCM</strong>.<br/> Não é necessário para a saída digital.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Número de bits válidos de dados de áudio em cada amostra de áudio.</td>
<td>Opcional para saída de PCM. Se definido, o valor deve ser idêntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.<br/> Não é necessário para os subtipos de saída digital.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Alinhamento de bloco, em bytes.</td>
<td>Opcional para saída de PCM. Não é necessário para a saída digital.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Número médio de bytes por segundo.</td>
<td>Opcional para saída de PCM. Não é necessário para a saída digital.</td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a>Atributos de transformação

O decodificador de áudio Dolby implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . O aplicativo pode usar esse método para obter ou definir os atributos a seguir.



| Atributo                                                                                | Descrição                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecAudioDualMono](../directshow/avdecaudiodualmono-property.md)                        | Especifica se um fluxo de áudio Dolby de 2 canais é codificado como estéreo ou dual-mono. Antes de o primeiro quadro Dolby ser decodificado, o valor é **EAVDecAudioDualMono \_ não especificado**. Após o início da decodificação, o valor reflete o quadro Dolby mais recente.<br/> Somente leitura. <br/> |
| [CODECAPI \_ AVDecAudioDualMonoReproMode](../directshow/avdecaudiodualmonorepromode-property.md)      | Especifica como o decodificador Reproduz áudio dual-mono. O valor padrão é **eAVDecAudioDualMonoReproMode \_ esquerdo \_ mono**. O aplicativo pode definir essa propriedade a qualquer momento.<br/> Leitura/gravação.<br/>                                                                            |
| [CODECAPI \_ AVDecCommonMeanBitRate](../directshow/avdeccommonmeanbitrate.md)                         | Para fluxos Dolby Digital (AC-3), especifica a taxa de bits do fluxo de entrada em bits por segundo. Para o Dolby Digital Plus (E-AC3), o valor é sempre zero.<br/> Somente leitura.<br/>                                                                                              |
| [CODECAPI \_ AVDecDDDynamicRangeScaleHigh](../directshow/avdecdddynamicrangescalehigh-property.md)    | O corte de alto nível quando o decodificador executa o controle de intervalo dinâmico.<br/> Leitura/gravação.<br/>                                                                                                                                                                                    |
| [CODECAPI \_ AVDecDDDynamicRangeScaleLow](../directshow/avdecdddynamicrangescalelow-property.md)      | O aumento de nível baixo quando o decodificador executa o controle de intervalo dinâmico.<br/> Leitura/gravação.<br/>                                                                                                                                                                                   |
| [CODECAPI \_ AVDecDDOperationalMode](../directshow/avdecddoperationalmode-property.md)                | O modo de controle de compactação.<br/> Leitura/gravação.<br/>                                                                                                                                                                                                                          |
| [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md)              | O tipo de downmix estéreo. Essa propriedade se aplica quando a entrada é um fluxo multicanal e a saída é um fluxo estéreo.<br/> Leitura/gravação.<br/>                                                                                                                           |
| [o MFT \_ dá suporte à \_ alteração de \_ formato dinâmico \_](mft-support-dynamic-format-change-attribute.md) | Esse atributo retorna **false**, indicando que o decodificador deve ser esvaziado antes que um novo tipo de entrada seja definido.<br/> Leitura/gravação.<br/>                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

O decodificador aceita apenas fluxos Dolby brutos, conforme definido por um/52B. Não há suporte para cargas como os fluxos de elementar pacotes (PES). Para o Dolby Digital Plus, o decodificador decodifica até 5,1 canais. No Windows 10, 7,1 fluxos de canal são decodificados sem downmix. Nas versões anteriores do sistema operacional, se o fluxo for de 7,1 canais, somente o downmix do canal 5,1 será decodificado. Se o fluxo for Dolby Digital Plus com mais de um substream independente, somente substream independente 0 será decodificado. O decodificador ignora outros subfluxos independentes. Além disso, o decodificador ignora todos os subfluxos dependentes. O decodificador dá suporte à descriptografia e decodificação de fluxos protegidos pela tecnologia de Rights Management digital (DRM).

Se o tipo de mídia de entrada tiver uma configuração de canal diferente de mono, estéreo ou dual-mono (tudo sem canal de LFE), o decodificador fornecerá duas opções para as configurações de canal de saída:

-   saída de 8 canais (configuração de canal de 7,1)
-   saída de 6 canais (configuração de canal de 5,1)
-   Downmix estéreo

Se downmix estéreo for selecionado, o tipo de downmix poderá ser definido no MFT usando a propriedade [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .

Se o tipo de saída for **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, cada buffer de saída conterá 6.144 bytes. O buffer começa com um cabeçalho S/PDIF de 8 bytes, seguido por um quadro AC-3 compactado, seguido por zero Padding para 6.144 bytes.

Se o tipo de saída for **KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital \_ Plus**, cada buffer de saída conterá 24.576 bytes. O buffer começa com um cabeçalho S/PDIF de 8 bytes, seguido de 1 a 6 quadros Dolby Digital Plus compactados correspondentes a 1.536 exemplos de PCM, seguidos de zero preenchimento para 24.576 bytes. Para saída de HDMI, somente substream independente 0 é empacotado.

O MFT do decodificador é registrado com o sinalizador de enumeração de MFT de sinalizador **\_ \_ \_ FIELDOFUSE**, que indica que o MFT deve ser desbloqueado pelo aplicativo antes do uso. Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msauddecmft.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
