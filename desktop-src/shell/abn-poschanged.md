---
description: Notifica um AppBar quando ocorreu um evento que pode afetar o tamanho e a posição do AppBar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Mensagem de ABN_POSCHANGED (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967369"
---
# <a name="abn_poschanged-message"></a>\_Mensagem POSCHANGED do ABN

Notifica um AppBar quando ocorreu um evento que pode afetar o tamanho e a posição do AppBar. Os eventos incluem alterações no estado de tamanho, posição e visibilidade da barra de tarefas, bem como a adição, remoção ou redimensionamento de outro AppBar no mesmo lado da tela.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parâmetros

Esta mensagem não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um AppBar deve responder a essa mensagem de notificação enviando as mensagens [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) . Se sua posição for alterada, o AppBar deverá chamar a função [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) para se mover para a nova posição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

