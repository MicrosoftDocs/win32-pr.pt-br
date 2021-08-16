---
title: CBEN_DRAGBEGIN de notificação (Commctrl.h)
description: Enviado quando o usuário começa a arrastar a imagem do item exibido na parte de edição do controle. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN de notificação Windows Controles
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626ad4d6abbcaaeb6f647aa94657ee1a681801a3ce13a9b5539216b1b67565a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414056"
---
# <a name="cben_dragbegin-notification-code"></a>Código de \_ notificação CBEN DRAGBEGIN

Enviado quando o usuário começa a arrastar a imagem do item exibido na parte de edição do controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Se o aplicativo receptor implementar a funcionalidade do tipo "arrastar e soltar" do controle , o aplicativo iniciará a operação do tipo "arrastar e soltar" em resposta a esse código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CBEN \_ DRAGBEGINW** (Unicode) e **CBEN \_ DRAGBEGINA** (ANSI)<br/>             |



 

 





