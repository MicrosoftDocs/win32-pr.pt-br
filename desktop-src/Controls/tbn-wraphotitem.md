---
title: TBN_WRAPHOTITEM de notificação (Commctrl.h)
description: Notifica um aplicativo com duas ou mais barras de ferramentas que o item quente está prestes a ser alterado. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c6bd1f2e750a2fd71dc053d31ca452fa581891037db73d356e5405476b28de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293356"
---
# <a name="tbn_wraphotitem-notification-code"></a>Código de \_ notificação TBN WRAPHOTITEM

Notifica um aplicativo com duas ou mais barras de ferramentas que o item quente está prestes a ser alterado. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que contém o item quente antigo (**iStart**) e se o novo item quente está antes dele (**iDir** = -1) ou depois dele (**iDir** = 1), bem como um motivo pelo qual o item quente está mudando.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**TRUE** se o aplicativo estiver tratando a própria alteração de item quente; caso **contrário, FALSE.**

## <a name="remarks"></a>Comentários

A **estrutura NMTBWRAPHOTITEM** deve ser definida pelo aplicativo da seguinte forma:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





