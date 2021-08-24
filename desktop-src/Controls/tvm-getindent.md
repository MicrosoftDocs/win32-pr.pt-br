---
title: TVM_GETINDENT mensagem (Commctrl.h)
description: Recupera a quantidade, em pixels, de que os itens filho são recuados em relação aos seus itens pai. Você pode enviar essa mensagem explicitamente ou usando a \_ macro TreeView GetIndent.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee65da49efc19954209b2694d783761017d8c2ae53030e755b8bea61213276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834176"
---
# <a name="tvm_getindent-message"></a>Mensagem \_ GETINDENT do TVM

Recupera a quantidade, em pixels, de que os itens filho são recuados em relação aos seus itens pai. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ TreeView GetIndent.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a quantidade de recuo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





