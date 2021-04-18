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
# <a name="isa-operator-for-schema-queries"></a><span data-ttu-id="e0f15-103">Operador ISA para consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="e0f15-103">ISA Operator for Schema Queries</span></span>

<span data-ttu-id="e0f15-104">O operador ISA é um operador específico de WQL que pode ser usado em consultas de dados, eventos e esquemas.</span><span class="sxs-lookup"><span data-stu-id="e0f15-104">The ISA operator is a WQL-specific operator that can be used in data, event, and schema queries.</span></span>

<span data-ttu-id="e0f15-105">Quando o ISA é incluído na [cláusula WHERE](where-clause.md) de uma consulta de esquema, ele solicita que a consulta seja aplicada a todas as subclasses da classe que você especificar.</span><span class="sxs-lookup"><span data-stu-id="e0f15-105">When ISA is included in the [WHERE clause](where-clause.md) of an schema query, it requests that the query be applied to all subclasses of the class you specify.</span></span>

<span data-ttu-id="e0f15-106">Por exemplo, a instrução a seguir solicita notificação a cada 10 minutos de eventos de modificação de instância para todas as instâncias que são membros de qualquer classe que deriva da classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="e0f15-106">For example, the following statement requests notification every 10 minutes of instance modification events for all instances that are members of any class deriving from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="e0f15-107">A consulta a seguir retorna a definição para a classe de [**\_ processador CIM**](/windows/desktop/CIMWin32Prov/cim-processor) e definições para todas as suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="e0f15-107">The following query returns the definition for the [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor) class and definitions for all of its subclasses.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



<span data-ttu-id="e0f15-108">A **\_ classe meta** Class identifica isso como uma consulta de esquema, a propriedade chamada **\_ \_ this** identifica a classe de destino da consulta e o operador ISA solicita definições para as subclasses da classe de destino.</span><span class="sxs-lookup"><span data-stu-id="e0f15-108">The class **meta\_class** identifies this as a schema query, the property called **\_\_this** identifies the target class of the query, and the ISA operator requests definitions for the subclasses of the target class.</span></span>

 

 
