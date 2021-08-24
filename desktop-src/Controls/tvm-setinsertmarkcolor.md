---
title: Mensagem de TVM_SETINSERTMARKCOLOR (commctrl. h)
description: Define a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetInsertMarkColor.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- controles de Windows de mensagem de TVM_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d5fd9984b77c99a13e1c7eab24c231e0ce7f601ecb79f8747cdf7ea3011327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636756"
---
# <a name="tvm_setinsertmarkcolor-message"></a>\_Mensagem TVM SETINSERTMARKCOLOR

Define a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor de marca de inserção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **COLORREF** que contém a cor de marca de inserção anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ GETINSERTMARKCOLOR**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

