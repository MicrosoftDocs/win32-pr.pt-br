---
description: Enviado para um aplicativo quando o IME termina a composição. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: WM_IME_ENDCOMPOSITION mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9e19bcf1834d4f9e721efb2a2be53ca20268c7be42109975a7dea52e75d214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560396"
---
# <a name="wm_ime_endcomposition-message"></a>Mensagem WM \_ IME \_ ENDCOMPOSITION

Enviado para um aplicativo quando o IME termina a composição. Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parâmetros

Essa mensagem não tem parâmetros.

<dl></dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo deverá processar essa mensagem se exibir os caracteres de composição em si.

Se o aplicativo tiver criado uma janela do IME, ele deverá passar essa mensagem para essa janela. A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  processa essa mensagem passando-a para a janela padrão do IME.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de Métodos de Entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
