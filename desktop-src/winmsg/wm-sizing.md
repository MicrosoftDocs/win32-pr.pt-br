---
description: Enviado para uma janela que o usuário está redimensionando. Ao processar essa mensagem, um aplicativo pode monitorar o tamanho e a posição do retângulo de arrastar e, se necessário, alterar seu tamanho ou posição.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Mensagem de WM_SIZING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662199"
---
# <a name="wm_sizing-message"></a>\_Mensagem de dimensionamento do WM

Enviado para uma janela que o usuário está redimensionando. Ao processar essa mensagem, um aplicativo pode monitorar o tamanho e a posição do retângulo de arrastar e, se necessário, alterar seu tamanho ou posição.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_**</dt> <dt>6</dt> últimos </dl>                | Borda inferior<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | Canto inferior esquerdo<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | Canto inferior direito<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_ ESQUERDA**</dt> <dt>1</dt> </dl>                      | Borda esquerda<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_ DIREITA**</dt> <dt>2</dt> </dl>                   | Borda direita<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_**</dt> <dt>3</dt> principais </dl>                         | Borda superior<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_ TOPLEFT**</dt> <dt>4</dt> </dl>             | Canto superior esquerdo<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_ CANTO superior**</dt> <dt>5</dt> </dl>          | Canto superior direito<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) com as coordenadas de tela do retângulo de arrastar. Para alterar o tamanho ou a posição do retângulo de arrastar, um aplicativo deve alterar os membros dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo deve retornar **true** se ele processar essa mensagem.

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

[**movimentação do WM \_**](wm-moving.md)
</dt> <dt>

[**tamanho do WM \_**](wm-size.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
