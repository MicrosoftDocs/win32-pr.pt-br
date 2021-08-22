---
description: Enviado para uma janela quando a função SetWindowLong está prestes a alterar um ou mais estilos da janela.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: WM_STYLECHANGING mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26574f000c23c918bc0dfb14c5ddd0afcbc439939d6719b95da8024b4828f30b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705836"
---
# <a name="wm_stylechanging-message"></a>Mensagem WM \_ STYLECHANGING

Enviado para uma janela quando a [**função SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) está prestes a alterar um ou mais estilos da janela.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se os estilos da janela ou os estilos de janela estendida estão mudando. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                            | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt> </dl> | Os estilos de janela estendida estão mudando.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Os estilos de janela estão mudando.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contém os novos estilos propostos para a janela. Um aplicativo pode examinar os estilos e, se necessário, alterá-los.

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

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ STYLECHANGED**](wm-stylechanged.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
