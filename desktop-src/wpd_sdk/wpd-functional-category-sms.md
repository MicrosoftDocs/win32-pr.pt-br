---
description: '\_categoria funcional \_ WPD \_ SMS'
ms.assetid: dbb536a6-9c12-459d-8098-ebe4fc4c8f2f
title: WPD_FUNCTIONAL_CATEGORY_SMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a08cb3df6bd74de843efaa3d0feed88ad86fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170974"
---
# <a name="wpd_functional_category_sms"></a>\_categoria funcional \_ WPD \_ SMS

Uma \_ categoria funcional \_ WPD \_ objeto funcional do SMS encapsula a funcionalidade do serviço de mensagem curta (normalmente chamada de "mensagens de texto") no dispositivo.



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                                                                                              |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Obrigatórios.                                                                                                                                              |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                                                                                              |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                                                                                              |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                                                                      |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).                                                                                  |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                                                                      |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                                                                              |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.                                                                                  |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                                                                                                |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                                                                                              |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                                                              |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                                                                 |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                                                                                              |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                                                                                           |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                                                                                              |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                                                                             |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                                                                                              |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                                                                                              |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Obrigatório se o objeto não puder ser excluído.                                                                                                              |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [\_categoria de \_ objeto \_ funcional WPD](miscellaneous-properties.md)                      | Obrigatórios. Consulte [**\_ \_ \_ \_ objeto funcional de tipo de conteúdo WPD**](wpd-content-type-functional-object.md) para categorias definidas por dispositivos portáteis do Windows. |
| [\_provedor de SMS WPD \_](sms-properties.md)                                                             | Obrigatórios.                                                                                                                                              |
| [\_tempo limite de SMS WPD \_](sms-properties.md)                                                               | Obrigatórios.                                                                                                                                              |
| [\_ \_ carga máxima de SMS WPD \_](sms-properties.md)                                                      | Obrigatórios.                                                                                                                                              |
| [\_codificação de SMS WPD \_](sms-properties.md)                                                             | Obrigatórios.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de conteúdo WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



