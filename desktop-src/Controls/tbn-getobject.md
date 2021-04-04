---
title: TBN_GETOBJECT código de notificação (commctrl. h)
description: Enviado por um controle ToolBar que usa o \_ estilo TBSTYLE REGISTERDROP para solicitar um objeto de destino drop quando o ponteiro passa sobre um de seus botões. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085153"
---
# <a name="tbn_getobject-notification-code"></a>\_Código de notificação GETobject do tbn

Enviado por um controle ToolBar que usa o estilo [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) para solicitar um objeto de destino drop quando o ponteiro passa sobre um de seus botões. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contém informações sobre o botão passado pelo ponteiro e recebe dados que o aplicativo fornece em resposta a esse código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O aplicativo que processa esse código de notificação deve retornar zero.

## <a name="remarks"></a>Comentários

Para fornecer um objeto, um aplicativo deve definir valores em alguns membros da estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) em *lParam*. O membro **pObject** deve ser definido como um ponteiro de objeto válido e o membro **HRESULT** deve ser definido como um sinalizador de êxito. Para obedecer aos padrões de Component Object Model (COM), sempre aumente a contagem de referência do objeto ao fornecer um ponteiro de objeto.

Se um aplicativo não fornecer um objeto, ele deverá definir **pObject** como **nulo** e **HRESULT** como um sinalizador de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





