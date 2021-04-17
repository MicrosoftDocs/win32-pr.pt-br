---
title: TTN_LINKCLICK código de notificação (commctrl. h)
description: Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK de código de notificação controles do Windows
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
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753563"
---
# <a name="ttn_linkclick-notification-code"></a>Código de notificação do TTN \_ LINKCLICK

Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parâmetros

Este código de notificação não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

Veja a seguir um exemplo de quando essa notificação é enviada. Suponha que a dica de ferramenta de balão contenha o seguinte texto, "Este é um <A>link</A>". Quando o "link" é clicado, o controle ToolTip envia um \_ código de notificação TTN LINKCLICK.

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





