---
description: Fornece a capacidade de retornar uma lista filtrada de \_ instâncias do CIM BaseMetricValue.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Método GetMetricValues da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758344"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a>Método GetMetricValues da \_ classe METRICSERVICE CIM

Fornece a capacidade de retornar uma lista filtrada de instâncias do [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) .

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

*Definição* \[ do no\]
</dt> <dd>

Identifica um [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) para o qual as métricas serão retornadas.

</dd> <dt>

*Intervalo* \[ de no\]
</dt> <dd>

Identifica como as instâncias são selecionadas. O algoritmo para instâncias de valor de ordenação é específico à definição de métrica.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Mínimo** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Máximo** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico do fornecedor** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Identifica o número máximo de instâncias a serem retornadas pelo método.

</dd> <dt>

*Valores* \[ de fora\]
</dt> <dd>

Após a conclusão bem-sucedida do método, contém referências a instâncias do [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md), filtradas de acordo com os valores dos parâmetros de entrada.

</dd> </dl>

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

 

 




