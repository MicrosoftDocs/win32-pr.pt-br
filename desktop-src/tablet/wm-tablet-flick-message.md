---
description: Enviado quando um usuário executa um movimento de caneta. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Mensagem de WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb01fce646d2e7c6cb4e1b25c2f49f0c4dde5258ba2167e117a23eff22a5d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842767"
---
# <a name="wm_tablet_flick-message"></a>Mensagem de movimento do \_ Tablet do WM \_

Enviado quando um usuário executa um movimento de caneta. Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uma [**\_ estrutura de dados de movimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) que contém informações sobre o movimento de caneta que ocorreu.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**\_ estrutura do ponto de movimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) que especifica onde ocorreu o movimento da caneta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um movimento de caneta é um gesto de caneta unidirecional que exige que o usuário contate o digitalizador em um movimento de movimentos rápido e reto. Um movimento é caracterizado por alta velocidade e um alto grau de reta. Um movimento é identificado pela sua direção. Os movimentos podem ser feitos em oito direções correspondentes às direções cardeal e secundária Compass.

quando ocorre um movimento de caneta, Windows primeiro notifica um aplicativo enviando uma mensagem **de \_ \_ movimento de TABLET do WM** , que uma janela recebe por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Retorne a constante de **movimento \_ \_ manipulada \_ pelo WM** , descrita em constantes de [movimentos](flicks-constants.md), para indicar que o aplicativo respondeu à mensagem de **\_ \_ movimento de Tablet do WM** . se o aplicativo não retornar a **\_ \_ \_ máscara manipulada do WM de movimento**, Windows executará a ação padrão especificada no painel de controle de movimentos enviando uma notificação de acompanhamento, como o [**wm \_ APPCOMMAND**](../inputdev/wm-appcommand.md), o [**wm \_ VSCROLL**](../controls/wm-vscroll.md)ou o [**wm \_ KEYDOWN**](../inputdev/wm-keydown.md), dependendo da ação associada ao movimento da caneta.

Tenha cuidado ao manipular a mensagem de **\_ \_ Tablet do WM** . **WM \_ O \_ movimento do Tablet** é passado por meio da função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Se você chamar métodos em uma interface COM, esse objeto deverá estar dentro do mesmo processo. Caso contrário, COM gera uma exceção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**mover \_ estrutura de dados**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**mensagem de movimento do \_ Tablet do WM \_**](wm-tablet-flick-message.md)
</dt> <dt>

[gestos de movimentos](flicks-gestures.md)
</dt> <dt>

[respondendo a movimentos de caneta](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
