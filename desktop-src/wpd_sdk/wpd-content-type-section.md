---
description: '\_seção de \_ tipo de conteúdo WPD \_'
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84294ff9949418ecc12f55472da202dddcc8f06c
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423776"
---
# <a name="wpd_content_type_section"></a>\_seção de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo como \_ \_ seção de tipo de conteúdo WPD \_ representa uma seção de dados contida em outro objeto. Por exemplo, um arquivo de áudio grande pode ser descrito como uma coleção de vários capítulos, e cada capítulo pode ser um \_ objeto de seção de tipo de conteúdo WPD \_ \_ .

A \_ propriedade de referências de objeto WPD \_ identifica um objeto pai de uma determinada seção.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da propriedade       | Obrigatório ou opcional             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                           | Obrigatórios.                                                             |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                            | Obrigatórios.                                                             |
| [\_nome do objeto WPD \_](object-properties.md)                                                                       | Necessário se o objeto representar um arquivo.                             |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                                     | Obrigatórios.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                                   | Obrigatórios.                                                             |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                                      | Obrigatórios.                                                             |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                               | Necessário se o objeto estiver oculto.                                     |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                               | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema). |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                                       | Necessário se o objeto tiver pelo menos um recurso.                     |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                                         | Necessário se o objeto representar um arquivo.                             |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                                  | Recomendado se o objeto não for destinado ao consumo pelo dispositivo. |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                           | Necessário se o objeto tiver referências a outros objetos.               |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                               | Opcional.                                                             |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                                | Opcional.                                                             |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                             | Necessário se o objeto estiver protegido pela tecnologia DRM.                |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                                      | Opcional.                                                             |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                                    | Recomendável.                                                          |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                                    | Opcional.                                                             |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                | Recomendado se o objeto tiver referências a outros objetos.            |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)                | Opcional.                                                             |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md)            | Opcional.                                                             |
| [O OBJETO WPD \_ \_ PODE \_ EXCLUIR](object-properties.md)                                                          | Necessário se o objeto não puder ser excluído.                             |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                           | Opcional.                                                             |
| [\_deslocamento de \_ dados da seção WPD \_](section-attribute-properties.md)                                           | Obrigatórios.                                                             |
| [\_comprimento de \_ dados da seção WPD \_](section-attribute-properties.md)                                           | Obrigatórios.                                                             |
| [\_unidades de \_ dados da seção WPD \_](section-attribute-properties.md)                                             | Recomendável.                                                          |
| [\_recurso de \_ \_ objeto referenciado de dados da \_ seção WPD \_](section-attribute-properties.md) | Recomendável.                                                          |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



