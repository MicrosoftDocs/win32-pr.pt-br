---
description: Enviado a um ícone quando o usuário solicita que a janela seja restaurada para seu tamanho e posição anteriores.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Mensagem de WM_QUERYOPEN (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011039"
---
# <a name="wm_queryopen-message"></a>Mensagem do WM \_ QUERYOPEN

Enviado a um ícone quando o usuário solicita que a janela seja restaurada para seu tamanho e posição anteriores.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se o ícone puder ser aberto, um aplicativo que processa essa mensagem deverá retornar **true**; caso contrário, ele deve retornar **false** para impedir que o ícone seja aberto.

## <a name="remarks"></a>Comentários

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna **true**.

Ao processar essa mensagem, o aplicativo não deve executar nenhuma ação que cause uma alteração de ativação ou de foco (por exemplo, criando uma caixa de diálogo).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
