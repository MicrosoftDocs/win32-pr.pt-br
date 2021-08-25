---
description: '\_calendário de \_ tipo de conteúdo WPD \_'
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819955c0554269deb26c6b6f7f7f3c74ee8715e2dca804b5d3d554b9657be524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927866"
---
# <a name="wpd_content_type_calendar"></a>\_calendário de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo de \_ calendário de tipo de conteúdo WPD \_ \_ representa um calendário. O objeto pode ser um arquivo que contém informações de calendário ou uma pasta que contém outros objetos relacionados a calendário, como tarefas, compromissos e assim por diante.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatórios.                                                             |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                             |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                             |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatórios.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                             |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                             |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                     |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema). |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                     |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                             |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo. |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.               |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                             |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                             |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                             |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                          |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                             |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                     | Recomendado se o objeto for referenciado por outro objeto.            |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                             |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                             |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                               | Necessário se o objeto puder ser excluído.                                |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                          | Obrigatório ou opcional                             | Descrição        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md) | Necessário se o objeto for apoiado por dados binários. | Contém os dados. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



