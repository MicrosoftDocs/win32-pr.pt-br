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
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757941"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





