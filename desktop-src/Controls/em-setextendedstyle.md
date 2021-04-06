---
title: Mensagem de EM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa o controle de edição para definir os estilos estendidos. Envie esta mensagem ou use a macro Edit \_ setextendedattribute.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Controles de EM_SETEXTENDEDSTYLE de mensagens do Windows
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
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086186"
---
# <a name="em_setextendedstyle-message"></a>\_Mensagem em SETextendedattributestyle

Informa o controle de edição para definir os estilos estendidos. Envie esta mensagem ou use a macro [**Edit \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

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

## <a name="return-value"></a>Retornar valor

Se essa mensagem tiver sucesso, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os estilos estendidos para um controle de edição não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1809\]<br/>                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

