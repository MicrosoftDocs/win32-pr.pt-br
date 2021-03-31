---
title: Mensagem de TB_ADDBITMAP (commctrl. h)
description: Adiciona uma ou mais imagens à lista de imagens de botão disponíveis para uma barra de ferramentas.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- Controles de TB_ADDBITMAP de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645267"
---
# <a name="tb_addbitmap-message"></a>\_Mensagem de ADDBITMAP TB

Adiciona uma ou mais imagens à lista de imagens de botão disponíveis para uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de imagens de botão no bitmap. Se *lParam* especificar um bitmap definido pelo sistema, esse parâmetro será ignorado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) que contém o identificador de um recurso de bitmap e o identificador para a instância de módulo com o arquivo executável que contém o recurso de bitmap.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice da primeira nova imagem, se for bem-sucedido, ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Se a barra de ferramentas foi criada usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , você deve enviar a mensagem [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) para a barra de ferramentas antes de enviar **TB \_ AddBitmap**.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um bitmap de um recurso (IDB \_ Bitmap1), mapeia a cor do plano de fundo (preto, neste caso) para a cor de face do botão do sistema e o adiciona à barra de ferramentas.


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

