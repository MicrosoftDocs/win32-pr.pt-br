---
description: Um aplicativo envia a mensagem do WM \_ MDIGETACTIVE para uma janela de cliente de interface de vários documentos (MDI) para recuperar o identificador para a janela filho MDI ativa.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Mensagem de WM_MDIGETACTIVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813703"
---
# <a name="wm_mdigetactive-message"></a>Mensagem do WM \_ MDIGETACTIVE

Um aplicativo envia a mensagem do **WM \_ MDIGETACTIVE** para uma janela de cliente de interface de vários documentos (MDI) para recuperar o identificador para a janela filho MDI ativa.


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

O estado maximizado. Se esse parâmetro não for **nulo**, ele será um ponteiro para um valor que indica o estado maximizado da janela filho MDI. Se o valor for **true**, a janela será maximizada; um valor **false** indica que não é. Se esse parâmetro for **nulo**, o parâmetro será ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HWND**

O valor de retorno é o identificador para a janela filho MDI ativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral da interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




