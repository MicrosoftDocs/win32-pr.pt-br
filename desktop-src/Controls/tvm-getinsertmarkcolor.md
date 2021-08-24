---
title: TVM_GETINSERTMARKCOLOR mensagem (Commctrl.h)
description: Recupera a cor usada para desenhar a marca de inserção para a exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro TreeView GetInsertMarkColor.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR controles de Windows mensagem
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
ms.openlocfilehash: 38c784f6b3c363d68472270f0f52cb97cea7c13b6eb709d1aba4975d3cd97bca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834146"
---
# <a name="tvm_getinsertmarkcolor-message"></a>Mensagem TVM \_ GETINSERTMARKCOLOR

Recupera a cor usada para desenhar a marca de inserção para a exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ TreeView GetInsertMarkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um [**valor COLORREF**](/windows/desktop/gdi/colorref) que contém a cor da marca de inserção atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

