---
title: TBN_MAPACCELERATOR de notificação (Commctrl.h)
description: Solicita o índice do botão na barra de ferramentas correspondente ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR código de notificação Windows Controles
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
ms.openlocfilehash: 488c78ff00b75c42f6646e314c75d63445c7400eb9130464b126e75bcf2df942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434186"
---
# <a name="tbn_mapaccelerator-notification-code"></a>Código de \_ notificação TBN MAPACCELERATOR

Solicita o índice do botão na barra de ferramentas correspondente ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém o caractere de chave do acelerador e que recebe o índice do botão correspondente. O **campo dwItemNext** será -1 se o acelerador não corresponder a um comando.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

TRUE se **NMCHAR.dwItemNext** estiver definido como um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





