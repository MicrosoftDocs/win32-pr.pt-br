---
title: TBN_SAVE código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está sendo salva. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645225"
---
# <a name="tbn_save-notification-code"></a>TBN \_ salvar código de notificação

Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está sendo salva. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O aplicativo receberá esse código de notificação uma vez no início do processo de salvamento e uma vez para cada botão. Esse código de notificação lhe dá a oportunidade de adicionar suas próprias informações ao salvas pelo shell. Se você não quiser adicionar informações, ignore o código de notificação. Consulte [personalização da barra de ferramentas](toolbar-controls-overview.md) para obter uma discussão mais detalhada sobre como lidar com tbn \_ Save.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[TBN \_ restauração](tbn-restore.md)
</dt> </dl>

 

 





