---
description: '\_compromisso de \_ tipo de conteúdo WPD \_'
ms.assetid: d41c26ef-9f51-4ba7-b1a4-57abec91925e
title: WPD_CONTENT_TYPE_APPOINTMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1ec4a316690241372bc7d0fa13789731dde925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772996"
---
# <a name="wpd_content_type_appointment"></a>\_compromisso de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo de \_ compromisso de tipo de conteúdo WPD \_ \_ representa um compromisso em um calendário.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                      |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                      |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                      |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                      |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                              |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).          |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                              |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                      |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.          |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                        |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                      |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                      |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                         |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                      |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                   |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                      |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                     |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                      |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                      |
| [\_local do compromisso WPD \_](appointment-properties.md)                                     | Obrigatórios.                                                                      |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Necessário se o objeto puder ser excluído.                                         |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                      |
| [\_assunto de \_ informações \_ comuns do WPD](object-properties.md)                                                            | Obrigatórios.                                                                      |
| [\_texto de \_ corpo de informações comuns \_ WPD \_](object-properties.md)                                                         | Recomendável.                                                                   |
| [\_prioridade de \_ informações \_ comuns WPD](object-properties.md)                                                           | Recomendável.                                                                   |
| [\_DateTime de \_ início de informações comuns \_ WPD \_](object-properties.md)                                                    | Recomendável.                                                                   |
| [\_data de \_ término de informações comuns \_ WPD \_](object-properties.md)                                                      | Recomendável.                                                                   |
| [\_observações de \_ informações \_ comuns do WPD](object-properties.md)                                                              | Opcional.                                                                      |
| [\_local do compromisso WPD \_](object-properties.md)                                                                   | Obrigatórios.                                                                      |
| [\_tipo de compromisso WPD \_](appointment-properties.md)                                             | Opcional.                                                                      |
| [\_ \_ participantes necessários para o compromisso WPD \_](appointment-properties.md)                | Opcional.                                                                      |
| [\_ \_ participantes opcionais de compromisso WPD \_](appointment-properties.md)                | Opcional.                                                                      |
| [\_ \_ participantes aceitos do compromisso WPD \_](appointment-properties.md)                | Opcional.                                                                      |
| [\_recursos de compromisso WPD \_](appointment-properties.md)                                   | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



