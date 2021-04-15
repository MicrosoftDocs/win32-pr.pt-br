---
title: HDN_FILTERCHANGE código de notificação (commctrl. h)
description: Notifica a janela pai do controle de cabeçalho que os atributos de um filtro de controle de cabeçalho estão sendo alterados ou editados. Esse código de notificação é enviado na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454700"
---
# <a name="hdn_filterchange-notification-code"></a>Código de notificação do HDN \_ FILTERCHANGE

Notifica a janela pai do controle de cabeçalho que os atributos de um filtro de controle de cabeçalho estão sendo alterados ou editados. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item de cabeçalho, incluindo os atributos que estão prestes a ser alterados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HDM \_ SETFILTERCHANGETIMEOUT**](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





