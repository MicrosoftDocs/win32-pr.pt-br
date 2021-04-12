---
title: TBN_WRAPHOTITEM código de notificação (commctrl. h)
description: Notifica um aplicativo com duas ou mais barras de ferramentas que o item ativo está prestes a alterar. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM de código de notificação controles do Windows
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
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455007"
---
# <a name="tbn_wraphotitem-notification-code"></a>Código de notificação do TBN \_ WRAPHOTITEM

Notifica um aplicativo com duas ou mais barras de ferramentas que o item ativo está prestes a alterar. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que contém o item quente antigo (**isniciar**) e se o novo item ativo está antes dele (**iDir** =-1) ou depois dele (**iDir** = 1), bem como um motivo pelo qual o item ativo está mudando.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True** se o aplicativo estiver lidando com a alteração de item quente; caso contrário, **false**.

## <a name="remarks"></a>Comentários

A estrutura **NMTBWRAPHOTITEM** deve ser definida pelo aplicativo da seguinte maneira:

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





