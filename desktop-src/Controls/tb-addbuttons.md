---
title: TB_ADDBUTTONS mensagem (Commctrl.h)
description: Adiciona um ou mais botões a uma barra de ferramentas.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd3a5a15ac1983d93ca161dae20876159e5f633cf580d485686d67889276747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168519"
---
# <a name="tb_addbuttons-message"></a>Mensagem \_ ADDBUTTONS de TB

Adiciona um ou mais botões a uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de botões a adicionar.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de [**estruturas TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contêm informações sobre os botões a adicionar. Deve haver o mesmo número de elementos na matriz que os botões especificados por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Se a barra de ferramentas tiver sido criada usando a função [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) você deverá enviar a mensagem [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) para a barra de ferramentas antes de **enviar TB \_ ADDBUTTONS**.

Consulte [**TB \_ SETIMAGELIST para**](tb-setimagelist.md) obter uma discussão sobre como atribuir bitmaps a botões de barra de ferramentas de uma ou mais listas de imagens.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir adiciona três botões a uma barra de ferramentas, usando o bitmap do sistema padrão para botões de exibição. A [**mensagem \_ ADDBITMAP de TB**](tb-addbitmap.md) retorna o índice da primeira imagem de botão dentro da lista de imagens. Imagens individuais são identificadas por seus deslocamentos desse valor.


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ ADDBUTTONSW** (Unicode) e **TB \_ ADDBUTTONSA** (ANSI)<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Valores de índice de imagem de botão padrão da barra de ferramentas**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

