---
description: Representa o estado configurado das configurações de segurança para.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Classe Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22bc30db51b103f50eaa4deed7ca6f479c5f94600fbb15ef2a6f4bb36595d159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148139"
---
# <a name="msvm_securitysettingdata-class"></a>\_Classe Msvm SecuritySettingData

Representa o estado configurado das configurações de segurança para uma máquina virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SecuritySettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SecuritySettingData** tem essas propriedades.

<dl> <dt>

**DataProtectionRequested**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para solicitar a proteção de dados para uma VM; caso contrário, **false**. O valor padrão é **false.**

</dd> <dt>

**EncryptStateAndVmMigrationTraffic**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para ter o estado e a migração do tráfego de uma VM criptografada; caso contrário, **false**. O valor padrão para uma VM recém-criada é **false**.

</dd> <dt>

**KsdEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para habilitar um dispositivo de armazenamento de chave (KSD) para esta máquina virtual; caso contrário, **false**. Uma VM recém-criada tem um Disable KSD.

</dd> <dt>

**ShieldingRequested**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para solicitar blindagem para uma VM; caso contrário, **false**. Uma VM recém-criada tem um estado de blindagem inicial solicitado de **false**.

</dd> <dt>

**TpmEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para habilitar um TPM (Nodule Platform) confiável para esta máquina virtual; caso contrário, **false**. Uma VM criada recentemente tem um desabilitar TPM.

</dd> <dt>

**VirtualizationBasedSecurityOptOut**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** para não oferecer uma segurança baseada em virtualização de VM; caso contrário, **false**. A configuração padrão para o estado de aceitação de uma VM recém-criada é **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

