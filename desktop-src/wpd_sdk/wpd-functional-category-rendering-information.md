---
description: '\_informações de \_ renderização de categoria funcional \_ WPD \_'
ms.assetid: 84ec6f14-fe90-42a5-ba2b-6c4cc406935c
title: WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf2a5b981b75820b566e3133faab22c2f35860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922379"
---
# <a name="wpd_functional_category_rendering_information"></a>\_informações de \_ renderização de categoria funcional \_ WPD \_

Um \_ objeto funcional de informações de renderização de categoria funcional de WPD \_ \_ \_ descreve que tipo de arquivos de mídia o dispositivo é capaz de renderizar.



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
| [\_perfis de \_ informações de renderização WPD \_](miscellaneous-properties.md)              | Obrigatórios.                                                                                                                                              |
| [\_tipo de \_ entrada do perfil de informações de renderização WPD \_ \_ \_](miscellaneous-properties.md)                                     | Opcional.                                                                                                                                              |
| [\_ \_ \_ \_ recurso CREATABLE de entrada do perfil de \_ informações \_ de renderização WPD](miscellaneous-properties.md)                      | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de conteúdo WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



