---
description: O operador ISA é um operador específico de WQL que pode ser usado em consultas de dados, eventos e esquemas.
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: Operador ISA para consultas de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb50146e4bd1219712c84bc1acec7fc7d50146b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792587"
---
# <a name="isa-operator-for-schema-queries"></a>Operador ISA para consultas de esquema

O operador ISA é um operador específico de WQL que pode ser usado em consultas de dados, eventos e esquemas.

Quando o ISA é incluído na [cláusula WHERE](where-clause.md) de uma consulta de esquema, ele solicita que a consulta seja aplicada a todas as subclasses da classe que você especificar.

Por exemplo, a instrução a seguir solicita notificação a cada 10 minutos de eventos de modificação de instância para todas as instâncias que são membros de qualquer classe que deriva da classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



A consulta a seguir retorna a definição para a classe de [**\_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor) e definições para todas as suas subclasses.


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



A **\_ classe meta** Class identifica isso como uma consulta de esquema, a propriedade chamada **\_ \_ this** identifica a classe de destino da consulta e o operador ISA solicita definições para as subclasses da classe de destino.

 

 
