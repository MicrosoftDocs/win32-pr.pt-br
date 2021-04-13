---
title: TBN_RESTORE código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está em processo de restauração. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455602"
---
# <a name="tbn_restore-notification-code"></a>Código de notificação de restauração do TBN \_

Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está em processo de restauração. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O aplicativo deve retornar zero em resposta ao primeiro código de notificação de **\_ restauração tbn** recebido no início do processo de restauração para continuar restaurando as informações do botão. Se o aplicativo retornar um valor diferente de zero, o processo de restauração será cancelado.

## <a name="remarks"></a>Comentários

O aplicativo receberá esse código de notificação uma vez no início do processo de restauração e uma vez para cada botão. Esse código de notificação lhe dá a oportunidade de extrair as informações do fluxo de dados que você salvou anteriormente. Se você não tiver salvo nenhuma informação, ignore o código de notificação. Consulte [personalização da barra de ferramentas](toolbar-controls-overview.md) para obter uma discussão mais detalhada sobre como lidar com a **tbn \_ Restore**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





