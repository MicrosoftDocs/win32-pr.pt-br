---
description: Usado para controlar a coleção de métricas para um elemento ou elementos gerenciados.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Método ControlMetrics da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811876"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Método ControlMetrics da \_ classe MetricService Msvm

Usado para controlar a coleção de métricas para um elemento ou elementos gerenciados.

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

*Assunto* \[ no\]
</dt> <dd>

Uma [**instância \_ gerenciada CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que identifica os elementos gerenciados para os quais as métricas serão coletadas. Se esse parâmetro for **nulo**, as métricas para todos os elementos gerenciados associados ao parâmetro de *definição* serão coletadas.

</dd> <dt>

*Definição* \[ do no\]
</dt> <dd>

Uma instância de [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que especifica quais métricas serão coletadas. Se esse parâmetro for **nulo**, as métricas para todas as definições associadas ao elemento gerenciado identificado pelo parâmetro *Subject* serão coletadas

</dd> <dt>

*MetricCollectionEnabled* \[ no\]
</dt> <dd>

Especifica a operação a ser executada na coleção de métricas. Deve ser um dos valores a seguir.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** (2)


</dt> <dd>

Habilitar a coleta de métricas.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** (3)


</dt> <dd>

Desabilitar a coleta de métricas.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (4)


</dt> <dd>

Redefinir valores de métricas.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)


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

## <a name="remarks"></a>Comentários

Esse método falhará nas seguintes instâncias:

-   Os parâmetros de *assunto* e *definição* são **nulos**.
-   Os parâmetros *Subject* e *Definition* não são **nulos** e não há uma instância de [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md) que associa as duas instâncias.
-   O parâmetro de *definição* é uma referência a uma instância de [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que não está associada com o [**Msvm \_ MetricService**](msvm-metricservice.md) por meio de [**Msvm \_ paraafetaelement**](msvm-serviceaffectselement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

