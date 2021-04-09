---
title: PSN_QUERYINITIALFOCUS código de notificação (Prsht. h)
description: Enviado por uma folha de propriedades para fornecer uma página de folha de propriedades a oportunidade de especificar qual controle de caixa de diálogo deve receber o foco inicial. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS de código de notificação controles do Windows
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
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085210"
---
# <a name="psn_queryinitialfocus-notification-code"></a>Código de notificação do PSN \_ QUERYINITIALFOCUS

Enviado por uma folha de propriedades para fornecer uma página de folha de propriedades a oportunidade de especificar qual controle de caixa de diálogo deve receber o foco inicial. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) . Converta o membro **lParam** dessa estrutura em um tipo **HWND** para recuperar o identificador do controle que receberá o foco por padrão. A estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para especificar qual controle deve receber o foco, retorne o identificador do controle. Caso contrário, retornará zero e o foco vai para o controle padrão. Para definir o valor de retorno, o procedimento da caixa de diálogo deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com um valor de **\_ MSGRESULT DWL** e retornar **true**.

## <a name="remarks"></a>Comentários

Um aplicativo não deve chamar a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) ao manipular esse código de notificação. Retornar o identificador do controle que deve receber o foco e o gerente da folha de propriedades tratará da alteração de foco.

O \_ código de notificação PSN QUERYINITIALFOCUS não será enviado se o gerente da folha de propriedades determinar que nenhum controle na página deve receber o foco.

Este fragmento de código implementa um manipulador simples para PSN \_ QUERYINITIALFOCUS. Ele solicita que o foco inicial seja fornecido ao controle de local **( \_ localização da IDC**).

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Não há suporte para este código de notificação ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

