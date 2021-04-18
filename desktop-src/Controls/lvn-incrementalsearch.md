---
title: LVN_INCREMENTALSEARCH código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma pesquisa incremental foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750941"
---
# <a name="lvn_incrementalsearch-notification-code"></a>\_Código de notificação INCREMENTALSEARCH LVN

Notifica uma janela pai do controle de exibição de lista que uma pesquisa incremental foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que descreve o código de notificação. O chamador é responsável por alocar essa estrutura, incluindo as estruturas [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) e [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contidas. Defina os membros da estrutura **NMHDR** . O membro do **código** deve ser definido como \_ INCREMENTALSEARCH LVN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . O parâmetro *wParam* contém a ID do controle que envia este código de notificação.

Esse código de notificação fornece a um aplicativo (ou o receptor de notificação) a oportunidade de personalizar uma pesquisa incremental. Por exemplo, se os itens de pesquisa forem numéricos, o aplicativo poderá executar uma pesquisa numérica em vez de uma pesquisa de cadeia de caracteres.

O aplicativo define o membro **lParam** da estrutura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contida na estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) para o resultado da pesquisa ou para outro valor definido do aplicativo para reprovar a pesquisa e indicar ao controle como proceder.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl>   |
| Nomes Unicode e ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) e **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





