---
title: Elemento headerfield (headerFieldsType)
description: Contém um campo para um cabeçalho em uma mensagem de email.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Elemento headerfield Agendador de Tarefas
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918e432ce7a8ea2d43769b9d9ee1315a4b35bce6f2c0cb23f1153ec7afe1a599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139209"
---
# <a name="headerfield-headerfieldstype-element"></a>Elemento headerfield (headerFieldsType)

Contém um campo para um cabeçalho em uma mensagem de email.

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

O elemento **headerfield** é definido pelo tipo complexo [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                        | Derivado de                                                                 | Descrição                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                            | Type                                                                    | Descrição                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nome**](taskschedulerschema-name-headerfieldtype-element.md)   | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica o nome do campo de cabeçalho em uma mensagem de email.<br/> |
| [**Valor**](taskschedulerschema-value-headerfieldtype-element.md) | **cadeia de caracteres**                                                              | Especifica o valor de um campo de cabeçalho em uma mensagem de email.<br/>  |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Para desenvolvimento de script, consulte [**emailaction. HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





