---
description: '\_ \_ objeto funcional de tipo de conteúdo WPD \_ \_'
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8516d29bf08b4873dc80c72b9a23de19dc50d0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775570"
---
# <a name="wpd_content_type_functional_object"></a>\_ \_ objeto funcional de tipo de conteúdo WPD \_ \_

Um objeto que descreve seu tipo como \_ objeto funcional de conteúdo WPD \_ \_ representa um objeto funcional, encapsulando a funcionalidade do dispositivo.

Todos os objetos funcionais, não importa o tipo, dão suporte às propriedades a seguir. (Se você definir um objeto funcional personalizado, ele também deverá oferecer suporte a essas propriedades.)



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.        |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                             |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Obrigatórios.                                                                             |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.        |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                             |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                             |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                     |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).                 |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                     |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                             |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.                 |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                               |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                             |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                             |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                             |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                          |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                             |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                            |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                             |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                             |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Obrigatório se o objeto não puder ser excluído.                                             |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                             |
| [\_categoria de \_ objeto \_ funcional WPD](miscellaneous-properties.md)                      | Obrigatórios. Consulte a tabela a seguir para obter categorias definidas por dispositivos portáteis do Windows. |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="functional-object-categories"></a>Categorias de objeto funcional

Os objetos funcionais podem ser agrupados em categorias, dependendo de suas funções. Uma categoria é descrita pela propriedade de \_ categoria de objeto funcional WPD \_ \_ (um valor de GUID). A categoria determina quais propriedades adicionais têm suporte.

A tabela a seguir descreve as categorias definidas por dispositivos portáteis do Windows. Consulte a descrição da categoria para saber quais recursos e propriedades adicionais são compatíveis com o objeto.



| Categoria funcional                                                                                        | Descrição                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_toda a \_ categoria \_ funcional WPD**](wpd-functional-category-all.md)                                      | Essa categoria funcional é válida somente como um parâmetro para determinadas funções de consulta (para indicar que todos os tipos de objeto funcional são aceitáveis) e não é uma categoria funcional relatada pelo driver. |
| [**\_captura de \_ áudio de categoria funcional \_ WPD \_**](wpd-functional-category-audio-capture.md)                 | O objeto encapsula a funcionalidade de captura de áudio no dispositivo, por exemplo, um gravador de voz ou outro componente de gravação de áudio.                                                                      |
| [**\_dispositivo de \_ categoria \_ funcional WPD**](wpd-functional-category-device.md)                                | O objeto encapsula o dispositivo (ou seja, o objeto mais alto do dispositivo).                                                                                                                          |
| [**\_configuração de \_ rede de categoria funcional \_ WPD \_**](wpd-functional-category-network-configuration.md) | O objeto encapsula a funcionalidade de configuração de rede para o dispositivo, por exemplo, perfis de WiFi ou parcerias.                                                                                   |
| [**\_informações de \_ renderização de categoria funcional \_ WPD \_**](wpd-functional-category-rendering-information.md) | O objeto descreve os tipos de arquivos de mídia que o dispositivo pode reproduzir.                                                                                                                            |
| [**\_categoria funcional \_ WPD \_ SMS**](wpd-functional-category-sms.md)                                      | O objeto encapsula a funcionalidade do serviço de mensagem curta (normalmente chamada de "mensagens de texto") no dispositivo.                                                                                             |
| [**a \_ categoria funcional WPD \_ \_ ainda \_ captura de imagem \_**](wpd-functional-category-still-image-capture.md)    | O objeto encapsula a funcionalidade de captura de imagem ainda em um dispositivo, como um anexo de câmera ou câmera.                                                                                              |
| [**\_armazenamento de \_ categoria \_ funcional WPD**](wpd-functional-category-storage.md)                              | O objeto encapsula o armazenamento de arquivos físico no dispositivo.                                                                                                                                              |
| [**\_captura de \_ vídeo de categoria funcional \_ WPD \_**](wpd-functional-category-video-capture.md)                 | O objeto encapsula a funcionalidade de captura de vídeo no dispositivo, por exemplo, um componente de gravador de vídeo. Um aplicativo usa esse objeto para obter controle programático.                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



