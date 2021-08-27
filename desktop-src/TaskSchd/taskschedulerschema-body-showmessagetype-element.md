---
title: Elemento body (defaultmessagetype)
description: Contém o texto a ser exibido no corpo da caixa de mensagem.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Elemento de corpo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6b1fbacd450c05b8ff71521dacfa6e95c7efc70fc7d8909ca66f3390bf22295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010866"
---
# <a name="body-showmessagetype-element"></a>Elemento body (defaultmessagetype)

Contém o texto a ser exibido no corpo da caixa de mensagem.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

O elemento **Body** é definido pelo tipo complexo [**exmessagetype**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                               | Descrição                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Exmessage (The Action)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**defaultmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Representa uma ação que mostra uma caixa de mensagem.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade MessageBody de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Para o desenvolvimento de script, consulte [**Permessageaction. MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





