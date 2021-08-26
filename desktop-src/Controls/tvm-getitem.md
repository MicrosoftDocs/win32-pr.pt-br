---
title: TVM_GETITEM mensagem (Commctrl.h)
description: Recupera alguns ou todos os atributos de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItem TreeView.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM controles de Windows mensagem
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425b0200df62b1cfcbc18556ad12513e43cebadf6e5742b36880464fad195fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984886"
---
# <a name="tvm_getitem-message"></a>Mensagem \_ GETITEM do TVM

Recupera alguns ou todos os atributos de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItem TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que especifica as informações a serem recuperadas e recebe informações sobre o item. Com [a versão 4.71](common-control-versions.md) e posterior, você pode usar uma [**estrutura TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Quando a mensagem é enviada, o membro **hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica o item sobre o que recuperar informações e o membro de máscara especifica os atributos a serem recuperados. 

Se o sinalizador TVIF TEXT for definido no membro de máscara da estrutura \_ [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX,**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) o membro **pszText** deverá apontar para um buffer válido e o membro **cchTextMax** deverá ser definido como o número de caracteres nesse  buffer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ GETITEMW** (Unicode) e **TVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





