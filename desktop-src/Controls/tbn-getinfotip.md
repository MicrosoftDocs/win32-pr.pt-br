---
title: TBN_GETINFOTIP código de notificação (commctrl. h)
description: Recupera informações de InfoTip para um item da barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009113"
---
# <a name="tbn_getinfotip-notification-code"></a>Código de notificação do TBN \_ GETINFOTIP

Recupera informações de InfoTip para um item da barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) que contém informações de item e recebe informações de InfoTip.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado pelo controle.

## <a name="remarks"></a>Comentários

O suporte de infotip na barra de ferramentas permite que a barra de ferramentas exiba dicas de ferramenta para itens que são tão grandes quanto INFOTIPSIZE caracteres. Se esse código de notificação não for processado, a barra de ferramentas usará o texto do item para o InfoTip.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **Tbn \_ GETINFOTIPW** (Unicode) e **tbn \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





