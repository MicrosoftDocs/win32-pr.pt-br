---
description: Enviado a um aplicativo para fornecer comandos e informações de solicitação. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Mensagem de WM_IME_REQUEST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d73f1f920efb2908104304fcbc08fd19d648e52fdb737f12027b47436531eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927626"
---
# <a name="wm_ime_request-message"></a>WM_IME_REQUEST mensagem

Enviado a um aplicativo para fornecer comandos e informações de solicitação. Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*wParam* 
</dt> <dd>

Comando. Esse parâmetro pode ter um dos seguintes valores:

<dl> 
<dd><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></dd> 
<dd><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></dd> 
<dd><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></dd> 
<dd><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></dd> 
<dd><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></dd> 
<dd><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></dd> 
<dd><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

Dados específicos do comando. Para obter mais informações, consulte a descrição de cada comando.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor específico de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h);</dt> <dt>Imm. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[IMR_CANDIDATEWINDOW](imr-candidatewindow.md)
</dt> <dt>

[IMR_COMPOSITIONFONT](imr-compositionfont.md)
</dt> <dt>

[IMR_COMPOSITIONWINDOW](imr-compositionwindow.md)
</dt> <dt>

[IMR_CONFIRMRECONVERTSTRING](imr-confirmreconvertstring.md)
</dt> <dt>

[IMR_DOCUMENTFEED](imr-documentfeed.md)
</dt> <dt>

[IMR_QUERYCHARPOSITION](imr-querycharposition.md)
</dt> <dt>

[IMR_RECONVERTSTRING](imr-reconvertstring.md)
</dt> </dl>

 

 
