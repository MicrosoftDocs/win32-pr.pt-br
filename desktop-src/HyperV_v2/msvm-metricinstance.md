---
description: Representa uma associação de objetos de valor de métrica com suas definições de métricas.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Classe Msvm_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759403"
---
# <a name="msvm_metricinstance-class"></a>\_Classe Msvm MetricInstance

Representa uma associação de objetos de valor de métrica com suas definições de métricas. Essa associação vincula uma instância de [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) ao seu [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md).

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ MetricInstance** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ MetricInstance** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: * * * * CIM \_ managedelement * * * *
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que representa as definições de métricas.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: * * * * CIM \_ managedelement * * * *
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) que representa as métricas que dependem do **Antecedent**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




