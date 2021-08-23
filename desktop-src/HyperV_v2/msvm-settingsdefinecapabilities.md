---
description: Fornece um link entre a instância de funcionalidades e as configurações mínimas, máximas, incrementais e padrão para um recurso.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities classe
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
ms.openlocfilehash: 7194632af7bc1154e6a9bbca1dd5ef0bcca0fb46ab13693d20160ea404068adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950456"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>Classe Msvm \_ SettingsDefineCapabilities

Fornece um link entre a instância de funcionalidades e as configurações mínimas, máximas, incrementais e padrão para um recurso.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe Msvm \_ SettingsDefineCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ SettingsDefineCapabilities** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ Funcionalidades CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A instância de funcionalidades. Essa propriedade é herdada de [**\_ Configurações cimDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ Configuração cimData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma configuração usada para definir a instância de funcionalidades associada. Essa propriedade é herdada de [**\_ Configurações cimDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se as propriedades não nulas e não chave da instância de dados de configuração associada são tratadas independentemente ou como um conjunto correlacionado. Essa propriedade é herdada de [**\_ Configurações cimDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) e é sempre definida como 0 (Independente).

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
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
> Era **NonProduction** na Windows 10, versão 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer semântica posterior sobre a interpretação de todas as propriedades não nulas não chave dos dados de configuração. Essa propriedade é herdada de [**\_ Configurações cimDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer outra semântica sobre a interpretação das propriedades não nulas e não chave dos dados de configuração. Essa propriedade é herdada de [**\_ Configurações cimDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores das **propriedades ValueRole** e **ValueRange** são usados nos seguintes pares:

-   Ponto/Padrão (0/0)
-   Mínimos/com suporte (1/3)
-   Máximos/com suporte (2/3)
-   Incrementos/com suporte (3/3).

"Point" significa que cada uma das propriedades no objeto **PartComponent** representa o padrão da plataforma.

"Mínimos" e "Máximos" significam que cada uma das propriedades no objeto **PartComponent** representa os menores e maiores valores possíveis para essas propriedades que têm suporte da plataforma com base na configuração atual do computador.

"Incrementos" indica a granularidade na qual você pode aumentar ou diminuir as configurações.

O acesso à **classe Msvm \_ SettingsDefineCapabilities** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações \_ cimDefineCapabilities**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**Configurações \_ cimDefineCapabilities**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**Configurações do \_ MsvmDefineCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Classes de gerenciamento de recursos](resource-management-classes.md)
</dt> </dl>

 

