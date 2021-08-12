---
title: Tipo complexo exmessagetype
description: Define os elementos que representam uma ação que mostra uma caixa de mensagem.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- tipo complexo de defaultmessagetype Agendador de Tarefas
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aeb2c0e1b3ac3e29502e7d998305674aaa283371be6a22324dde6d84c4330326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611238"
---
# <a name="showmessagetype-complex-type"></a>Tipo complexo exmessagetype

Define os elementos que representam uma ação que mostra uma caixa de mensagem.

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                            | Type           | Descrição                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Conteúdo**](taskschedulerschema-body-showmessagetype-element.md)   | não vazio | Especifica o texto a ser exibido no corpo da caixa de mensagem. <br/> |
| [**Título**](taskschedulerschema-title-showmessagetype-element.md) | não vazio | Especifica o título da caixa de mensagem. <br/>                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





