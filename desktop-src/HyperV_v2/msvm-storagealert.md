---
description: Representa um evento que é gerado cada vez que a propriedade OperationalStatus da \_ classe Msvm ResourcePool ou Msvm \_ LogicalDisk é alterada.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Classe Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011308"
---
# <a name="msvm_storagealert-class"></a>\_Classe Msvm StorageAlert

Representa um evento que é gerado cada vez que a propriedade **OperationalStatus** da classe [**Msvm \_ ResourcePool**](msvm-resourcepool.md) ou [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) é alterada.

A sintaxe a seguir é simplificada do código MOF e inclui essas propriedades.

## <a name="syntax"></a>Sintaxe

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ StorageAlert** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ StorageAlert** tem essas propriedades.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")
</dt> </dl>

Especifica o formato da propriedade **AlertingManagedElement** . O formato é um CIMObjectPath, com o formato *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\*", que especifica uma instância no esquema CIM.

Essa propriedade é herdada da classe **CIM \_ AlertIndication** .

Os valores possíveis são:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os caminhos WMI da instância para a qual o alerta é gerado.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a classificação primária do alerta. Os valores possíveis para essa propriedade são:

<dl> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerta de qualidade de serviço** (3)
</dt> </dl>

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que o evento subjacente foi detectado.

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma mensagem formatada que é construída pela combinação de alguns ou de todos os elementos dinâmicos especificados na propriedade **MessageArguments** com os elementos estáticos exclusivamente identificados pela propriedade **MessageId** em um registro de mensagem ou outro catálogo associado à propriedade **OwningEntity** .

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém o conteúdo dinâmico da mensagem. Se o valor de **MessageId** for 32930, o argumento na posição 0 será o **poolid** da instância [**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md) para a qual o alerta é gerado.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica exclusivamente, dentro do escopo da propriedade **OwningEntity** , o formato da propriedade **Message** . Os valores possíveis para essa propriedade são:

32930 ("mensagem de taxa de transferência insuficiente do QoS do pool de armazenamento")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que define "other" valores para **AlertingManagedElement**. Esse valor deve ser definido como um valor não nulo quando **AlertingManagedElement** é definido como um valor de 1 ("other"). Para todos os outros valores de **AlertingManagedElement**, o valor dessa cadeia de caracteres deve ser definido como nulo.

Essa propriedade é herdada da classe **CIM \_ AlertIndication** .

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica exclusivamente a entidade que possui a definição do formato da **mensagem** descrita nesta instância. O valor dessa propriedade é sempre "Microsoft-Windows-Hyper-V."

"Microsoft-Windows-Hyper-V"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve a severidade da indicação de alerta. Os valores possíveis para essa propriedade são:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/aviso** (3)
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve a causa provável da situação que resultou na indicação de alerta.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema de capacidade de armazenamento** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerta anterior limpo** (59)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição textual que corresponde ao valor da propriedade **ProbableCause** .

</dd> </dl>

## <a name="remarks"></a>Comentários

O provedor WMI do Hyper-V não gerará eventos para discos virtuais individuais para evitar a inundação de clientes com eventos em caso de problemas de grande escala dos sistemas de armazenamento subjacentes.

Quando um cliente recebe um evento **Msvm \_ StorageAlert** , se o valor da propriedade **ProbableCause** for 50 (problema de capacidade de armazenamento), o cliente poderá descobrir quais discos virtuais estão operando fora de sua política de QoS usando um destes procedimentos:

-   Consulte todas as instâncias do [**\_ LogicalDisk Msvm**](msvm-logicaldisk.md) que foram alocadas do pool de recursos para o qual o evento foi gerado. Essas instâncias do **Msvm \_ LogicalDisk** estão associadas ao pool de recursos por meio da Associação [**Msvm \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) .
-   Filtre a lista de resultados selecionando instâncias cujo OperationalStatus contém taxa de transferência insuficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ALERTINDICATION CIM**](cim-alertindication.md)
</dt> <dt>

[**\_LogicalDisk Msvm**](msvm-logicaldisk.md)
</dt> <dt>

[**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




