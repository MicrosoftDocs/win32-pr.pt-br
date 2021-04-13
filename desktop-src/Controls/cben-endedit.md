---
title: CBEN_ENDEDIT código de notificação (commctrl. h)
description: Enviado quando o usuário concluiu uma operação na caixa de edição ou selecionou um item na lista suspensa do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT de código de notificação controles do Windows
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
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369254"
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

## <a name="return-value"></a>Retornar valor

**False** para aceitar o código de notificação e permitir que o controle exiba o item selecionado; caso contrário, **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CBEN \_ ENDEDITW** (Unicode) e **CBEN \_ endediçãoa** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





