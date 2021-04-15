---
title: TVN_SINGLEEXPAND código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore com o \_ estilo de TVs SINGLEEXPAND quando o usuário abre ou fecha um item de árvore usando um único clique do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND de código de notificação controles do Windows
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
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454822"
---
# <a name="tvn_singleexpand-notification-code"></a>Código de notificação do TVN \_ SINGLEEXPAND

Enviado por um controle de exibição de árvore com o estilo de [**TVs \_ SINGLEEXPAND**](tree-view-control-window-styles.md) quando o usuário abre ou fecha um item de árvore usando um único clique do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) que contém informações sobre este código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne \_ o padrão TVNRET para permitir que o comportamento padrão ocorra. Para modificar o comportamento padrão, retorne:



| Código de retorno                                                                                    | Descrição                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**TVNRET \_ SKIPOLD**</dt> </dl> | Ignorar o processamento padrão do item que está sendo desmarcado.<br/> |
| <dl> <dt>**TVNRET \_ SKIPNEW**</dt> </dl> | Ignorar o processamento padrão do item que está sendo selecionado.<br/>   |



 

## <a name="remarks"></a>Comentários

Para ignorar o processamento padrão de itens selecionados e não selecionados, retorne TVNRET \_ SKIPOLD e TVNRET \_ SKIPNEW combinando-os com um OR lógico.

Esse código de notificação é enviado somente por controles de exibição de árvore que têm o estilo [**\_ SINGLEEXPAND de TVs**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





