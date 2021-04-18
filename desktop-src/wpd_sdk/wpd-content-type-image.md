---
description: '\_imagem de \_ tipo de conteúdo WPD \_'
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d547a6190df01f495c0a340010b4305f5c77bf5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798242"
---
# <a name="wpd_content_type_image"></a>\_imagem de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo como \_ imagem de tipo de conteúdo WPD \_ \_ representa uma imagem ainda.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                   |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                                        |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                                        |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                   |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                                        |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                                        |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).                            |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                        |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.                            |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                                          |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                                        |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                        |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                           |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                                        |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                                     |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                                        |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                       |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                                        |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                                        |
| [\_BITDEPTH de imagem WPD \_](image-properties.md)                                                       | Recomendável.                                                                                     |
| [\_ \_ status cortado da imagem WPD \_](image-properties.md)                                          | Opcional.                                                                                        |
| [\_ \_ status corrigido da cor da imagem WPD \_ \_](image-properties.md)                         | Opcional.                                                                                        |
| [\_FNUMBER de imagem WPD \_](image-properties.md)                                                                           | Opcional.                                                                                        |
| [\_tempo de \_ exposição da imagem WPD \_](image-properties.md)                                                                    | Opcional.                                                                                        |
| [\_índice de \_ exposição de imagem WPD \_](image-properties.md)                                                                   | Opcional.                                                                                        |
| [\_ \_ resolução horizontal de imagem WPD \_](image-properties.md)                                                            | Opcional.                                                                                        |
| [\_ \_ resolução vertical da imagem WPD \_](image-properties.md)                                                              | Opcional.                                                                                        |
| [\_ \_ direitos autorais de mídia WPD](media-properties.md)                                                     | Opcional.                                                                                        |
| [\_largura de mídia WPD \_](media-properties.md)                                                             | Obrigatórios.                                                                                        |
| [\_altura de mídia WPD \_](media-properties.md)                                                           | Obrigatórios.                                                                                        |
| [\_artista de mídia WPD \_](media-properties.md)                                                                            | Recomendável.                                                                                     |
| [\_artista do \_ álbum de mídia WPD \_](media-properties.md)                                                                     | Recomendável. Essa propriedade identifica a pessoa, ou pessoas, que originalmente criou esse objeto. |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                                                                       | Opcional.                                                                                        |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)                                                                  | Opcional.                                                                                        |
| [\_Descrição da mídia WPD \_](media-properties.md)                                                                       | Opcional.                                                                                        |
| [\_gênero de mídia WPD \_](media-properties.md)                                                                             | Opcional.                                                                                        |
| [\_indicador de \_ byte de mídia WPD \_](media-properties.md)                                                                    | Opcional.                                                                                        |
| [\_GUID de mídia WPD \_](media-properties.md)                                                                              | Opcional.                                                                                        |
| [subdescrição de \_ mídia WPD \_ \_](media-properties.md)                                                                  | Opcional.                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                                 | Obrigatório ou opcional | Descrição                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md)        | Obrigatórios.            | Contém os dados da imagem.                                                                 |
| [**\_miniatura do recurso WPD \_**](wpd-resource-thumbnail.md)    | Recomendável.         | Contém a miniatura da imagem.                                                    |
| [**\_clipe de \_ áudio de recursos WPD \_**](wpd-resource-audio-clip.md) | Opcional.            | Se essa imagem tiver uma anotação de áudio associada, esse recurso conterá os dados de áudio. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



