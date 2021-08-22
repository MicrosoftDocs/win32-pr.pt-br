---
description: Enviado para uma janela para recuperar um alça para o ícone grande ou pequeno associado a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT+TAB e o ícone pequeno na legenda da janela.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: WM_GETICON mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df8922fa09cf425594a07768f0d7c9ae0ac09222647f181f45331c2b0d47fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587416"
---
# <a name="wm_geticon-message"></a>Mensagem \_ GETICON wm

Enviado para uma janela para recuperar um alça para o ícone grande ou pequeno associado a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT+TAB e o ícone pequeno na legenda da janela.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de ícone que está sendo recuperado. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                          | Significado                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**ÍCONE \_ BIG**</dt> <dt>1</dt> </dl>          | Recupere o ícone grande da janela.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**ÍCONE \_ PEQUENO**</dt> <dt>0</dt> </dl>    | Recupere o ícone pequeno para a janela.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**ÍCONE \_ SMALL2**</dt> <dt>2</dt> </dl> | Recupera o ícone pequeno fornecido pelo aplicativo. Se o aplicativo não fornecer um, o sistema usará o ícone gerado pelo sistema para essa janela.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O DPI do ícone que está sendo recuperado. Isso pode ser usado para fornecer ícones diferentes dependendo do tamanho do ícone.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HICON**

O valor de retorno é um handle para o ícone grande ou pequeno, dependendo do valor *de wParam*. Quando um aplicativo recebe essa mensagem, ele pode retornar um alça para um ícone grande ou pequeno ou passar a mensagem para a [**função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Comentários

Quando um aplicativo recebe essa mensagem, ele pode retornar um alça para um ícone grande ou pequeno ou passar a mensagem para [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna um alça para o ícone grande ou pequeno associado à janela, dependendo do valor *de wParam*.

Uma janela que não tem nenhum ícone definido explicitamente (com **WM \_ SETICON**) usa o ícone para a classe de janela registrada e, nesse caso, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retornará 0 para uma mensagem **\_ GETICON wm.** Se o **envio de uma mensagem \_ GETICON wm** para uma janela retornar 0, tente chamar a função [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) para a janela. Se isso retornar 0, tente a [**função LoadIcon.**](/windows/win32/api/winuser/nf-winuser-loadicona)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ SETICON**](wm-seticon.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
