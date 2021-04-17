---
description: A mensagem do WM \_ Tablet \_ adicionado é postada quando um dispositivo de Tablet é adicionado ao Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Mensagem de WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811451"
---
# <a name="wm_tablet_added-message"></a>Mensagem do WM \_ Tablet \_ adicionado

A mensagem do **WM \_ Tablet \_ adicionado** é postada quando um dispositivo de Tablet é adicionado ao Windows.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do dispositivo do Tablet que está sendo adicionado

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



 

 
