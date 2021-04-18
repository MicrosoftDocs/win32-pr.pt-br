---
description: Fornece um link entre a instância de recursos e as configurações mínima, máxima, incremental e padrão para um recurso.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Classe Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758797"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>\_Classe Msvm SettingsDefineCapabilities

Fornece um link entre a instância de recursos e as configurações mínima, máxima, incremental e padrão para um recurso.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SettingsDefineCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SettingsDefineCapabilities** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ recursos CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A instância de recursos. Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma configuração usada para definir a instância de recursos associados. Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se as propriedades não nulas e não-chave da instância de dados de configuração associada são tratadas de forma independente ou como um conjunto correlacionado. Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) e é sempre definida como 0 (independente).

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a instrução de suporte.

> [!Note]  
> Essa propriedade foi adicionada no Windows 10, versão 1703.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produção** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Pré-lançamento** (1)


</dt> <dd>

> [!Note]  
> Was não **produto** no Windows 10, versão 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer semântica adicional na interpretação de todas as propriedades não nulas e não chave dos dados de configuração. Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer semântica adicional na interpretação das propriedades não nulas e não chave dos dados de configuração. Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores para as propriedades **ValueRole** e **ValueRange** são usados nos seguintes pares:

-   Ponto/padrão (0/0)
-   Mínimos/com suporte (1/3)
-   Máximos/com suporte (2/3)
-   Incrementos/com suporte (3/3).

"Point" significa que cada uma das propriedades no objeto **PartComponent** representa o padrão da plataforma.

"Mínimos" e "máximos" significam que cada uma das propriedades no objeto **PartComponent** representa os menores e os maiores valores possíveis para essas propriedades com suporte da plataforma com base na configuração atual do computador.

"Incrementos" indica a granularidade na qual você pode aumentar ou diminuir as configurações.

O acesso à classe **Msvm \_ SettingsDefineCapabilities** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_SETTINGSDEFINECAPABILITIES CIM**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**Msvm \_ SettingsDefineCapabilities (v1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Classes de gerenciamento de recursos](resource-management-classes.md)
</dt> </dl>

 

