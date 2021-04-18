---
description: Representa um serviço de dispositivo virtual da plataforma Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Classe Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780973"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a><span data-ttu-id="7c95c-103">\_Classe Msvm VirtualSystemResourceComponent</span><span class="sxs-lookup"><span data-stu-id="7c95c-103">Msvm\_VirtualSystemResourceComponent class</span></span>

<span data-ttu-id="7c95c-104">Representa um serviço de dispositivo virtual da plataforma Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="7c95c-104">Represents a virtual device service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="7c95c-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7c95c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c95c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c95c-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a><span data-ttu-id="7c95c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7c95c-107">Members</span></span>

<span data-ttu-id="7c95c-108">A classe **Msvm \_ VirtualSystemResourceComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7c95c-108">The **Msvm\_VirtualSystemResourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="7c95c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7c95c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c95c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7c95c-110">Properties</span></span>

<span data-ttu-id="7c95c-111">A classe **Msvm \_ VirtualSystemResourceComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7c95c-111">The **Msvm\_VirtualSystemResourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c95c-112">**AdditionalClassNames**</span><span class="sxs-lookup"><span data-stu-id="7c95c-112">**AdditionalClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7c95c-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-115">Uma matriz de cadeias de caracteres que contém classes de não associação adicionais superfícieda por essa instância de **\_ VirtualSystemResourceComponent de Msvm** .</span><span class="sxs-lookup"><span data-stu-id="7c95c-115">An array of strings containing additional non-association classes surfaced by this **Msvm\_VirtualSystemResourceComponent** instance.</span></span> <span data-ttu-id="7c95c-116">Essas classes devem derivar de [**nenhum \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nem de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c95c-116">These classes must derive from neither [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nor [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c95c-117">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="7c95c-117">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7c95c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-120">Um GUID que representa o identificador de classe do objeto COM do serviço.</span><span class="sxs-lookup"><span data-stu-id="7c95c-120">A GUID that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="7c95c-121">Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="7c95c-121">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c95c-122">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="7c95c-122">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-123">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c95c-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-125">O contexto no qual o objeto recém-criado será executado.</span><span class="sxs-lookup"><span data-stu-id="7c95c-125">The context in which the newly created object will run.</span></span> <span data-ttu-id="7c95c-126">Esse valor é passado no parâmetro *dwClsContext* para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7c95c-126">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="7c95c-127">Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="7c95c-127">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="7c95c-128">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="7c95c-128">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7c95c-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-131">**True** se esta instância estiver habilitada e puder ser usada para concluir solicitações de cliente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7c95c-131">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="7c95c-132">Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="7c95c-132">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="7c95c-133">**HotAdd**</span><span class="sxs-lookup"><span data-stu-id="7c95c-133">**HotAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7c95c-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-136">**True** se esta instância puder ser adicionada em uma máquina virtual; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7c95c-136">**True** if this instance can be hot-added to a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="7c95c-137">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="7c95c-137">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="7c95c-138">**HotRemove**</span><span class="sxs-lookup"><span data-stu-id="7c95c-138">**HotRemove**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7c95c-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-141">**True** se esta instância puder ser removida de uma máquina virtual; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7c95c-141">**True** if this instance can be hot-removed from a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="7c95c-142">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="7c95c-142">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="7c95c-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7c95c-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7c95c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-146">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="7c95c-146">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-147">Uma cadeia de caracteres neutra em idioma que identifica exclusivamente o serviço.</span><span class="sxs-lookup"><span data-stu-id="7c95c-147">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="7c95c-148">O seguinte formato é sugerido para evitar conflitos de nomenclatura: " \| versão do componente do fornecedor \| ".</span><span class="sxs-lookup"><span data-stu-id="7c95c-148">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="7c95c-149">Por exemplo, esse nome representa a versão 1,0 do componente de porta de rede emulada da Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="7c95c-149">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="7c95c-150">Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="7c95c-150">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c95c-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c95c-151">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c95c-152">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c95c-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c95c-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c95c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c95c-154">A relação do objeto WMI que é descrita aqui com o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="7c95c-154">The relationship of the WMI object that is described here with the virtual device.</span></span>



| <span data-ttu-id="7c95c-155">Valor</span><span class="sxs-lookup"><span data-stu-id="7c95c-155">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="7c95c-156">Significado</span><span class="sxs-lookup"><span data-stu-id="7c95c-156">Meaning</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <span data-ttu-id="7c95c-157"><dt>**"Não alterado"**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c95c-157"><dt>**"Not Changeable"**</dt> <dt>0</dt></span></span> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <span data-ttu-id="7c95c-158"><dt>**"Singleton"**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7c95c-158"><dt>**"Singleton"**</dt> <dt>1</dt></span></span> </dl>                     | <span data-ttu-id="7c95c-159">Singleton é um objeto WMI de nível superior que está vinculado 1:1 a um dispositivo virtual e só pode existir uma vez por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7c95c-159">Singleton is a top level WMI object that is tied 1:1 with a Virtual Device and can only exist once per virtual machine.</span></span> <span data-ttu-id="7c95c-160">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="7c95c-160">This is the default value.</span></span><br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <span data-ttu-id="7c95c-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7c95c-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="7c95c-162">MultiInstance é um objeto WMI de nível superior que pode existir várias vezes por máquina virtual e está vinculado 1:1 a um dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="7c95c-162">MultiInstance is a top level WMI object that can exist multiple times per virtual machine and is tied 1:1 with a Virtual Device.</span></span><br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <span data-ttu-id="7c95c-163"><dt>**"Subdispositivo"**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7c95c-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span></span> </dl>                     | <span data-ttu-id="7c95c-164">O subdispositivo é um objeto WMI que não tem referência pai, mas é controlado por apenas um dispositivo virtual que pode existir apenas uma vez por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7c95c-164">Subdevice is a WMI object that has not parent reference but is controlled by only one Virtual Device that can exist only once per virtual machine.</span></span> <span data-ttu-id="7c95c-165">Embora o objeto WMI possa existir várias vezes.</span><span class="sxs-lookup"><span data-stu-id="7c95c-165">The WMI object though can exist multiples times.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c95c-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c95c-166">Remarks</span></span>

<span data-ttu-id="7c95c-167">O acesso à classe **Msvm \_ VirtualSystemResourceComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="7c95c-167">Access to the **Msvm\_VirtualSystemResourceComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7c95c-168">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7c95c-168">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c95c-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c95c-169">Requirements</span></span>



| <span data-ttu-id="7c95c-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c95c-170">Requirement</span></span> | <span data-ttu-id="7c95c-171">Valor</span><span class="sxs-lookup"><span data-stu-id="7c95c-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c95c-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c95c-172">Minimum supported client</span></span><br/> | <span data-ttu-id="7c95c-173">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c95c-173">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7c95c-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c95c-174">Minimum supported server</span></span><br/> | <span data-ttu-id="7c95c-175">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c95c-175">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c95c-176">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7c95c-176">End of client support</span></span><br/>    | <span data-ttu-id="7c95c-177">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7c95c-177">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7c95c-178">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7c95c-178">End of server support</span></span><br/>    | <span data-ttu-id="7c95c-179">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7c95c-179">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7c95c-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c95c-180">Namespace</span></span><br/>                | <span data-ttu-id="7c95c-181">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7c95c-181">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7c95c-182">MOF</span><span class="sxs-lookup"><span data-stu-id="7c95c-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c95c-183"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c95c-183"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c95c-184">DLL</span><span class="sxs-lookup"><span data-stu-id="7c95c-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c95c-185"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c95c-185"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c95c-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c95c-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c95c-187">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="7c95c-187">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="7c95c-188">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="7c95c-188">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

