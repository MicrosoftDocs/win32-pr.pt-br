---
title: HDN_TRACK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário está arrastando um divisor no controle de cabeçalho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK código de notificação Windows controles
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
ms.openlocfilehash: 2fb32a553c85c8fb1bc8321dae5e85b3e7832cf90e4a6652ad163511ad4420d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435216"
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

## <a name="return-value"></a>Valor retornado

Retorna **false** para continuar acompanhando o divisor ou **verdadeiro** para o rastreamento final.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ TRACKW** (Unicode) e **HDN \_ tracka** (ANSI)<br/>                       |



 

 





