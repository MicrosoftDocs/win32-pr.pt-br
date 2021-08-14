---
title: CBEN_ENDEDIT código de notificação (commctrl. h)
description: Enviado quando o usuário concluiu uma operação na caixa de edição ou selecionou um item na lista suspensa do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT código de notificação Windows controles
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae9205e84e4f1c0b10e516b1f406f2d167f1bc5cc38417a31379d20e16fcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413946"
---
# <a name="cben_endedit-notification-code"></a>Código de notificação do CBEN \_ ENDEDIT

Enviado quando o usuário concluiu uma operação na caixa de edição ou selecionou um item na lista suspensa do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) que contém informações sobre como o usuário concluiu a operação de edição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**False** para aceitar o código de notificação e permitir que o controle exiba o item selecionado; caso contrário, **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CBEN \_ ENDEDITW** (Unicode) e **CBEN \_ endediçãoa** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





