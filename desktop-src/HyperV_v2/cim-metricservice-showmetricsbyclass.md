---
description: 'Relata o seguinte: as métricas disponíveis para serem coletadas para todas as instâncias de uma classe CIM, as classes CIM para as quais uma métrica definida por uma instância do CIM \_ BaseMetricDefinition está disponível para ser coletada e se uma métrica específica está sendo coletada ou não para um elemento gerenciado.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Método ShowMetricsByClass da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828600"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>Método ShowMetricsByClass da \_ classe METRICSERVICE CIM

Relata o seguinte: as métricas disponíveis para serem coletadas para todas as instâncias de uma classe CIM, as classes CIM para as quais uma métrica definida por uma instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) está disponível para ser coletada e se uma métrica específica está sendo coletada ou não para um elemento gerenciado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Assunto* \[ no\]
</dt> <dd>

Identifica uma classe CIM para a qual o método retorna referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem métricas que estão disponíveis para serem capturadas para todas as instâncias da classe.

</dd> <dt>

*Definição* \[ do no\]
</dt> <dd>

Identifica uma instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md). O método retorna referências a instâncias de [**CIM \_ managedelement**](cim-managedelement.md) para as quais as métricas definidas pela instância do **CIM \_ BaseMetricDefinition** estão disponíveis para serem coletadas.

</dd> <dt>

*Definitionlist* \[ fora\]
</dt> <dd>

Em caso de sucesso, pode conter referências a instâncias de objetos [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) que definem métricas disponíveis para coleta para o [**CIM \_ managedelement**](cim-managedelement.md) identificado pelo parâmetro *Subject* .

</dd> <dt>

*Métricas* \[ fora\]
</dt> <dd>

Em caso de sucesso, cada índice de matriz deve conter o valor da propriedade **Name** para a instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *definitionlist* .

</dd> <dt>

*MetricCollectionEnabled* \[ fora\]
</dt> <dd>

Indica se uma métrica está sendo coletada para todas as instâncias de uma classe de elementos gerenciados.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (3)


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

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

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

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 




