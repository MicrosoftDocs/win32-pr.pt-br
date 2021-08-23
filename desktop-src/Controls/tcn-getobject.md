---
title: TCN_GETOBJECT de notificação (Commctrl.h)
description: Enviado por um controle de tabulação quando ele tem o estilo estendido TCS EX REGISTERDROP e um objeto é arrastado sobre um \_ item de guia no controle \_ . Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT de notificação Windows controles
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf5ec3a314a7380ccff5f8613145c890f8f304d73289ad5354b8668a09070b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166899"
---
# <a name="tcn_getobject-notification-code"></a>Código de \_ notificação TCN GETOBJECT

Enviado por um controle de tabulação quando ele tem o estilo [**estendido TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) e um objeto é arrastado sobre um item de guia no controle . Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contém informações sobre o item de guia pelo qual o objeto é arrastado e recebe dados que o aplicativo retorna em resposta a essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O aplicativo que está processando esse código de notificação deve retornar zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





