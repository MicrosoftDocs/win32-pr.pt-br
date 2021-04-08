---
description: '\_documento de \_ tipo de conteúdo WPD \_'
ms.assetid: c3859590-7674-4315-b171-3747e5d9350b
title: WPD_CONTENT_TYPE_DOCUMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8a0a902fb30eb0343a3846eaf3668a4a005a82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011568"
---
# <a name="wpd_content_type_document"></a>\_documento de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo de \_ documento de tipo de conteúdo WPD \_ \_ representa um documento. Os exemplos incluem Microsoft Office arquivos do Word, Microsoft Office arquivos do Excel, arquivos de texto sem formatação e outros formatos de documentos proprietários.

Esse tipo de objeto pode hospedar as propriedades a seguir.



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
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Obrigatório se o objeto não puder ser excluído.                                      |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                      |
| [\_URL de \_ origem de mídia WPD \_](object-properties.md)                                                                      | Opcional.                                                                      |
| [\_URL de \_ destino de mídia WPD \_](object-properties.md)                                                                 | Opcional.                                                                      |
| [\_Descrição da mídia WPD \_](object-properties.md)                                                                      | Opcional.                                                                      |
| [\_gênero de mídia WPD \_](object-properties.md)                                                                            | Opcional.                                                                      |
| [\_indicador de \_ byte de mídia WPD \_](object-properties.md)                                                                   | Opcional.                                                                      |
| [\_GUID de mídia WPD \_](object-properties.md)                                                                             | Opcional.                                                                      |
| [subdescrição de \_ mídia WPD \_ \_](object-properties.md)                                                                 | Opcional.                                                                      |
| [\_informações comuns do WPD \_](object-properties.md)                                                                     | Recomendável.                                                                   |
| [\_texto de \_ corpo de informações comuns \_ WPD \_](object-properties.md)                                                         | Recomendável.                                                                   |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                          | Obrigatório ou opcional | Descrição                     |
|--------------------------------------------------------|----------------------|---------------------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md) | Obrigatório             | Contém o documento físico. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



