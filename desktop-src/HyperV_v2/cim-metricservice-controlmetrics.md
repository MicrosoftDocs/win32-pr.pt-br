---
description: Método ControlMetrics da classe CIM_MetricService - Habilita e desabilita a coleção de métricas.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Método ControlMetrics da classe CIM_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c78f575bb68673c364fe627766b3709944c2a062e0407f927262ff019764b7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068646"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>Método ControlMetrics da classe CIM \_ MetricService

Habilita e desabilita a coleção de métricas. **ControlMetrics** é usado para controlar a coleção de cada tipo de métrica para um [**\_ ManagedElement cim**](cim-managedelement.md), a coleção de um determinado tipo de métrica para todos os elementos gerenciados ou a coleção de uma métrica específica para um elemento gerenciado específico.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Assunto* \[ Em\]
</dt> <dd>

Um [**\_ ManagedElement cim**](cim-managedelement.md) que identifica os elementos gerenciados para os quais as métricas serão controladas.

</dd> <dt>

*Definição* \[ Em\]
</dt> <dd>

Identifica uma [**\_ BaseMetricDefinition cim**](cim-basemetricdefinition.md) para a qual as métricas serão controladas.

</dd> <dt>

*MetricCollectionEnabled* \[ Em\]
</dt> <dd>

Indica a operação desejada a ser realizada nas métricas.

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

**DMTF Reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor Reservado** (32768..65535)


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

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




