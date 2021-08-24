---
description: Representa uma associação entre as propriedades de uma \_ instância do CIM SettingData e uma instância de recursos de CIM \_ .
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: Classe CIM_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b53f0e72e21b73932c144602308ee599c523ea755b45dae12774109f6a9e010f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899656"
---
# <a name="cim_settingsdefinecapabilities-class"></a>\_Classe CIM SettingsDefineCapabilities

Representa uma associação entre as propriedades de uma instância do [**CIM \_ SettingData**](cim-settingdata.md) e uma instância de [**\_ recursos de CIM**](cim-capabilities.md) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SettingsDefineCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SettingsDefineCapabilities** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ recursos CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Uma referência à instância [**de \_ recursos de CIM**](cim-capabilities.md) .

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Uma referência à instância de [**CIM \_ SettingData**](cim-settingdata.md) usada para definir a instância de [**\_ recursos de CIM**](cim-capabilities.md) .

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

Indica se as propriedades não nulas e não-chave da instância de [**CIM \_ SettingData**](cim-settingdata.md) associada são tratadas de forma independente ou como um conjunto correlacionado. Por exemplo, um conjunto independente de propriedades máximas pode ser definido quando não há nenhuma relação entre cada propriedade. Por outro lado, vários conjuntos correlacionados de propriedades máximas podem precisar ser definidos quando os valores máximos de cada um dependem de alguns dos outros.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Independente** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Correlacionado** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRole**")
</dt> </dl>

Indica o tipo de intervalo de valores usado pelas propriedades das propriedades não nulas e não chave da instância do [**CIM \_ SettingData**](cim-settingdata.md) .

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Ponto** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Mínimos** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Máximo** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Incrementos** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

A semântica adicional para a interpretação das propriedades não nulas e não chave da instância do [**CIM \_ SettingData**](cim-settingdata.md) .

"Default" indica que os valores de propriedade da instância do componente SettingData serão usados como valores padrão, quando uma nova instância de SettingData for criada para elementos cujos recursos são definidos pela instância de recursos associados.

Em instâncias de SettingData, para propriedades específicas com a mesma finalidade semântica, no máximo uma dessas instâncias de SettingData deve ser especificada como padrão.

"Ideal" indica que a instância de SettingData representa valores de configuração ideais para elementos associados à instância de recursos associados. Várias instâncias do componente SettingData podem ser declaradas como ótimas. " Mean "indica que as propriedades numéricas não-nulas, não chave, não enumeradas, não boolianas da instância SettingData associada representam um ponto médio em uma dimensão. Para diferentes combinações de propriedades SettingData, várias instâncias do componente SettingData podem ser declaradas como "Mean". "Supported" indica que as propriedades não nulas e não chave da instância do componente SettingData representam um conjunto de valores de propriedade com suporte que não são qualificados de outra forma.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Padrão** (0)


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**Ideal** (1)


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Média** (2)


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**Com suporte** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

