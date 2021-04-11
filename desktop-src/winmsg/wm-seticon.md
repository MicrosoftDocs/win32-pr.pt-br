---
description: Associa um novo ícone grande ou pequeno a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Mensagem de WM_SETICON (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169528"
---
# <a name="wm_seticon-message"></a>\_Mensagem de SETicon do WM

Associa um novo ícone grande ou pequeno a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de ícone a ser definido. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                       | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Ícone \_ do BIG**</dt> <dt>1</dt> </dl>       | Defina o ícone grande para a janela.<br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Ícone \_ do PEQUENO**</dt> <dt>0</dt> </dl> | Defina o ícone pequeno para a janela.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o novo ícone grande ou pequeno. Se esse parâmetro for **NULL**, o ícone indicado por *wParam* será removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

O valor de retorno é um identificador para o ícone grande ou pequeno anterior, dependendo do valor de *wParam*. Será **nulo** se a janela não tivesse nenhum ícone do tipo indicado por *wParam*.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna um identificador para o ícone grande ou pequeno anterior associado à janela, dependendo do valor de *wParam*.

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

[**WM \_ GETicon**](wm-geticon.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
