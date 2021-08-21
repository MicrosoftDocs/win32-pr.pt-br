---
description: Representa o estado configurado do serviço de desligamento.
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Msvm_ShutdownComponentSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60e69c7ceafb574824412e54f40749dbbc0adf250470a1c9fd53042d45688219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950305"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a>Classe Msvm \_ ShutdownComponentSettingData

Representa o estado configurado do serviço de desligamento.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ ShutdownComponentSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ ShutdownComponentSettingData** tem essas propriedades.

<dl> <dt>

**Endereço**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço do recurso. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve o endereço desse recurso no contexto do pai. As **propriedades Parent** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordenação de dispositivos em um controlador. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As unidades de alocação usadas pelas **propriedades Reserva** **e** Limite. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o recurso será alocado automaticamente. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o recurso será desalocado automaticamente. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Desligamento".

</dd> <dt>

**Conexão**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A coisa à qual esse recurso está conectado. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A visibilidade dos consumidores para o recurso alocado. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).



| Valor                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>3</dt> </dl> | Virtualizado<br/> |



 

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os estados habilitados e desabilitados de um elemento. Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Expõe uma atribuição específica para hospedar ou recursos subjacentes. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**\_ ManagedElement do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O limite superior ou a quantidade máxima de recursos que será concedida para essa alocação. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica como esse recurso é mapeados para recursos subjacentes. Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor 1 (Outro). Essa propriedade é herdada de [**Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Pai**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O pai do recurso. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Poolid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ID do pool de recursos do qual o recurso está alocado. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade de recursos com garantia disponível para essa alocação. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de recurso que essa configuração de alocação representa. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).



| Valor                                                                        | Significado          |
|------------------------------------------------------------------------------|------------------|
| <dl> <dt>1</dt> </dl> | Outro<br/> |



 

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade de recursos apresentados ao consumidor. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a unidade de medida para essa alocação de recursos. O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos. Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ ShutdownComponentSettingData** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

