---
title: WM_NCPOINTERUPDATE mensagem
description: Postado para fornecer uma atualização em um ponteiro que fez contato sobre a área não cliente de uma janela ou quando um contato sem controle de foco se move sobre a área não cliente de uma janela.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUPDATE mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6f1cf786af00175f75b5faee11b384aa31618d89427826f9c1454006df461f0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062416"
---
# <a name="wm_ncpointerupdate-message"></a>WM_NCPOINTERUPDATE mensagem

Postado para fornecer uma atualização em um ponteiro que fez contato sobre a área não cliente de uma janela ou quando um contato sem controle de foco se move sobre a área não cliente de uma janela. Enquanto o ponteiro está passeando, a mensagem tem como alvo qualquer janela em que o ponteiro está acima. Enquanto o ponteiro está em contato com a superfície, o ponteiro é implicitamente capturado para a janela sobre a qual o ponteiro fez contato e essa janela continua recebendo entrada para o ponteiro até que ele interrompe o contato.

Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, [**WM_POINTERUPDATE**](wm-pointerupdate.md) é postado na janela que capturou esse ponteiro.

> \[! Importante\]  
> Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém o identificador de ponteiro e informações adicionais. Use as macros a seguir para recuperar essas informações.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de ponteiro

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de teste de acerto retornado do processamento da [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Contém o local do ponto do ponteiro.

> [!Note]  
> Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa. Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.

 

Use as macros a seguir para recuperar as coordenadas de tela física do ponto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada x (ponto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada y (ponto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

Se o aplicativo não processar essa mensagem, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá executar uma ou mais ações do sistema, dependendo do resultado do teste de acerto incluído na mensagem. Normalmente, os aplicativos não devem precisar lidar com essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

