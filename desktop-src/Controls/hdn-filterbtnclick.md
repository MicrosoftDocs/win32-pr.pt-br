---
title: HDN_FILTERBTNCLICK código de notificação (commctrl. h)
description: Notifica a janela pai do controle de cabeçalho quando o botão de filtro é clicado ou em resposta a uma \_ mensagem HDM SETITEM. Esse código de notificação é enviado na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824197"
---
# <a name="hdn_filterbtnclick-notification-code"></a>Código de notificação do HDN \_ FILTERBTNCLICK

Notifica a janela pai do controle de cabeçalho quando o botão de filtro é clicado ou em resposta a uma mensagem [**HDM \_ SETITEM**](hdm-setitem.md) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) que contém informações sobre o controle de cabeçalho e o botão de filtro de cabeçalho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se você retornar **true**, um código de notificação [HDN \_ FILTERCHANGE](hdn-filterchange.md) será enviado para a janela pai do controle de cabeçalho. Esse código de notificação dá à janela pai uma oportunidade de sincronizar seus elementos de interface do usuário. Retorne **false** se você não quiser que a notificação seja enviada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





