---
description: '\_contato de \_ tipo de conteúdo WPD \_'
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fed10e0abb36a482141e5c796f5494b00b99f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793294"
---
# <a name="wpd_content_type_contact"></a>\_contato de \_ tipo de conteúdo WPD \_

Um objeto que descreve seu tipo como \_ contato de tipo de conteúdo WPD \_ \_ representa dados de contato pessoal.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                                   | Obrigatório ou opcional                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                           | Obrigatórios.                                                                      |
| [\_nome do objeto WPD \_](object-properties.md)                                                                      | Necessário se o objeto representar um arquivo.                                      |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                                    | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [\_formato de objeto WPD \_](object-properties.md)                                                                  | Obrigatórios.                                                                      |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                                     | Obrigatórios.                                                                      |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                              | Necessário se o objeto estiver oculto.                                              |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                              | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).          |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                                      | Necessário se o objeto tiver pelo menos um recurso.                              |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                                        | Necessário se o objeto representar um arquivo.                                      |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                                 | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.          |
| [\_referências de objetos WPD \_](object-properties.md)                                                          | Obrigatório se o objeto tiver referências a outros objetos.                        |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                              | Opcional.                                                                      |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                               | Opcional.                                                                      |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                            | Necessário se o objeto estiver protegido pela tecnologia DRM.                         |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                                     | Opcional.                                                                      |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                                   | Recomendável.                                                                   |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                                   | Opcional.                                                                      |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                          | Recomendado se o objeto for referenciado por outro objeto.                     |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)               | Opcional.                                                                      |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md)           | Opcional.                                                                      |
| [\_nome de \_ exibição de contato WPD \_](contact-properties.md)                                                  | Obrigatórios.                                                                      |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                               | Obrigatório se o objeto não puder ser excluído.                                      |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                          | Opcional.                                                                      |
| [\_nome de \_ exibição de contato WPD \_](contact-properties.md)                                                                           | Obrigatórios.                                                                      |
| [\_ \_ primeiro nome do contato WPD \_](contact-properties.md)                                                      | Recomendável.                                                                   |
| [\_nomes de \_ meio do contato WPD \_](contact-properties.md)                                                  | Recomendável.                                                                   |
| [\_sobrenome de contato do WPD \_ \_](contact-properties.md)                                                        | Recomendável.                                                                   |
| [\_prefixo de contato WPD \_](contact-properties.md)                                                               | Recomendável.                                                                   |
| [\_sufixo de contato WPD \_](contact-properties.md)                                                               | Recomendável.                                                                   |
| [\_ \_ \_ primeiro \_ nome FONÉTICO de contato do WPD](contact-properties.md)                                   | Opcional.                                                                      |
| [\_ \_ \_ último \_ nome fonético de contato WPD](contact-properties.md)                                     | Opcional.                                                                      |
| [\_ \_ \_ \_ Endereço postal completo pessoal de contato WPD \_](contact-properties.md)                | Recomendável.                                                                   |
| [\_Contato com \_ o \_ Endereço postal pessoal \_ \_ da WPD](contact-properties.md)              | Opcional.                                                                      |
| [\_ \_ \_ Endereço postal pessoal \_ de contato \_ WPD](contact-properties.md)              | Opcional.                                                                      |
| [\_cidade de \_ \_ Endereço postal \_ pessoal \_ de contato WPD](contact-properties.md)                | Opcional.                                                                      |
| [\_região de \_ \_ Endereço postal \_ pessoal \_ de contato WPD](contact-properties.md)            | Opcional.                                                                      |
| [código postal do \_ \_ \_ \_ Endereço postal \_ pessoal do contato WPD \_](contact-properties.md) | Opcional.                                                                      |
| [\_país de \_ \_ Endereço postal \_ pessoal \_ do contato WPD](contact-properties.md)          | Opcional.                                                                      |
| [\_ \_ \_ \_ Endereço postal completo comercial de contato WPD \_](contact-properties.md)                | Opcional.                                                                      |
| [\_ \_ \_ Endereço postal da empresa \_ de \_ contato WPD](contact-properties.md)              | Opcional.                                                                      |
| [\_ \_ \_ Endereço postal da empresa \_ de \_ contato WPD](contact-properties.md)              | Opcional.                                                                      |
| [\_cidade de \_ \_ Endereço postal \_ de negócios de contato WPD \_](contact-properties.md)                | Opcional.                                                                      |
| [\_região de \_ \_ Endereço postal \_ de negócios de contato WPD \_](contact-properties.md)            | Opcional.                                                                      |
| [\_ \_ \_ \_ \_ código postal da empresa \_ de contato WPD](contact-properties.md) | Opcional.                                                                      |
| [\_país de \_ \_ Endereço postal \_ da empresa de contato WPD \_](contact-properties.md)          | Opcional.                                                                      |
| [\_contato com \_ outros \_ \_ endereços postais completos \_](contact-properties.md)                      | Opcional.                                                                      |
| [\_Contato WPD \_ com \_ outro \_ Endereço postal \_ linha1](contact-properties.md)                    | Opcional.                                                                      |
| [Contato de WPD \_ com \_ outro \_ \_ Endereço postal \_ Linha2](contact-properties.md)                    | Opcional.                                                                      |
| [contato de WPD \_ com \_ outra \_ \_ cidade de endereço postal \_](contact-properties.md)                      | Opcional.                                                                      |
| [\_ \_ outra região de \_ \_ Endereço postal \_ de contato WPD](contact-properties.md)                  | Opcional.                                                                      |
| [\_ \_ \_ \_ \_ código postal de outro endereço \_ postal de contato WPD](contact-properties.md)       | Opcional.                                                                      |
| [contato de WPD \_ \_ outro \_ \_ Endereço postal \_ postal \_](contact-properties.md) | Opcional.                                                                      |
| [\_endereço de \_ \_ email principal do contato \_ WPD](contact-properties.md)                               | Recomendável.                                                                   |
| [\_ \_ email pessoal de contato WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [\_ \_ EMAIL2 pessoal de contato WPD \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_ \_ email comercial de contato WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [\_EMAIL2 de \_ negócios de contato WPD \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_ \_ outros \_ emails de contato WPD](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_ \_ telefone principal de contato WPD \_](contact-properties.md)                                                | Recomendável.                                                                   |
| [\_ \_ telefone pessoal de contato WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [\_ \_ PHONE2 pessoal de contato WPD \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_ \_ telefone comercial de contato WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [\_PHONE2 de \_ negócios de contato WPD \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_contato com \_ o \_ telefone celular da WPD](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_PHONE2 de contato para \_ dispositivos móveis \_](contact-properties.md)                                                | Opcional.                                                                      |
| [\_ \_ fax pessoal de contato WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_fax de \_ negócios de contato WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_pager de contato WPD \_](contact-properties.md)                                                                 | Opcional.                                                                      |
| [\_ \_ outros telefones em contato com WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_ \_ \_ endereço da Web primário de contato WPD \_](contact-properties.md)                                   | Recomendável.                                                                   |
| [\_ \_ \_ endereço da Web pessoal de contato WPD \_](contact-properties.md)                                 | Opcional.                                                                      |
| [\_ \_ \_ endereço da Web comercial de contato WPD \_](contact-properties.md)                                 | Opcional.                                                                      |
| [WPD \_ em contato com o \_ Instant \_ Messenger](contact-properties.md)                                        | Recomendadas                                                                    |
| [\_MESSENGER2 de contato WPD \_ \_](contact-properties.md)                                      | Opcional.                                                                      |
| [\_MESSENGER3 de contato WPD \_ \_](contact-properties.md)                                      | Opcional.                                                                      |
| [\_ \_ nome da empresa de contato WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_ \_ \_ nome da empresa fonética do contato WPD \_](contact-properties.md)                               | Opcional                                                                       |
| [\_função de contato WPD \_](contact-properties.md)                                                                   | Opcional.                                                                      |
| [\_DataDeNascimento de contato WPD \_](contact-properties.md)                                                         | Opcional.                                                                      |
| [\_ \_ fax principal de contato do WPD \_](contact-properties.md)                                                                            | Opcional.                                                                      |
| [\_cônjuge de contato WPD \_](contact-properties.md)                                                                                  | Opcional.                                                                      |
| [\_filhos de contato WPD \_](contact-properties.md)                                                                                | Opcional.                                                                      |
| [\_Assistente de contato WPD \_](contact-properties.md)                                                                               | Opcional.                                                                      |
| [\_data de \_ aniversário do contato WPD \_](contact-properties.md)                                                                       | Opcional.                                                                      |
| [\_toque de contato WPD \_](contact-properties.md)                                                                                | Opcional.                                                                      |
| [\_observações de \_ informações \_ comuns do WPD](object-properties.md)                                                                        | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                                       | Obrigatório ou opcional       | Descrição                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md)              | Opcional.                  | Contém os dados de contato.         |
| [**\_foto de \_ contato de recursos WPD \_**](wpd-resource-contact-photo.md) | Recomendado, se disponível. | Contém uma imagem do contato. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



