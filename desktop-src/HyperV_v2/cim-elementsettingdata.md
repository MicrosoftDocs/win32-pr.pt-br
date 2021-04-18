---
description: Representa uma associação entre um elemento gerenciado e seus dados de configuração associados. Essa associação também descreve se esta é uma configuração padrão ou atual.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Classe CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780541"
---
# <a name="cim_elementsettingdata-class"></a><span data-ttu-id="d0548-104">\_Classe CIM ElementSettingData</span><span class="sxs-lookup"><span data-stu-id="d0548-104">CIM\_ElementSettingData class</span></span>

<span data-ttu-id="d0548-105">Representa uma associação entre um elemento gerenciado e seus dados de configuração associados.</span><span class="sxs-lookup"><span data-stu-id="d0548-105">Represents an association between a managed element and its associated setting data.</span></span> <span data-ttu-id="d0548-106">Essa associação também descreve se esta é uma configuração padrão ou atual.</span><span class="sxs-lookup"><span data-stu-id="d0548-106">This association also describes whether this is a default or current setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0548-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0548-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a><span data-ttu-id="d0548-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d0548-108">Members</span></span>

<span data-ttu-id="d0548-109">A classe **CIM \_ ElementSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d0548-109">The **CIM\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d0548-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d0548-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0548-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d0548-111">Properties</span></span>

<span data-ttu-id="d0548-112">A classe **CIM \_ ElementSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d0548-112">The **CIM\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0548-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="d0548-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0548-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0548-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0548-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0548-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0548-116">Indica se a configuração referenciada está sendo usada no momento pelo elemento.</span><span class="sxs-lookup"><span data-stu-id="d0548-116">Indicates whether the referenced setting is currently being used by the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0548-117">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d0548-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

<span data-ttu-id="d0548-118">**Está atual** (1)</span><span class="sxs-lookup"><span data-stu-id="d0548-118">**Is Current** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

<span data-ttu-id="d0548-119">**Não é atual** (2)</span><span class="sxs-lookup"><span data-stu-id="d0548-119">**Is Not Current** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0548-120">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="d0548-120">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0548-121">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0548-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0548-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0548-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0548-123">Indicando se a configuração é uma configuração padrão para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d0548-123">Indicating whether the setting is a default setting for the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0548-124">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d0548-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

<span data-ttu-id="d0548-125">**É padrão** (1)</span><span class="sxs-lookup"><span data-stu-id="d0548-125">**Is Default** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

<span data-ttu-id="d0548-126">**Não é o padrão** (2)</span><span class="sxs-lookup"><span data-stu-id="d0548-126">**Is Not Default** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0548-127">**Isnext**</span><span class="sxs-lookup"><span data-stu-id="d0548-127">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0548-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0548-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0548-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0548-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0548-130">Um sinalizador que indica quando e com que frequência aplicar a configuração.</span><span class="sxs-lookup"><span data-stu-id="d0548-130">A flag that indicates when and how often to apply the setting.</span></span>

<span data-ttu-id="d0548-131">Por exemplo, a configuração pode ser aplicada em uma solicitação de reinicialização, redefinição e reconfiguração.</span><span class="sxs-lookup"><span data-stu-id="d0548-131">For example, the setting could be applied on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="d0548-132">Essa pode ser uma configuração permanente ou uma configuração usada apenas uma vez, conforme indicado pelo sinalizador.</span><span class="sxs-lookup"><span data-stu-id="d0548-132">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="d0548-133">Se for uma configuração permanente, a configuração será aplicada toda vez que o elemento gerenciado for reinicializado, até que esse sinalizador seja redefinido manualmente.</span><span class="sxs-lookup"><span data-stu-id="d0548-133">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="d0548-134">No entanto, se for um uso único, o sinalizador será limpo automaticamente depois que as configurações forem aplicadas.</span><span class="sxs-lookup"><span data-stu-id="d0548-134">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="d0548-135">Além disso, se esse sinalizador for definido com um valor diferente de 0 (desconhecido), isso terá precedência sobre uma propriedade **SettingData** definida como "padrão".</span><span class="sxs-lookup"><span data-stu-id="d0548-135">In addition, if this flag is set to value other than 0 (Unknown), then this takes precedence over a **SettingData** property that is set to "Default".</span></span>

<span data-ttu-id="d0548-136">Se o elemento gerenciado for um sistema de computador, e o valor desse sinalizador for "Next", a configuração entrará em vigor na próxima vez que o sistema for redefinido.</span><span class="sxs-lookup"><span data-stu-id="d0548-136">If the managed element is a computer system, and the value of this flag is "Is Next", then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="d0548-137">E, a menos que esse sinalizador seja alterado, ele será mantido para redefinições subsequentes do sistema.</span><span class="sxs-lookup"><span data-stu-id="d0548-137">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="d0548-138">No entanto, se esse sinalizador for definido como "é próximo para uso único", essa configuração será usada apenas uma vez e o sinalizador será redefinido depois disso para 2 (não é próximo).</span><span class="sxs-lookup"><span data-stu-id="d0548-138">However, if this flag is set to "Is Next For Single Use", then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="d0548-139">Portanto, no exemplo acima, se o sistema reinicializar em uma rápida sucessão, a configuração não será usada na segunda reinicialização.</span><span class="sxs-lookup"><span data-stu-id="d0548-139">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0548-140">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d0548-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

<span data-ttu-id="d0548-141">**É próximo** (1)</span><span class="sxs-lookup"><span data-stu-id="d0548-141">**Is Next** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

<span data-ttu-id="d0548-142">**Não é próximo** (2)</span><span class="sxs-lookup"><span data-stu-id="d0548-142">**Is Not Next** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

<span data-ttu-id="d0548-143">**É o próximo para uso único** (3)</span><span class="sxs-lookup"><span data-stu-id="d0548-143">**Is Next For Single Use** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0548-144">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="d0548-144">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0548-145">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="d0548-145">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d0548-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0548-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0548-147">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d0548-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d0548-148">O elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d0548-148">The managed element.</span></span>

</dd> <dt>

<span data-ttu-id="d0548-149">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="d0548-149">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0548-150">Tipo de dados: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="d0548-150">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d0548-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0548-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0548-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d0548-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d0548-153">Os dados de configuração associados ao elemento.</span><span class="sxs-lookup"><span data-stu-id="d0548-153">The setting data associated with the element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0548-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0548-154">Requirements</span></span>



| <span data-ttu-id="d0548-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0548-155">Requirement</span></span> | <span data-ttu-id="d0548-156">Valor</span><span class="sxs-lookup"><span data-stu-id="d0548-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0548-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0548-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d0548-158">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d0548-158">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d0548-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0548-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d0548-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0548-160">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d0548-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0548-161">Namespace</span></span><br/>                | <span data-ttu-id="d0548-162">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d0548-162">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d0548-163">MOF</span><span class="sxs-lookup"><span data-stu-id="d0548-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0548-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0548-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0548-165">DLL</span><span class="sxs-lookup"><span data-stu-id="d0548-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0548-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d0548-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

