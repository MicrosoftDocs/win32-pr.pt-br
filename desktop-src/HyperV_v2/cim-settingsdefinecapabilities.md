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
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758986"
---
# <a name="cim_settingsdefinecapabilities-class"></a><span data-ttu-id="dbcda-103">\_Classe CIM SettingsDefineCapabilities</span><span class="sxs-lookup"><span data-stu-id="dbcda-103">CIM\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="dbcda-104">Representa uma associação entre as propriedades de uma instância do [**CIM \_ SettingData**](cim-settingdata.md) e uma instância de [**\_ recursos de CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcda-104">Represents an association between properties of a [**CIM\_SettingData**](cim-settingdata.md) instance and a [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcda-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbcda-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="dbcda-106">Membros</span><span class="sxs-lookup"><span data-stu-id="dbcda-106">Members</span></span>

<span data-ttu-id="dbcda-107">A classe **CIM \_ SettingsDefineCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dbcda-107">The **CIM\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="dbcda-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbcda-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbcda-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbcda-109">Properties</span></span>

<span data-ttu-id="dbcda-110">A classe **CIM \_ SettingsDefineCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dbcda-110">The **CIM\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbcda-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="dbcda-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbcda-112">Tipo de dados **: \_ recursos CIM**</span><span class="sxs-lookup"><span data-stu-id="dbcda-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbcda-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-114">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dbcda-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dbcda-115">Uma referência à instância [**de \_ recursos de CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcda-115">A reference to the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="dbcda-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dbcda-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbcda-117">Tipo de dados: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="dbcda-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbcda-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="dbcda-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="dbcda-120">Uma referência à instância de [**CIM \_ SettingData**](cim-settingdata.md) usada para definir a instância de [**\_ recursos de CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcda-120">A reference to the [**CIM\_SettingData**](cim-settingdata.md) instance used to define the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="dbcda-121">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="dbcda-121">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbcda-122">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbcda-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbcda-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-124">Qualificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="dbcda-124">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**ValueRole**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="dbcda-125">Indica se as propriedades não nulas e não-chave da instância de [**CIM \_ SettingData**](cim-settingdata.md) associada são tratadas de forma independente ou como um conjunto correlacionado.</span><span class="sxs-lookup"><span data-stu-id="dbcda-125">Indicates whether the non-null, non-key properties of the associated [**CIM\_SettingData**](cim-settingdata.md) instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="dbcda-126">Por exemplo, um conjunto independente de propriedades máximas pode ser definido quando não há nenhuma relação entre cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="dbcda-126">For instance, an independent set of maximum properties might be defined when there is no relationship between each property.</span></span> <span data-ttu-id="dbcda-127">Por outro lado, vários conjuntos correlacionados de propriedades máximas podem precisar ser definidos quando os valores máximos de cada um dependem de alguns dos outros.</span><span class="sxs-lookup"><span data-stu-id="dbcda-127">In contrast, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="dbcda-128">**Independente** (0)</span><span class="sxs-lookup"><span data-stu-id="dbcda-128">**Independent** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

<span data-ttu-id="dbcda-129">**Correlacionado** (1)</span><span class="sxs-lookup"><span data-stu-id="dbcda-129">**Correlated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dbcda-130">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dbcda-130">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbcda-131">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="dbcda-131">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbcda-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbcda-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbcda-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-134">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRole**")</span><span class="sxs-lookup"><span data-stu-id="dbcda-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRole**")</span></span>
</dt> </dl>

<span data-ttu-id="dbcda-135">Indica o tipo de intervalo de valores usado pelas propriedades das propriedades não nulas e não chave da instância do [**CIM \_ SettingData**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcda-135">Indicates the type of value range used by properties of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="dbcda-136">**Ponto** (0)</span><span class="sxs-lookup"><span data-stu-id="dbcda-136">**Point** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

<span data-ttu-id="dbcda-137">**Mínimos** (1)</span><span class="sxs-lookup"><span data-stu-id="dbcda-137">**Minimums** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

<span data-ttu-id="dbcda-138">**Máximo** (2)</span><span class="sxs-lookup"><span data-stu-id="dbcda-138">**Maximums** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

<span data-ttu-id="dbcda-139">**Incrementos** (3)</span><span class="sxs-lookup"><span data-stu-id="dbcda-139">**Increments** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dbcda-140">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dbcda-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbcda-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="dbcda-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbcda-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbcda-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbcda-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbcda-144">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="dbcda-144">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="dbcda-145">A semântica adicional para a interpretação das propriedades não nulas e não chave da instância do [**CIM \_ SettingData**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcda-145">The additional semantics for the interpretation of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<span data-ttu-id="dbcda-146">"Default" indica que os valores de propriedade da instância do componente SettingData serão usados como valores padrão, quando uma nova instância de SettingData for criada para elementos cujos recursos são definidos pela instância de recursos associados.</span><span class="sxs-lookup"><span data-stu-id="dbcda-146">"Default" indicates that property values of the component SettingData instance will be used as default values, when a new SettingData instance is created for elements whose capabilities are defined by the associated Capabilities instance.</span></span>

<span data-ttu-id="dbcda-147">Em instâncias de SettingData, para propriedades específicas com a mesma finalidade semântica, no máximo uma dessas instâncias de SettingData deve ser especificada como padrão.</span><span class="sxs-lookup"><span data-stu-id="dbcda-147">Across instances of settingdata, for particular properties having the same semantic purpose, at most one such settingdata instance shall be specified as a default.</span></span>

<span data-ttu-id="dbcda-148">"Ideal" indica que a instância de SettingData representa valores de configuração ideais para elementos associados à instância de recursos associados.</span><span class="sxs-lookup"><span data-stu-id="dbcda-148">"Optimal" indicates that the SettingData instance represents optimal setting values for elements associated with the associated capabilities instance.</span></span> <span data-ttu-id="dbcda-149">Várias instâncias do componente SettingData podem ser declaradas como ótimas. " Mean "indica que as propriedades numéricas não-nulas, não chave, não enumeradas, não boolianas da instância SettingData associada representam um ponto médio em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="dbcda-149">Multiple component SettingData instances may be declared as optimal."Mean" indicates that the non-null, non-key, non-enumerated, non-boolean, numeric properties of the associated SettingData instance represents an average point along some dimension.</span></span> <span data-ttu-id="dbcda-150">Para diferentes combinações de propriedades SettingData, várias instâncias do componente SettingData podem ser declaradas como "Mean".</span><span class="sxs-lookup"><span data-stu-id="dbcda-150">For different combinations of SettingData properties, multiple component SettingData instances may be declared as "Mean".</span></span> <span data-ttu-id="dbcda-151">"Supported" indica que as propriedades não nulas e não chave da instância do componente SettingData representam um conjunto de valores de propriedade com suporte que não são qualificados de outra forma.</span><span class="sxs-lookup"><span data-stu-id="dbcda-151">"Supported" indicates that the non-null, non-key properties of the Component SettingData instance represents a set of supported property values that are not otherwise qualified.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="dbcda-152">**Padrão** (0)</span><span class="sxs-lookup"><span data-stu-id="dbcda-152">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

<span data-ttu-id="dbcda-153">**Ideal** (1)</span><span class="sxs-lookup"><span data-stu-id="dbcda-153">**Optimal** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

<span data-ttu-id="dbcda-154">**Média** (2)</span><span class="sxs-lookup"><span data-stu-id="dbcda-154">**Mean** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="dbcda-155">**Com suporte** (3)</span><span class="sxs-lookup"><span data-stu-id="dbcda-155">**Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dbcda-156">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dbcda-156">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="dbcda-157"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dbcda-157"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dbcda-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbcda-158">Requirements</span></span>



| <span data-ttu-id="dbcda-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbcda-159">Requirement</span></span> | <span data-ttu-id="dbcda-160">Valor</span><span class="sxs-lookup"><span data-stu-id="dbcda-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbcda-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbcda-161">Minimum supported client</span></span><br/> | <span data-ttu-id="dbcda-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dbcda-162">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dbcda-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbcda-163">Minimum supported server</span></span><br/> | <span data-ttu-id="dbcda-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbcda-164">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dbcda-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbcda-165">Namespace</span></span><br/>                | <span data-ttu-id="dbcda-166">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dbcda-166">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dbcda-167">MOF</span><span class="sxs-lookup"><span data-stu-id="dbcda-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbcda-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbcda-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbcda-169">DLL</span><span class="sxs-lookup"><span data-stu-id="dbcda-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbcda-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbcda-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbcda-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbcda-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbcda-172">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="dbcda-172">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

