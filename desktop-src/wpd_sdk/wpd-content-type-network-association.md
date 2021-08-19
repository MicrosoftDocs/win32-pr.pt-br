---
description: ASSOCIAÇÃO DE REDE DO \_ \_ TIPO DE CONTEÚDO \_ WPD \_
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c383ac251d410e03fc5d26dd969d4161ae555ebf2cdd3802ca7228b1739ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842286"
---
# <a name="wpd_content_type_network_association"></a>ASSOCIAÇÃO DE REDE DO \_ \_ TIPO DE CONTEÚDO \_ WPD \_

Um objeto que descreve seu tipo como WPD CONTENT TYPE NETWORK ASSOCIATION representa uma \_ associação entre um host e um \_ \_ \_ dispositivo.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade         | Obrigatório ou Opcional        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                                       | Obrigatórios.                                                             |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                                        | Obrigatórios.                                                             |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                                                   | Necessário se o objeto representar um arquivo.                             |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                             |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                                               | Obrigatórios.                                                             |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                                  | Obrigatórios.                                                             |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                                           | Necessário se o objeto estiver oculto.                                     |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                                           | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema). |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                                                   | Necessário se o objeto tiver pelo menos um recurso.                     |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                                                     | Necessário se o objeto representar um arquivo.                             |
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
| [WPD \_ NETWORK \_ ASSOCIATION \_ X509V3SEQUENCE](network-association-properties.md)                       | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



