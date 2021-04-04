---
title: TBN_MAPACCELERATOR código de notificação (commctrl. h)
description: Solicita o índice do botão na barra de ferramentas correspondente ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917980"
---
# <a name="tbn_mapaccelerator-notification-code"></a>Código de notificação do TBN \_ MAPACCELERATOR

Solicita o índice do botão na barra de ferramentas correspondente ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém o caractere de tecla acelerador e que recebe o índice do botão correspondente. O campo **dwItemNext** será-1 se o acelerador não corresponder a um comando.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

TRUE se **NMCHAR. dwItemNext** for definido como um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





