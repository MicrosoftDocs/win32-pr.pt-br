---
description: Representa um elemento do pool de recursos da plataforma Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Classe Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748996"
---
# <a name="msvm_resourcepoolcomponent-class"></a>\_Classe Msvm ResourcePoolComponent

Representa um elemento do pool de recursos da plataforma Microsoft Windows Hyper-V.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ResourcePoolComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ResourcePoolComponent** tem essas propriedades.

<dl> <dt>

**AllocationCapabilitiesClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe derivada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) que descreve os recursos de alocação desse pool de recursos.

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um **GUID** que representa o identificador de classe do objeto com do serviço. Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O contexto no qual o objeto recém-criado será executado. Esse valor é passado no parâmetro *dwClsContext* para **CoCreateInstance**. Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se esta instância estiver habilitada e puder ser usada para concluir solicitações de cliente; caso contrário, **false**. Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como **true**.

</dd> <dt>

**MaxParentPools**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número máximo de pools de recursos pai aos quais um pool filho dá suporte.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Uma cadeia de caracteres neutra em idioma que identifica exclusivamente o elemento. O seguinte formato é sugerido para evitar conflitos de nomenclatura: " \| versão do componente do fornecedor \| ". Por exemplo, esse nome representa a versão 1,0 do componente de porta de rede emulada da Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0". Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**PhysicalDeviceClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe derivada do [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que implementa o dispositivo físico do qual esse pool aloca recursos. Essa propriedade poderá ser **nula** se a classe de dispositivo virtual alocada desse pool for igual à classe de dispositivo físico.

</dd> <dt>

**ResourcePoolClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe derivada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) que implementa o pool de recursos.

</dd> <dt>

**ResourcePoolSettingDataClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe derivada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que descreve as configurações relacionadas à não alocação do pool de recursos.

</dd> <dt>

**WmiFactoryCLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um **GUID** que representa o identificador de classe da fábrica de objetos WMI do componente.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ ResourcePoolComponent** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Fim do suporte do cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

