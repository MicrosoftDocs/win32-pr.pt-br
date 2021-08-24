---
description: Obtém valores de métrica.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Método GetMetricValues da classe Msvm_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c22aa9adab9fc69876329f6be0ff011765da61a714c518241c47d3b2bd882ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521456"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a>Método GetMetricValues da classe Msvm \_ MetricService

Obtém valores de métrica.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Definição* \[ Em\]
</dt> <dd>

Identifica um [**\_ BaseMetricDefinition cim para**](cim-basemetricdefinition.md) o qual as métricas serão retornadas.

</dd> <dt>

*Intervalo* \[ Em\]
</dt> <dd>

Identifica como as instâncias são selecionadas. O algoritmo para ordenar instâncias de valor é específico da definição de métrica.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Mínimo** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Máximo** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico do** fornecedor (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Contagem* \[ Em\]
</dt> <dd>

Identifica o número máximo de instâncias a serem retornadas pelo método .

</dd> <dt>

*Valores* \[ out\]
</dt> <dd>

Após a conclusão bem-sucedida do método, contém referências a instâncias de [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md), filtradas de acordo com os valores dos parâmetros de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

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

 

 




