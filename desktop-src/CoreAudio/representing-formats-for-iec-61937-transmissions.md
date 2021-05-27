---
description: Com o aumento nos dispositivos de armazenamento de mídia que exigem formatos de áudio compactados, os aplicativos devem identificar, descrever e usar uma variedade de novos conteúdos de áudio codificados para transmitir conteúdo de PCs para dispositivos como receptores de HDMI ou DisplayPort.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Representando formatos para transmissões IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a607770a388a11978d0e4666b5046506b6698c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549291"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Representando formatos para transmissões IEC 61937

Com o aumento nos dispositivos de armazenamento de mídia que exigem formatos de áudio compactados, os aplicativos devem identificar, descrever e usar uma variedade de novos conteúdos de áudio codificados para transmitir conteúdo de PCs para dispositivos como receptores de HDMI ou DisplayPort.

Para representar um fluxo de áudio codificado a ser transmitido em uma interface compatível com IEC 61937, um aplicativo deve fornecer:

-   As características de um fluxo de áudio codificado a ser transmitido.

-   As características de um fluxo de áudio decodificado no dispositivo de destino.

No Windows Vista e em sistemas operacionais Windows anteriores, um aplicativo pode inferir o nível de qualidade de um formato de áudio a partir do número de canais, do tamanho da amostra e da taxa de dados de um fluxo de áudio que usa o formato. Para um formato PCM, essas informações estão disponíveis nos membros **nChannels**, **nSamplesPerSec** e **nAvgBytesPerSec** da estrutura **WAVEFORMATEX** que especifica o formato. Para um formato não PCM, esses três membros foram commandeered para armazenar informações sobre os dados compactados no fluxo de áudio. Assim, a estrutura **WAVEFORMATEX** não tem informações sobre o número efetivo de canais, o tamanho da amostra e a taxa de dados do fluxo de áudio não PCM após o fluxo ser descompactado e reproduzido. Com base nas informações dessa estrutura, um usuário ou um aplicativo pode ter dificuldade em inferir o nível de qualidade do fluxo não PCM.

O **WAVEFORMATEX** foi estendido para a estrutura **WAVEFORMATEXTENSIBLE** para fornecer as características do fluxo extra. No entanto, essa estrutura também não é adequada para descrever o fluxo para transmissões do IEC 61937, pois foi destinada a representar um único conjunto de características e usada para dados PCM de vários canais descompactados.

No Windows 7, o sistema operacional resolve esse problema fornecendo suporte para uma nova estrutura, **WAVEFORMATEXTENSIBLE \_ IEC61937,** que estende a estrutura **WAVEFORMATEXTENSIBLE** para armazenar dois conjuntos de características de fluxo de áudio: o formato de áudio codificado antes da transmissão e as características do fluxo de áudio depois de decodificado. A nova estrutura especifica explicitamente o número efetivo de canais, o tamanho da amostra e a taxa de dados de um formato não PCM. Com essas informações, um aplicativo pode inferir o nível de qualidade do fluxo não PCM depois que ele é descompactado e tocado.

A **estrutura WAVEFORMATEXTENSIBLE \_ IEC61937** é declarada no header KsMedia.h incluído no SDK do Windows 7. O **membro FormatExt** é a **estrutura WAVEFORMATEXTENSIBLE** que armazena as características do fluxo a ser transmitido. O **membro** Format da estrutura **WAVEFORMATEXTENSIBLE** é a **estrutura WAVEFORMATEX.** O conteúdo desse **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** indica a um aplicativo se a estrutura pode ser interpretada como uma estrutura **WAVEFORMATEXTENSIBLE \_ IEC61937.** Para uma **estrutura WAVEFORMATEXTENSIBLE \_ IEC61937:**

-   O **membro wFormatTag** de **WAVEFORMATEX** deve conter WAVE \_ FORMAT \_ EXTENSIBLE ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).

-   O **membro SubFormat** da **estrutura WAVEFORMATEXTENSIBLE** especifica o GUID do formato codificado a ser transmitido. Por exemplo, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indica o formato Dolby Digital Plus. Para os GUIDs com suporte, consulte GUIDs de subformatação.

-   O tamanho indicado pelo **membro cbSize** do WAVEFORMATEX é de 34 bytes. (`FormatExt.Format.cbSize = 34`). O tamanho total de **WAVEFORMATEXTENSIBLE \_ IEC61937** é de 52 bytes.

Os membros **dwEncodedSamplesPerSec**, **dwEncodedChannelCount** e **dwAverageBytesPerSec** de **WAVEFORMATEXTENSIBLE \_ IEC61937** descrevem a taxa de amostragem, o número de canais e a taxa de bits em bytes do fluxo do fluxo de áudio depois que ele é decodificado.

## <a name="subformat-guids"></a>GUIDs de subformatação

No Windows 7, o cabeçalho KsMedia. h contém definições para os GUIDs de subformato para os formatos de áudio compactados definidos por CEA-861-D. Os GUIDs são especificados no membro de subformato do **WAVEFORMATEXTENSIBLE**, especificado no membro **FormatExt** da estrutura **WAVEFORMATEXTENSIBLE \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

Os GUIDs para os formatos de áudio compactados que estão disponíveis como formatos de áudio codificados Standard IEC 61937 são listados na tabela a seguir. Esses formatos são semelhantes às representações existentes de codificação ativa 3 (AC-3) e de som digital Theater (DTS) no Windows.



| Tipo CEA 861 | GUID do subformato                                                                                                          | Description                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Consulte o fluxo.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ subtipo \_ WAVEFORMATEX<br/>                          | PCM IEC 60958                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ subtipo \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (camada 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ subtipo \_ IEC61937 \_ MPEG3<br/>                       | MPEG-3 (camada 3)                             |
| 0x05         | 000000005-0cea-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2(multicanal)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ AAC<br/>                         | Codificação de áudio avançada (MPEG-2/4 AAC no ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0a         | 0000000a-0cea-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL \_ PLUS<br/>        | Dolby Digital Plus                           |
| 0x0a         | 0000010a-0cea-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL PLUS \_ \_ ATMOS<br/> | Dolby Atmos codificado com Dolby Digital Plus  |
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DTS \_ HD<br/> | DTS HD  |
| 0x0b         | 0000010b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DTSX \_ E1<br/> | DTS:X E1  |
| 0x0b         | 0000030b-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ subtipo \_ IEC61937 \_ dtsx \_ E2<br/> | DTS: X E2  |
| 0x0f         |                                                                                                                         | Não usado reservado                              |



 

Os GUIDs dos formatos de áudio compactados que são transmitidos em pacotes de exemplo de alta taxa de bits são listados na tabela a seguir.



| Tipo CEA 861 | GUID do subformato                                                                                           | Description                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> \_SUBTIPO KSDATAFORMAT \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (96Khz de 24 bits)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> \_SUBTIPO KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MLP<br/>   | Dolby-esteira 1,0:<br/> Dolby TrueHD (MLP – embalagem do meridiano sem perdas) – 192KHz de 24 bits/até 18 Mbps, 8 canais) <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ MAT20<br/> | Dolby-esteira 2,0: <br/> Dolby TrueHD – 192KHz de 24 bits/até 18 Mbps, 8 canais ou LPCM até 24 Mbps. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ MAT21<br/> | Dolby MAT 2.1: <br/> Dolby TrueHD – 192KHz de 24 bits/até 18 Mbps, 8 canais ou LPCM de até 24 Mbps. <br/>           |
| 0x0e         | 00000164-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ WMA \_ PRO<br/>     | WMA (Windows Media Audio) Pro                                                                                                   |



 

O driver de classe HD Audio fornecido pela Microsoft dá suporte a formatos PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP). Os GUIDs para os formatos de áudio compactados que não são suportados pelo driver de classe de áudio HD e podem ser implementados por soluções de terceiros são listados na tabela a seguir.



| Tipo CEA 861 | GUID de subformatação                                                                                              | Description                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ ATRAC<br/>           | ATRAC (Codificação Acústico de Transformação Adaptável)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ ÁUDIO DE UM \_ \_ BIT<br/> | One-Bit áudio                                                                  |
| 0x0d         | 0000000d-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DST<br/>             | DST (Direct Stream Transport) – DSD compactado sem perdas (Direct Stream digital). |



 

## <a name="dolby-digital-plus-format"></a>Formato Dolby Digital Plus

Quando o conteúdo Dolby Digital Plus é transmitido pelo IEC 60958, a taxa de amostragem de link deve ser quatro vezes a taxa de amostragem do conteúdo. O Dolby Digital Plus dá suporte a taxas de exemplo de conteúdo de 32 KHz, 44,1 KHz e 48 KHz. Interfaces como HDMI não dão suporte a 128 KHz (32 KHz x 4), de modo que apenas taxas de amostra de conteúdo 44,1 e 48 KHz podem ter suporte.

Os valores definidos por um aplicativo na estrutura WAVEFORMATEXTENSIBLE \_ IEC61937 para representar o formato Dolby Digital Plus a uma taxa de amostra de conteúdo de 48 kHz são mostrados no exemplo a seguir.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a>Dolby TrueHD (passe-partout)

O conteúdo Dolby TrueHD é transmitido por meio de IEC 60958 em canais 176,4 kHz/8 (exigindo uma taxa de quadros IEC 60958 de 705,6 kHz) para taxas de amostra de conteúdo de 44,1, 88,2 e 176,4 kHz e 192 canais kHz/8 (exigindo uma taxa de quadros IEC 60958 de 768 kHz) para taxas de exemplo de conteúdo de 48, 96 e 192 kHz.

Os valores definidos por um aplicativo na estrutura WAVEFORMATEXTENSIBLE \_ IEC61937 para representar o Dolby TrueHD em uma taxa de amostra de conteúdo de 96 kHz são mostrados nos exemplos a seguir.

Dolby-esteira 1,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby-esteira 2,0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby-esteira 2,1


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> O suporte para uma versão do Dolby enquadrant não significa suporte para Dolbyout com um número de versão inferior. Como o Dolby enquadramento 2,1 é compatível com versões anteriores do Dolbyout, um driver de classe que indica suporte para Dolby enquadrable 2,1 normalmente também indicará suporte para Dolby enquadrable 2,0 e Dolby PASSEs 1,0, usando uma \_ estrutura IEC61937 WAVEFORMATEXTENSIBLE separada para cada versão.

 

## <a name="wma-pro"></a>WMA Pro

O conteúdo de áudio do WMA pro pode ser codificado em um dos quatro perfis listados na tabela a seguir.



| Perfil | Propriedade-valor                                                                                                                                                                                                                                                      | Description                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Taxa de bits máxima – 192000 bps <br/> Taxa de amostragem máxima – 48 KHz <br/> Contagem máxima de canais – 2 <br/> Tamanho máximo do buffer – 600 \* 1024 bits <br/> Máximo de amostras por quadro – 2048 <br/> Máximo de bits por quadro – 655536<br/>   | Recomendado para música e streaming over-the-air.<br/> A taxa máxima de bits em um quadro de áudio é de 1536000 bps.<br/>          |
| M1      | Taxa de bits máxima – 385.000 bps <br/> Taxa máxima de amostragem – 48 KHz <br/> Contagem máxima de canais – 6 <br/> Tamanho máximo do buffer – 600 \* 1024 bits <br/> Máximo de amostras por quadro – 4096 <br/> Máximo de bits por quadro – 131072<br/>   | Recomendado para filmes de definição padrão de som ao redor.<br/> A taxa máxima de bits em um quadro de áudio é de 1536000 bps.<br/> |
| M2      | Taxa de bits máxima – 769000 bps <br/> Taxa máxima de amostragem – 96 KHz <br/> Contagem máxima de canais – 6 <br/> Tamanho máximo do buffer – 1200 \* 1024 bits <br/> Máximo de amostras por quadro – 4096 <br/> Máximo de bits por quadro – 131072<br/>  | Recomendado para filmes de alta definição de som surround.<br/> A taxa máxima em um quadro de áudio é de 3072000 bps.<br/>         |
| M3      | Taxa de bits máxima – 3 milhões bps <br/> Taxa de amostragem máxima – 96 KHz <br/> Contagem máxima de canais – 8 <br/> Tamanho máximo do buffer – 2400 \* 1024 bits <br/> Máximo de amostras por quadro – 4096 <br/> Máximo de bits por quadro-131072<br/> | Recomendado para o teatro digital.<br/> A taxa máxima em um quadro de áudio é de 3072000 bps.<br/>                               |



 

Os perfis M0 e M1 se encaixam em um fluxo 48 KHz/16 bits/estéreo (1536000 bps) IEC 60958. Os perfis m2 e M3 se enquadram em um fluxo 96 KHz/16 bits/estéreo (3072000 bps) IEC 60958.

Os valores definidos por um aplicativo na estrutura WAVEFORMATEXTENSIBLE \_ IEC61937 para representar o WMA pro como um perfil m2 são mostrados no exemplo a seguir.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de dispositivo](device-formats.md)
</dt> </dl>

 

 




