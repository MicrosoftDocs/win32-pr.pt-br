---
description: '\_memorando de \_ tipo de conteúdo WPD \_'
ms.assetid: 6d89681c-1183-44d3-a39e-5fb343f1abbe
title: WPD_CONTENT_TYPE_MEMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563148d28a03558843060bedfb76a6f91ca6805c0498e8a8d66e3dd53a68ed82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006036"
---
# <a name="wpd_content_type_memo"></a>\_memorando de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo de \_ memorando de tipo de conteúdo WPD \_ \_ representa uma nota de texto.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade      |   Obrigatório ou opcional      |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                      |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                      |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade mesmo no momento da criação.  |
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
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Obrigatório se o objeto não puder ser excluído.                                      |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                      |
| [\_assunto de \_ informações \_ comuns do WPD](object-properties.md)                                                            | Obrigatórios.                                                                      |
| [\_texto de \_ corpo de informações comuns \_ WPD \_](object-properties.md)                                                         | Recomendável.                                                                   |
| [\_prioridade de \_ informações \_ comuns WPD](object-properties.md)                                                           | Recomendável.                                                                   |
| [\_DateTime de \_ início de informações comuns \_ WPD \_](object-properties.md)                                                    | Recomendável.                                                                   |
| [\_data de \_ término de informações comuns \_ WPD \_](object-properties.md)                                                      | Recomendável.                                                                   |
| [\_observações de \_ informações \_ comuns do WPD](object-properties.md)                                                              | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



