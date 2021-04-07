---
description: Enviado a uma janela quando a função SetWindowLong está prestes a alterar um ou mais dos estilos da janela.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Mensagem de WM_STYLECHANGING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828447"
---
# <a name="wm_stylechanging-message"></a>Mensagem do WM \_ STYLECHANGING

Enviado a uma janela quando a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) está prestes a alterar um ou mais dos estilos da janela.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se os estilos da janela ou os estilos de janela estendidos estão sendo alterados. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                            | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ Filestyle**</dt> <dt>-20</dt> </dl> | Os estilos de janela estendidos estão sendo alterados.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ ESTILO**</dt> <dt>-16</dt> </dl>       | Os estilos de janela estão sendo alterados.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contém os novos estilos propostos para a janela. Um aplicativo pode examinar os estilos e, se necessário, alterá-los.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo deve retornar zero se ele processar essa mensagem.

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

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**estilo do WMchanged \_**](wm-stylechanged.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
