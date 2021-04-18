---
description: A \_ \_ mensagem excluída do WM Tablet é postada quando um dispositivo tablet é removido do Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Mensagem de WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781156"
---
# <a name="wm_tablet_deleted-message"></a>\_ \_ Mensagem excluída do WM Tablet

A **mensagem \_ \_ excluída do WM Tablet** é postada quando um dispositivo tablet é removido do Windows.


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do dispositivo tablet que está sendo removido.

</dd> <dt>

*lParam* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é enviada para todas as janelas de nível superior no sistema, incluindo janelas desativas ou invisíveis, janelas e janelas pop-up sem proprietário. Mas a mensagem não é enviada para janelas filhas.

Os índices passados em *wParam* estão relacionados ao índice usado pelo método [**ITabletManager:: getTableName**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
