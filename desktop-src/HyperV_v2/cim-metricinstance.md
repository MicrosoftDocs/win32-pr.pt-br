---
description: Representa uma associação entre uma instância de um valor de métrica e uma definição de métrica.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: CIM_MetricInstance classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ff08757b8043e51d43079be6011b69731bdc761f22da27ff85272b95d4795c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695056"
---
# <a name="cim_metricinstance-class"></a>Classe \_ MetricInstance cim

Representa uma associação entre uma instância de um valor de métrica e uma definição de métrica.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe \_ MetricInstance cim** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ MetricInstance cim** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ BaseMetricDefinition do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

A definição do valor da métrica.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ BaseMetricValue**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

O valor de métrica associado à definição de métrica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

