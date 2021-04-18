---
description: '\_vídeo de \_ tipo de conteúdo WPD \_'
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afde065ef233ff64a4eb72af8be5f7308050ff75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765273"
---
# <a name="wpd_content_type_video"></a>\_vídeo de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo de \_ vídeo de tipo de conteúdo WPD \_ \_ representa um arquivo de vídeo.

Esse tipo de objeto dá suporte às propriedades a seguir.



|                                                                                                                       |                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Nome da propriedade**                                                                                                     | **Obrigatório ou opcional**                                                                                                     |
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                               |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                                                                    |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                                                                    |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                               |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                                                                    |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                                                                    |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                                            |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).                                                        |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                                            |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                                                    |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.                                                        |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                                                                      |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                                                                    |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                                    |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                                       |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                                                                    |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                                                                 |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                                                                    |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                                                   |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                                                                    |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                                                                    |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Obrigatório se o objeto não puder ser excluído.                                                                                    |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                                                                    |
| [\_taxa de \_ bits total de mídia WPD \_](media-properties.md)                                            | Recomendável.                                                                                                                 |
| [\_tipo de \_ taxa de bits de mídia WPD \_](media-properties.md)                                              | Opcional.                                                                                                                    |
| [\_ \_ direitos autorais de mídia WPD](media-properties.md)                                                     | Opcional.                                                                                                                    |
| [\_ID de \_ conteúdo de assinatura de mídia WPD \_ \_](media-properties.md)                       | Recomendado, se esse objeto representar o conteúdo de um serviço de assinatura online.                                          |
| [\_contagem de \_ uso de mídia WPD \_](media-properties.md)                                                    | Recomendável.                                                                                                                 |
| [\_contagem de \_ ignorar \_ mídia WPD](media-properties.md)                                                  | Opcional.                                                                                                                    |
| [\_hora do \_ último \_ acesso à mídia \_ WPD](media-properties.md)                                 | Opcional.                                                                                                                    |
| [\_classificação de \_ controle de nível de mídia WPD \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [metagênero de \_ mídia WPD \_ \_](media-properties.md)                                                  | Opcional.                                                                                                                    |
| [\_COMPOSER de mídia WPD \_](media-properties.md)                                                       | Opcional.                                                                                                                    |
| [\_ \_ classificação efetiva de mídia WPD \_](media-properties.md)                                      | Opcional.                                                                                                                    |
| [subtítulo de \_ mídia WPD \_ \_](media-properties.md)                                                    | Opcional.                                                                                                                    |
| [\_data de \_ lançamento de mídia WPD \_](media-properties.md)                                              | Recomendável.                                                                                                                 |
| [\_taxa de \_ amostragem de mídia WPD \_](media-properties.md)                                                | Opcional.                                                                                                                    |
| [\_classificação de \_ estrela de mídia WPD \_](media-properties.md)                                                | Recomendável.                                                                                                                 |
| [\_ \_ classificação efetiva do usuário de mídia WPD \_ \_](media-properties.md)                           | Recomendável.                                                                                                                 |
| [\_título de mídia WPD \_](media-properties.md)                                                             | Obrigatórios.                                                                                                                    |
| [\_duração da mídia WPD \_](media-properties.md)                                                       | Obrigatórios.                                                                                                                    |
| [a \_ mídia WPD \_ adquire \_ agora](media-properties.md)                                                        | Recomendável.                                                                                                                 |
| [\_perfil de \_ codificação de mídia WPD \_](media-properties.md)                                      | Opcional.                                                                                                                    |
| [\_largura de mídia WPD \_](media-properties.md)                                                             | Obrigatórios.                                                                                                                    |
| [\_altura de mídia WPD \_](media-properties.md)                                                           | Obrigatórios.                                                                                                                    |
| [\_artista de mídia WPD \_](media-properties.md)                                                           | Recomendável.                                                                                                                 |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                                                  | Recomendável.                                                                                                                 |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [\_Descrição da mídia WPD \_](media-properties.md)                                                 | Opcional.                                                                                                                    |
| [\_gênero de mídia WPD \_](media-properties.md)                                                             | Opcional.                                                                                                                    |
| [\_indicador de \_ tempo de mídia WPD \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [\_indicador de \_ byte de mídia WPD \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [\_GUID de mídia WPD \_](media-properties.md)                                                               | Opcional.                                                                                                                    |
| [subdescrição de \_ mídia WPD \_ \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [\_autor de vídeo WPD \_](video-properties.md)                                                           | Opcional.                                                                                                                    |
| [\_nome da \_ \_ estação RECORDEDTV de vídeo \_ WPD](video-properties.md)                       | Opcional.                                                                                                                    |
| [\_número de \_ \_ canal RECORDEDTV de vídeo \_ WPD](video-properties.md)                   | Opcional.                                                                                                                    |
| [\_repetição de \_ RECORDEDTV de vídeo WPD \_](video-properties.md)                                    | Opcional.                                                                                                                    |
| [\_tamanho do \_ buffer de vídeo WPD \_](video-properties.md)                                                | Opcional.                                                                                                                    |
| [\_créditos de vídeo WPD \_](video-properties.md)                                                         | Opcional.                                                                                                                    |
| [\_distância do \_ quadro da chave de vídeo WPD \_ \_](video-properties.md)                                 | Opcional.                                                                                                                    |
| [\_configuração de \_ qualidade de vídeo WPD \_](video-properties.md)                                        | Opcional.                                                                                                                    |
| [\_tipo de \_ exame de vídeo WPD \_](video-properties.md)                                                    | Obrigatórios.                                                                                                                    |
| [taxa de bits de \_ vídeo WPD \_](video-properties.md)                                                         | Obrigatórios.                                                                                                                    |
| [\_ \_ código FOURCC de vídeo WPD \_](video-properties.md)                                                | Necessário se o codec for um suportado pelo Microsoft Video for Windows (VFW), Microsoft DirectShow e Windows Media Format. |
| [taxa de quadros de \_ vídeo WPD \_](video-properties.md)                                                     | Opcional.                                                                                                                    |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                              | Obrigatório ou opcional       | Descrição                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md)     | Obrigatórios.                  | Contém os dados de vídeo (arquivo).                                      |
| [**\_miniatura do recurso WPD \_**](wpd-resource-thumbnail.md) | Recomendado, se disponível. | Contém o quadro-chave ou outro quadro de exemplo não em branco para o vídeo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



