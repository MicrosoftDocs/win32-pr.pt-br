---
description: As tabelas a seguir listam os GUIDs de subtipo de mídia para áudio. Quando aplicável, cada tabela lista a marca de formato equivalente, declarada em Mmreg. h.
ms.assetid: 55012be5-2d61-4d38-aab7-0c42f161f555
title: Subtipos de áudio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b9ccbe83a20f23976e506124c674119eee3a96
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456588"
---
# <a name="audio-subtypes"></a>Subtipos de áudio

As tabelas a seguir listam os GUIDs de subtipo de mídia para áudio. Quando aplicável, cada tabela lista a marca de formato equivalente, declarada em Mmreg. h.

## <a name="uncompressed-audio-types"></a>Tipos de áudio não compactados



| GUID                          | Descrição                | Cabeçalho  | Marca de formato equivalente                  |
|-------------------------------|----------------------------|---------|----------------------------------------|
| **MEDIASUBTYPE \_ IEEE \_ float** | Áudio de ponto flutuante do IEEE. | UUIDs. h | **Onda \_ Formatar \_ IEEE \_ float** (0x0003) |
| **\_PCM MEDIASUBTYPE**         | Áudio PCM.                 | UUIDs. h | **Onda \_ FORMATO \_ PCM** (0x0001)         |



 

## <a name="mpeg-4-and-aac-audio-types"></a>Tipos de áudio MPEG-4 e AAC



| GUID                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Cabeçalho       | Marca de formato equivalente                      |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------|
| **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC** | Áudio AAC (codificação de áudio avançado) no formato de fluxo de transporte de dados de áudio (ADTS).<br/> O bloco de formato é uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) com **wFormatTag** igual **ao \_ formato Wave \_ MPEG \_ ADTS \_ AAC**.<br/> A estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica a taxa de amostra AAC-LC principal e o número de canais, antes de aplicar as ferramentas SBR (replicação de banda Spectral) ou PS (estéreo paramétrica), se presentes.<br/> Nenhum dado adicional é necessário após a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                 | wmcodecdsp. h | **Onda \_ FORMAT \_ MPEG \_ ADTS \_ AAC** (0x1600) |
| **MEDIASUBTYPE \_ MPEG \_ HEAAC**     | Fluxo de High-Efficiency codificação de áudio avançada (HE-AAC).<br/> O bloco de formato é uma estrutura [**HEAACWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveformat) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | wmcodecdsp. h | **Onda \_ FORMAT \_ MPEG \_ HEAAC** (0x1610)     |
| **MEDIASUBTYPE \_ MPEG \_ loas**      | Fluxo de transporte de áudio MPEG-4 com uma camada de sincronização (LOAS) e uma camada de multiplexação (LATM).<br/> O bloco de formato é uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) com **wFormatTag** igual **ao \_ formato Wave \_ MPEG \_ loas**.<br/> A estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica a taxa de amostra AAC-LC principal e o número de canais, antes da aplicação de ferramentas de Spectral SBR ou PS, se presente.<br/> Nenhum dado adicional é necessário após a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                                             | wmcodecdsp. h | **Onda \_ FORMAT \_ MPEG \_ loas** (0x1602)      |
| **\_AAC1 bruto \_ MEDIASUBTYPE**       | AAC bruto.<br/> O bloco de formato é uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) com **WFormatTag** igual a **Wave \_ Format \_ RAW \_ AAC1**.<br/> A estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica a taxa de amostra e o número de canais no áudio decodificado após a aplicação das ferramentas SBR e PS, se presentes.<br/> A estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) é seguida por bytes adicionais que contêm os dados de AudioSpecificConfig (), conforme definido pelo ISO/IEC 14496-3 (áudio MPEG-4). <br/> O comprimento dos dados de AudioSpecificConfig () é de 2 bytes para AAC-LC ou HE-AAC com sinalização implícita de SBR/PS. É mais de 2 bytes para HE-AAC com sinalização explícita de SBR/PS.<br/> | wmcodecdps. h | **Onda \_ Formatar \_ \_ AAC1 bruto** (0x00FF)       |



 

## <a name="dolby-audio-types"></a>Tipos de áudio Dolby



| GUID                                | Descrição                                                                                                                                                                                                             | Cabeçalho       | Marca de formato equivalente                        |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------------------------|
| **MEDIASUBTYPE \_ Dolby \_ DDPLUS**     | Áudio Dolby Digital Plus.                                                                                                                                                                                               | wmcodecdsp. h | N/D                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3**        | Áudio Dolby Digital (AC-3).                                                                                                                                                                                             | ksuuids. h    | N/D                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** | Dolby AC-3 sobre S/PDIF.                                                                                                                                                                                                 | UUIDs. h      | **Onda \_ FORMAT \_ Dolby \_ AC3 \_ SPDIF** (0x0092) |
| **MEDIASUBTYPE \_ DVM**               | Codec DVM AC-3. Usado ao reproduzir arquivos AVI com áudio Dolby Digital.<br/> O bloco de formato é uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) com a marca de formato igual ao **\_ formato Wave \_ DVM**.<br/> | wmcodecdsp. h | **Onda \_ FORMAT \_ DVM** (0x2000)               |
| **\_esporte bruto \_ MEDIASUBTYPE**        | AC-3 sobre S/PDIF; consulte comentários.                                                                                                                                                                                          | UUIDs. h      | **Onda \_ Formatar \_ \_ esporte bruto** (0x0240)        |
| **MEDIASUBTYPE \_ \_ 241h marca \_ SPDIF**  | AC-3 sobre S/PDIF; consulte comentários.                                                                                                                                                                                          | UUIDs. h      | **Onda \_ FORMAT \_ ESST \_ AC3** (0x0241)         |



 

Para especificar preenchido AC-3, use o subtipo **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF**, que corresponde a uma marca de formato de 0x0092 (Wave \_ Format \_ Dolby \_ AC3 \_ SPDIF). Os valores 0x240 e 0x241 também foram usados para indicar o preenchido AC-3, mas a Microsoft incentiva o uso de 0x0092.

## <a name="miscellaneous-audio-types"></a>Diversos tipos de áudio



| GUID                                | Descrição                                                                                                                                                                                                                                                                          | Cabeçalho       | Marca de formato equivalente           |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------|
| **\_Áudio MEDIASUBTYPE DRM \_**        | Áudio com proteção de DRM (gerenciamento de direitos digitais).                                                                                                                                                                                                                               | UUIDs. h      | **Onda \_ FORMATO \_ DRM** (0x0009)  |
| **MEDIASUBTYPE \_ Dts**               | Áudio de DTS (Digital Theater Systems).<br/> O bloco de formato é uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) com a marca de formato igual ao **\_ formato Wave \_ desconhecido**.<br/>                                                                                              | ksuuids. h    | N/D                             |
| **MEDIASUBTYPE \_ DTS2**              | Áudio de DTS (Digital Theater Systems).<br/> O bloco de formato é uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) com a marca de formato igual ao **\_ formato Wave \_ DTS2**.<br/> Esse subtipo é equivalente ao **MEDIASUBTYPE \_ DTS** , mas usa uma marca de formato diferente.<br/> | wmcodecdsp. h | **Onda \_ FORMAT \_ DTS2** (0x2001) |
| **\_áudio MEDIASUBTYPE DVD \_ LPCM \_**  | Dados de áudio de DVD.                                                                                                                                                                                                                                                                      | ksuuids. h    | N/D                             |
| **MEDIASUBTYPE \_ MPEG1AudioPayload** | Carga de áudio MPEG-1.                                                                                                                                                                                                                                                                | UUIDs. h      | **Onda \_ FORMAT \_ MPEG** (0x0050) |
| **MEDIASUBTYPE \_ MPEG1Packet**       | Pacote de áudio MPEG1.                                                                                                                                                                                                                                                                  | UUIDs. h      | N/D                             |
| **MEDIASUBTYPE \_ MPEG1Payload**      | Carga de áudio MPEG1.                                                                                                                                                                                                                                                                 | UUIDs. h      | N/D                             |
| **\_Áudio MEDIASUBTYPE MPEG2 \_**      | Dados de áudio MPEG-2.                                                                                                                                                                                                                                                                   | ksuuids. h    | N/D                             |



 

## <a name="audio-format-tags"></a>Marcas de formato de áudio

O campo **wFormatTag** na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) especifica o tipo de formato de áudio. Exemplos de mídia geralmente são um número inteiro de amostras, conforme especificado no campo **wBitsPerSample** na estrutura **WAVEFORMATEX** . Isso não é necessariamente verdadeiro para exemplos de áudio MPEG que podem vir de fluxos empacotados e, portanto, não são necessariamente empacotados em limites de amostra/quadro. Para áudio MPEG, o carimbo de data/hora em um exemplo de mídia é o carimbo de data/hora do primeiro quadro cujo primeiro byte está contido no exemplo de mídia.

Os subtipos de mídia são definidos para cada **wFormatTag** da seguinte maneira:

-   O subcampo data1 do GUID do subtipo é o mesmo que o valor **wFormatTag** .
-   O campo Data 2 é 0.
-   O campo Data 3 é 0x0010.
-   O campo data 4 é 0x80, 0x00, 0x00, 0xAA, 0x00, 0x38, 0x9B, 0x71.

Portanto, para áudio PCM, o GUID do subtipo (definido em UUIDs. h como **MEDIASUBTYPE \_ PCM**) é:

`{00000001-0000-0010-8000-00AA00389B71}`

A função [**CreateAudioMediaType**](createaudiomediatype.md) pode ser usada para criar uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) de uma estrutura **WAVEFORMATEX** .

## <a name="obsolete-audio-types"></a>Tipos de áudio obsoletos

Os seguintes subtipos de áudio são obsoletos e não devem ser usados:

-   **\_ \_ AAC bruto MEDIASUBTYPE \_ MPEG**
-   **MEDIASUBTYPE \_ PCMAudioObsolete**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de mídia am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

