---
description: Usado para associar uma máquina virtual a seu BIOS.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Classe Msvm_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090007"
---
# <a name="msvm_systembios-class"></a><span data-ttu-id="58988-103">\_Classe Msvm SystemBIOS</span><span class="sxs-lookup"><span data-stu-id="58988-103">Msvm\_SystemBIOS class</span></span>

<span data-ttu-id="58988-104">Usado para associar uma máquina virtual a seu BIOS.</span><span class="sxs-lookup"><span data-stu-id="58988-104">Used to associate a virtual machine with its BIOS.</span></span>

<span data-ttu-id="58988-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="58988-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58988-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58988-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="58988-107">Membros</span><span class="sxs-lookup"><span data-stu-id="58988-107">Members</span></span>

<span data-ttu-id="58988-108">A classe **Msvm \_ SystemBIOS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58988-108">The **Msvm\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="58988-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58988-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58988-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58988-110">Properties</span></span>

<span data-ttu-id="58988-111">A classe **Msvm \_ SystemBIOS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58988-111">The **Msvm\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58988-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="58988-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58988-113">Tipo de dados: **[ **\_ sistema de ComputerSystem CIM**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="58988-113">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="58988-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58988-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58988-115">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="58988-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="58988-116">A máquina virtual que inicia a partir do BIOS.</span><span class="sxs-lookup"><span data-stu-id="58988-116">The virtual machine that starts from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="58988-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="58988-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58988-118">Tipo de dados: **[ **Msvm \_ bioselement**](msvm-bioselement.md)**</span><span class="sxs-lookup"><span data-stu-id="58988-118">Data type: **[**Msvm\_BIOSElement**](msvm-bioselement.md)**</span></span>
</dt> <dt>

<span data-ttu-id="58988-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58988-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58988-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="58988-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="58988-121">O BIOS associado à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="58988-121">The BIOS associated with the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58988-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="58988-122">Remarks</span></span>

<span data-ttu-id="58988-123">O acesso à classe **Msvm \_ SystemBIOS** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="58988-123">Access to the **Msvm\_SystemBIOS** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="58988-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="58988-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="58988-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58988-125">Requirements</span></span>



| <span data-ttu-id="58988-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="58988-126">Requirement</span></span> | <span data-ttu-id="58988-127">Valor</span><span class="sxs-lookup"><span data-stu-id="58988-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58988-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58988-128">Minimum supported client</span></span><br/> | <span data-ttu-id="58988-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="58988-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58988-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58988-130">Minimum supported server</span></span><br/> | <span data-ttu-id="58988-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="58988-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58988-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="58988-132">Namespace</span></span><br/>                | <span data-ttu-id="58988-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="58988-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="58988-134">MOF</span><span class="sxs-lookup"><span data-stu-id="58988-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58988-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58988-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58988-136">DLL</span><span class="sxs-lookup"><span data-stu-id="58988-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58988-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58988-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58988-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="58988-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58988-139">**\_SYSTEMBIOS CIM**</span><span class="sxs-lookup"><span data-stu-id="58988-139">**CIM\_SystemBIOS**</span></span>](cim-systembios.md)
</dt> <dt>

[<span data-ttu-id="58988-140">Classes do BIOS</span><span class="sxs-lookup"><span data-stu-id="58988-140">BIOS Classes</span></span>](bios-classes.md)
</dt> </dl>

 

