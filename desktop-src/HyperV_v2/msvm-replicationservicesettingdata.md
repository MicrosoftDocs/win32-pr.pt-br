---
description: Representa as configurações do serviço de replicação em um host de recuperação. As propriedades desta classe não podem ser modificadas diretamente. O cliente deve chamar o \_ método Msvm ReplicationService. ModifyServiceSettings para modificar qualquer uma dessas propriedades.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Classe Msvm_ReplicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828890"
---
# <a name="msvm_replicationservicesettingdata-class"></a>\_Classe Msvm ReplicationServiceSettingData

Representa as configurações do serviço de replicação em um host de recuperação. As propriedades desta classe não podem ser modificadas diretamente. O cliente deve chamar o método [**Msvm \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) para modificar qualquer uma dessas propriedades.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ReplicationServiceSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ReplicationServiceSettingData** tem essas propriedades.

<dl> <dt>

**AllowedAuthenticationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Defina modos de autenticação permitidos para conexão com o servidor de host de recuperação.

<dt>

0
</dt> <dd>

Não definido.

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticação Kerberos** (1)


</dt> <dd>

Autenticação Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticação baseada em certificado** (2)


</dt> <dd>

Autenticação baseada em certificado.

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Autenticação baseada em certificado e autenticação Kerberos** (3)


</dt> <dd>

Autenticação baseada em certificado e autenticação integrada.

</dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações do serviço de replicação".

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Impressão digital do certificado a ser usada quando a **AuthenticationType** for autenticação baseada em certificado.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "dados de configurações de replicação da máquina virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações do serviço de replicação".

</dd> <dt>

**HttpPort**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número da porta do servidor de recuperação a ser usado ao aceitar uma conexão não segura para replicação. O valor padrão é 80.

</dd> <dt>

**HttpsPort**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número da porta do servidor de recuperação a ser usado ao aceitar conexão segura para replicação. O valor padrão é 443.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**MonitoringInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo, em segundos, no qual as estatísticas de replicação devem ser redefinidas. O intervalo padrão é de 12 horas (43200 segundos). O valor mínimo válido é de 60 minutos (3600 segundos) e o valor máximo válido é de 7 dias (604800 segundos).

</dd> <dt>

**MonitoringStartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora de início para o monitoramento de replicação, em UTC. O valor padrão é 9:00 A.M., hora local, representado em UTC. Os elementos de data do objeto **DateTime** devem ser zero.

</dd> <dt>

**RecoveryServerEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o host Hyper-V está habilitado como um servidor de recuperação.

</dd> </dl>

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

