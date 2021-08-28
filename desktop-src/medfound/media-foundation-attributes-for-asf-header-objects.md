---
description: Media Foundation atributos para objetos de header ASF
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Media Foundation atributos para objetos de header ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f0125373000c370f848239717b00aa2615fc16faa84270236704e124cb3bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061176"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Media Foundation atributos para objetos de header ASF

O objeto de header ASF de nível superior para um arquivo contém vários objetos de sub-header ASF. O objeto ContentInfo armazena informações de todos esses Objetos de Título e expõe determinados valores a um aplicativo por meio de atributos.

## <a name="file-properties-object"></a>Objeto Propriedades do Arquivo

Esse objeto de header está presente em todos os arquivos ASF. Esses campos descrevem os atributos de nível de arquivo de toda a apresentação. A tabela a seguir lista os campos no Objeto de Propriedades do Arquivo e os atributos do descritor de apresentação correspondentes.



| Campo Objeto Propriedades do Arquivo | Atributo do descritor de apresentação                                                                            | Descrição                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| ID do Arquivo                      | [**ID DE ARQUIVO \_ \_ ASF \_ FILEPROPERTIES \_ do \_ MF PD**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Identificador exclusivo para esse arquivo.                                                               |
| Tamanho do arquivo                    | [**TAMANHO TOTAL \_ DO ARQUIVO MF PD \_ \_ \_**](mf-pd-total-file-size-attribute.md)                                         | Tamanho do arquivo, em bytes.                                                                    |
| Data de Criação                | [**HORA DE \_ CRIAÇÃO \_ DE ARQUIVO ASF ASF \_ MF \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | A data e hora de criação do arquivo.                                                               |
| Contagem de Pacotes de Dados           | [**PACOTES MF \_ PD \_ ASF \_ FILEPROPERTIES \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Número de pacotes de dados no objeto de dados ASF.                                                 |
| Duração da reprodução                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PLAY \_ DURATION**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Tempo necessário para reproduzir o arquivo, em unidades de 100 nanossegundos. Esse valor inclui o tempo de pré-roll. |
| Duração do envio                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Tempo necessário para enviar o arquivo, em unidades de 100 nanossegundos.                                       |
| Preroll                      | [**\_PRÉ-REGISTRO DE \_ ARQUIVO ASF \_ DO \_ MF PD**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Período de tempo para buffer de dados antes da reprodução do arquivo, em unidades de 100 nanossegundos.            |
| Flags                        | [**SINALIZADORES \_ \_ \_ FILEPROPERTIES DO MF PD ASF \_**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Sinalizadores que indicam se o arquivo é difuso ou que pode ser buscado.                                    |
| Tamanho mínimo do pacote de dados     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Tamanho mínimo dos pacotes de dados no arquivo, em bytes.                                        |
| Tamanho máximo do pacote de dados     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Tamanho máximo dos pacotes de dados no arquivo, em bytes.                                        |
| Taxa de bits máxima              | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Taxa de bits instantânea máxima, em bits por segundo.                                            |



 

## <a name="stream-properties-object"></a>Objeto Propriedades do Fluxo

Esse objeto de header descreve as propriedades dos fluxos no arquivo ASF. No Media Foundation, isso é gerenciado pelo objeto de perfil e pelo objeto de configuração de fluxo. Para obter mais informações, [consulte Criando e configurando o ASF Fluxos](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Objeto Codec List

Se esse objeto de header estiver presente, o atributo [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md) fornece uma lista de codecs que foram usados para codificar os fluxos dentro do arquivo ASF. Cada fluxo deve ter suas informações de codec neste objeto.

## <a name="script-command-object"></a>Objeto de comando Script

Se esse objeto de header estiver presente, ele especificará uma lista de comandos de script com suporte no arquivo ASF. Um comando de script consiste em um tipo de comando, um nome de comando e uma hora de apresentação. O tipo de comando e o nome do comando são cadeias de caracteres largos. Esses comandos podem ser usados para notificar o cliente para executar uma ação em um determinado ponto da apresentação. Por exemplo, um aplicativo pode usar o tipo de comando "FILENAME" para reproduzir uma sequência contínua de arquivos ASF.

Para obter a lista de comandos de script, obter o atributo [**\_ \_ \_ MF PD ASF SCRIPT**](mf-pd-asf-script-attribute.md) do descritor de apresentação. Um aplicativo deve recuperar todos os comandos de script antes de iniciar a reprodução.

## <a name="marker-object"></a>Objeto Marker

Um marcador é um indicador dentro de um arquivo ASF. Um aplicativo pode usar marcadores para buscar vários pontos dentro do conteúdo. Cada marcador consiste em um nome de marcador, a hora de apresentação associada e o deslocamento do início do arquivo. O [**atributo MF \_ PD \_ ASF \_ MARKER**](mf-pd-asf-marker-attribute.md) fornece uma lista de marcadores que estão disponíveis para o arquivo.

## <a name="stream-bitrate-properties-object"></a>Objeto propriedades de taxa de bits de fluxo

Esse header armazena a taxa média de bits de cada fluxo presente no arquivo ASF. Esse valor é armazenado no descritor de fluxo para o fluxo no atributo [**\_ \_ \_ STREAMBITRATES \_ BITRATE do ASF SD SD.**](mf-sd-asf-streambitrates-bitrate-attribute.md)

## <a name="content-encryption-object"></a>Objeto de criptografia de conteúdo

Esse objeto de título estará presente se o provedor de conteúdo tiver protegido o conteúdo usando o Microsoft Digital Rights Management. A tabela a seguir lista os campos no Objeto de Criptografia de Conteúdo e os atributos de descritor de apresentação correspondentes:



| Campo Objeto de Criptografia de Conteúdo | Atributo do descritor de apresentação                                                                         | Descrição                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Dados secretos                     | [**DADOS SECRETOS \_ \_ DE ASF PD \_ ASF CONFORMENCRYPTION \_ \_**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Matriz de byte que contém dados secretos.                                                                 |
| Tipo de proteção                 | [**MF \_ PD \_ ASF TIPO \_ ASNCRYPTION \_**](mf-pd-asf-contentencryption-type-attribute.md)                | Cadeia de caracteres terminada em nulo que tem o valor "DRM".                                                       |
| Identificação da Chave                          | [**KEYID \_ \_ DE ASF PD \_ ASF QUENCRYPTION \_**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Cadeia de caracteres terminada em nulo que descreve o identificador de chave.                                          |
| URL da licença                     | [**URL DE \_ LICENÇA DO MF PD \_ ASF \_ ASFCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) | Cadeia de caracteres terminada em nulo que contém a URL da qual adquirir a licença para usar o conteúdo. |



 

## <a name="extended-content-encryption-object"></a>Objeto de criptografia de conteúdo estendido

Esse objeto de título estará presente se o provedor de conteúdo tiver protegido o conteúdo usando o SDK Windows Media Rights Manager 7. O atributo URL DE LICENÇA [**\_ DE ASF PD \_ ASF \_ QUENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) fornece uma matriz de byte que corresponde ao campo Dados do objeto de título. Esse campo é necessário para usar o conteúdo.

## <a name="extended-stream-properties-object"></a>Objeto Propriedades de Fluxo Estendido

Esse header faz parte do Objeto de Extensão de Header. O Objeto de Propriedades de Fluxo Estendido fornece propriedades do fluxo que não estão definidas no objeto Propriedades do Fluxo. Essas propriedades são usadas principalmente para determinar os parâmetros "bucket vazado", que são usados pelo decodificador. Essas propriedades também são usadas pelo codificador ao compactar dados. Isso é gerenciado pelo objeto de perfil e pelo objeto de configuração de fluxo. Para obter mais informações, [consulte Criando e configurando o ASF Fluxos](creating-and-configuring-asf-streams.md).

A tabela a seguir lista os campos Objeto de Propriedades de Fluxo Estendido e os atributos de descritor de fluxo correspondentes.



| Campo Propriedades de Fluxo Estendido | Atributo de descritor de fluxo                                                                                | Descrição                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Taxa de bits de dados                     | [**\_taxa de \_ \_ \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Taxa média de dados, em bits por segundo.                                                                                   |
| Tamanho do Buffer                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ média \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Tamanho do Bucket de vazamentos. Valor é o número de milissegundos de dados que podem caber no buffer na taxa média de dados.      |
| Taxa de bits de dados alternativa           | [**\_taxa de \_ \_ \_ bits máxima de \_ dados EXTSTRMPROP \_ MF SD**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Taxa de dados de pico, em Bites por segundo. A taxa de dados de pico é usada para fluxos com uma taxa de bits variável.                    |
| Tamanho de buffer alternativo            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Tamanho máximo do Bucket de vazamento. Valor é o número de milissegundos de dados que podem caber no buffer na taxa de dados de pico. |
| ID da linguagem do fluxo               | [**índice de ID de idioma do MF \_ SD \_ ASF \_ EXTSTRMPROP \_ \_ \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | O idioma usado pelo fluxo, especificado como um índice na lista de idiomas no objeto da lista de idiomas.         |



 

## <a name="language-list-object"></a>Objeto de lista de idiomas

Esse objeto de cabeçalho faz parte do objeto de extensão de cabeçalho. Se estiver presente, o atributo [**MF \_ PD \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) fornecerá uma lista de identificadores de idioma com suporte no arquivo. Os identificadores são compatíveis com RFC 1766 para especificar idiomas.

## <a name="mutual-exclusion-object"></a>Objeto de exclusão mútua

Esse cabeçalho especifica grupos de fluxos e suas propriedades, apenas um dos quais será entregue de cada vez. para obter mais informações, consulte [usando a exclusão mútua para o Fluxos ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto ASF ContentInfo](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



