---
description: Método ControlMetricsByClass da classe CIM_MetricService – habilita e desabilita a coleção de métricas.
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Método ControlMetricsByClass da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fda8407d49ed3eec7ff86abc94ced6b63d2d77c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109704"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a>Método ControlMetricsByClass da \_ classe METRICSERVICE CIM

Habilita e desabilita a coleção de métricas. **ControlMetricsByClass** é usado para controlar a coleção de cada tipo de métrica para todas as instâncias de uma classe ou a coleção de uma métrica específica para todas as instâncias de uma classe.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Assunto* \[ no\]
</dt> <dd>

Identifica a classe [**CIM \_ managedelement**](cim-managedelement.md) para a qual as métricas serão controladas.

</dd> <dt>

*Definição* \[ do no\]
</dt> <dd>

Identifica um [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) para o qual as métricas serão controladas.

</dd> <dt>

*MetricCollectionEnabled* \[ no\]
</dt> <dd>

Indica a operação desejada a ser executada nas métricas.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Habilitar** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Desabilitar** (3)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Redefinir** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 




