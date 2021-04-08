---
description: O operador ISA é um operador específico de WQL que pode ser usado em consultas de eventos. Quando o ISA é incluído na cláusula WHERE de uma consulta de evento, ele solicita a notificação de eventos para todas as classes dentro de uma hierarquia de classe, em vez de uma classe de evento específica.
ms.assetid: 68b7a903-a206-4491-95c4-4a412537f6f5
ms.tgt_platform: multiple
title: Operador ISA para consultas de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acdd262492bfd876867bdfa7e13fd50e5380270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011441"
---
# <a name="isa-operator-for-event-queries"></a>Operador ISA para consultas de evento

O operador ISA é um operador específico de WQL que pode ser usado em consultas de eventos. Quando o ISA é incluído na [cláusula WHERE](where-clause.md) de uma consulta de evento, ele solicita a notificação de eventos para todas as classes dentro de uma hierarquia de classe, em vez de uma classe de evento específica.

O exemplo a seguir solicita notificação a cada 10 minutos de eventos de modificação de instância para todas as instâncias que são membros de qualquer classe derivada da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Para obter mais informações sobre como usar o ISA com uma consulta de evento, consulte [criando um evento de timer com Win32 \_ localtime ou Win32 \_ UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

 

 
