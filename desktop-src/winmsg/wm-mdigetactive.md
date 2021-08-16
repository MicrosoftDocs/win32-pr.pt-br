---
description: Um aplicativo envia a mensagem WM MDIGETACTIVE para uma janela de cliente MDI (interface MDI) para recuperar o alça para a janela \_ filho MDI ativa.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: WM_MDIGETACTIVE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7716138028f7fe7447cc89d8feded7806f4f8757cd4a18b4bef6f2d812de3f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200136"
---
# <a name="wm_mdigetactive-message"></a>Mensagem \_ WM MDIGETACTIVE

Um aplicativo envia a **mensagem WM \_ MDIGETACTIVE** para uma janela de cliente MDI (interface MDI) para recuperar o alça para a janela filho MDI ativa.


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

O estado maximizada. Se esse parâmetro não for **NULL,** ele será um ponteiro para um valor que indica o estado maximizada da janela filho MDI. Se o valor for **TRUE,** a janela será maximizada; um valor **false** indica que não é. Se esse parâmetro for **NULL,** o parâmetro será ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Digite: **HWND**

O valor de retorno é o alça para a janela filho MDI ativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral da interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




