---
title: TBN_WRAPACCELERATOR código de notificação (commctrl. h)
description: Solicita o índice do botão em uma ou mais barras de ferramentas correspondentes ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR de código de notificação controles do Windows
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
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748252"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>Código de notificação do TBN \_ WRAPACCELERATOR

Solicita o índice do botão em uma ou mais barras de ferramentas correspondentes ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que contém o caractere de tecla acelerador e que recebe o índice do botão correspondente. O índice será-1 se o acelerador não corresponder a um comando.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True** se um índice for retornado, caso contrário, **false**.

## <a name="remarks"></a>Comentários

Aplicativos com uma ou mais barras de ferramentas podem receber esse código de notificação.

A estrutura **NMTBWRAPACCELERATOR** deve ser definida pelo aplicativo da seguinte maneira:

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





