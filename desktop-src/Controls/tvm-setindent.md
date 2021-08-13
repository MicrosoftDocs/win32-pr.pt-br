---
title: TVM_SETINDENT mensagem (Commctrl.h)
description: Define a largura do recuo para um controle de exibição de árvore e redesenha o controle para refletir a nova largura. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetIndent.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538a89439909afe346ae8776d31a2104c7f6014664a33bdd3864bf43b0387e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669661"
---
# <a name="tvm_setindent-message"></a>Mensagem TVM \_ SETINDENT

Define a largura do recuo para um controle de exibição de árvore e redesenha o controle para refletir a nova largura. Você pode enviar essa mensagem explicitamente ou usando a [**macro TreeView \_ SetIndent.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Largura, em pixels, do recuo. Se esse parâmetro for menor que a largura mínima definida pelo sistema, a nova largura será definida como o mínimo definido pelo sistema.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O valor de recuo mínimo definido pelo sistema normalmente é de cinco pixels, mas não é fixo. Para recuperar o valor exato do recuo mínimo em um sistema específico, envie uma mensagem **\_ TVM SETINDENT** com *wParam definido* como zero. Em seguida, [**envie uma \_ mensagem GETINDENT do TVM**](tvm-getindent.md) para recuperar o valor mínimo de recuo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





