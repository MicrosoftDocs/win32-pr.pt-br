---
description: Essa associação indica que uma subclasse de dispositivo lógico (por exemplo, um volume de armazenamento) é conectada por meio de um controlador de protocolo específico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Classe Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761710"
---
# <a name="msvm_protocolcontrollerforunit-class"></a><span data-ttu-id="7f91e-103">\_Classe Msvm ProtocolControllerForUnit</span><span class="sxs-lookup"><span data-stu-id="7f91e-103">Msvm\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="7f91e-104">Essa associação indica que uma subclasse de dispositivo lógico (por exemplo, um volume de armazenamento) é conectada por meio de um controlador de protocolo específico.</span><span class="sxs-lookup"><span data-stu-id="7f91e-104">This association indicates that a subclass of logical device (for example a storage volume) is connected through a specific protocol controller.</span></span> <span data-ttu-id="7f91e-105">Em muitas situações (por exemplo, mascaramento de LUN de armazenamento), pode haver muitas dessas associações usadas para se relacionar a objetos diferentes.</span><span class="sxs-lookup"><span data-stu-id="7f91e-105">In many situations (for example storage LUN masking), there may be many of these associations used to relate to different objects.</span></span> <span data-ttu-id="7f91e-106">Portanto, as subclasses foram definidas para otimizar a enumeração das associações.</span><span class="sxs-lookup"><span data-stu-id="7f91e-106">Therefore, subclasses have been defined to optimize enumeration of the associations.</span></span>

<span data-ttu-id="7f91e-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7f91e-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f91e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f91e-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="7f91e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="7f91e-109">Members</span></span>

<span data-ttu-id="7f91e-110">A classe **Msvm \_ ProtocolControllerForUnit** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7f91e-110">The **Msvm\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="7f91e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7f91e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f91e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7f91e-112">Properties</span></span>

<span data-ttu-id="7f91e-113">A classe **Msvm \_ ProtocolControllerForUnit** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7f91e-113">The **Msvm\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f91e-114">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="7f91e-114">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f91e-115">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f91e-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f91e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f91e-117">A prioridade fornecida para acessar o dispositivo por meio desse controlador.</span><span class="sxs-lookup"><span data-stu-id="7f91e-117">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="7f91e-118">O caminho de prioridade mais alta terá o valor mais baixo para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7f91e-118">The highest priority path will have the lowest value for this parameter.</span></span> <span data-ttu-id="7f91e-119">Essa classe é herdada do **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="7f91e-119">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> <dt>

<span data-ttu-id="7f91e-120">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="7f91e-120">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f91e-121">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f91e-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f91e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f91e-123">Indica se o controlador está ativando ou acessando ativamente o dispositivo (2) ou não (3).</span><span class="sxs-lookup"><span data-stu-id="7f91e-123">Indicates whether the controller is actively commanding or accessing the device (2) or not (3).</span></span> <span data-ttu-id="7f91e-124">Além disso, o valor, 0 (desconhecido), pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="7f91e-124">Also, the value, 0 (Unknown), can be defined.</span></span> <span data-ttu-id="7f91e-125">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores de protocolo.</span><span class="sxs-lookup"><span data-stu-id="7f91e-125">This information is necessary when a logical device can be commanded by, or accessed through, multiple protocol controllers.</span></span> <span data-ttu-id="7f91e-126">Essa classe é herdada do **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="7f91e-126">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

<dl> <dt>

<span data-ttu-id="7f91e-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7f91e-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Ativo** (2)</span><span class="sxs-lookup"><span data-stu-id="7f91e-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inativo** (3)</span><span class="sxs-lookup"><span data-stu-id="7f91e-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactive** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f91e-130">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="7f91e-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f91e-131">Tipo de dados: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span><span class="sxs-lookup"><span data-stu-id="7f91e-131">Data type: **[**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f91e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f91e-133">O controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="7f91e-133">The protocol controller.</span></span> <span data-ttu-id="7f91e-134">Essa classe é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7f91e-134">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7f91e-135">**Depende**</span><span class="sxs-lookup"><span data-stu-id="7f91e-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f91e-136">Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="7f91e-136">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f91e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f91e-138">O dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="7f91e-138">The controlled device.</span></span> <span data-ttu-id="7f91e-139">Essa classe é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7f91e-139">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7f91e-140">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="7f91e-140">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f91e-141">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f91e-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f91e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f91e-143">Os direitos de acesso concedidos ao dispositivo por meio desse controlador.</span><span class="sxs-lookup"><span data-stu-id="7f91e-143">The access rights granted to the device through this controller.</span></span> <span data-ttu-id="7f91e-144">Essa classe é herdada do **CIM \_ ProtocolControllerForUnit**.</span><span class="sxs-lookup"><span data-stu-id="7f91e-144">This class is inherited from **CIM\_ProtocolControllerForUnit**.</span></span>



| <span data-ttu-id="7f91e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7f91e-145">Value</span></span>                                                                               | <span data-ttu-id="7f91e-146">Significado</span><span class="sxs-lookup"><span data-stu-id="7f91e-146">Meaning</span></span>                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="7f91e-147"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-147"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="7f91e-148">Unknown</span><span class="sxs-lookup"><span data-stu-id="7f91e-148">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="7f91e-149"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-149"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="7f91e-150">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="7f91e-150">Read/Write</span></span><br/>      |
| <dl> <span data-ttu-id="7f91e-151"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-151"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="7f91e-152">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f91e-152">Read-only</span></span><br/>       |
| <dl> <span data-ttu-id="7f91e-153"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-153"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="7f91e-154">Sem acesso.</span><span class="sxs-lookup"><span data-stu-id="7f91e-154">No access.</span></span><br/>      |
| <dl> <span data-ttu-id="7f91e-155"><dt>5.. 15999</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-155"><dt>5..15999</dt></span></span> </dl> | <span data-ttu-id="7f91e-156">DMTF reservado</span><span class="sxs-lookup"><span data-stu-id="7f91e-156">DMTF Reserved</span></span><br/>   |
| <dl> <span data-ttu-id="7f91e-157"><dt>16000..</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-157"><dt>16000..</dt></span></span> </dl>  | <span data-ttu-id="7f91e-158">Fornecedor reservado</span><span class="sxs-lookup"><span data-stu-id="7f91e-158">Vendor reserved</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7f91e-159">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="7f91e-159">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f91e-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f91e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f91e-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f91e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f91e-162">O endereço do dispositivo associado no contexto do controlador Antecedent.</span><span class="sxs-lookup"><span data-stu-id="7f91e-162">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="7f91e-163">Essa classe é herdada do **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="7f91e-163">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f91e-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f91e-164">Remarks</span></span>

<span data-ttu-id="7f91e-165">O acesso à classe **Msvm \_ ProtocolControllerForUnit** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="7f91e-165">Access to the **Msvm\_ProtocolControllerForUnit** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7f91e-166">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7f91e-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f91e-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f91e-167">Requirements</span></span>



| <span data-ttu-id="7f91e-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f91e-168">Requirement</span></span> | <span data-ttu-id="7f91e-169">Valor</span><span class="sxs-lookup"><span data-stu-id="7f91e-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f91e-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f91e-170">Minimum supported client</span></span><br/> | <span data-ttu-id="7f91e-171">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7f91e-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7f91e-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f91e-172">Minimum supported server</span></span><br/> | <span data-ttu-id="7f91e-173">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7f91e-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f91e-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f91e-174">Namespace</span></span><br/>                | <span data-ttu-id="7f91e-175">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7f91e-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7f91e-176">MOF</span><span class="sxs-lookup"><span data-stu-id="7f91e-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f91e-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f91e-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7f91e-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f91e-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f91e-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7f91e-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f91e-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f91e-181">**\_PROTOCOLCONTROLLERFORUNIT CIM**</span><span class="sxs-lookup"><span data-stu-id="7f91e-181">**CIM\_ProtocolControllerForUnit**</span></span>](cim-protocolcontrollerforunit.md)
</dt> <dt>

<span data-ttu-id="7f91e-182">[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f91e-182">[**CIM\_ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7f91e-183">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7f91e-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

