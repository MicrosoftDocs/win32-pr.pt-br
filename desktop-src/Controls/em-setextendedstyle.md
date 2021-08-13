---
title: EM_SETEXTENDEDSTYLE mensagem (Commctrl.h)
description: Informa o controle de edição para definir estilos estendidos. Envie essa mensagem ou use a macro Editar \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 710ad6535bd7891f322a4bf02a5fed0f766dd97c2569fa5ec9b961478bf6a457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673072"
---
# <a name="em_setextendedstyle-message"></a>Mensagem \_ EM SETEXTENDEDSTYLE

Informa o controle de edição para definir estilos estendidos. Envie essa mensagem ou use a macro [**Editar \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Máscara usada para selecionar os estilos a serem definidos.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que indica o estilo estendido. Para obter mais informações sobre estilos, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa mensagem for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os estilos estendidos para um controle de edição não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10, versão 1809 somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2019 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

