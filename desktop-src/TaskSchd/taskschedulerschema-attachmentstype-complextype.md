---
title: Tipo complexo AttachmentType
description: Define os elementos usados para especificar um anexo enviado com uma mensagem de email.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- tipo complexo AttachmentType Agendador de Tarefas
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d98b266fcb15fbd47fbb2a5bb792b95e4fb765a48b2fbcf6c1185aad9475df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772386"
---
# <a name="attachmentstype-complex-type"></a>Tipo complexo AttachmentType

Define os elementos usados para especificar um anexo enviado com uma mensagem de email.

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                          | Type                                                                    | Descrição                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Arquivo**](taskschedulerschema-file-attachmentstype-element.md) | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica o caminho para um arquivo que é enviado como um anexo em uma mensagem de email.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





