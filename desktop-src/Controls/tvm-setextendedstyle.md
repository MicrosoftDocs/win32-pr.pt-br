---
title: Mensagem de TVM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa o controle de exibição de árvore para definir estilos estendidos. Envie esta mensagem ou use a macro TreeView \_ setextendedattribute.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Controles de TVM_SETEXTENDEDSTYLE de mensagens do Windows
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
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499434"
---
# <a name="tvm_setextendedstyle-message"></a>\_Mensagem TVM SETextendedattribute

Informa o controle de exibição de árvore para definir estilos estendidos. Envie esta mensagem ou use a macro [**TreeView \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Máscara usada para selecionar os estilos a serem definidos.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que indica o estilo estendido. Para obter mais informações sobre estilos, consulte [controle de exibição de árvore estilos estendidos](tree-view-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa mensagem tiver sucesso, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os estilos estendidos para um controle de exibição em árvore não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

