---
title: Mensagem de TVM_SETINDENT (commctrl. h)
description: Define a largura do recuo para um controle de exibição de árvore e redesenha o controle para refletir a nova largura. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetIndent de TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- Controles de TVM_SETINDENT de mensagens do Windows
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
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085722"
---
# <a name="tvm_setindent-message"></a>Mensagem de TVM de \_ SUBrecuo

Define a largura do recuo para um controle de exibição de árvore e redesenha o controle para refletir a nova largura. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetIndent de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Largura, em pixels, do recuo. Se esse parâmetro for menor que a largura mínima definida pelo sistema, a nova largura será definida como o mínimo definido pelo sistema.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O valor de recuo mínimo definido pelo sistema normalmente é de cinco pixels, mas não é fixo. Para recuperar o valor exato do recuo mínimo em um sistema específico, envie uma mensagem **TVM \_ SetIndent** com *wParam* definido como zero. Em seguida, envie uma mensagem [**TVM \_ GetIndent**](tvm-getindent.md) para recuperar o valor mínimo de recuo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Defaultindent de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





