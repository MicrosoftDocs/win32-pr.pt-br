---
description: '\_seção de \_ tipo de conteúdo WPD \_'
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fbb63821f75115c5855653dc811067891652615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011566"
---
# <a name="wpd_content_type_section"></a>\_seção de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo como \_ \_ seção de tipo de conteúdo WPD \_ representa uma seção de dados contida em outro objeto. Por exemplo, um arquivo de áudio grande pode ser descrito como uma coleção de vários capítulos, e cada capítulo pode ser um \_ objeto de seção de tipo de conteúdo WPD \_ \_ .

A \_ propriedade de referências de objeto WPD \_ identifica um objeto pai de uma determinada seção.

Esse tipo de objeto dá suporte às propriedades a seguir.



|                                                                                                                                  |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nome da propriedade**                                                                                                                | **Obrigatório ou opcional**                                              |
| [\_ID de objeto WPD \_](object-properties.md)                                                                           | Obrigatórios.                                                             |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                            | Obrigatórios.                                                             |
| [\_nome do objeto WPD \_](object-properties.md)                                                                       | Necessário se o objeto representar um arquivo.                             |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                                     | Obrigatórios.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                                   | Obrigatórios.                                                             |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                                      | Obrigatórios.                                                             |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                               | Necessário se o objeto estiver oculto.                                     |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                               | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema). |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                                       | Necessário se o objeto tiver pelo menos um recurso.                     |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                                         | Necessário se o objeto representar um arquivo.                             |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                                  | Recomendado se o objeto não for destinada ao consumo pelo dispositivo. |
| [\_referências de objetos WPD \_](object-properties.md)                                                           | Obrigatório se o objeto tiver referências a outros objetos.               |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                               | Opcional.                                                             |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                             |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                             | Necessário se o objeto estiver protegido pela tecnologia DRM.                |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                                      | Opcional.                                                             |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                                    | Recomendável.                                                          |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                                    | Opcional.                                                             |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                | Recomendado se o objeto tiver referências a outros objetos.            |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)                | Opcional.                                                             |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md)            | Opcional.                                                             |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                          | Obrigatório se o objeto não puder ser excluído.                             |
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

 

 



