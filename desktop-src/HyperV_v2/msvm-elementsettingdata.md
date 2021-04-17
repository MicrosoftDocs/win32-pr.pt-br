---
description: Associa um elemento gerenciado a seus dados de configuração.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Classe Msvm_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759244"
---
# <a name="msvm_elementsettingdata-class"></a><span data-ttu-id="d67b5-103">\_Classe Msvm ElementSettingData</span><span class="sxs-lookup"><span data-stu-id="d67b5-103">Msvm\_ElementSettingData class</span></span>

<span data-ttu-id="d67b5-104">Associa um elemento gerenciado a seus dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="d67b5-104">Associates a managed element with its configuration data.</span></span> <span data-ttu-id="d67b5-105">Alguns dos aplicativos mais notáveis dessa associação são o seu uso na vinculação de uma máquina virtual e dos dispositivos lógicos que foram atribuídos a esse sistema com suas informações de configuração de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="d67b5-105">Some of the more notable applications of this association are its use in linking a virtual machine and the logical devices that have been assigned to that system with their snapshot configuration information.</span></span> <span data-ttu-id="d67b5-106">As informações de configuração atuais são associadas à máquina virtual e seus dispositivos por meio da Associação [**Msvm \_ SettingsDefineState**](msvm-settingsdefinestate.md) .</span><span class="sxs-lookup"><span data-stu-id="d67b5-106">Current configuration information is associated with the virtual machine and its devices through the [**Msvm\_SettingsDefineState**](msvm-settingsdefinestate.md) association.</span></span>

<span data-ttu-id="d67b5-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d67b5-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d67b5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d67b5-108">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="d67b5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d67b5-109">Members</span></span>

<span data-ttu-id="d67b5-110">A classe **Msvm \_ ElementSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d67b5-110">The **Msvm\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d67b5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d67b5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d67b5-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d67b5-112">Properties</span></span>

<span data-ttu-id="d67b5-113">A classe **Msvm \_ ElementSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d67b5-113">The **Msvm\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d67b5-114">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="d67b5-114">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d67b5-115">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d67b5-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d67b5-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d67b5-117">Indica que a configuração referenciada está sendo usada no momento na operação do elemento ou que essas informações são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="d67b5-117">Indicates that the referenced setting is currently being used in the operation of the element or that this information is unknown.</span></span> <span data-ttu-id="d67b5-118">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d67b5-118">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="d67b5-119">O valor padrão é 0 (desconhecido).</span><span class="sxs-lookup"><span data-stu-id="d67b5-119">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="d67b5-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d67b5-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Está atual** (1)</span><span class="sxs-lookup"><span data-stu-id="d67b5-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Is Current** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Não é atual** (2)</span><span class="sxs-lookup"><span data-stu-id="d67b5-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Is Not Current** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d67b5-123">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="d67b5-123">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d67b5-124">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d67b5-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d67b5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d67b5-126">Indica que a configuração referenciada é uma configuração padrão para o elemento ou que essas informações são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="d67b5-126">Indicates that the referenced setting is a default setting for the element or that this information is unknown.</span></span> <span data-ttu-id="d67b5-127">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d67b5-127">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="d67b5-128">O valor padrão é 0 (desconhecido).</span><span class="sxs-lookup"><span data-stu-id="d67b5-128">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="d67b5-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d67b5-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**É padrão** (1)</span><span class="sxs-lookup"><span data-stu-id="d67b5-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Is Default** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Não é o padrão** (2)</span><span class="sxs-lookup"><span data-stu-id="d67b5-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Is Not Default** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d67b5-132">**Isnext**</span><span class="sxs-lookup"><span data-stu-id="d67b5-132">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d67b5-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d67b5-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d67b5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d67b5-135">Indica se a configuração referenciada é a próxima configuração a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d67b5-135">Indicates whether the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="d67b5-136">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d67b5-136">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="d67b5-137">O valor padrão é 0 (desconhecido).</span><span class="sxs-lookup"><span data-stu-id="d67b5-137">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="d67b5-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d67b5-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**É próximo** (1)</span><span class="sxs-lookup"><span data-stu-id="d67b5-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Is Next** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Não é próximo** (2)</span><span class="sxs-lookup"><span data-stu-id="d67b5-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Is Not Next** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**É o próximo para uso único** (3)</span><span class="sxs-lookup"><span data-stu-id="d67b5-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Is Next For Single Use** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d67b5-142">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="d67b5-142">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d67b5-143">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="d67b5-143">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d67b5-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d67b5-145">Referência à máquina virtual ou dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d67b5-145">Reference to the virtual machine or virtual device.</span></span> <span data-ttu-id="d67b5-146">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d67b5-146">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d67b5-147">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="d67b5-147">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d67b5-148">Tipo de dados: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d67b5-148">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="d67b5-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d67b5-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d67b5-150">Referência às configurações de instantâneo para a máquina virtual ou dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d67b5-150">Reference to the snapshotted settings for the virtual machine or virtual device.</span></span> <span data-ttu-id="d67b5-151">Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d67b5-151">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d67b5-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="d67b5-152">Remarks</span></span>

<span data-ttu-id="d67b5-153">O acesso à classe **Msvm \_ ElementSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d67b5-153">Access to the **Msvm\_ElementSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d67b5-154">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d67b5-154">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d67b5-155">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d67b5-155">Examples</span></span>

<span data-ttu-id="d67b5-156">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d67b5-156">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d67b5-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d67b5-157">Requirements</span></span>



| <span data-ttu-id="d67b5-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="d67b5-158">Requirement</span></span> | <span data-ttu-id="d67b5-159">Valor</span><span class="sxs-lookup"><span data-stu-id="d67b5-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d67b5-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d67b5-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d67b5-161">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d67b5-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d67b5-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d67b5-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d67b5-163">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d67b5-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d67b5-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="d67b5-164">Namespace</span></span><br/>                | <span data-ttu-id="d67b5-165">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d67b5-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d67b5-166">MOF</span><span class="sxs-lookup"><span data-stu-id="d67b5-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d67b5-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d67b5-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d67b5-168">DLL</span><span class="sxs-lookup"><span data-stu-id="d67b5-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d67b5-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d67b5-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d67b5-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="d67b5-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d67b5-171">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d67b5-171">**CIM\_ElementSettingData**</span></span>](cim-elementsettingdata.md)
</dt> <dt>

[<span data-ttu-id="d67b5-172">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d67b5-172">**CIM\_ElementSettingData**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[<span data-ttu-id="d67b5-173">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="d67b5-173">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

