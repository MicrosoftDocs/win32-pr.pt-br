---
description: a \_ categoria funcional WPD \_ \_ ainda \_ captura de imagem \_
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d821f1182012fbf29960fae4fc06b14ec53ecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922474"
---
# <a name="wpd_functional_category_still_image_capture"></a>a \_ categoria funcional WPD \_ \_ ainda \_ captura de imagem \_

Uma \_ categoria funcional WPD ainda é um \_ \_ \_ objeto funcional de captura de imagem que encapsula a \_ funcionalidade de captura de imagem ainda em um dispositivo, como um anexo de câmera ou câmera.



| Nome da Propriedade                                                                                                            | Obrigatório ou opcional                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                   | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                    | Obrigatórios.                                                                                                                                              |
| [\_nome do objeto WPD \_](object-properties.md)                                                               | Obrigatórios.                                                                                                                                              |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                             | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [\_formato de objeto WPD \_](object-properties.md)                                                           | Obrigatórios.                                                                                                                                              |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                              | Obrigatórios.                                                                                                                                              |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                       | Necessário se o objeto estiver oculto.                                                                                                                      |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                       | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).                                                                                  |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                               | Necessário se o objeto tiver pelo menos um recurso.                                                                                                      |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                                 | Necessário se o objeto representar um arquivo.                                                                                                              |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                          | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.                                                                                  |
| [\_referências de objetos WPD \_](object-properties.md)                                                   | Obrigatório se o objeto tiver referências a outros objetos.                                                                                                |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                       | Opcional.                                                                                                                                              |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                        | Opcional.                                                                                                                                              |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                     | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                                                                 |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                              | Opcional.                                                                                                                                              |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                            | Recomendável.                                                                                                                                           |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                            | Opcional.                                                                                                                                              |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                   | Recomendado se o objeto for referenciado por outro objeto.                                                                                             |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)        | Opcional.                                                                                                                                              |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md)    | Opcional.                                                                                                                                              |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                        | Obrigatório se o objeto não puder ser excluído.                                                                                                              |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                   | Opcional.                                                                                                                                              |
| [\_categoria de \_ objeto \_ funcional WPD](miscellaneous-properties.md)                         | Obrigatórios. Consulte [**\_ \_ \_ \_ objeto funcional de tipo de conteúdo WPD**](wpd-content-type-functional-object.md) para categorias definidas por dispositivos portáteis do Windows. |
| [\_resolução de \_ captura de imagem \_ \_ do WPD ainda](still-image-properties.md)                  | Obrigatórios.                                                                                                                                              |
| [\_formato de \_ captura de imagem \_ \_ do WPD ainda](still-image-properties.md)                          | Obrigatórios.                                                                                                                                              |
| [\_configuração de \_ \_ compactação de imagem \_ do WPD ainda](still-image-properties.md)                | Opcional.                                                                                                                                              |
| [\_proporção de \_ branco de imagem ainda \_ WPD \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [a imagem de WPD ainda tem um \_ \_ \_ \_ lucro RGB](still-image-properties.md)                                      | Opcional.                                                                                                                                              |
| [\_FNUMBER de \_ imagens WPD ainda \_](still-image-properties.md)                                         | Opcional.                                                                                                                                              |
| [\_ \_ comprimento focal da imagem ainda \_ WPD \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [a \_ \_ distância do \_ foco da imagem WPD ainda \_](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [o \_ \_ modo de \_ foco de imagem \_ do WPD ainda](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [\_modo de \_ medição de exposição de imagem \_ WPD \_ e ainda \_](still-image-properties.md)         | Opcional.                                                                                                                                              |
| [\_modo de \_ flash de imagem ainda \_ mais WPD \_](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [\_tempo de \_ exposição da imagem \_ \_ do WPD ainda](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [\_modo de \_ programa de exposição de imagem \_ \_ WPD \_](still-image-properties.md)           | Opcional.                                                                                                                                              |
| [\_índice de \_ exposição de imagem \_ \_ do WPD ainda](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [o WPD ainda é uma \_ compensação de desvio de \_ exposição de imagem \_ \_ \_](still-image-properties.md) | Opcional.                                                                                                                                              |
| [\_atraso de \_ captura de imagem \_ \_ do WPD ainda](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [\_modo de \_ captura de imagem ainda \_ WPD \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [a WPD ainda é o \_ \_ contraste da imagem \_](still-image-properties.md)                                       | Opcional.                                                                                                                                              |
| [a \_ \_ nitidez da imagem \_ do WPD ainda](still-image-properties.md)                                     | Opcional.                                                                                                                                              |
| [\_ \_ \_ zoom digital da imagem \_ do WPD ainda](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [\_modo de \_ efeito de imagem ainda \_ mais WPD \_](still-image-properties.md)                                | Opcional.                                                                                                                                              |
| [\_número de \_ intermitência de imagem ainda \_ WPD \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [\_intervalo de \_ intermitência de imagem ainda \_ mais WPD \_](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [\_TIMELAPSE WPD \_ ainda \_ \_ número de imagem](still-image-properties.md)                      | Opcional.                                                                                                                                              |
| [\_intervalo de \_ TIMELAPSE de imagens WPD ainda \_ \_](still-image-properties.md)                  | Opcional.                                                                                                                                              |
| [\_modo de \_ medição de foco de imagem \_ WPD \_ \_](still-image-properties.md)               | Opcional.                                                                                                                                              |
| [\_URL de \_ upload de imagem \_ \_ do WPD ainda](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [\_artista de \_ imagem \_ ainda mais WPD](still-image-properties.md)                                           | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

Muitas dessas propriedades têm efeitos interconectados. Por exemplo, se **o \_ \_ modo de \_ \_ medição \_ de exposição de imagem do WPD ainda** estiver definido como automático, o indicador de exposição e o tempo de exposição e o medidor de exposições serão vinculados; a variação de um fará com que os outros variem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de conteúdo WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



