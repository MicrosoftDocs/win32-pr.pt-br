---
description: Enviado quando o tamanho e a posição da área do cliente de uma janela devem ser calculados. Ao processar essa mensagem, um aplicativo pode controlar o conteúdo da área do cliente da janela quando o tamanho ou a posição da janela é alterada.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: Mensagem de WM_NCCALCSIZE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7d63fea3ad0a80bba686d8d86aa5354f0bb45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762133"
---
# <a name="wm_nccalcsize-message"></a>Mensagem do WM \_ NCCALCSIZE

Enviado quando o tamanho e a posição da área do cliente de uma janela devem ser calculados. Ao processar essa mensagem, um aplicativo pode controlar o conteúdo da área do cliente da janela quando o tamanho ou a posição da janela é alterada.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Se *wParam* for **true**, ele especificará que o aplicativo deve indicar qual parte da área do cliente contém informações válidas. O sistema copia as informações válidas para a área especificada dentro da nova área do cliente.

Se *wParam* for **false**, o aplicativo não precisará indicar a parte válida da área do cliente.

</dd> <dt>

*lParam* 
</dt> <dd>

Se *wParam* for **true**, *lParam* apontará para uma estrutura de [**\_ parâmetros de NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) que contém informações que um aplicativo pode usar para calcular o novo tamanho e a posição do retângulo do cliente.

Se *wParam* for **false**, *lParam* apontará para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Na entrada, a estrutura contém o retângulo de janela proposto para a janela. Ao sair, a estrutura deve conter as coordenadas de tela da área de cliente da janela correspondente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se o parâmetro *wParam* for **false**, o aplicativo deverá retornar zero.

Se *wParam* for **true**, o aplicativo deverá retornar zero ou uma combinação dos valores a seguir.

Se *wParam* for **true** e um aplicativo retornar zero, a área de cliente antiga será preservada e alinhada com o canto superior esquerdo da nova área do cliente.



| Código/valor de retorno                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ ALIGNTOP**</dt> <dt>0x0010</dt> </dl>    | Especifica que a área do cliente da janela deve ser preservada e alinhada com a parte superior da nova posição da janela. Por exemplo, para alinhar a área do cliente ao canto superior esquerdo, retorne os \_ valores WVR ALIGNTOP e **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ ALIGNRIGHT**</dt> <dt>0x0080</dt> </dl>  | Especifica que a área do cliente da janela deve ser preservada e alinhada com o lado direito da nova posição da janela. Por exemplo, para alinhar a área do cliente ao canto inferior direito, retorne os valores **\_ ALIGNRIGHT WVR** e WVR \_ ALIGNBOTTOM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_ ALIGNLEFT**</dt> <dt>0x0020</dt> </dl>   | Especifica que a área do cliente da janela deve ser preservada e alinhada com o lado esquerdo da nova posição da janela. Por exemplo, para alinhar a área do cliente ao canto inferior esquerdo, retorne os valores **WVR \_ ALIGNLEFT** e **WVR \_ ALIGNBOTTOM** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_ ALIGNBOTTOM**</dt> <dt>0x0040</dt> </dl> | Especifica que a área do cliente da janela deve ser preservada e alinhada com a parte inferior da nova posição da janela. Por exemplo, para alinhar a área do cliente ao canto superior esquerdo, retorne os \_ valores ALIGNTOP WVR e **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_ HREDRAW**</dt> <dt>0x0100</dt> </dl>     | Usado em combinação com quaisquer outros valores, exceto **WVR \_ VALIDRECTS**, faz com que a janela seja completamente redesenhada se o retângulo do cliente mudar de tamanho horizontalmente. Esse valor é semelhante ao estilo de classe [cs \_ HREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_ VREDRAW**</dt> <dt>0x0200</dt> </dl>     | Usado em combinação com quaisquer outros valores, exceto **WVR \_ VALIDRECTS**, faz com que a janela seja completamente redesenhada se o retângulo do cliente muda de tamanho verticalmente. Esse valor é semelhante ao estilo de classe [cs \_ VREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_ Redesenhar**</dt> <dt>0x0300</dt> </dl>      | Esse valor faz com que toda a janela seja redesenhada. É uma combinação de valores **WVR \_ HREDRAW** e **WVR \_ VREDRAW** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_ VALIDRECTS**</dt> <dt>0x0400</dt> </dl>  | Esse valor indica que, ao retornar do [**WM \_ NCCALCSIZE**](wm-nccalcsize.md), os retângulos especificados pelos membros **rgrc** \[ 1 \] e **rgrc** \[ 2 \] da estrutura [**\_ params de NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) contêm retângulos de destino e área de origem válidos, respectivamente. O sistema combina esses retângulos para calcular a área da janela a ser preservada. O sistema copia qualquer parte da imagem da janela que está dentro do retângulo de origem e corta a imagem para o retângulo de destino. Ambos os retângulos estão em coordenadas de pai ou relativas à tela. Esse sinalizador não pode ser combinado com outros sinalizadores. <br/> Esse valor de retorno permite que um aplicativo implemente estratégias de preservação de área de cliente mais elaboradas, como centralizar ou preservar um subconjunto da área do cliente.<br/> |



 

## <a name="remarks"></a>Comentários

A janela pode ser redesenhada, dependendo se o estilo de classe [cs \_ HREDRAW](about-window-classes.md) ou cs \_ VREDRAW for especificado. Esse é o processamento padrão, compatível com versões anteriores dessa mensagem pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) (além do cálculo do retângulo do cliente usual, descrito na tabela anterior).

Quando *wParam* é **true**, simplesmente retornar 0 sem processar os retângulos de [**\_ params NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) fará com que a área do cliente seja redimensionada para o tamanho da janela, incluindo o quadro da janela. Isso removerá os itens de quadro e legenda da janela da janela, deixando apenas a área do cliente exibida.

Começando com o Windows Vista, remover o quadro padrão simplesmente retornando 0 quando *wParam* é **true** não afeta os quadros estendidos na área do cliente usando a função [**DwmExtendFrameIntoClientArea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Somente o quadro padrão será removido.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**parâmetros de NCCALCSIZE \_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
