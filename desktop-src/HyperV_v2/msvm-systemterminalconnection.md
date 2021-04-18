---
description: Associa uma máquina virtual a uma conexão de terminal.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Classe Msvm_SystemTerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792515"
---
# <a name="msvm_systemterminalconnection-class"></a><span data-ttu-id="d7780-103">\_Classe Msvm SystemTerminalConnection</span><span class="sxs-lookup"><span data-stu-id="d7780-103">Msvm\_SystemTerminalConnection class</span></span>

<span data-ttu-id="d7780-104">Associa uma máquina virtual a uma conexão de terminal.</span><span class="sxs-lookup"><span data-stu-id="d7780-104">Associates a virtual machine with a terminal connection.</span></span>

<span data-ttu-id="d7780-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d7780-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7780-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7780-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d7780-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d7780-107">Members</span></span>

<span data-ttu-id="d7780-108">A classe **Msvm \_ SystemTerminalConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7780-108">The **Msvm\_SystemTerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="d7780-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7780-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7780-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7780-110">Properties</span></span>

<span data-ttu-id="d7780-111">A classe **Msvm \_ SystemTerminalConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d7780-111">The **Msvm\_SystemTerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7780-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d7780-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7780-113">Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="d7780-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="d7780-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7780-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7780-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d7780-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d7780-116">A máquina virtual à qual a conexão está anexada.</span><span class="sxs-lookup"><span data-stu-id="d7780-116">The virtual machine to which the connection is attached.</span></span>

</dd> <dt>

<span data-ttu-id="d7780-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d7780-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7780-118">Tipo de dados: **[ **Msvm \_ TerminalConnection**](msvm-terminalconnection.md)**</span><span class="sxs-lookup"><span data-stu-id="d7780-118">Data type: **[**Msvm\_TerminalConnection**](msvm-terminalconnection.md)**</span></span>
</dt> <dt>

<span data-ttu-id="d7780-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7780-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7780-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="d7780-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d7780-121">A conexão com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d7780-121">The connection to the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7780-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7780-122">Remarks</span></span>

<span data-ttu-id="d7780-123">O acesso à classe **Msvm \_ SystemTerminalConnection** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d7780-123">Access to the **Msvm\_SystemTerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d7780-124">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d7780-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7780-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7780-125">Requirements</span></span>



| <span data-ttu-id="d7780-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7780-126">Requirement</span></span> | <span data-ttu-id="d7780-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d7780-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7780-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7780-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7780-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d7780-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d7780-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7780-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7780-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d7780-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7780-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7780-132">Namespace</span></span><br/>                | <span data-ttu-id="d7780-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d7780-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d7780-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d7780-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7780-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7780-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7780-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d7780-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7780-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7780-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d7780-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7780-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7780-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="d7780-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="d7780-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7780-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d7780-141">Classes de vídeo</span><span class="sxs-lookup"><span data-stu-id="d7780-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

