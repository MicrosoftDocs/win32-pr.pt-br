---
description: Mostra as métricas especificadas.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Método de permétricas da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837133"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Método de permétricas da \_ classe Msvm MetricService

Mostra as métricas especificadas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Assunto* \[ no\]
</dt> <dd>

O parâmetro Subject identifica uma instância de [**CIM \_ managedelement**](cim-managedelement.md) para a qual o método retorna referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem as métricas que estão sendo capturadas para o **CIM \_ managedelement**.

</dd> <dt>

*Definição* \[ do no\]
</dt> <dd>

O parâmetro de definição identifica uma instância [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md). O método retorna referências a instâncias de [**CIM \_ managedelement**](cim-managedelement.md) para as quais as métricas definidas pela instância do **CIM \_ BaseMetricDefinition** estão disponíveis para serem coletadas.

</dd> <dt>

*ManagedElements* \[ fora\]
</dt> <dd>

Após a conclusão bem-sucedida do método, o  \[ \] parâmetro ManagedElements pode conter referências ao [**CIM \_ managedelement**](cim-managedelement.md) para o qual a métrica identificada pelo parâmetro de *definição* está disponível para coleta.

</dd> <dt>

*Definitionlist* \[ fora\]
</dt> <dd>

Após a conclusão bem-sucedida do método, o parâmetro *definitionlist* pode conter referências a instâncias de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem as métricas disponíveis para a coleção para o [**CIM \_ managedelement**](cim-managedelement.md) identificado pelo parâmetro *Subject* .

</dd> <dt>

*Métricas* \[ fora\]
</dt> <dd>

Após a conclusão bem-sucedida do método, cada índice de matriz do parâmetro *metricnames* deverá conter o valor da propriedade Name para a instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *definitionlist* .

</dd> <dt>

*MetricCollectionEnabled* \[ fora\]
</dt> <dd>

O parâmetro *MetricCollectionEnabled* indica se uma métrica está sendo coletada para um elemento gerenciado.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Habilitar** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Desabilitar** (3)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Método reservado** (..)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




