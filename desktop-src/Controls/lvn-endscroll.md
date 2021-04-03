---
title: Mensagem de LVN_ENDSCROLL (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem termina. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- Controles de LVN_ENDSCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824861"
---
# <a name="lvn_endscroll-message"></a>\_Mensagem de ENDrolagem do LVN

Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem termina. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contém a posição horizontal ou vertical de onde a operação de rolagem termina.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





