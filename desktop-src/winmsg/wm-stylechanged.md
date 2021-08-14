---
description: Enviado para uma janela depois que a função SetWindowLong tiver alterado um ou mais estilos da janela.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: WM_STYLECHANGED mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc84d3df087cb8667367830998675903a83f633eba4797e64125269d0c937c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705936"
---
# <a name="wm_stylechanged-message"></a>Mensagem WM \_ STYLECHANGED

Enviado para uma janela depois que [**a função SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) tiver alterado um ou mais estilos da janela.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se os estilos da janela ou os estilos de janela estendida foram alterados. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                            | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt> </dl> | Os estilos de janela estendida foram alterados.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Os estilos de janela foram alterados.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contém os novos estilos para a janela. Um aplicativo pode examinar os estilos, mas não pode alterá-los.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Um aplicativo deverá retornar zero se ele processa essa mensagem.

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

[**Setwindowlong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ STYLECHANGING**](wm-stylechanging.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
