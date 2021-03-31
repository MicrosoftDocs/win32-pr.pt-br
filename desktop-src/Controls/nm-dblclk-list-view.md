---
title: Código de notificação de NM_DBLCLK (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário clica duas vezes em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- NM_DBLCLK de código de notificação (exibição de lista) controles do Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add6af24b4272631be7c2be387a7ffda899469b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824162"
---
# <a name="nm_dblclk-list-view-notification-code"></a>\_Código de notificação nm DBLCLK (exibição de lista)

Enviado por um controle de exibição de lista quando o usuário clica duas vezes em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_DBLCLK
        
    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versão 4,71](common-control-versions.md). Ponteiro para uma estrutura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações adicionais sobre esta notificação. Os membros **iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

O membro **iItem** de *lParam* só será válido se o ícone ou rótulo de primeira coluna tiver sido clicado. Para determinar qual item é selecionado quando um clique ocorre em outro lugar em uma linha, envie uma mensagem [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





