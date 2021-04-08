---
description: '\_serviço de \_ tipo de conteúdo WPD \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922384"
---
# <a name="wpd_content_type_service"></a>\_serviço de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo de \_ serviço de tipo de conteúdo WPD \_ \_ representa um serviço de dispositivo.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade                                                                                        | Obrigatório ou opcional                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                               | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                | Obrigatórios.                                                                      |
| [\_nome do objeto WPD \_](object-properties.md)                                           | Necessário se o objeto representar um arquivo.                                      |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)         | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                   | Necessário se o serviço não deve ser mostrado ao usuário.                       |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                   | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).          |
| [\_categoria de \_ objeto \_ funcional WPD](object-properties.md) | Obrigatórios. Isso representa o tipo de serviço do dispositivo.                             |
| [\_versão do serviço WPD \_](object-properties.md)           | Obrigatórios.                                                                      |
| [\_tipo de armazenamento WPD \_](object-properties.md)                                                          | Necessário se o serviço for usado para armazenar objetos.                              |
| [\_capacidade de armazenamento WPD \_](object-properties.md)                                                      | Necessário se o serviço for usado para armazenar objetos.                              |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



