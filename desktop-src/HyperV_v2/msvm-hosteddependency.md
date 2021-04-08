---
description: Associa uma instância de máquina virtual ao objeto do sistema de computador que representa o sistema físico, de hospedagem.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Classe Msvm_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ce580e6b478dbdf320377c2738708d0eb7689fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826866"
---
# <a name="msvm_hosteddependency-class"></a><span data-ttu-id="cdfe1-103">\_Classe Msvm HostedDependency</span><span class="sxs-lookup"><span data-stu-id="cdfe1-103">Msvm\_HostedDependency class</span></span>

<span data-ttu-id="cdfe1-104">Associa uma instância de máquina virtual ao objeto do sistema de computador que representa o sistema físico, de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="cdfe1-104">Associates a virtual machine instance with the computer system object that represents the physical, hosting system.</span></span>

<span data-ttu-id="cdfe1-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cdfe1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdfe1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdfe1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cdfe1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cdfe1-107">Members</span></span>

<span data-ttu-id="cdfe1-108">A classe **Msvm \_ HostedDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cdfe1-108">The **Msvm\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="cdfe1-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cdfe1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdfe1-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cdfe1-110">Properties</span></span>

<span data-ttu-id="cdfe1-111">A classe **Msvm \_ HostedDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cdfe1-111">The **Msvm\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdfe1-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="cdfe1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdfe1-113">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="cdfe1-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="cdfe1-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cdfe1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdfe1-115">Uma referência ao sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="cdfe1-115">A reference to the hosting computer system.</span></span> <span data-ttu-id="cdfe1-116">Essa propriedade é herdada do [**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdfe1-116">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cdfe1-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="cdfe1-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdfe1-118">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="cdfe1-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="cdfe1-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cdfe1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdfe1-120">Uma referência à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cdfe1-120">A reference to the virtual machine.</span></span> <span data-ttu-id="cdfe1-121">Essa propriedade é herdada do [**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdfe1-121">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdfe1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdfe1-122">Remarks</span></span>

<span data-ttu-id="cdfe1-123">O acesso à classe **Msvm \_ HostedDependency** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="cdfe1-123">Access to the **Msvm\_HostedDependency** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cdfe1-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cdfe1-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdfe1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdfe1-125">Requirements</span></span>



| <span data-ttu-id="cdfe1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdfe1-126">Requirement</span></span> | <span data-ttu-id="cdfe1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cdfe1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdfe1-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdfe1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cdfe1-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cdfe1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cdfe1-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdfe1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cdfe1-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cdfe1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdfe1-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdfe1-132">Namespace</span></span><br/>                | <span data-ttu-id="cdfe1-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cdfe1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cdfe1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cdfe1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdfe1-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdfe1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cdfe1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdfe1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cdfe1-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdfe1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdfe1-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="cdfe1-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="cdfe1-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cdfe1-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cdfe1-141">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="cdfe1-141">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

