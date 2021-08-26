---
title: TBN_WRAPACCELERATOR de notificação (Commctrl.h)
description: Solicita o índice do botão em uma ou mais barras de ferramentas correspondentes ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR de notificação Windows Controles
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c5ec222f387108e2cb4d240e6dddf0fcb904d814097a96624a177425eb805ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105026"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>Código de \_ notificação TBN WRAPACCELERATOR

Solicita o índice do botão em uma ou mais barras de ferramentas correspondentes ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que contém o caractere de chave do acelerador e que recebe o índice do botão correspondente. O índice será -1 se o acelerador não corresponder a um comando.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**TRUE** se um índice for retornado, caso **contrário, FALSE.**

## <a name="remarks"></a>Comentários

Aplicativos com uma ou mais barras de ferramentas podem receber esse código de notificação.

A **estrutura NMTBWRAPACCELERATOR** deve ser definida pelo aplicativo da seguinte forma:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





