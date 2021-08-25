---
title: TBN_SAVE de notificação (Commctrl.h)
description: Notifica a janela pai de uma barra de ferramentas de que uma barra de ferramentas está no processo de ser salva. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE código de notificação Windows Controles
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
ms.openlocfilehash: 7f9d4fb40d0e5beafcd720b4de52a8cf09d17c3e4c6f7b4dcfa8da78e00e97ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876586"
---
# <a name="tbn_save-notification-code"></a>Código de \_ notificação TBN SAVE

Notifica a janela pai de uma barra de ferramentas de que uma barra de ferramentas está no processo de ser salva. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTBSAVE.**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O aplicativo receberá esse código de notificação uma vez no início do processo de salvar e uma vez para cada botão. Esse código de notificação oferece a oportunidade de adicionar suas próprias informações às salvas pelo Shell. Se você não quiser adicionar informações, ignore o código de notificação. Consulte [Personalização da barra de ferramentas](toolbar-controls-overview.md) para obter uma discussão mais detalhada sobre como lidar com o TBN \_ SAVE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TBN \_ RESTORE](tbn-restore.md)
</dt> </dl>

 

 





