---
title: LVN_INCREMENTALSEARCH de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista de que uma pesquisa incremental foi iniciada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH código de notificação Windows Controles
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
ms.openlocfilehash: 0ec3207fbb16bca23bf44ac61fee58bb6e4fad1ff74c38d7b56910ed52997f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826116"
---
# <a name="lvn_incrementalsearch-notification-code"></a>Código de notificação LVN \_ INCREMENTALSEARCH

Notifica a janela pai de um controle de exibição de lista de que uma pesquisa incremental foi iniciada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* \[ Em\]
</dt> <dd>

Ponteiro para uma [**estrutura NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que descreve o código de notificação. O chamador é responsável por alocar essa estrutura, incluindo as estruturas [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) e [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contidas. Definir os membros da estrutura **NMHDR.** O **membro** de código deve ser definido como LVN \_ INCREMENTALSEARCH.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação *lança lParam* para recuperar a [**estrutura NMLVFINDITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) O *parâmetro wParam* contém a ID do controle que envia esse código de notificação.

Esse código de notificação oferece a um aplicativo (ou ao receptor de notificação) a oportunidade de personalizar uma pesquisa incremental. Por exemplo, se os itens de pesquisa são numéricos, o aplicativo pode executar uma pesquisa numérica em vez de uma pesquisa de cadeia de caracteres.

O aplicativo define o membro **lParam** da estrutura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contida na estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) para o resultado da pesquisa ou para outro valor definido pelo aplicativo para falhar na pesquisa e indicar ao controle como continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl>   |
| Nomes Unicode e ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) e **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





