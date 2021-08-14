---
description: Enviado para uma janela que o usuário está reizing. Ao processar essa mensagem, um aplicativo pode monitorar o tamanho e a posição do retângulo de arrastar e, se necessário, alterar seu tamanho ou posição.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: WM_SIZING mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645c9aaf778d5866050b45496298a46c4488e39b12f449f3ee0e8607dfc367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436151"
---
# <a name="wm_sizing-message"></a>Mensagem WM \_ SIZING

Enviado para uma janela que o usuário está reizing. Ao processar essa mensagem, um aplicativo pode monitorar o tamanho e a posição do retângulo de arrastar e, se necessário, alterar seu tamanho ou posição.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A borda da janela que está sendo dimensionada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                         | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_ INFERIOR**</dt> <dt>6</dt> </dl>                | Borda inferior<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | Canto inferior esquerdo<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | Canto inferior direito<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_ LEFT**</dt> <dt>1</dt> </dl>                      | Borda esquerda<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_ RIGHT**</dt> <dt>2</dt> </dl>                   | Borda direita<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_ TOP**</dt> <dt>3</dt> </dl>                         | Borda superior<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_ TOPLEFT**</dt> <dt>4</dt> </dl>             | Canto superior esquerdo<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_ TOPRIGHT**</dt> <dt>5</dt> </dl>          | Canto superior direito<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) com as coordenadas de tela do retângulo de arrastar. Para alterar o tamanho ou a posição do retângulo de arrastar, um aplicativo deve alterar os membros dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Um aplicativo deverá retornar **TRUE** se ele processa essa mensagem.

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

[**WM \_ MOVING**](wm-moving.md)
</dt> <dt>

[**TAMANHO \_ DO WM**](wm-size.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
