---
title: HDN_TRACK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário está arrastando um divisor no controle de cabeçalho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824567"
---
# <a name="hdn_track-notification-code"></a>Código de notificação do HDN \_ Track

Notifica uma janela pai do controle de cabeçalho que o usuário está arrastando um divisor no controle de cabeçalho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item cujo divisor está sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **false** para continuar acompanhando o divisor ou **verdadeiro** para o rastreamento final.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ TRACKW** (Unicode) e **HDN \_ tracka** (ANSI)<br/>                       |



 

 





