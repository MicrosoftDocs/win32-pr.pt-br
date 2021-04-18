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
# <a name="msvm_featuresettingsdefinecapabilities-class"></a><span data-ttu-id="cfb90-103">\_Classe Msvm FeatureSettingsDefineCapabilities</span><span class="sxs-lookup"><span data-stu-id="cfb90-103">Msvm\_FeatureSettingsDefineCapabilities class</span></span>

<span data-ttu-id="cfb90-104">Fornece um link entre a instância de recursos de recurso de comutador Ethernet e as configurações mínima, máxima, incremental e padrão para um recurso.</span><span class="sxs-lookup"><span data-stu-id="cfb90-104">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="cfb90-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cfb90-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb90-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfb90-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="cfb90-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cfb90-107">Members</span></span>

<span data-ttu-id="cfb90-108">A classe **Msvm \_ FeatureSettingsDefineCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cfb90-108">The **Msvm\_FeatureSettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="cfb90-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cfb90-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cfb90-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cfb90-110">Properties</span></span>

<span data-ttu-id="cfb90-111">A classe **Msvm \_ FeatureSettingsDefineCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cfb90-111">The **Msvm\_FeatureSettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cfb90-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cfb90-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb90-113">Tipo de dados: **[ **Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="cfb90-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfb90-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="cfb90-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cfb90-116">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) que representa os recursos do recurso de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="cfb90-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the Ethernet switch feature capabilities.</span></span> <span data-ttu-id="cfb90-117">Esta propriedade é herdada [**do \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="cfb90-117">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="cfb90-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cfb90-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb90-119">Tipo de dados: **[ **Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="cfb90-119">Data type: **[**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfb90-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="cfb90-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cfb90-122">Uma referência a uma instância da classe [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) que representa as configurações de recurso.</span><span class="sxs-lookup"><span data-stu-id="cfb90-122">A reference to an instance of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represents the resource settings.</span></span> <span data-ttu-id="cfb90-123">Esta propriedade é herdada [**do \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="cfb90-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="cfb90-124">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="cfb90-124">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb90-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfb90-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfb90-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfb90-127">Especifica se as propriedades não **nulas** e não-chave de **PartComponent** são tratadas de forma independente ou como um conjunto correlacionado.</span><span class="sxs-lookup"><span data-stu-id="cfb90-127">Specifies whether the non-**Null**, non-key properties of the **PartComponent** are treated independently or as a correlated set.</span></span> <span data-ttu-id="cfb90-128">Por exemplo, um conjunto independente de propriedades máximas pode ser definido, mas não há nenhuma relação entre cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="cfb90-128">For example, an independent set of maximum properties might be defined, yet there is no relationship between each property.</span></span> <span data-ttu-id="cfb90-129">Por outro lado, vários conjuntos correlacionados de propriedades máximas podem precisar ser definidos quando os valores máximos de cada um dependem de alguns dos outros.</span><span class="sxs-lookup"><span data-stu-id="cfb90-129">On the other hand, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<span data-ttu-id="cfb90-130">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cfb90-130">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="cfb90-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independente** (0)</span><span class="sxs-lookup"><span data-stu-id="cfb90-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independent** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlacionado** (1)</span><span class="sxs-lookup"><span data-stu-id="cfb90-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlated** (1)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cfb90-133">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="cfb90-133">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb90-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfb90-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfb90-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-136">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="cfb90-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cfb90-137">Indica uma semântica adicional na interpretação de todas as propriedades não **nulas** e não chave dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cfb90-137">Indicates further semantics on the interpretation of all non-**Null**, non-key properties of the setting data.</span></span>

<span data-ttu-id="cfb90-138">Os valores a seguir são avaliados somente nas propriedades numéricas não **nulas**, não chave, não enumeradas, não booleanas, dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cfb90-138">The values below are only evaluated against non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the setting data.</span></span> <span data-ttu-id="cfb90-139">Cada propriedade desse conjunto deve ser matematicamente comparável a outras instâncias dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cfb90-139">Each property of that set must be mathematically comparable to other instances of that property.</span></span>

<span data-ttu-id="cfb90-140">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cfb90-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="cfb90-141">Valor</span><span class="sxs-lookup"><span data-stu-id="cfb90-141">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="cfb90-142">Significado</span><span class="sxs-lookup"><span data-stu-id="cfb90-142">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="cfb90-143"><dt>**Ponto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-143"><dt>**Point**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="cfb90-144">Essa instância de dados de configuração fornece um conjunto único de valores.</span><span class="sxs-lookup"><span data-stu-id="cfb90-144">This setting data instance provides a single set of values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <span data-ttu-id="cfb90-145"><dt>**Mínimos**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-145"><dt>**Minimums**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="cfb90-146">Esses dados de configuração fornecem valores mínimos para propriedades avaliadas.</span><span class="sxs-lookup"><span data-stu-id="cfb90-146">This setting data provides minimum values for evaluated properties.</span></span> <span data-ttu-id="cfb90-147">Quando usado com **PropertyPolicy** = "Independent", apenas uma dessas configurações por instância de dados de configuração específica deve ser especificada para qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="cfb90-147">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="cfb90-148">A menos que seja restringido por um valor máximo no mesmo conjunto de propriedades, todos os valores que se comparam maior do que os valores especificados também são considerados compatíveis com a instância de recursos associados.</span><span class="sxs-lookup"><span data-stu-id="cfb90-148">Unless restricted by a Maximums value on the same set of properties, all values that compare higher than the specified values are also considered to be supported by the associated capabilities instance.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <span data-ttu-id="cfb90-149"><dt>**Máximos**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-149"><dt>**Maximums**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="cfb90-150">Esses dados de configuração fornecem valores máximos para propriedades avaliadas.</span><span class="sxs-lookup"><span data-stu-id="cfb90-150">This setting data provides maximum values for evaluated properties.</span></span> <span data-ttu-id="cfb90-151">Quando usado com **PropertyPolicy** = "Independent", apenas uma dessas configurações por instância de dados de configuração específica deve ser especificada para qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="cfb90-151">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="cfb90-152">A menos que seja restringido por um valor mínimo no mesmo conjunto de propriedades, todos os valores que se comparam com menor do que os valores especificados também são considerados compatíveis com a instância de recursos associados.</span><span class="sxs-lookup"><span data-stu-id="cfb90-152">Unless restricted by a Minimums value on the same set of properties, all values that compare lower than the specified values are also considered to be supported by the associated capabilities instance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <span data-ttu-id="cfb90-153"><dt>**Incrementos**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-153"><dt>**Increments**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="cfb90-154">Esses dados de configuração fornecem valores de incremento para propriedades avaliadas.</span><span class="sxs-lookup"><span data-stu-id="cfb90-154">This setting data provides increment values for evaluated properties.</span></span> <span data-ttu-id="cfb90-155">Para os recursos associados, se uma propriedade avaliada atualmente não tiver valores mínimos ou máximos correspondentes, a propriedade não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="cfb90-155">For the associated capabilities, if an evaluated property currently has no corresponding Minimums or Maximums values, then the property has no affect.</span></span> <span data-ttu-id="cfb90-156">Caso contrário, para cada propriedade avaliada, seu valor (*x*) deve estar entre os valores *mínimo* e *máximo*, inclusive, e deve ter a propriedade que o resultado de *MaximumValue* menos *x* e o resultado de *x* menos *mínimovalue* são cada um inteiro múltiplo do *incremento*.</span><span class="sxs-lookup"><span data-stu-id="cfb90-156">Otherwise, for each evaluated property, its value (*x*) must be between the *MinimumValue* and *MaximumValue*, inclusively, and must have the property that both the result of *MaximumValue* minus *x* and the result of *x* minus *MinimumValue* are each an integer multiple of the *Increment*.</span></span> <span data-ttu-id="cfb90-157">Se *MinimumValue* ou *MaximumValue* não for especificado e o outro for, o valor ausente deverá ser, respectivamente, considerado o valor mais baixo ou mais alto com suporte para o tipo de dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="cfb90-157">If either *MinimumValue* or *MaximumValue* is not specified and the other is, then the missing value must be respectively assumed to be the lowest or highest supported value for the property's data type.</span></span> <span data-ttu-id="cfb90-158">Além disso, se um *valor mínimo* e um *valor máximo* forem especificados para uma propriedade avaliada, o resultado do *valor* *mínimo* de menos deve ser um múltiplo inteiro do *incremento*.</span><span class="sxs-lookup"><span data-stu-id="cfb90-158">Additionally, if both a *MinimumValue* and a *MaximumValue* are specified for an evaluated property, then the result of *MaximumValue* minus *MinimumValue* must be an integer multiple of the *Increment*.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="cfb90-159">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="cfb90-159">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb90-160">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfb90-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfb90-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb90-162">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="cfb90-162">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cfb90-163">Especifica uma semântica adicional na interpretação das propriedades não **nulas** e não chave dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cfb90-163">Specifies further semantics on the interpretation of the non-**Null**, non-key properties of the setting data.</span></span> <span data-ttu-id="cfb90-164">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cfb90-164">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="cfb90-165">Valor</span><span class="sxs-lookup"><span data-stu-id="cfb90-165">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="cfb90-166">Significado</span><span class="sxs-lookup"><span data-stu-id="cfb90-166">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="cfb90-167"><dt>**Padrão**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-167"><dt>**Default**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="cfb90-168">Os valores de propriedade dos dados de configuração serão usados como valores padrão, quando uma nova instância de dados de configuração for criada para elementos cujos recursos são definidos pelos recursos associados.</span><span class="sxs-lookup"><span data-stu-id="cfb90-168">The property values of the setting data will be used as default values, when a new setting data instance is created for elements whose capabilities are defined by the associated capabilities.</span></span> <span data-ttu-id="cfb90-169">Em instâncias dos dados de configuração, para propriedades específicas com a mesma finalidade semântica, no máximo uma instância de dados de configuração deve ser especificada como padrão.</span><span class="sxs-lookup"><span data-stu-id="cfb90-169">Across instances of the setting data, for particular properties having the same semantic purpose, at most one such setting data instance must be specified as a default.</span></span><br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <span data-ttu-id="cfb90-170"><dt>**Ideal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-170"><dt>**Optimal**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="cfb90-171">A instância de dados de configuração representa os valores de configuração ideais para elementos associados aos recursos associados.</span><span class="sxs-lookup"><span data-stu-id="cfb90-171">The setting data instance represents optimal setting values for elements associated with the associated capabilities.</span></span> <span data-ttu-id="cfb90-172">Várias instâncias de dados de configuração de componente podem ser declaradas como ideal.</span><span class="sxs-lookup"><span data-stu-id="cfb90-172">Multiple component setting data instances may be declared as optimal.</span></span><br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <span data-ttu-id="cfb90-173"><dt>**Média**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-173"><dt>**Mean**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="cfb90-174">As propriedades numéricas não **nulas**, não chave, não enumeradas, não booleanas e não boolianas da instância de dados de configuração associada representam um ponto médio em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="cfb90-174">The non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the associated setting data instance represents an average point along some dimension.</span></span> <span data-ttu-id="cfb90-175">Para diferentes combinações de propriedades de dados de configuração, várias instâncias de dados de configuração de componentes podem ser declaradas como **média**.</span><span class="sxs-lookup"><span data-stu-id="cfb90-175">For different combinations of setting data properties, multiple component setting data instances may be declared as **Mean**.</span></span> <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <span data-ttu-id="cfb90-176"><dt>**Com suporte**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-176"><dt>**Supported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="cfb90-177">As propriedades não **nulas** e não-chave dos dados de configuração representam um conjunto de valores de propriedade com suporte que não são qualificados de outra forma.</span><span class="sxs-lookup"><span data-stu-id="cfb90-177">The non-**Null**, non-key properties of the setting data represents a set of supported property values that are not otherwise qualified.</span></span> <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfb90-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfb90-178">Requirements</span></span>



| <span data-ttu-id="cfb90-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb90-179">Requirement</span></span> | <span data-ttu-id="cfb90-180">Valor</span><span class="sxs-lookup"><span data-stu-id="cfb90-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb90-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfb90-181">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb90-182">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cfb90-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cfb90-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfb90-183">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb90-184">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cfb90-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cfb90-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfb90-185">Namespace</span></span><br/>                | <span data-ttu-id="cfb90-186">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cfb90-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cfb90-187">MOF</span><span class="sxs-lookup"><span data-stu-id="cfb90-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfb90-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfb90-189">DLL</span><span class="sxs-lookup"><span data-stu-id="cfb90-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfb90-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cfb90-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

