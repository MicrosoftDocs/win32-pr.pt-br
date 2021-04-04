---
title: Elemento Title (defaultmessagetype)
description: Contém o título da caixa de mensagem.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Elemento de título Agendador de Tarefas
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085278"
---
# <a name="title-showmessagetype-element"></a>Elemento Title (defaultmessagetype)

Contém o título da caixa de mensagem.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

O elemento **title** é definido pelo tipo complexo [**exmessagetype**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                               | Descrição                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Exmessage (The Action)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**defaultmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Representa uma ação que mostra uma caixa de mensagem.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade Title de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Para o desenvolvimento de scripts, consulte o " [**nome do email". título**](showmessageaction-title.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





