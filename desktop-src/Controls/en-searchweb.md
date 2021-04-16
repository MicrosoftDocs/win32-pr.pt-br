---
title: EN_SEARCHWEB código de notificação (CommCtrl. h)
description: Enviado quando um controle de edição perde o foco do teclado. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de notificação do WM \_ .
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454703"
---
# <a name="en_searchweb-notification-code"></a>\_Código de notificação en SEARCHWEB

Enviado depois que um controle de edição realizou uma pesquisa na Web quando o recurso "Pesquisar na Web" estiver habilitado, consulte [EM_ENABLESEARCHWEB](em-enablesearchweb.md). A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para o controle de edição.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 10, 1809\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**notificação do WM \_**](wm-notify.md)
</dt> </dl>

 

 





