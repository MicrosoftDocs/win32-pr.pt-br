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
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918741"
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
| [**Corpo**](taskschedulerschema-body-showmessagetype-element.md)   | não vazio | Especifica o texto a ser exibido no corpo da caixa de mensagem. <br/> |
| [**Título**](taskschedulerschema-title-showmessagetype-element.md) | não vazio | Especifica o título da caixa de mensagem. <br/>                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





