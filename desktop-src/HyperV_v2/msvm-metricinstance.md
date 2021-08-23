---
description: Representa uma associação de objetos de valor de métrica com suas definições de métricas.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance classe
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
ms.openlocfilehash: 18a15ff6479caa690a8645e89d9b68f4a15f523bd7cee56fedb6957e20373214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521536"
---
# <a name="msvm_metricinstance-class"></a>Classe Msvm \_ MetricInstance

Representa uma associação de objetos de valor de métrica com suas definições de métricas. Essa associação vincula uma instância de [**Msvm \_ BaseMetricValue a**](msvm-basemetricvalue.md) [**seu Msvm \_ BaseMetricDefinition.**](msvm-basemetricdefinition.md)

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe Msvm \_ MetricInstance** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ MetricInstance** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: ****Cim \_ ManagedElement****
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que representa as definições de métricas.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: ****Cim \_ ManagedElement****
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) que representa as métricas que dependem do **Antecessor.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




