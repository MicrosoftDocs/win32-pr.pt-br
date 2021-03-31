---
title: Mensagem de TVM_EDITLABEL (commctrl. h)
description: Inicia a edição in-loco do texto do item especificado, substituindo o texto do item por um controle de edição de linha única que contém o texto.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- Controles de TVM_EDITLABEL de mensagens do Windows
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
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918263"
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

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de edição usado para editar o texto do item, se for bem-sucedido, ou **NULL** de outra forma.

## <a name="remarks"></a>Comentários

Essa mensagem envia um código de notificação [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) para o pai do controle de exibição de árvore.

Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido. Você pode subclassear o controle de edição, mas não destruí-lo.

O controle deve ter o foco antes de você enviar esta mensagem para o controle. O foco pode ser definido usando a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ EDITLABELW** (Unicode) e **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

