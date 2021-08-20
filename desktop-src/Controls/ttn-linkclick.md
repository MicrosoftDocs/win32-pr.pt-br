---
title: TTN_LINKCLICK de notificação (Commctrl.h)
description: Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a31b1f942627ee22fb050bbddd0b74ac10dd09a7a8f14018189620f6c8155f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166092"
---
# <a name="ttn_linkclick-notification-code"></a>Código de notificação \_ TTN LINKCLICK

Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parâmetros

Esse código de notificação não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

Veja a seguir um exemplo de quando essa notificação é enviada. Suponha que sua dica de ferramenta de balão contenha o seguinte texto, "Este é um <A>link".</A> Quando o "link" é clicado, o controle de dica de ferramenta envia um código de notificação TTN \_ LINKCLICK.

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





