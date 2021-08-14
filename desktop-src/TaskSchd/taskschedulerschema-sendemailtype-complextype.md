---
title: Tipo complexo sendEmailType
description: Define o tipo de ação usado para especificar que um email será enviado quando uma tarefa for executada. Esse tipo define todos os elementos usados para modelar a mensagem de email.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- Agendador de Tarefas tipo complexo sendEmailType
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0242700b2f22050741d9de175b7dae532cc5ef4bb2097fadb23799ce3b2f82b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356338"
---
# <a name="sendemailtype-complex-type"></a>Tipo complexo sendEmailType

Define o tipo de ação usado para especificar que um email será enviado quando uma tarefa for executada. Esse tipo define todos os elementos usados para modelar a mensagem de email.

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                        | Type                                                                         | Descrição                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Anexos**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**AttachmentType**](taskschedulerschema-attachmentstype-complextype.md)   | Especifica uma lista de anexos na mensagem de email.<br/>                                 |
| [**Cco**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **cadeia de caracteres**                                                                   | Especifica os endereços de email usados na linha Cco de uma mensagem de email.<br/>               |
| [**Corpo**](taskschedulerschema-body-sendemailtype-element.md)                 | **cadeia de caracteres**                                                                   | Especifica o texto no corpo da mensagem de email.<br/>                                  |
| [**CC**](taskschedulerschema-cc-sendemailtype-element.md)                     | **cadeia de caracteres**                                                                   | Especifica os endereços de email usados na linha CC de uma mensagem de email.<br/>                |
| [**De**](taskschedulerschema-from-sendemailtype-element.md)                 | **cadeia de caracteres**                                                                   | Especifica o endereço de email do remetente.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **cadeia de caracteres**                                                                   | Especifica os endereços de email que são respondidos na mensagem de email.<br/>               |
| [**Servidor**](taskschedulerschema-server-sendemailtype-element.md)             | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md)      | Especifica o servidor de email usado para enviar a mensagem de email. <br/>                           |
| [**Assunto**](taskschedulerschema-subject-sendemailtype-element.md)           | **cadeia de caracteres**                                                                   | Especifica o assunto da mensagem de email.<br/>                                           |
| [**Para**](taskschedulerschema-to-sendemailtype-element.md)                     | **cadeia de caracteres**                                                                   | Especifica os endereços de email para os quais o email será enviado.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





