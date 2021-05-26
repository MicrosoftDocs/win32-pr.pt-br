---
description: tipo de conteúdo WPD de \_ \_ \_ Associação de rede \_
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c92f76080db4167a12578c58e9d85c9506c28b
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423709"
---
# <a name="wpd_content_type_network_association"></a>tipo de conteúdo WPD de \_ \_ \_ Associação de rede \_

Um objeto que descreve seu tipo de \_ Associação de rede de tipo de conteúdo WPD \_ \_ \_ representa uma associação entre um host e um dispositivo.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da propriedade         | Obrigatório ou opcional        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                                       | Obrigatórios.                                                             |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                                        | Obrigatórios.                                                             |
| [\_nome do objeto WPD \_](object-properties.md)                                                                                   | Necessário se o objeto representar um arquivo.                             |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                                               | Obrigatórios.                                                             |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                                                  | Obrigatórios.                                                             |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                                           | Necessário se o objeto estiver oculto.                                     |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                                           | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema). |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                                                   | Necessário se o objeto tiver pelo menos um recurso.                     |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                                                     | Necessário se o objeto representar um arquivo.                             |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                                              | Recomendado se o objeto não for destinado ao consumo pelo dispositivo. |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                                       | Necessário se o objeto tiver referências a outros objetos.               |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                                           | Opcional.                                                             |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                                            | Opcional.                                                             |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                                         | Necessário se o objeto estiver protegido pela tecnologia DRM.                |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                                                  | Opcional.                                                             |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                                                | Recomendável.                                                          |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                                                | Opcional.                                                             |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                                       | Recomendado se o objeto for referenciado por outro objeto.            |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)                            | Opcional.                                                             |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md)                        | Opcional.                                                             |
| [O OBJETO WPD \_ \_ PODE \_ EXCLUIR](object-properties.md)                                                                      | Necessário se o objeto não puder ser excluído.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCAL](object-properties.md)                                                                                        | Opcional.                                                             |
| [IDENTIFICADORES DE REDE DE HOST DE ASSOCIAÇÃO \_ \_ \_ \_ \_ DE REDE WPD](network-association-properties.md) | Obrigatórios.                                                             |
| [\_X509V3SEQUENCE de \_ Associação de rede WPD \_](network-association-properties.md)                       | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



