---
title: Código de notificação EN_ERRSPACE (WinUser. h)
description: Enviado quando um controle de edição não pode alocar memória suficiente para atender a uma solicitação específica. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de comando do WM \_ .
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824201"
---
# <a name="en_errspace-notification-code"></a>\_Código de notificação en ERRSPACE

Enviado quando um controle de edição não pode alocar memória suficiente para atender a uma solicitação específica. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o controle de edição.

</dd> </dl>

## <a name="remarks"></a>Comentários

A janela pai sempre receberá uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para esse evento; ela não requer uma máscara de notificação enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

