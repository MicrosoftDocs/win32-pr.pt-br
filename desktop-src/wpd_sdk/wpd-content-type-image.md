---
description: IMAGEM DO TIPO \_ DE \_ CONTEÚDO \_ WPD
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846347ac83345ed685a10739126028ca1728bb16a52fe7083fcc7dd823447c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193490"
---
# <a name="wpd_content_type_image"></a>IMAGEM DO TIPO \_ DE \_ CONTEÚDO \_ WPD

Um objeto que descreve seu tipo como WPD \_ CONTENT TYPE IMAGE representa uma imagem \_ \_ ainda.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                         | Obrigatório ou Opcional                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                   |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                                                        |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                                        |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                   |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                        | Obrigatórios.                                                                                        |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                           | Obrigatórios.                                                                                        |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema).                            |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                        |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                       | Recomendado se o objeto não for destinado ao consumo pelo dispositivo.                            |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto tiver referências a outros objetos.                                          |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                                                        |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                                                        |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                           |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                           | Opcional.                                                                                        |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                         | Recomendável.                                                                                     |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                         | Opcional.                                                                                        |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                       |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                        |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                                                        |
| [WPD \_ IMAGE \_ BITDEPTH](image-properties.md)                                                       | Recomendável.                                                                                     |
| [STATUS CORTADO DA IMAGEM WPD \_ \_ \_](image-properties.md)                                          | Opcional.                                                                                        |
| [STATUS CORRIGIDO \_ DA \_ COR DA \_ IMAGEM \_ WPD](image-properties.md)                         | Opcional.                                                                                        |
| [\_FNUMBER DE \_ IMAGEM WPD](image-properties.md)                                                                           | Opcional.                                                                                        |
| [TEMPO DE EXPOSIÇÃO DE IMAGEM WPD \_ \_ \_](image-properties.md)                                                                    | Opcional.                                                                                        |
| [ÍNDICE DE EXPOSIÇÃO DE IMAGEM WPD \_ \_ \_](image-properties.md)                                                                   | Opcional.                                                                                        |
| [RESOLUÇÃO HORIZONTAL DA \_ IMAGEM \_ \_ WPD](image-properties.md)                                                            | Opcional.                                                                                        |
| [RESOLUÇÃO VERTICAL DA IMAGEM WPD \_ \_ \_](image-properties.md)                                                              | Opcional.                                                                                        |
| [DIREITOS \_ AUTORAIS DA MÍDIA WPD \_](media-properties.md)                                                     | Opcional.                                                                                        |
| [LARGURA DE MÍDIA WPD \_ \_](media-properties.md)                                                             | Obrigatórios.                                                                                        |
| [ALTURA DA MÍDIA WPD \_ \_](media-properties.md)                                                           | Obrigatórios.                                                                                        |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                                            | Recomendável.                                                                                     |
| [WPD \_ MEDIA \_ ALBUM \_ ARTIST](media-properties.md)                                                                     | Recomendável. Essa propriedade identifica a pessoa ou as pessoas que originalmente criaram esse objeto. |
| [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)                                                                       | Opcional.                                                                                        |
| [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md)                                                                  | Opcional.                                                                                        |
| [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)                                                                       | Opcional.                                                                                        |
| [GÊNERO DE MÍDIA WPD \_ \_](media-properties.md)                                                                             | Opcional.                                                                                        |
| [INDICADOR DE BYTE DE MÍDIA WPD \_ \_ \_](media-properties.md)                                                                    | Opcional.                                                                                        |
| [GUID DE \_ MÍDIA WPD \_](media-properties.md)                                                                              | Opcional.                                                                                        |
| [SUB DESCRIÇÃO DA MÍDIA WPD \_ \_ \_](media-properties.md)                                                                  | Opcional.                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os recursos a seguir.



| Nome do Recurso                                                 | Obrigatório ou Opcional | Descrição                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)        | Obrigatórios.            | Contém os dados da imagem.                                                                 |
| [**MINIATURA DO RECURSO WPD \_ \_**](wpd-resource-thumbnail.md)    | Recomendável.         | Contém a miniatura da imagem.                                                    |
| [**CLIPE DE ÁUDIO DE RECURSO WPD \_ \_ \_**](wpd-resource-audio-clip.md) | Opcional.            | Se essa imagem tiver uma anotação de áudio associada, esse recurso conterá os dados de áudio. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



