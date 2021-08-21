---
title: TBN_DUPACCELERATOR código de notificação (commctrl. h)
description: Asseguro se uma tecla aceleradora pode ser usada em duas ou mais barras de ferramentas ativas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR código de notificação Windows controles
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ff0059a6071db79cab91fcf903a1e68f3550c766b3d16cd3571c3a785e7368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829320"
---
# <a name="tbn_dupaccelerator-notification-code"></a>Código de notificação do TBN \_ DUPACCELERATOR

Asseguro se uma tecla aceleradora pode ser usada em duas ou mais barras de ferramentas ativas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que fornece um acelerador e que recebe um valor que especifica se várias barras de ferramentas respondem ao mesmo caractere.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido; caso contrário, **false**.

## <a name="remarks"></a>Comentários

O aplicativo deve declarar a estrutura **NMTBDUPACCELERATOR** da seguinte maneira:

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





