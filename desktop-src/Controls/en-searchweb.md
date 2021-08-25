---
title: EN_SEARCHWEB de notificação (CommCtrl.h)
description: Enviado quando um controle de edição perde o foco do teclado. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem WM \_ NOTIFY.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB de notificação Windows Controles
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
ms.openlocfilehash: 606f53427426e4c9d20c2e4c12245569ed1d8a53ed7ea29162516f6d65fd1baa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047466"
---
# <a name="en_searchweb-notification-code"></a>Código de notificação EN \_ SEARCHWEB

Enviado depois que um controle de edição realizou uma pesquisa na Web quando o recurso "Pesquisar na Web" está [habilitado, consulte EM_ENABLESEARCHWEB](em-enablesearchweb.md). A janela pai do controle de edição recebe esse código de notificação por meio de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lidar com o controle de edição.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMSEARCHWEB.**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, somente 1809 \[ aplicativos da área de trabalho\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2019 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





