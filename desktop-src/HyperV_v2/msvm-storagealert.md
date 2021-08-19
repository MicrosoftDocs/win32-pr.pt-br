---
description: Representa um evento gerado sempre que a propriedade OperationalStatus da classe Msvm \_ ResourcePool ou Msvm \_ LogicalDisk é muda.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert classe
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
ms.openlocfilehash: 478b4617f56c73e425d833842b313767f85c385e9142314a7ca8978b5783f492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950225"
---
# <a name="msvm_storagealert-class"></a>Classe Msvm \_ StorageAlert

Representa um evento gerado sempre que a propriedade **OperationalStatus** da classe [**Msvm \_ ResourcePool**](msvm-resourcepool.md) ou [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) é muda.

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

A **classe \_ StorageAlert do Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ StorageAlert** tem essas propriedades.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **ModelCorrespondence** ("CIM \_ AlertIndication.AlertingManagedElement", "CIM \_ AlertIndication.OtherAlertingElementFormat")
</dt> </dl>

Especifica o formato da **propriedade AlertingManagedElement.** O formato é um CIMObjectPath, com o formato *<NamespacePath> : . " <ClassName> <Prop1> = \\ <Value1> \\ ", <Prop2> = \\ " " <Value2> \\ " ,* que especifica uma instância no esquema CIM.

Essa propriedade é herdada da **classe CIM \_ AlertIndication.**

Os valores possíveis são:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os caminhos WMI da instância para a qual o alerta é gerado.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
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

Tipo de dados: **datetime**
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

Uma mensagem formatada que é construída combinando alguns ou todos os elementos dinâmicos especificados na propriedade **MessageArguments** com os elementos estáticos identificados exclusivamente pela propriedade **MessageID** em um registro de mensagens ou outro catálogo associado à propriedade **OwningEntity.**

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém o conteúdo dinâmico da mensagem. Se o valor de **MessageID** for 32930, o argumento na posição 0 será o **PoolID** da instância [**do Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md) para a qual o alerta é gerado.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica exclusivamente, dentro do escopo da **propriedade OwningEntity,** o formato da **propriedade** Message. Os valores possíveis para essa propriedade são:

32930 ("mensagem de Armazenamento de QoS de pool insuficiente")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que define valores "Outros" **para AlertingManagedElement.** Esse valor DEVE ser definido como um valor não NULL **quando AlertingManagedElement** é definido como um valor de 1 ("Outro"). Para todos os outros valores **de AlertingManagedElement**, o valor dessa cadeia de caracteres deve ser definido como NULL.

Essa propriedade é herdada da **classe CIM \_ AlertIndication.**

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica exclusivamente a entidade que possui a definição do formato da **Mensagem** descrita nesta instância. O valor dessa propriedade é sempre "Microsoft-Windows- Hyper-V".

"Microsoft-Windows- Hyper-V"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve a severidade da indicação de alerta. Os valores possíveis para essa propriedade são:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/Aviso** (3)
</dt> </dl>

</dd> <dt>

**ProvávelCause**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve a causa provável da situação que resultou na indicação de alerta.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Armazenamento de capacidade** (50)
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

Uma descrição textual que corresponde ao valor da propriedade **ProbableCause.**

</dd> </dl>

## <a name="remarks"></a>Comentários

O provedor WMI do Hyper-V não gera eventos para discos virtuais individuais para evitar inundar clientes com eventos em caso de mau funcionamento em grande escala dos sistemas de armazenamento subjacentes.

Quando um cliente recebe um evento **Msvm \_ StorageAlert,** se o valor da propriedade **ProbableCause** for 50 ( problema de capacidade do Armazenamento ), o cliente poderá descobrir quais discos virtuais estão operando fora de sua política de QoS usando um destes procedimentos:

-   Consulte todas as [**instâncias \_ logicalDisk do Msvm**](msvm-logicaldisk.md) que foram alocadas do pool de recursos para o qual o evento foi gerado. Essas **instâncias do Msvm \_ LogicalDisk** são associadas ao pool de recursos por meio da associação [**\_ ElementAllocatedFromPool do Msvm.**](msvm-elementallocatedfrompool.md)
-   Filtre a lista de resultados selecionando instâncias cujo OperationalStatus contém Produtividade Insuficiente .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ AlertIndication**](cim-alertindication.md)
</dt> <dt>

[**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




