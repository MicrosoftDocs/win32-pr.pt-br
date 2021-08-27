---
title: Mensagem de WM_MEASUREITEM (WinUser. h)
description: Enviado para a janela do proprietário de uma caixa de combinação, caixa de listagem, controle de exibição de lista ou item de menu quando o controle ou o menu é criado.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- controles de Windows de mensagem de WM_MEASUREITEM
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eae57fc163f19edcef6dc924072cd3389146b66e614b61d6f121237e82e1344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957505"
---
# <a name="wm_measureitem-message"></a>Mensagem do WM \_ MEASUREITEM

Enviado para a janela do proprietário de uma caixa de combinação, caixa de listagem, controle de exibição de lista ou item de menu quando o controle ou o menu é criado.

Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém o valor do membro **CtlID** da estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lParam* . Esse valor identifica o controle que enviou a mensagem de **\_ MEASUREITEM do WM** . Se o valor for zero, a mensagem foi enviada por um menu. Se o valor for diferente de zero, a mensagem foi enviada por uma caixa de combinação ou por uma caixa de listagem. Se o valor for diferente de zero e o valor do membro **ItemId** do **MEASUREITEMSTRUCT** apontado por *lParam* for (UINT) 1, a mensagem foi enviada por um campo de edição de combinação.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contém as dimensões do controle ou item de menu desenhado pelo proprietário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar **true**.

## <a name="remarks"></a>Comentários

Quando a janela do proprietário recebe a mensagem **\_ MEASUREITEM do WM** , o proprietário preenche a estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lParam* da mensagem e retorna; isso informa o sistema das dimensões do controle. Se uma caixa de listagem ou caixa de combinação for criada com o estilo [**de \_ OwnerDrawVariable**](combo-box-styles.md) [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ou CBS, essa mensagem será enviada ao proprietário de cada item no controle; caso contrário, essa mensagem será enviada uma vez.

O sistema envia a mensagem do **WM \_ MEASUREITEM** para a janela do proprietário de caixas de combinação e caixas de listagem criadas com o estilo OwnerDrawFixed antes de enviar a mensagem [**\_ INITDIALOG do WM**](/windows/desktop/dlgbox/wm-initdialog) . Como resultado, quando o proprietário recebe essa mensagem, o sistema ainda não determinou a altura e a largura da fonte usada no controle; as chamadas de função e os cálculos que exigem esses valores devem ocorrer na função principal do aplicativo ou da biblioteca.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**INITDIALOG do WM \_**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

