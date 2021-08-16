---
title: Mensagem de TVM_EDITLABEL (commctrl. h)
description: Inicia a edição in-loco do texto do item especificado, substituindo o texto do item por um controle de edição de linha única que contém o texto.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- controles de Windows de mensagem de TVM_EDITLABEL
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ba9f9d0af4d6afb3c454f5e5477ccd67728bdec7f378b0f0a04adc901ba322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408583"
---
# <a name="tvm_editlabel-message"></a>\_Mensagem TVM EDITLABEL

Inicia a edição in-loco do texto do item especificado, substituindo o texto do item por um controle de edição de linha única que contém o texto. Essa mensagem seleciona implicitamente e concentra o item especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o item a ser editado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador para o controle de edição usado para editar o texto do item, se for bem-sucedido, ou **NULL** de outra forma.

## <a name="remarks"></a>Comentários

Essa mensagem envia um código de notificação [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) para o pai do controle de exibição de árvore.

Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido. Você pode subclassear o controle de edição, mas não destruí-lo.

O controle deve ter o foco antes de você enviar esta mensagem para o controle. O foco pode ser definido usando a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ EDITLABELW** (Unicode) e **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

