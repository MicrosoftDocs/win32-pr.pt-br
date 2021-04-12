---
description: Atributos de Media Foundation para objetos de cabeçalho ASF
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Atributos de Media Foundation para objetos de cabeçalho ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db74ccb03536c7766dd7e1564119edbd41d5dbe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297969"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Atributos de Media Foundation para objetos de cabeçalho ASF

O objeto de cabeçalho ASF de nível superior de um arquivo contém vários objetos de subcabeçalho ASF. O objeto ContentInfo armazena informações de todos esses objetos de cabeçalho e expõe determinados valores a um aplicativo por meio de atributos.

## <a name="file-properties-object"></a>Objeto de propriedades do arquivo

Esse objeto de cabeçalho está presente em todos os arquivos ASF. Esses campos descrevem os atributos de nível de arquivo da apresentação inteira. A tabela a seguir lista os campos no objeto de propriedades de arquivo e os atributos do descritor de apresentação correspondentes.



| Campo de objeto de propriedades de arquivo | Atributo de descritor de apresentação                                                                            | Descrição                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| ID do Arquivo                      | [**\_ID do \_ \_ arquivo FileProperties \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Identificador exclusivo deste arquivo.                                                               |
| Tamanho do arquivo                    | [**\_tamanho do \_ \_ arquivo total \_ do MF PD**](mf-pd-total-file-size-attribute.md)                                         | Tamanho do arquivo, em bytes.                                                                    |
| Data de Criação                | [**\_hora de \_ \_ criação de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | A data e a hora de criação do arquivo.                                                               |
| Contagem de pacotes de dados           | [**\_ \_ \_ pacotes FileProperties do MF PD ASF \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Número de pacotes de dados no objeto de dados ASF.                                                 |
| Duração da reprodução                | [**\_duração da \_ \_ reprodução de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Tempo necessário para executar o arquivo, em unidades de 100 a nanossegundos. Esse valor inclui o tempo de preversão. |
| Duração do envio                | [**\_duração de \_ \_ envio de FileProperties do \_ MF PD ASF \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Tempo necessário para enviar o arquivo, em unidades de 100 a nanossegundos.                                       |
| Prelance                      | [**arquivo de arquivos do MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Período de tempo para armazenar em buffer os dados antes da reprodução do arquivo, em unidades de 100 nanossegundos.            |
| Flags                        | [**\_sinalizadores de \_ \_ FileProperties do MF PD ASF \_**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Sinalizadores que indicam se o arquivo é difundido ou pesquisável.                                    |
| Tamanho mínimo do pacote de dados     | [**\_tamanho de \_ \_ pacote FileProperties \_ min \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Tamanho mínimo dos pacotes de dados no arquivo, em bytes.                                        |
| Tamanho máximo do pacote de dados     | [**\_ \_ \_ \_ tamanho máximo do pacote FileProperties \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Tamanho máximo dos pacotes de dados no arquivo, em bytes.                                        |
| Taxa de bits máxima              | [**\_taxa de \_ \_ \_ bits máxima de arquivo MF PD ASF \_**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Taxa máxima de bits instantâneas, em bits por segundo.                                            |



 

## <a name="stream-properties-object"></a>Objeto de propriedades do fluxo

Esse objeto de cabeçalho descreve as propriedades dos fluxos no arquivo ASF. No Media Foundation, isso é gerenciado pelo objeto de perfil e o objeto de configuração de fluxo. Para obter mais informações, consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Objeto de lista de codecs

Se esse objeto de cabeçalho estiver presente, o atributo [**MF \_ PD \_ ASF \_**](mf-pd-asf-codeclist-attribute.md) . defaultlist fornecerá uma lista de codecs que foram usados para codificar os fluxos dentro do arquivo asf. Cada fluxo deve ter suas informações de codec neste objeto.

## <a name="script-command-object"></a>Objeto de comando de script

Se esse objeto de cabeçalho estiver presente, ele especificará uma lista de comandos de script com suporte no arquivo ASF. Um comando de script consiste em um tipo de comando, um nome de comando e uma hora de apresentação. O tipo de comando e o nome do comando são cadeias de caracteres largos. Esses comandos podem ser usados para notificar o cliente para executar uma ação em um determinado ponto da apresentação. Por exemplo, um aplicativo pode usar o tipo de comando "FILENAME" para reproduzir uma sequência contínua de arquivos ASF.

Para obter a lista de comandos de script, obtenha o atributo de [**\_ \_ \_ script MF PD ASF**](mf-pd-asf-script-attribute.md) do descritor de apresentação. Um aplicativo deve recuperar todos os comandos de script antes de iniciar a reprodução.

## <a name="marker-object"></a>Objeto de marcador

Um marcador é um indicador dentro de um arquivo ASF. Um aplicativo pode usar marcadores para buscar vários pontos dentro do conteúdo. Cada marcador consiste em um nome de marcador, na hora da apresentação associada e no deslocamento do início do arquivo. O atributo de [**\_ \_ \_ marcador MF PD ASF**](mf-pd-asf-marker-attribute.md) fornece uma lista de marcadores que estão disponíveis para o arquivo.

## <a name="stream-bitrate-properties-object"></a>Objeto de propriedades de taxa de bits de fluxo

Esse cabeçalho armazena a taxa média de bits de cada fluxo presente no arquivo ASF. Esse valor é armazenado no descritor de fluxo para o fluxo no atributo [**MF \_ SD \_ ASF \_ STREAMBITRATES taxa de \_ bits**](mf-sd-asf-streambitrates-bitrate-attribute.md) .

## <a name="content-encryption-object"></a>Objeto de criptografia de conteúdo

Esse objeto de cabeçalho estará presente se o provedor de conteúdo tiver protegido o conteúdo usando o Microsoft Digital Rights Management. A tabela a seguir lista os campos no objeto de criptografia de conteúdo e os atributos do descritor de apresentação correspondentes:



| Campo de objeto de criptografia de conteúdo | Atributo de descritor de apresentação                                                                         | Descrição                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Dados secretos                     | [**dados de segredo de CONTENTENCRYPTION do MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Matriz de bytes que contém dados secretos.                                                                 |
| Tipo de proteção                 | [**\_tipo de CONTENTENCRYPTION MF PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-type-attribute.md)                | Cadeia de caracteres terminada em nulo com o valor "DRM".                                                       |
| Identificação da Chave                          | [**\_keyid PD \_ ASF \_ CONTENTENCRYPTION \_ do MF**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Cadeia de caracteres terminada em nulo que descreve o identificador de chave.                                          |
| URL da licença                     | [**URL de licença do MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) | Cadeia de caracteres terminada em nulo que contém a URL da qual adquirir a licença para usar o conteúdo. |



 

## <a name="extended-content-encryption-object"></a>Objeto de criptografia de conteúdo estendido

Esse objeto de cabeçalho estará presente se o provedor de conteúdo tiver protegido o conteúdo usando o SDK do Windows Media Rights Manager 7. O atributo de [**\_ URL de licença MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) fornece uma matriz de bytes que corresponde ao campo de dados do objeto de cabeçalho. Este campo é necessário para usar o conteúdo.

## <a name="extended-stream-properties-object"></a>Objeto de propriedades de fluxo estendido

Esse cabeçalho faz parte do objeto de extensão de cabeçalho. O objeto de propriedades de fluxo estendido fornece propriedades do fluxo que não estão definidas no objeto de propriedades de fluxo. Essas propriedades são usadas principalmente para determinar os parâmetros de "Bucket de vazamentos", que são usados pelo decodificador. Essas propriedades também são usadas pelo codificador ao compactar dados. Isso é gerenciado pelo objeto de perfil e o objeto de configuração de fluxo. Para obter mais informações, consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md).

A tabela a seguir lista os campos de objeto de propriedades de fluxo estendidos e os atributos de descritor de fluxo correspondentes.



| Campo de propriedades de fluxo estendido | Atributo de descritor de fluxo                                                                                | Descrição                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Taxa de bits de dados                     | [**\_taxa de \_ \_ \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Taxa média de dados, em bits por segundo.                                                                                   |
| Tamanho do Buffer                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ média \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Tamanho do Bucket de vazamentos. Valor é o número de milissegundos de dados que podem caber no buffer na taxa média de dados.      |
| Taxa de bits de dados alternativa           | [**\_taxa de \_ \_ \_ bits máxima de \_ dados EXTSTRMPROP \_ MF SD**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Taxa de dados de pico, em Bites por segundo. A taxa de dados de pico é usada para fluxos com uma taxa de bits variável.                    |
| Tamanho de buffer alternativo            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Tamanho máximo do Bucket de vazamento. Valor é o número de milissegundos de dados que podem caber no buffer na taxa de dados de pico. |
| ID da linguagem do fluxo               | [**índice de ID de idioma do MF \_ SD \_ ASF \_ EXTSTRMPROP \_ \_ \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | O idioma usado pelo fluxo, especificado como um índice na lista de idiomas no objeto da lista de idiomas.         |



 

## <a name="language-list-object"></a>Objeto de lista de idiomas

Esse objeto de cabeçalho faz parte do objeto de extensão de cabeçalho. Se estiver presente, o atributo [**MF \_ PD \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) fornecerá uma lista de identificadores de idioma com suporte no arquivo. Os identificadores são compatíveis com RFC 1766 para especificar idiomas.

## <a name="mutual-exclusion-object"></a>Objeto de exclusão mútua

Esse cabeçalho especifica grupos de fluxos e suas propriedades, apenas um dos quais será entregue de cada vez. Para obter mais informações, consulte [usando a exclusão mútua para fluxos ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto ASF ContentInfo](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



