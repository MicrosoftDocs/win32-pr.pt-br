---
description: Representa as configurações do serviço de virtualização presente em um único sistema de host.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Classe Msvm_VirtualSystemManagementServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ccb0a1a9bc4a10ec7f8a366f012446e0374dab299f8ee779f16cfeb38fb005b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147969"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a>\_Classe Msvm VirtualSystemManagementServiceSettingData

Representa as configurações do serviço de virtualização presente em um único sistema de host. As propriedades desta classe não podem ser modificadas diretamente. O cliente deve chamar o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar qualquer uma dessas propriedades.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemManagementServiceSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemManagementServiceSettingData** tem essas propriedades.

<dl> <dt>

**BiosLockString**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)
</dt> </dl>

usado pelos OEMs para permitir que sistemas operacionais Windowss bloqueados por BIOS sejam executados na máquina virtual. Essa cadeia de caracteres deve ter exatamente 32 caracteres de comprimento.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de sistema virtual do Hyper-V".

</dd> <dt>

**CurrentWWNNAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço WWNN (World Wide node Name) para endereços de World Wide Name gerados dinamicamente usados para adaptadores de barramento de host sintético.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**DefaultExternalDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")
</dt> </dl>

A raiz de dados externa padrão. por padrão, "*root* \\ ProgramData \\ Microsoft \\ Windows \\ Virtualization".

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**DefaultVirtualHardDiskCachingMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o cache de arquivos na memória deve ser usado para discos por padrão. Esse valor pode ser substituído em uma base por disco no campo **cachingmode** da classe [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) .

> [!Note]  
> adicionado em Windows 10 e Windows Server 2016.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**sem Caching** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Pais compartilháveis do cache** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultVirtualHardDiskPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do disco rígido virtual padrão. Por padrão, " \\ usuários raiz \\ \\ documentos públicos \\ discos rígidos virtuais".

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "Configurações para o serviço de gerenciamento de sistema Virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de sistema virtual do Hyper-V". A alteração dessa propriedade alterará a propriedade **ElementName** do derivativo [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associado.

</dd> <dt>

**EnhancedSessionModeEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o modo de sessão avançada é permitido no servidor. **True** indica permitido; caso contrário, **false**.

**Windows 8.1:** não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**HbaLunTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a quantidade de tempo que o dispositivo virtual Fibre Channel sintético aguardará que um LUN (número de unidade lógica) apareça antes de iniciar uma máquina virtual.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**HypervisorRootSchedulerEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se o Agendador raiz do hipervisor está habilitado ou não.

> [!Note]  
> adicionado em Windows 10, versão 1709.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "Microsoft:*host*", em que *host* é o nome NetBIOS do sistema de computador host.

</dd> <dt>

**MaximumMacAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço MAC máximo para endereços MAC gerados dinamicamente.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**MaximumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço de WWPN (World Wide Port Name) máximo para endereços de World Wide Name gerados dinamicamente usados para adaptadores de barramento de host sintético.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**MinimumMacAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço MAC mínimo para endereços MAC gerados dinamicamente.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**MinimumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço de World Wide Name de porta mínimo para endereços de World Wide Name gerados dinamicamente usados para adaptadores de barramento de host sintético.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**NumaSpanningEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se a memória pode ser alocada de nós NUMA (acesso remoto não uniforme à memória) ao iniciar uma máquina virtual ou ao atribuir memória a uma máquina virtual por memória dinâmica. Isso pode ser um dos valores a seguir.



| Valor                                                                                | Significado                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**Verdadeiro**</dt> </dl>  | A memória pode ser alocada de nós NUMA locais e remotos.<br/>                   |
| <dl> <dt>**Falso**</dt> </dl> | A memória pode ser alocada somente a partir do nó NUMA atribuído à máquina virtual.<br/> |



 

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,4 ")
</dt> </dl>

Descreve como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone ou endereço de email). Por padrão, vazio. Esse nome não pode exceder 256 caracteres de comprimento.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,3 ")
</dt> </dl>

O nome do proprietário do sistema primário. Por padrão, "administradores". Esse valor não pode exceder 64 caracteres de comprimento.

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VirtualSystemManagementServiceSettingData** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> <dt>

[Classes de gerenciamento do sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

