---
description: '\_áudio de \_ tipo de conteúdo WPD \_'
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83d43fcef539579fc0a687a97ba51e52278e4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773075"
---
# <a name="wpd_content_type_audio"></a>\_áudio de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo como \_ áudio de tipo de conteúdo WPD \_ \_ representa um arquivo de áudio, como um arquivo de áudio do Windows Media (WMA) ou MP3.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.     |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                          |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                          |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.     |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                          |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                          |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                  |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).              |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                  |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                          |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.              |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                            |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                          |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                          |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                             |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                          |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                       |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                          |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                         |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                          |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                          |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Necessário se o objeto puder ser excluído.                                             |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                          |
| [\_taxa de \_ bits total de mídia WPD \_](media-properties.md)                                            | Recomendável.                                                                       |
| [\_tipo de \_ taxa de bits de mídia WPD \_](media-properties.md)                                              | Opcional.                                                                          |
| [\_ \_ direitos autorais de mídia WPD](media-properties.md)                                                     | Opcional.                                                                          |
| [\_ID de \_ conteúdo de assinatura de mídia WPD \_ \_](media-properties.md)                       | Recomendado se esse objeto representar o conteúdo de um serviço de assinatura online. |
| [\_contagem de \_ uso de mídia WPD \_](media-properties.md)                                                    | Recomendável.                                                                       |
| [\_contagem de \_ ignorar \_ mídia WPD](media-properties.md)                                                  | Opcional.                                                                          |
| [\_hora do \_ último \_ acesso à mídia \_ WPD](media-properties.md)                                 | Opcional.                                                                          |
| [\_classificação de \_ controle de nível de mídia WPD \_](media-properties.md)                                        | Opcional.                                                                          |
| [metagênero de \_ mídia WPD \_ \_](media-properties.md)                                                  | Opcional.                                                                          |
| [\_COMPOSER de mídia WPD \_](media-properties.md)                                                       | Opcional.                                                                          |
| [\_ \_ classificação efetiva de mídia WPD \_](media-properties.md)                                      | Opcional.                                                                          |
| [subtítulo de \_ mídia WPD \_ \_](media-properties.md)                                                    | Opcional.                                                                          |
| [\_data de \_ lançamento de mídia WPD \_](media-properties.md)                                              | Recomendável.                                                                       |
| [\_taxa de \_ amostragem de mídia WPD \_](media-properties.md)                                                | Opcional.                                                                          |
| [\_classificação de \_ estrela de mídia WPD \_](media-properties.md)                                                | Recomendável.                                                                       |
| [\_ \_ classificação efetiva do usuário de mídia WPD \_ \_](media-properties.md)                           | Recomendável.                                                                       |
| [\_título de mídia WPD \_](media-properties.md)                                                             | Obrigatórios.                                                                          |
| [\_duração da mídia WPD \_](media-properties.md)                                                       | Obrigatórios.                                                                          |
| [a \_ mídia WPD \_ adquire \_ agora](media-properties.md)                                                        | Recomendável.                                                                       |
| [\_perfil de \_ codificação de mídia WPD \_](media-properties.md)                                      | Opcional.                                                                          |
| [\_artista de mídia WPD \_](media-properties.md)                                                                            | Recomendável.                                                                       |
| [\_artista do \_ álbum de mídia WPD \_](media-properties.md)                                                                     | Recomendável.                                                                       |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                                                                       | Opcional.                                                                          |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)                                                                  | Opcional.                                                                          |
| [\_Descrição da mídia WPD \_](media-properties.md)                                                                       | Opcional.                                                                          |
| [\_gênero de mídia WPD \_](media-properties.md)                                                                             | Opcional.                                                                          |
| [\_indicador de \_ tempo de mídia WPD \_](media-properties.md)                                                                    | Opcional.                                                                          |
| [\_indicador de \_ byte de mídia WPD \_](media-properties.md)                                                                    | Opcional.                                                                          |
| [\_GUID de mídia WPD \_](media-properties.md)                                                                              | Opcional.                                                                          |
| [subdescrição de \_ mídia WPD \_ \_](media-properties.md)                                                                  | Opcional.                                                                          |
| [\_álbum de música WPD \_](music-properties.md)                                                             | Recomendável.                                                                       |
| [\_faixa de música WPD \_](music-properties.md)                                                             | Recomendável.                                                                       |
| [\_letras de música WPD \_](music-properties.md)                                                           | Opcional.                                                                          |
| [\_humor de música WPD \_](music-properties.md)                                                               | Opcional.                                                                          |
| [taxa de bits de \_ áudio WPD \_](audio-properties.md)                                                         | Recomendável.                                                                       |
| [\_contagem de \_ canais de áudio WPD \_](audio-properties.md)                                            | Opcional.                                                                          |
| [\_código de \_ formato de áudio WPD \_](audio-properties.md)                                                | Opcional.                                                                          |
| [\_profundidade de \_ bit de áudio WPD \_](audio-properties.md)                                                    | Opcional.                                                                          |
| [\_alinhamento de \_ bloco de áudio WPD \_](audio-properties.md)                                        | Opcional.                                                                          |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                               | Obrigatório ou opcional       | Descrição                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md)      | Opcional.                  | Contém o arquivo de áudio completo.                  |
| [**\_arte do \_ álbum de recursos WPD \_**](wpd-resource-album-art.md) | Recomendado, se disponível. | Contém a imagem do álbum.                |
| [**\_AUDIOCLIP de recursos WPD \_**](wpd-resource-audio-clip.md) | Opcional.                  | Contém um clipe de exemplo do arquivo de áudio completo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



