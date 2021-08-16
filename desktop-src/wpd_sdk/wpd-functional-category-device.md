---
description: '\_dispositivo de \_ categoria \_ funcional WPD'
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f39cf60e247c0abbbcc66f7fad52099a2a83a93f348b1ac9636bb790b9354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842212"
---
# <a name="wpd_functional_category_device"></a>\_dispositivo de \_ categoria \_ funcional WPD

Um \_ \_ objeto funcional do dispositivo de categoria funcional WPD \_ encapsula o dispositivo (ou seja, o objeto mais alto do dispositivo). Se um dispositivo implementar essa categoria funcional, ele deverá dar suporte a essas propriedades além das propriedades listadas para o [objeto de dispositivo](device-object.md).



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                      |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                                                           |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Obrigatórios.                                                                                                           |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                      |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                                                           |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                                                           |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                                   |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).                                               |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                                   |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                                           |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.                                               |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                                                             |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                                                           |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                           |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                              |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                                                           |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                                                        |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                                                           |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                                          |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                                                           |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                                                           |
| [\_categoria de \_ objeto \_ funcional WPD](miscellaneous-properties.md)                      | Obrigatórios.                                                                                                           |
| [\_parceiro de \_ sincronização de dispositivos WPD \_](device-properties.md)                                           | Opcional.                                                                                                           |
| [\_versão do \_ firmware do dispositivo WPD \_](device-properties.md)                                   | Obrigatórios.                                                                                                           |
| [\_nível de \_ energia do dispositivo WPD \_](device-properties.md)                                             | Recomendado se o dispositivo tiver uma bateria.                                                                                |
| [\_fonte de \_ energia do dispositivo WPD \_](device-properties.md)                                           | Recomendável.                                                                                                        |
| [\_protocolo de dispositivo WPD \_](device-properties.md)                                                    | Recomendável.                                                                                                        |
| [\_fabricante do dispositivo WPD \_](device-properties.md)                                            | Obrigatórios.                                                                                                           |
| [\_modelo de dispositivo WPD \_](device-properties.md)                                                          | Obrigatórios.                                                                                                           |
| [\_número de \_ série do dispositivo WPD \_](device-properties.md)                                         | Obrigatórios.                                                                                                           |
| [o \_ dispositivo WPD \_ dá suporte a \_ não \_ consumível](device-properties.md)                    | Necessário se o dispositivo oferecer suporte a objetos não consumíveis; ou seja, se o dispositivo puder ser usado para armazenamento de dados simples. |
| [data e hora do \_ dispositivo WPD \_](device-properties.md)                                                    | Opcional.                                                                                                           |
| [\_ \_ nome amigável do dispositivo WPD \_](device-properties.md)                                         | Recomendável.                                                                                                        |
| [\_ \_ esquemas DRM com suporte do dispositivo WPD \_ \_](device-properties.md)                        | Recomendado se o dispositivo oferecer suporte à tecnologia DRM.                                                                  |
| [os \_ \_ formatos com suporte do dispositivo WPD \_ \_ são \_ ordenados](device-properties.md)       | Recomendado se o dispositivo der suporte à ordenação de formato preferencial.                                                       |
| [\_tipo de dispositivo WPD \_](device-properties.md)                                                            | Recomendável.                                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de conteúdo WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



