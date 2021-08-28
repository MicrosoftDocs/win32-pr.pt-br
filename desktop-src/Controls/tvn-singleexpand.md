---
title: TVN_SINGLEEXPAND de notificação (Commctrl.h)
description: Enviado por um controle de exibição de árvore com o estilo TVS SINGLEEXPAND quando o usuário abre ou fecha um item de árvore usando um único clique \_ do mouse. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61cd83dedbe16bad81c340f35a176b18804de6b7db6847fb65bc847160a2ff8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132196"
---
# <a name="tvn_singleexpand-notification-code"></a>Código de \_ notificação TVN SINGLEEXPAND

Enviado por um controle de exibição de árvore com o estilo [**TVS \_ SINGLEEXPAND**](tree-view-control-window-styles.md) quando o usuário abre ou fecha um item de árvore usando um único clique do mouse. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) que contém informações sobre esse código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar TVNRET \_ DEFAULT para permitir que o comportamento padrão ocorra. Para modificar o comportamento padrão, retorne:



| Código de retorno                                                                                    | Descrição                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**TVNRET \_ SKIPOLD**</dt> </dl> | Ignore o processamento padrão do item que está sendo deseletivo.<br/> |
| <dl> <dt>**TVNRET \_ SKIPNEW**</dt> </dl> | Ignore o processamento padrão do item que está sendo selecionado.<br/>   |



 

## <a name="remarks"></a>Comentários

Para ignorar o processamento padrão de itens selecionados e não selecionados, retorne TVNRET SKIPOLD e TVNRET SKIPNEW combinando-os \_ \_ com um OR lógico.

Esse código de notificação só é enviado por controles de exibição de árvore que têm o [**\_ estilo TVS SINGLEEXPAND.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





