---
description: Um aplicativo envia a mensagem do WM \_ MDINEXT para uma janela de cliente MDI (interface de vários documentos) para ativar a janela filho seguinte ou anterior.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Mensagem de WM_MDINEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647076"
---
# <a name="wm_mdinext-message"></a>Mensagem do WM \_ MDINEXT

Um aplicativo envia a mensagem do **WM \_ MDINEXT** para uma janela de cliente MDI (interface de vários documentos) para ativar a janela filho seguinte ou anterior.


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela filho MDI. O sistema ativa a janela filho imediatamente antes ou depois da janela filho especificada, dependendo do valor do parâmetro *lParam* . Se o parâmetro *wParam* for **nulo**, o sistema ativará a janela filho imediatamente antes ou depois da janela filho ativa no momento.

</dd> <dt>

*lParam* 
</dt> <dd>

Se esse parâmetro for zero, o sistema ativará a próxima janela filho MDI e colocará a janela filho identificada pelo parâmetro *wParam* por trás de todas as outras janelas filhas. Se esse parâmetro for diferente de zero, o sistema ativará a janela filho anterior, colocando-o na frente da janela filho identificada por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **zero**

O valor de retorno é sempre zero.

## <a name="remarks"></a>Comentários

Se uma janela do cliente MDI receber qualquer mensagem que altere a ativação de suas janelas filhas enquanto a janela filho MDI ativa for maximizada, o sistema restaura a janela filho ativa e maximiza a janela filho ativada recentemente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**MDIACTIVATE do WM \_**](wm-mdiactivate.md)
</dt> <dt>

[**MDIGETACTIVE do WM \_**](wm-mdigetactive.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




