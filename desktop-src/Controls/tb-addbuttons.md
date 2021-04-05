---
title: Mensagem de TB_ADDBUTTONS (commctrl. h)
description: Adiciona um ou mais botões a uma barra de ferramentas.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- Controles de TB_ADDBUTTONS de mensagens do Windows
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
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919235"
---
# <a name="tb_addbuttons-message"></a>\_Mensagem de HIPERbotãos TB

Adiciona um ou mais botões a uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de botões a serem adicionados.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de estruturas [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contêm informações sobre os botões a serem adicionados. Deve haver o mesmo número de elementos na matriz como botões especificados por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se a barra de ferramentas foi criada usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , você deve enviar a mensagem [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) para a barra de ferramentas antes de enviar os **\_ botões addbotãors**.

Consulte [**TB \_ SetImageList**](tb-setimagelist.md) para obter uma discussão sobre como atribuir bitmaps a botões da barra de ferramentas de uma ou mais listas de imagens.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir adiciona três botões a uma barra de ferramentas, usando o bitmap do sistema padrão para botões de exibição. A mensagem do [**\_ AddBitmap TB**](tb-addbitmap.md) retorna o índice da primeira imagem de botão na lista de imagens. As imagens individuais são identificadas por seus deslocamentos a partir desse valor.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ ADDBUTTONSW** (Unicode) e **TB \_ AddButtons** (ANSI)<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Valores de índice da imagem do botão padrão da barra de ferramentas**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

