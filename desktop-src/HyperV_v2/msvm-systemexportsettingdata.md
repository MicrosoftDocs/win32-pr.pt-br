---
description: Associa uma máquina virtual e seus dados de configuração de exportação.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Classe Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752472"
---
# <a name="msvm_systemexportsettingdata-class"></a><span data-ttu-id="a663e-103">\_Classe Msvm SystemExportSettingData</span><span class="sxs-lookup"><span data-stu-id="a663e-103">Msvm\_SystemExportSettingData class</span></span>

<span data-ttu-id="a663e-104">Associa uma máquina virtual e seus dados de configuração de exportação.</span><span class="sxs-lookup"><span data-stu-id="a663e-104">Associates a virtual machine and its export setting data.</span></span> <span data-ttu-id="a663e-105">Antes de chamar o método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) , uma instância de [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) pode ser recuperada usando essa associação.</span><span class="sxs-lookup"><span data-stu-id="a663e-105">Before calling the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class, an instance of [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) can be retrieved using this association.</span></span>

<span data-ttu-id="a663e-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a663e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a663e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a663e-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="a663e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a663e-108">Members</span></span>

<span data-ttu-id="a663e-109">A classe **Msvm \_ SystemExportSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a663e-109">The **Msvm\_SystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a663e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a663e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a663e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a663e-111">Properties</span></span>

<span data-ttu-id="a663e-112">A classe **Msvm \_ SystemExportSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a663e-112">The **Msvm\_SystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a663e-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="a663e-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a663e-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a663e-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a663e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a663e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a663e-116">Indica se a configuração referenciada está sendo usada no momento na operação do elemento ou se essas informações são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="a663e-116">Indicates if the referenced setting is currently being used in the operation of the element, or that this information is unknown.</span></span> <span data-ttu-id="a663e-117">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a663e-117">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="a663e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a663e-118">Value</span></span>                                                                        | <span data-ttu-id="a663e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="a663e-119">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="a663e-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-120"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a663e-121">Unknown</span><span class="sxs-lookup"><span data-stu-id="a663e-121">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="a663e-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a663e-123">Current</span><span class="sxs-lookup"><span data-stu-id="a663e-123">Current</span></span><br/>     |
| <dl> <span data-ttu-id="a663e-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a663e-125">Não atual</span><span class="sxs-lookup"><span data-stu-id="a663e-125">Not Current</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a663e-126">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="a663e-126">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a663e-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a663e-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a663e-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a663e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a663e-129">Indica se a configuração referenciada é uma configuração padrão para o elemento ou se essas informações são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="a663e-129">Indicates if the referenced setting is a default setting for the element, or that this information is unknown.</span></span> <span data-ttu-id="a663e-130">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a663e-130">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="a663e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a663e-131">Value</span></span>                                                                        | <span data-ttu-id="a663e-132">Significado</span><span class="sxs-lookup"><span data-stu-id="a663e-132">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="a663e-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a663e-134">Unknown</span><span class="sxs-lookup"><span data-stu-id="a663e-134">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="a663e-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a663e-136">Padrão</span><span class="sxs-lookup"><span data-stu-id="a663e-136">Default</span></span><br/>     |
| <dl> <span data-ttu-id="a663e-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a663e-138">Não padrão</span><span class="sxs-lookup"><span data-stu-id="a663e-138">Not Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a663e-139">**Isnext**</span><span class="sxs-lookup"><span data-stu-id="a663e-139">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a663e-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a663e-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a663e-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a663e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a663e-142">Indica se a configuração referenciada é a próxima configuração a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="a663e-142">Indicates whether or not the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="a663e-143">Por exemplo, o aplicativo pode ocorrer em uma solicitação de reinicialização, redefinição e reconfiguração.</span><span class="sxs-lookup"><span data-stu-id="a663e-143">For example, the application could take place on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="a663e-144">Essa pode ser uma configuração permanente ou uma configuração usada apenas uma vez, conforme indicado pelo sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a663e-144">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="a663e-145">Se for uma configuração permanente, a configuração será aplicada toda vez que o elemento gerenciado for reinicializado, até que esse sinalizador seja redefinido manualmente.</span><span class="sxs-lookup"><span data-stu-id="a663e-145">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="a663e-146">No entanto, se for um uso único, o sinalizador será limpo automaticamente depois que as configurações forem aplicadas.</span><span class="sxs-lookup"><span data-stu-id="a663e-146">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="a663e-147">Além disso, se esse sinalizador for especificado (ou seja, definido com um valor diferente de 0 (desconhecido)), isso terá precedência sobre quaisquer dados de configuração que possam ter sido especificados como padrão.</span><span class="sxs-lookup"><span data-stu-id="a663e-147">Also, if this flag is specified (i.e. set to value other than 0 (Unknown)), then this takes precedence over any setting data that may have been specified as default.</span></span> <span data-ttu-id="a663e-148">Por exemplo: se o elemento gerenciado for um sistema de computador e o valor desse sinalizador for 1 (próximo), a configuração entrará em vigor na próxima vez que o sistema for redefinido.</span><span class="sxs-lookup"><span data-stu-id="a663e-148">For example: If the managed element is a computer system, and the value of this flag is 1 (Is Next), then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="a663e-149">E, a menos que esse sinalizador seja alterado, ele será mantido para redefinições subsequentes do sistema.</span><span class="sxs-lookup"><span data-stu-id="a663e-149">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="a663e-150">No entanto, se esse sinalizador for definido como 3 (é próximo para uso único), essa configuração será usada apenas uma vez e o sinalizador será redefinido depois de 2 (não está próximo).</span><span class="sxs-lookup"><span data-stu-id="a663e-150">However, if this flag is set to 3 (Is Next For Single Use), then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="a663e-151">Portanto, no exemplo acima, se o sistema reinicializar em uma rápida sucessão, a configuração não será usada na segunda reinicialização.</span><span class="sxs-lookup"><span data-stu-id="a663e-151">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<span data-ttu-id="a663e-152">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a663e-152">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="a663e-153">Valor</span><span class="sxs-lookup"><span data-stu-id="a663e-153">Value</span></span>                                                                        | <span data-ttu-id="a663e-154">Significado</span><span class="sxs-lookup"><span data-stu-id="a663e-154">Meaning</span></span>                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="a663e-155"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-155"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a663e-156">Unknown</span><span class="sxs-lookup"><span data-stu-id="a663e-156">Unknown</span></span><br/>                |
| <dl> <span data-ttu-id="a663e-157"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-157"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a663e-158">É o próximo</span><span class="sxs-lookup"><span data-stu-id="a663e-158">Is Next</span></span><br/>                |
| <dl> <span data-ttu-id="a663e-159"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-159"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a663e-160">Não é o próximo</span><span class="sxs-lookup"><span data-stu-id="a663e-160">Is Not Next</span></span><br/>            |
| <dl> <span data-ttu-id="a663e-161"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-161"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a663e-162">É o próximo para uso único</span><span class="sxs-lookup"><span data-stu-id="a663e-162">Is Next For Single Use</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a663e-163">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="a663e-163">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a663e-164">Tipo de dados: **[ **\_ sistema de ComputerSystem CIM**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="a663e-164">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a663e-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a663e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a663e-166">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. managedelement")</span><span class="sxs-lookup"><span data-stu-id="a663e-166">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="a663e-167">Referência à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a663e-167">Reference to the virtual machine.</span></span> <span data-ttu-id="a663e-168">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a663e-168">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a663e-169">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="a663e-169">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a663e-170">Tipo de dados: **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="a663e-170">Data type: **[**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a663e-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a663e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a663e-172">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")</span><span class="sxs-lookup"><span data-stu-id="a663e-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.SettingData")</span></span>
</dt> </dl>

<span data-ttu-id="a663e-173">Referência aos dados de configuração de exportação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a663e-173">Reference to the export setting data for the virtual machine.</span></span> <span data-ttu-id="a663e-174">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a663e-174">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a663e-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="a663e-175">Remarks</span></span>

<span data-ttu-id="a663e-176">O acesso à classe **Msvm \_ SystemExportSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="a663e-176">Access to the **Msvm\_SystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a663e-177">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a663e-177">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a663e-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a663e-178">Requirements</span></span>



| <span data-ttu-id="a663e-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="a663e-179">Requirement</span></span> | <span data-ttu-id="a663e-180">Valor</span><span class="sxs-lookup"><span data-stu-id="a663e-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a663e-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a663e-181">Minimum supported client</span></span><br/> | <span data-ttu-id="a663e-182">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a663e-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a663e-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a663e-183">Minimum supported server</span></span><br/> | <span data-ttu-id="a663e-184">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a663e-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a663e-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="a663e-185">Namespace</span></span><br/>                | <span data-ttu-id="a663e-186">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a663e-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a663e-187">MOF</span><span class="sxs-lookup"><span data-stu-id="a663e-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a663e-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a663e-189">DLL</span><span class="sxs-lookup"><span data-stu-id="a663e-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a663e-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a663e-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

