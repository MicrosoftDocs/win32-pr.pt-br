---
description: Associa uma porta serial a um controlador serial.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Classe Msvm_SerialPortOnSerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827355"
---
# <a name="msvm_serialportonserialcontroller-class"></a><span data-ttu-id="e61d4-103">\_Classe Msvm SerialPortOnSerialController</span><span class="sxs-lookup"><span data-stu-id="e61d4-103">Msvm\_SerialPortOnSerialController class</span></span>

<span data-ttu-id="e61d4-104">Associa uma porta serial a um controlador serial.</span><span class="sxs-lookup"><span data-stu-id="e61d4-104">Associates a serial port with a serial controller.</span></span>

<span data-ttu-id="e61d4-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e61d4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61d4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e61d4-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e61d4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e61d4-107">Members</span></span>

<span data-ttu-id="e61d4-108">A classe **Msvm \_ SerialPortOnSerialController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e61d4-108">The **Msvm\_SerialPortOnSerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="e61d4-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e61d4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e61d4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e61d4-110">Properties</span></span>

<span data-ttu-id="e61d4-111">A classe **Msvm \_ SerialPortOnSerialController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e61d4-111">The **Msvm\_SerialPortOnSerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e61d4-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e61d4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61d4-113">Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="e61d4-113">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="e61d4-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61d4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61d4-115">O controlador serial ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="e61d4-115">The serial controller to which the port is connected.</span></span> <span data-ttu-id="e61d4-116">Essa propriedade é herdada do [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="e61d4-116">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> <dt>

<span data-ttu-id="e61d4-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e61d4-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61d4-118">Tipo de dados: **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e61d4-118">Data type: **[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="e61d4-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61d4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61d4-120">A porta do controlador serial.</span><span class="sxs-lookup"><span data-stu-id="e61d4-120">The port of the serial controller.</span></span> <span data-ttu-id="e61d4-121">Essa propriedade é herdada do [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="e61d4-121">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e61d4-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e61d4-122">Remarks</span></span>

<span data-ttu-id="e61d4-123">O acesso à classe **Msvm \_ SerialPortOnSerialController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e61d4-123">Access to the **Msvm\_SerialPortOnSerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e61d4-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e61d4-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e61d4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e61d4-125">Requirements</span></span>



| <span data-ttu-id="e61d4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61d4-126">Requirement</span></span> | <span data-ttu-id="e61d4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e61d4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e61d4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61d4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e61d4-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e61d4-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e61d4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61d4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e61d4-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e61d4-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e61d4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e61d4-132">Namespace</span></span><br/>                | <span data-ttu-id="e61d4-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e61d4-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e61d4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e61d4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e61d4-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e61d4-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e61d4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e61d4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e61d4-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e61d4-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e61d4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e61d4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61d4-139">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e61d4-139">**CIM\_PortOnDevice**</span></span>](cim-portondevice.md)
</dt> <dt>

[<span data-ttu-id="e61d4-140">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e61d4-140">**CIM\_PortOnDevice**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[<span data-ttu-id="e61d4-141">Classes de dispositivos seriais</span><span class="sxs-lookup"><span data-stu-id="e61d4-141">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

