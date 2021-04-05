---
title: PSN_GETOBJECT código de notificação (Prsht. h)
description: Enviado por uma folha de propriedades para solicitar um objeto de destino de soltar quando o cursor passa sobre um dos botões do controle de guia. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009072"
---
# <a name="psn_getobject-notification-code"></a>\_Código de notificação GETobject do PSN

Enviado por uma folha de propriedades para solicitar um objeto de destino de soltar quando o cursor passa sobre um dos botões do controle de guia. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que, na entrada, contém informações sobre o código de notificação. Se esse código de notificação for processado, você deverá inserir informações de objeto nessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O aplicativo que processa esse código de notificação deve retornar zero.

## <a name="remarks"></a>Comentários

Para fornecer um objeto, um aplicativo deve definir valores em alguns membros da estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) em *lParam*. O membro **pObject** deve ser definido como um ponteiro de objeto válido e o membro **HRESULT** deve ser definido como um sinalizador de êxito. Para obedecer aos padrões de Component Object Model (COM), sempre aumente a contagem de referência do objeto ao fornecer um ponteiro de objeto.

Se um aplicativo não fornecer um objeto, ele deverá definir **pObject** como **nulo** e **HRESULT** como um sinalizador de falha.

> [!Note]  
> Não há suporte para este código de notificação ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





