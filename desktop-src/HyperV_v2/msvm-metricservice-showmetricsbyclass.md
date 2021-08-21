---
description: Mostra as métricas por classe.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Método ShowMetricsByClass da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 40865847b1deef877c70c1c99349c12915a464b394a38b5b804ea9139d5d0cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147505"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Método ShowMetricsByClass da \_ classe MetricService Msvm

Mostra as métricas por classe.

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

Após a conclusão bem-sucedida do método, o pode conter referências a instâncias [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que definem as métricas disponíveis para coleta para o [**CIM \_ managedelement**](cim-managedelement.md) identificado pelo parâmetro *Subject* .

</dd> <dt>

*Métricas* \[ fora\]
</dt> <dd>

Após a conclusão bem-sucedida do método, cada índice de matriz contém o valor da propriedade **Name** para a instância do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *definitionlist* .

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

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

<dl> <dt>

**Êxito** ()
</dt> <dt>

**Sem suporte** ()
</dt> <dt>

**Falha** ()
</dt> <dt>

**Método reservado** ()
</dt> <dt>

**Específico do fornecedor** ()
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

 

 




