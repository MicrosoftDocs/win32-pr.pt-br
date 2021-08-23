---
description: Mostra as métricas especificadas.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Método ShowMetrics da Msvm_MetricService classe
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
ms.openlocfilehash: 052f708f07a8e1074eeaa6c8089ccd410bb63af478072545d5db92af7933fc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521465"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Método ShowMetrics da classe Msvm \_ MetricService

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

*Assunto* \[ Em\]
</dt> <dd>

O parâmetro Subject identifica uma instância do [**\_ ManagedElement CIM**](cim-managedelement.md) para a qual o método retorna referências a instâncias do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) que definem as métricas que estão sendo capturadas para o **\_ ManagedElement do CIM.**

</dd> <dt>

*Definição* \[ Em\]
</dt> <dd>

O parâmetro Definition identifica uma instância de [**\_ BASEMetricDefinition do CIM.**](cim-basemetricdefinition.md) O método retorna referências a instâncias do [**\_ ManagedElement cim**](cim-managedelement.md) para as quais as métricas definidas pela instância do **CIM \_ BaseMetricDefinition** estão disponíveis para serem coletadas.

</dd> <dt>

*ManagedElements* \[ out\]
</dt> <dd>

Após a conclusão bem-sucedida do método, o parâmetro *ManagedElements* pode conter referências ao \[ \] [**\_ ManagedElement cim**](cim-managedelement.md) para o qual a métrica identificada pelo parâmetro *Definition* está disponível para coleta.

</dd> <dt>

*DefinitionList* \[ out\]
</dt> <dd>

Após a conclusão bem-sucedida do método, o parâmetro *DefinitionList* pode conter referências a instâncias do [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) que definem as métricas disponíveis para a coleção para o [**\_ ManagedElement CIM**](cim-managedelement.md) identificado pelo parâmetro *Subject.*

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Após a conclusão bem-sucedida do método, cada índice de matriz do parâmetro *MetricNames* deverá conter o valor da propriedade Name para a instância de [**\_ BaseMetricDefinition cim**](cim-basemetricdefinition.md) referenciada pelo índice de matriz correspondente do parâmetro *DefinitionList.*

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
</dt> <dd>

O *parâmetro MetricCollectionEnabled* indica se uma métrica está sendo coletada para um elemento gerenciado.

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

**DMTF Reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor Reservado** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Método Reservado** (..)
</dt> <dt>

**Específico do** fornecedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




