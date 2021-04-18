---
description: Fornece um link entre a instância de recursos de recurso de comutador Ethernet e as configurações mínima, máxima, incremental e padrão para um recurso.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Classe Msvm_FeatureSettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753291"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a>\_Classe Msvm FeatureSettingsDefineCapabilities

Fornece um link entre a instância de recursos de recurso de comutador Ethernet e as configurações mínima, máxima, incremental e padrão para um recurso.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ FeatureSettingsDefineCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ FeatureSettingsDefineCapabilities** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) que representa os recursos do recurso de comutador Ethernet. Esta propriedade é herdada [**do \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) que representa as configurações de recurso. Esta propriedade é herdada [**do \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se as propriedades não **nulas** e não-chave de **PartComponent** são tratadas de forma independente ou como um conjunto correlacionado. Por exemplo, um conjunto independente de propriedades máximas pode ser definido, mas não há nenhuma relação entre cada propriedade. Por outro lado, vários conjuntos correlacionados de propriedades máximas podem precisar ser definidos quando os valores máximos de cada um dependem de alguns dos outros.

Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

<dl> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independente** (0)
</dt> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlacionado** (1)
</dt> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Indica uma semântica adicional na interpretação de todas as propriedades não **nulas** e não chave dos dados de configuração.

Os valores a seguir são avaliados somente nas propriedades numéricas não **nulas**, não chave, não enumeradas, não booleanas, dos dados de configuração. Cada propriedade desse conjunto deve ser matematicamente comparável a outras instâncias dessa propriedade.

Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).



| Valor                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Ponto**</dt> <dt>0</dt> </dl>                     | Essa instância de dados de configuração fornece um conjunto único de valores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <dt>**Mínimos**</dt> <dt>1</dt> </dl>         | Esses dados de configuração fornecem valores mínimos para propriedades avaliadas. Quando usado com **PropertyPolicy** = "Independent", apenas uma dessas configurações por instância de dados de configuração específica deve ser especificada para qualquer recurso. A menos que seja restringido por um valor máximo no mesmo conjunto de propriedades, todos os valores que se comparam maior do que os valores especificados também são considerados compatíveis com a instância de recursos associados. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <dt>**Máximos**</dt> <dt>2</dt> </dl>         | Esses dados de configuração fornecem valores máximos para propriedades avaliadas. Quando usado com **PropertyPolicy** = "Independent", apenas uma dessas configurações por instância de dados de configuração específica deve ser especificada para qualquer recurso. A menos que seja restringido por um valor mínimo no mesmo conjunto de propriedades, todos os valores que se comparam com menor do que os valores especificados também são considerados compatíveis com a instância de recursos associados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <dt>**Incrementos**</dt> <dt>3</dt> </dl> | Esses dados de configuração fornecem valores de incremento para propriedades avaliadas. Para os recursos associados, se uma propriedade avaliada atualmente não tiver valores mínimos ou máximos correspondentes, a propriedade não terá nenhum efeito. Caso contrário, para cada propriedade avaliada, seu valor (*x*) deve estar entre os valores *mínimo* e *máximo*, inclusive, e deve ter a propriedade que o resultado de *MaximumValue* menos *x* e o resultado de *x* menos *mínimovalue* são cada um inteiro múltiplo do *incremento*. Se *MinimumValue* ou *MaximumValue* não for especificado e o outro for, o valor ausente deverá ser, respectivamente, considerado o valor mais baixo ou mais alto com suporte para o tipo de dados da propriedade. Além disso, se um *valor mínimo* e um *valor máximo* forem especificados para uma propriedade avaliada, o resultado do *valor* *mínimo* de menos deve ser um múltiplo inteiro do *incremento*. <br/> |



 

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Especifica uma semântica adicional na interpretação das propriedades não **nulas** e não chave dos dados de configuração. Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).



| Valor                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Padrão**</dt> <dt>0</dt> </dl>         | Os valores de propriedade dos dados de configuração serão usados como valores padrão, quando uma nova instância de dados de configuração for criada para elementos cujos recursos são definidos pelos recursos associados. Em instâncias dos dados de configuração, para propriedades específicas com a mesma finalidade semântica, no máximo uma instância de dados de configuração deve ser especificada como padrão.<br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <dt>**Ideal**</dt> <dt>1</dt> </dl>         | A instância de dados de configuração representa os valores de configuração ideais para elementos associados aos recursos associados. Várias instâncias de dados de configuração de componente podem ser declaradas como ideal.<br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <dt>**Média**</dt> <dt>2</dt> </dl>                     | As propriedades numéricas não **nulas**, não chave, não enumeradas, não booleanas e não boolianas da instância de dados de configuração associada representam um ponto médio em uma dimensão. Para diferentes combinações de propriedades de dados de configuração, várias instâncias de dados de configuração de componentes podem ser declaradas como **média**. <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <dt>**Com suporte**</dt> <dt>3</dt> </dl> | As propriedades não **nulas** e não-chave dos dados de configuração representam um conjunto de valores de propriedade com suporte que não são qualificados de outra forma. <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

