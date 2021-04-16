---
description: Controla as métricas por classe.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Método ControlMetricsByClass da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759238"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Método ControlMetricsByClass da \_ classe MetricService Msvm

Controla as métricas por classe.

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

Identifica a classe CIM para a qual as métricas serão controladas.

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

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos seguintes valores:

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

 

 




