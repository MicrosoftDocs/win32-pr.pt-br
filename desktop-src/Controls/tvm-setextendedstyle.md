---
title: TVM_SETEXTENDEDSTYLE mensagem (Commctrl.h)
description: Informa o controle de exibição de árvore para definir estilos estendidos. Envie essa mensagem ou use a macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13d99a2f7a27475c30867f007f45d7525118d3077ebdce235c6bd33e1f8aafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750956"
---
# <a name="tvm_setextendedstyle-message"></a>Mensagem TVM \_ SETEXTENDEDSTYLE

Informa o controle de exibição de árvore para definir estilos estendidos. Envie essa mensagem ou use a macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Máscara usada para selecionar os estilos a serem definidos.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que indica o estilo estendido. Para obter mais informações sobre estilos, consulte Estilos estendidos do [controle de exibição de árvore.](tree-view-control-window-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa mensagem for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os estilos estendidos para um controle de exibição de árvore não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

