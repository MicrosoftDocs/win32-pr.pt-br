---
title: Elemento exmessage (The Action)
description: Representa uma ação que mostra uma caixa de mensagem.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Elemento exmessage Agendador de Tarefas
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294783"
---
# <a name="showmessage-actiongroup-element"></a>Elemento exmessage (The Action)

Representa uma ação que mostra uma caixa de mensagem.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

O elemento **exmessage** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                    | Derivado de                                                       | Descrição                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Ações (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**ActionType**](taskschedulerschema-actionstype-complextype.md) | Contém as ações executadas pela tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                            | Type           | Descrição                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Corpo**](taskschedulerschema-body-showmessagetype-element.md)   | não vazio | Especifica o texto a ser exibido no corpo da caixa de mensagem. <br/> |
| [**Título**](taskschedulerschema-title-showmessagetype-element.md) | não vazio | Especifica o título da caixa de mensagem. <br/>                       |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, uma ação da caixa de mensagem é especificada usando o objeto [**Exmessageaction**](showmessageaction.md) .

Para desenvolvimento em C++, uma ação de caixa de mensagem é especificada usando a interface [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .

**Windows 8 e Windows Server 2012:** Este elemento foi removido. Você pode usar o IExecAction com a função script do Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar uma mensagem na sessão do usuário.

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que usa uma ação de caixa de mensagem, consulte [exemplo de caixa de mensagem (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                 |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                    |



 

