---
title: Mensagem de TVM_GETINSERTMARKCOLOR (commctrl. h)
description: Recupera a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetInsertMarkColor.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Controles de TVM_GETINSERTMARKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919076"
---
# <a name="tvm_getinsertmarkcolor-message"></a>\_Mensagem TVM GETINSERTMARKCOLOR

Recupera a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a cor da marca de inserção atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

