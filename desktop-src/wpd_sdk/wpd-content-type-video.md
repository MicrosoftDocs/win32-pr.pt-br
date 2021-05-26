---
description: '\_vídeo de \_ tipo de conteúdo WPD \_'
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aacf30a9e646a6089058104bd39577fad832e31
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424117"
---
# <a name="wpd_content_type_video"></a>\_vídeo de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo de \_ vídeo de tipo de conteúdo WPD \_ \_ representa um arquivo de vídeo.

Esse tipo de objeto dá suporte às propriedades a seguir.



|  Nome da propriedade                             | Obrigatório ou opcional              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                               |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                                                                    |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                                                                    |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                               |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                                                                    |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                                                                    |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                                            |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema).                                                        |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                                            |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                                                    |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                       | Recomendado se o objeto não for destinado ao consumo pelo dispositivo.                                                        |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto tiver referências a outros objetos.                                                                      |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                                                                                    |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                                    |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                                       |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                           | Opcional.                                                                                                                    |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                         | Recomendável.                                                                                                                 |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                         | Opcional.                                                                                                                    |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                                                   |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                                    |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                                                                                    |
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
| [TÍTULO DA \_ MÍDIA \_ WPD](media-properties.md)                                                             | Obrigatórios.                                                                                                                    |
| [DURAÇÃO DA \_ MÍDIA \_ WPD](media-properties.md)                                                       | Obrigatórios.                                                                                                                    |
| [WPD \_ MEDIA \_ BUY \_ NOW](media-properties.md)                                                        | Recomendável.                                                                                                                 |
| [PERFIL DE \_ \_ CODIFICAÇÃO DE MÍDIA WPD \_](media-properties.md)                                      | Opcional.                                                                                                                    |
| [LARGURA DE MÍDIA WPD \_ \_](media-properties.md)                                                             | Obrigatórios.                                                                                                                    |
| [ALTURA DA MÍDIA WPD \_ \_](media-properties.md)                                                           | Obrigatórios.                                                                                                                    |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                           | Recomendável.                                                                                                                 |
| [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)                                                  | Recomendável.                                                                                                                 |
| [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)                                                 | Opcional.                                                                                                                    |
| [GÊNERO DE MÍDIA WPD \_ \_](media-properties.md)                                                             | Opcional.                                                                                                                    |
| [INDICADOR DE TEMPO \_ \_ DE MÍDIA WPD \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [INDICADOR DE BYTE DE MÍDIA WPD \_ \_ \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [GUID DE \_ MÍDIA WPD \_](media-properties.md)                                                               | Opcional.                                                                                                                    |
| [SUB DESCRIÇÃO DA MÍDIA WPD \_ \_ \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [WPD \_ VIDEO \_ AUTHOR](video-properties.md)                                                           | Opcional.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ STATION \_ NAME](video-properties.md)                       | Opcional.                                                                                                                    |
| [NÚMERO DO CANAL DE WPD \_ \_ VIDEO RECORDEDTV \_ \_](video-properties.md)                   | Opcional.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT](video-properties.md)                                    | Opcional.                                                                                                                    |
| [TAMANHO DO BUFFER DE VÍDEO WPD \_ \_ \_](video-properties.md)                                                | Opcional.                                                                                                                    |
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

 

 



