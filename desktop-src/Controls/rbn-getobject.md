---
title: RBN_GETOBJECT código de notificação (commctrl. h)
description: Enviado por um controle rebar criado com o \_ estilo RBS REGISTERDROP quando um objeto é arrastado sobre uma banda no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT código de notificação Windows controles
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9709313a16d068e44b847f5e0862adf1e133b9f0ea92136a12e9aae24ffb14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985036"
---
# <a name="rbn_getobject-notification-code"></a>\_Código de notificação GETobject do RBN

Enviado por um controle rebar criado com o estilo [**RBS \_ REGISTERDROP**](rebar-control-styles.md) quando um objeto é arrastado sobre uma banda no controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contém informações sobre a faixa em que o objeto é arrastado e também recebe os dados fornecidos pelo aplicativo de recebimento em resposta a esse código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para este código de notificação deve ser zero.

## <a name="remarks"></a>Comentários

Para receber o \_ código de notificação GetObject do RBN, inicialize o OLE com uma chamada para [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ou [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

