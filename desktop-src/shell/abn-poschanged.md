---
description: Notifica uma barra de aplicativos quando ocorreu um evento que pode afetar o tamanho e a posição da barra de aplicativos.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: ABN_POSCHANGED mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92528de38b60c1f4705873427616b1ed7a5be6be5875a21e352d2136313c84df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943596"
---
# <a name="abn_poschanged-message"></a>Mensagem POSCHANGED do ABN \_

Notifica uma barra de aplicativos quando ocorreu um evento que pode afetar o tamanho e a posição da barra de aplicativos. Os eventos incluem alterações no tamanho, na posição e no estado de visibilidade da barra de tarefas, bem como a adição, remoção ou replicação de outra barra de aplicativos no mesmo lado da tela.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parâmetros

Essa mensagem não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Uma barra de aplicativos deve responder a essa mensagem de notificação enviando as mensagens [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS.**](abm-setpos.md) Se sua posição tiver sido alterada, a barra de aplicativos deverá chamar a [**função MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) para se mover para a nova posição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

