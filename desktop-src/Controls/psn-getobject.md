---
title: PSN_GETOBJECT de notificação (Prsht.h)
description: Enviado por uma folha de propriedades para solicitar um objeto de destino de soltar quando o cursor passa sobre um dos botões do controle de tabulação. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT código de notificação Windows Controles
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
ms.openlocfilehash: 6e81803a950c7b8eb9a41d31178c8f57d7e4199f802538616d4ced20c5a5cb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798626"
---
# <a name="psn_getobject-notification-code"></a>Código de \_ notificação GETOBJECT PSN

Enviado por uma folha de propriedades para solicitar um objeto de destino de soltar quando o cursor passa sobre um dos botões do controle de tabulação. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que, na entrada, contém informações sobre o código de notificação. Se esse código de notificação for processado, você deverá inserir informações de objeto nessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O aplicativo que está processando esse código de notificação deve retornar zero.

## <a name="remarks"></a>Comentários

Para fornecer um objeto , um aplicativo deve definir valores em alguns membros da estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) em *lParam*. O **membro pObject** deve ser definido como um ponteiro de objeto válido e o **membro hResult** deve ser definido como um sinalizador de êxito. Para atender aos Component Object Model (COM), sempre incremente a contagem de referência do objeto ao fornecer um ponteiro de objeto.

Se um aplicativo não fornecer um objeto, ele deverá definir **pObject** como **NULL** e **hResult** como um sinalizador de falha.

> [!Note]  
> Não há suporte para esse código de notificação ao usar o estilo do assistente do Aero [**(PSH \_ AEROWIZARD).**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





