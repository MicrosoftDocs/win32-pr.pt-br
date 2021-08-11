---
description: Atributos do descritor de apresentação
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Atributos do descritor de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb9947a926fc6ea5e21f81219e6bd8d85a8d74bea9b9432ac497c539450b638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238962"
---
# <a name="presentation-descriptor-attributes"></a>Atributos do descritor de apresentação

## <a name="common-presentation-descriptor-attributes"></a>Atributos comuns do descritor de apresentação

Os atributos a seguir podem ser aplicados a qualquer descritor de apresentação.



| Atributo                                                                          | Descrição                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CONTEXTO DO \_ APLICATIVO MF PD \_ \_**](mf-pd-app-context-attribute.md)                        | Contém um ponteiro para o descritor de apresentação do caminho de mídia protegido (PMP).                                                          |
| [**TAXA DE BITS DE \_ \_ \_ CODIFICAÇÃO DE ÁUDIO DE MF PD \_**](mf-pd-audio-encoding-bitrate-attribute.md) | Especifica a taxa de bits de codificação de áudio para a apresentação, em bits por segundo.                                                                 |
| [MF \_ PD \_ AUDIO \_ ISVARIABLEBITRATE](mf-pd-audio-isvariablebitrate.md)              | Especifica se os fluxos de áudio na apresentação têm uma taxa de bits variável.                                                               |
| [**DURAÇÃO DA PD DO MF \_ \_**](mf-pd-duration-attribute.md)                               | Especifica a duração de uma apresentação, em unidades de 100 nanossegundos.                                                                              |
| [**HORA DA ÚLTIMA \_ MODIFICAÇÃO DA PD \_ \_ \_ MF**](mf-pd-last-modified-time-attribute.md)         | Especifica quando uma apresentação foi modificada pela última vez.                                                                                                |
| [**MF \_ PD \_ MIME \_ TYPE**](mf-pd-mime-type-attribute.md)                            | Especifica o tipo MIME do conteúdo.                                                                                                         |
| [TEMPO DE \_ LIMITE DE REPRODUÇÃO DE PD \_ \_ MF \_](mf-pd-playback-boundary-time.md)               | A hora em que a apresentação deve começar, em relação ao início da fonte de mídia.                                                       |
| [ID DO ELEMENTO MF \_ PD \_ \_ PLAYBACK \_](mf-pd-playback-element-id.md)                     | O identificador do elemento de playlist na apresentação.                                                                                     |
| [**CONTEXTO \_ \_ PMPHOST MF PD \_**](mf-pd-pmphost-context-attribute.md)                | Contém um ponteiro para o objeto proxy para o descritor de apresentação do aplicativo.                                                           |
| [LINGUAGEM PREFERENCIAL DO MF \_ PD \_ \_](mf-pd-preferred-language.md)                        | Contém a linguagem RFC 1766 preferencial da fonte de mídia.                                                                                   |
| [**MF \_ PD \_ SAMI \_ STYLELIST**](mf-pd-sami-stylelist-attribute.md)                  | Contém o nome amigável dos estilos SAMI (Synchronized Accessible Media Interchange) com suporte. Esse atributo se aplica somente a arquivos SAMI. |
| [**TAMANHO TOTAL \_ DO ARQUIVO MF PD \_ \_ \_**](mf-pd-total-file-size-attribute.md)               | Especifica o tamanho total do arquivo de origem, em bytes.                                                                                          |
| [**TAXA DE BITS DE \_ \_ \_ CODIFICAÇÃO DE VÍDEO DE MF PD \_**](mf-pd-video-encoding-bitrate-attribute.md) | Especifica a taxa de bits de codificação de vídeo para a apresentação, em bits por segundo.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Atributos do descritor de apresentação para ASF

Os atributos a seguir se aplicam a descritores de apresentação para arquivos ASF (Advanced Systems Format).



| Atributo                                                                                                             | Descrição                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md)                                                       | Contém informações sobre os codecs usados para codificar o conteúdo em um arquivo ASF.                     |
| [**KEYID \_ \_ DE ASF PD \_ ASF QUENCRYPTION \_**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Especifica o identificador de chave para um arquivo ASF criptografado.                                              |
| [**URL DE \_ LICENÇA DO MF PD \_ ASF \_ ASFCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Especifica a URL de aquisição de licença para um arquivo ASF criptografado.                                     |
| [**DADOS SECRETOS \_ \_ DE ASF PD \_ ASF CONFORMENCRYPTION \_ \_**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Contém dados secretos para um arquivo ASF criptografado.                                                      |
| [**MF \_ PD \_ ASF TIPO \_ ASNCRYPTION \_**](mf-pd-asf-contentencryption-type-attribute.md)                            | Especifica o tipo de mecanismo de proteção usado em um arquivo ASF.                                      |
| [**DADOS DE CRIPTOGRAFIA DO MF \_ PD \_ ASF \_ ASFCRYPTIONEX \_ \_**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Contém dados de criptografia para um arquivo ASF.                                                            |
| [**MF \_ PD \_ ASF \_ DATA \_ LENGTH**](mf-pd-asf-data-length-attribute.md)                                                  | Especifica o tamanho, em bytes, da seção de dados de um arquivo ASF.                                    |
| [**DESLOCAMENTO DE \_ INÍCIO \_ DE DADOS ASF \_ DO \_ \_ MF PD**](mf-pd-asf-data-start-offset-attribute.md)                                     | Especifica o deslocamento, em bytes, do início de um arquivo ASF ao início do primeiro pacote de dados. |
| [**HORA DE \_ CRIAÇÃO \_ DE ARQUIVO ASF ASF \_ MF \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Especifica a data e a hora em que um arquivo ASF foi criado inicialmente.                                  |
| [**ID DE ARQUIVO \_ \_ ASF \_ FILEPROPERTIES \_ do \_ MF PD**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Especifica o identificador de arquivo de um arquivo ASF.                                                        |
| [**SINALIZADORES \_ \_ \_ FILEPROPERTIES DO MF PD ASF \_**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Contém sinalizadores diversos de um header ASF.                                                     |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Especifica a taxa de bits instantânea máxima, em bits por segundo, para um arquivo ASF.                   |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Especifica o tamanho máximo do pacote, em bytes, para um arquivo ASF                                         |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Especifica o tamanho mínimo do pacote, em bytes, para um arquivo ASF.                                        |
| [**PACOTES MF \_ PD \_ ASF \_ FILEPROPERTIES \_**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Especifica o número de pacotes na seção de dados de um arquivo ASF.                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PLAY \_ DURATION**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Especifica o tempo necessário para reproduzir um arquivo ASF, em unidades de 100 nanossegundos.                              |
| [**\_PRÉ-REGISTRO DE \_ ARQUIVO ASF \_ DO \_ MF PD**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Especifica a quantidade de tempo para buffer de dados antes de começar a reproduzir um arquivo ASF, em milissegundos.    |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Especifica o tempo necessário para enviar um arquivo ASF, em unidades de 100 nanossegundos.                              |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ AUDIO**](mf-pd-asf-info-has-audio-attribute.md)                                           | Especifica se um arquivo ASF contém pelo menos um fluxo de áudio.                                    |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ NON \_ AUDIO \_ VIDEO**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Especifica se um arquivo ASF contém fluxos que não são de áudio e não vídeo.                             |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ VIDEO**](mf-pd-asf-info-has-video-attribute.md)                                           | Especifica se um arquivo ASF contém pelo menos um fluxo de vídeo.                                    |
| [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)                                                         | Especifica a lista de idiomas usados em um arquivo ASF.                                                 |
| [MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | Contém uma lista de idiomas RFC 1766 usados na apresentação atual.                              |
| [**MARCADOR \_ \_ ASF PD MF \_**](mf-pd-asf-marker-attribute.md)                                                             | Especifica os marcadores em um arquivo ASF.                                                                |
| [**OS \_ METADADOS \_ DO ASF PD MF \_ SÃO \_ \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Especifica se um arquivo ASF usa codificação VBR (taxa de bits variável).                                 |
| [**PARES DE BUCKET COM VAZAMENTO DE \_ \_ METADADOS DO MF PD ASF \_ \_ \_ \_**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Descreve os requisitos de buffer para um arquivo ASF VBR.                                             |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ BUFFERAVERAGE**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Especifica o tamanho médio do buffer necessário para um arquivo ASF VBR.                                         |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ VBRPEAK**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Especifica a taxa de bits momentânea mais alta em um arquivo ASF VBR.                                          |
| [**MF \_ PD \_ ASF \_ SCRIPT**](mf-pd-asf-script-attribute.md)                                                             | Especifica os comandos de script em um arquivo ASF.                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



