---
description: '\_contato de \_ tipo de conteúdo WPD \_'
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8354aa444f476e7c0b64d2e3d14d474c6eea02f90e8313c20073db2d0368fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083330"
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
| [WPD \_ ENTRE EM CONTATO COM OUTRO ENDEREÇO POSTAL \_ \_ \_ \_ COMPLETO](contact-properties.md)                      | Opcional.                                                                      |
| [WPD \_ ENTRE EM CONTATO COM OUTRO ENDEREÇO POSTAL \_ \_ \_ \_ LINE1](contact-properties.md)                    | Opcional.                                                                      |
| [WPD \_ ENTRE EM CONTATO COM OUTRO ENDEREÇO POSTAL \_ \_ \_ \_ LINE2](contact-properties.md)                    | Opcional.                                                                      |
| [WPD \_ ENTRE EM CONTATO COM OUTRA CIDADE DE ENDEREÇO \_ \_ \_ \_ POSTAL](contact-properties.md)                      | Opcional.                                                                      |
| [WPD \_ ENTRE EM CONTATO COM OUTRA REGIÃO DE ENDEREÇO \_ \_ \_ \_ POSTAL](contact-properties.md)                  | Opcional.                                                                      |
| [WPD \_ ENTRE EM CONTATO COM OUTRO CEP DE ENDEREÇO \_ \_ \_ \_ \_ POSTAL](contact-properties.md)       | Opcional.                                                                      |
| [WPD \_ ENTRE EM CONTATO COM OUTRO PAÍS POSTAL DE ENDEREÇO \_ \_ \_ \_ \_ POSTAL](contact-properties.md) | Opcional.                                                                      |
| [ENDEREÇO DE \_ EMAIL PRIMÁRIO \_ DE CONTATO \_ WPD \_](contact-properties.md)                               | Recomendável.                                                                   |
| [EMAIL PESSOAL \_ DO WPD CONTACT \_ \_](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ EMAIL2](contact-properties.md)                                            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL2](contact-properties.md)                                            | Opcional.                                                                      |
| [ENTRE EM \_ CONTATO COM WPD \_ OUTROS \_ EMAILS](contact-properties.md)                                                  | Opcional.                                                                      |
| [TELEFONE PRIMÁRIO \_ DE \_ CONTATO WPD \_](contact-properties.md)                                                | Recomendável.                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE2](contact-properties.md)                                            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE](contact-properties.md)                                              | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE2](contact-properties.md)                                            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ PHONE](contact-properties.md)                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ PHONE2](contact-properties.md)                                                | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ FAX](contact-properties.md)                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ FAX](contact-properties.md)                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PAGER](contact-properties.md)                                                                 | Opcional.                                                                      |
| [WPD \_ ENTRE EM CONTATO COM OUTROS \_ \_ TELEFONES](contact-properties.md)                                                  | Opcional.                                                                      |
| [ENDEREÇO WEB \_ \_ PRIMÁRIO DO CONTATO \_ WPD \_](contact-properties.md)                                   | Recomendável.                                                                   |
| [ENDEREÇO WEB \_ \_ PESSOAL DO WPD CONTACT \_ \_](contact-properties.md)                                 | Opcional.                                                                      |
| [ENDEREÇO WEB DO WPD \_ \_ CONTACT BUSINESS \_ \_](contact-properties.md)                                 | Opcional.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER](contact-properties.md)                                        | Recomendado                                                                    |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER2](contact-properties.md)                                      | Opcional.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER3](contact-properties.md)                                      | Opcional.                                                                      |
| [WPD \_ CONTACT \_ COMPANY \_ NAME](contact-properties.md)                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ PHONETIC \_ COMPANY \_ NAME](contact-properties.md)                               | Opcional                                                                       |
| [FUNÇÃO DE \_ CONTATO WPD \_](contact-properties.md)                                                                   | Opcional.                                                                      |
| [WPD \_ CONTACT \_ BIRTHDATE](contact-properties.md)                                                         | Opcional.                                                                      |
| [FAX PRIMÁRIO \_ DE \_ CONTATO WPD \_](contact-properties.md)                                                                            | Opcional.                                                                      |
| [WPD \_ CONTACT \_ SPOUSE](contact-properties.md)                                                                                  | Opcional.                                                                      |
| [WPD \_ CONTACT \_ CHILDREN](contact-properties.md)                                                                                | Opcional.                                                                      |
| [ASSISTENTE DE \_ CONTATO \_ WPD](contact-properties.md)                                                                               | Opcional.                                                                      |
| [DATA DE \_ ANIVERSÁRIO DO CONTATO \_ WPD \_](contact-properties.md)                                                                       | Opcional.                                                                      |
| [WPD \_ CONTACT \_ RINGTONE](contact-properties.md)                                                                                | Opcional.                                                                      |
| [NOTAS DE \_ INFORMAÇÕES \_ COMUNS DO \_ WPD](object-properties.md)                                                                        | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os recursos a seguir.



| Nome do Recurso                                                       | Obrigatório ou Opcional       | Descrição                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)              | Opcional.                  | Contém os dados de contato.         |
| [**WPD \_ RESOURCE \_ CONTACT \_ PHOTO**](wpd-resource-contact-photo.md) | Recomendado, se disponível. | Contém uma imagem do contato. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



