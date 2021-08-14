---
title: PSN_QUERYINITIALFOCUS de notificação (Prsht.h)
description: Enviado por uma folha de propriedades para fornecer a uma página de folha de propriedades uma oportunidade de especificar qual controle de caixa de diálogo deve receber o foco inicial. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS código de notificação Windows Controles
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc82fe11893e728fbc9301868d9acdca5f7110bedfd37b4a16b473de0821f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169636"
---
# <a name="psn_queryinitialfocus-notification-code"></a>Código de \_ notificação PSN QUERYINITIALFOCUS

Enviado por uma folha de propriedades para fornecer a uma página de folha de propriedades uma oportunidade de especificar qual controle de caixa de diálogo deve receber o foco inicial. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura PSHNOTIFY.**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) Caste **o membro lParam** dessa estrutura para um tipo **HWND** para recuperar o identificador do controle que receberá o foco por padrão. A estrutura contém uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **hdr**. O **membro hwndFrom** dessa estrutura **NMHDR** contém o handle para a folha de propriedades.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para especificar qual controle deve receber o foco, retorne o alça do controle. Caso contrário, retorne zero e o foco irá para o controle padrão. Para definir o valor de retorno, o procedimento da caixa de diálogo deve chamar a [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com um **valor \_ MSGRESULT do DWL** e retornar **TRUE.**

## <a name="remarks"></a>Comentários

Um aplicativo não deve chamar a [**função SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) ao manipular esse código de notificação. Retorne o controle que deve receber o foco e o gerenciador de folha de propriedades manipulará a alteração de foco.

O código de notificação PSN QUERYINITIALFOCUS não será enviado se o gerenciador de planilhas de propriedades determinar que nenhum controle na \_ página deve receber foco.

Esse fragmento de código implementa um manipulador simples para PSN \_ QUERYINITIALFOCUS. Ele solicita que o foco inicial seja dado ao controle Local (**IDC \_ LOCATION).**

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Não há suporte para esse código de notificação ao usar o estilo do assistente do Aero [**(PSH \_ AEROWIZARD).**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

