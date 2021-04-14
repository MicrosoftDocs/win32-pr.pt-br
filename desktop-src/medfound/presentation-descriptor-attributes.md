---
description: Atributos do descritor de apresentação
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Atributos do descritor de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502256"
---
# <a name="presentation-descriptor-attributes"></a>Atributos do descritor de apresentação

## <a name="common-presentation-descriptor-attributes"></a>Atributos de descritor de apresentação comum

Os atributos a seguir podem ser aplicados a qualquer descritor de apresentação.



| Atributo                                                                          | Descrição                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contexto de \_ aplicativo MF PD \_**](mf-pd-app-context-attribute.md)                        | Contém um ponteiro para o descritor de apresentação do caminho de mídia protegido (PMP).                                                          |
| [**\_taxa de \_ bits de codificação de áudio MF PD \_ \_**](mf-pd-audio-encoding-bitrate-attribute.md) | Especifica a taxa de bits de codificação de áudio para a apresentação, em bits por segundo.                                                                 |
| [áudio de PD de MF \_ \_ \_ ISVARIABLEBITRATE](mf-pd-audio-isvariablebitrate.md)              | Especifica se os fluxos de áudio na apresentação têm uma taxa de bits variável.                                                               |
| [**\_duração de PD MF \_**](mf-pd-duration-attribute.md)                               | Especifica a duração de uma apresentação, em unidades de 100 a nanossegundos.                                                                              |
| [**\_hora da \_ última \_ modificação \_ do MF PD**](mf-pd-last-modified-time-attribute.md)         | Especifica quando uma apresentação foi modificada pela última vez.                                                                                                |
| [**\_ \_ tipo MIME do MF PD \_**](mf-pd-mime-type-attribute.md)                            | Especifica o tipo MIME do conteúdo.                                                                                                         |
| [\_ \_ tempo limite de reprodução de PD MF \_ \_](mf-pd-playback-boundary-time.md)               | A hora em que a apresentação deve começar, em relação ao início da origem da mídia.                                                       |
| [\_ID do \_ elemento de reprodução de PD MF \_ \_](mf-pd-playback-element-id.md)                     | O identificador do elemento playlist na apresentação.                                                                                     |
| [**contexto de PMPHOST do MF \_ PD \_ \_**](mf-pd-pmphost-context-attribute.md)                | Contém um ponteiro para o objeto proxy para o descritor de apresentação do aplicativo.                                                           |
| [\_ \_ idioma preferencial do MF PD \_](mf-pd-preferred-language.md)                        | Contém o idioma preferencial RFC 1766 da fonte de mídia.                                                                                   |
| [**estilo do MF \_ PD \_ samilist \_**](mf-pd-sami-stylelist-attribute.md)                  | Contém o nome amigável dos estilos SAMI (intercâmbio de mídia acessível) com suporte. Esse atributo só se aplica a arquivos SAMI. |
| [**\_tamanho do \_ \_ arquivo total \_ do MF PD**](mf-pd-total-file-size-attribute.md)               | Especifica o tamanho total do arquivo de origem, em bytes.                                                                                          |
| [**\_taxa de \_ bits de codificação de vídeo MF PD \_ \_**](mf-pd-video-encoding-bitrate-attribute.md) | Especifica a taxa de bits de codificação de vídeo para a apresentação, em bits por segundo.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Atributos do descritor de apresentação para ASF

Os atributos a seguir se aplicam aos descritores de apresentação para arquivos ASF (Advanced Systems Format).



| Atributo                                                                                                             | Descrição                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**\_codec MF PD \_ asflist \_**](mf-pd-asf-codeclist-attribute.md)                                                       | Contém informações sobre os codecs usados para codificar o conteúdo em um arquivo ASF.                     |
| [**\_keyid PD \_ ASF \_ CONTENTENCRYPTION \_ do MF**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Especifica o identificador de chave para um arquivo ASF criptografado.                                              |
| [**URL de licença do MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Especifica a URL de aquisição de licença para um arquivo ASF criptografado.                                     |
| [**dados de segredo de CONTENTENCRYPTION do MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Contém dados secretos para um arquivo ASF criptografado.                                                      |
| [**\_tipo de CONTENTENCRYPTION MF PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-type-attribute.md)                            | Especifica o tipo de mecanismo de proteção usado em um arquivo ASF.                                      |
| [**\_dados de criptografia MF PD \_ ASF \_ CONTENTENCRYPTIONEX \_ \_**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Contém dados de criptografia para um arquivo ASF.                                                            |
| [**\_comprimento de \_ \_ dados ASF \_ do MF PD**](mf-pd-asf-data-length-attribute.md)                                                  | Especifica o tamanho, em bytes, da seção de dados de um arquivo ASF.                                    |
| [**deslocamento de início de dados do MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-data-start-offset-attribute.md)                                     | Especifica o deslocamento, em bytes, desde o início de um arquivo ASF até o início do primeiro pacote de dados. |
| [**\_hora de \_ \_ criação de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Especifica a data e a hora em que um arquivo ASF foi inicialmente criado.                                  |
| [**\_ID do \_ \_ arquivo FileProperties \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Especifica o identificador de arquivo de um arquivo ASF.                                                        |
| [**\_sinalizadores de \_ \_ FileProperties do MF PD ASF \_**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Contém sinalizadores diversos de um cabeçalho ASF.                                                     |
| [**\_taxa de \_ \_ \_ bits máxima de arquivo MF PD ASF \_**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Especifica a taxa máxima de bits instantâneas, em bits por segundo, para um arquivo ASF.                   |
| [**\_ \_ \_ \_ tamanho máximo do pacote FileProperties \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Especifica o tamanho máximo do pacote, em bytes, para um arquivo ASF                                         |
| [**\_tamanho de \_ \_ pacote FileProperties \_ min \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Especifica o tamanho mínimo do pacote, em bytes, para um arquivo ASF.                                        |
| [**\_ \_ \_ pacotes FileProperties do MF PD ASF \_**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Especifica o número de pacotes na seção de dados de um arquivo ASF.                                  |
| [**\_duração da \_ \_ reprodução de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Especifica o tempo necessário para reproduzir um arquivo ASF, em unidades de 100 a nanossegundos.                              |
| [**arquivo de arquivos do MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Especifica a quantidade de tempo para armazenar em buffer os dados antes de começar a reproduzir um arquivo ASF, em milissegundos.    |
| [**\_duração de \_ \_ envio de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Especifica o tempo necessário para enviar um arquivo ASF, em unidades de 100 a nanossegundos.                              |
| [**as \_ informações do MF PD \_ ASF \_ \_ têm \_ áudio**](mf-pd-asf-info-has-audio-attribute.md)                                           | Especifica se um arquivo ASF contém pelo menos um fluxo de áudio.                                    |
| [**as \_ informações do MF PD \_ ASF \_ \_ têm \_ \_ vídeo sem áudio \_**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Especifica se um arquivo ASF contém qualquer fluxo de não áudio e não vídeo.                             |
| [**informações do MF \_ PD \_ ASF \_ \_ têm \_ vídeo**](mf-pd-asf-info-has-video-attribute.md)                                           | Especifica se um arquivo ASF contém pelo menos um fluxo de vídeo.                                    |
| [**MF \_ PD \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md)                                                         | Especifica a lista de idiomas usados em um arquivo ASF.                                                 |
| [MF \_ PD \_ ASF \_ langlist \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | Contém uma lista de idiomas RFC 1766 usados na apresentação atual.                              |
| [**\_marcador de \_ ASF \_ PD MF**](mf-pd-asf-marker-attribute.md)                                                             | Especifica os marcadores em um arquivo ASF.                                                                |
| [**os \_ metadados de ASF PD MF \_ \_ \_ são \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Especifica se um arquivo ASF usa codificação de taxa de bits variável (VBR).                                 |
| [**\_pares de \_ \_ \_ \_ buckets de vazamento de \_ metadados do MF PD ASF**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Descreve os requisitos de buffer para um arquivo ASF de VBR.                                             |
| [**\_ \_ \_ \_ V8 \_ BUFFERAVERAGE do MF PD ASF de metadados**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Especifica o tamanho médio do buffer necessário para um arquivo ASF de VBR.                                         |
| [**\_ \_ \_ \_ V8 \_ VBRPEAK do MF PD ASF de metadados**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Especifica a taxa de bits momentânea mais alta em um arquivo ASF de VBR.                                          |
| [**\_script MF PD \_ ASF \_**](mf-pd-asf-script-attribute.md)                                                             | Especifica os comandos de script em um arquivo ASF.                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



