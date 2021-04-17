---
description: A \_ classe WMI de associação do Win32 LogicalProgramGroupDirectory relaciona grupos de programas lógicos (agrupamentos no menu Iniciar) e os diretórios de arquivos nos quais eles são armazenados.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754387"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a><span data-ttu-id="9fbd2-103">\_Classe Win32 LogicalProgramGroupDirectory</span><span class="sxs-lookup"><span data-stu-id="9fbd2-103">Win32\_LogicalProgramGroupDirectory class</span></span>

<span data-ttu-id="9fbd2-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ LogicalProgramGroupDirectory** relaciona grupos de programas lógicos (agrupamentos no menu **Iniciar** ) e os diretórios de arquivos nos quais eles são armazenados.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-104">The **Win32\_LogicalProgramGroupDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical program groups (groupings in the **Start** menu) and the file directories in which they are stored.</span></span>

<span data-ttu-id="9fbd2-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9fbd2-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fbd2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fbd2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9fbd2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9fbd2-108">Members</span></span>

<span data-ttu-id="9fbd2-109">A classe **Win32 \_ LogicalProgramGroupDirectory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9fbd2-109">The **Win32\_LogicalProgramGroupDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="9fbd2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9fbd2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fbd2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9fbd2-111">Properties</span></span>

<span data-ttu-id="9fbd2-112">A classe **Win32 \_ LogicalProgramGroupDirectory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-112">The **Win32\_LogicalProgramGroupDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fbd2-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="9fbd2-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fbd2-114">Tipo de dados: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="9fbd2-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="9fbd2-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9fbd2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fbd2-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="9fbd2-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="9fbd2-117">Referência à instância que representa o grupo de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-117">Reference to the instance representing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="9fbd2-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="9fbd2-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fbd2-119">Tipo de dados **: \_ diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="9fbd2-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="9fbd2-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9fbd2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fbd2-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| diretório WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="9fbd2-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="9fbd2-122">Referência à instância que representa o diretório de arquivos para o grupo de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-122">Reference to the instance representing the file directory for the logical program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fbd2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fbd2-123">Remarks</span></span>

<span data-ttu-id="9fbd2-124">A classe **Win32 \_ LogicalProgramGroupDirectory** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9fbd2-124">The **Win32\_LogicalProgramGroupDirectory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9fbd2-125">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="9fbd2-126">Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="9fbd2-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="9fbd2-127">Para obter mais informações, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="9fbd2-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fbd2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fbd2-128">Requirements</span></span>



| <span data-ttu-id="9fbd2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fbd2-129">Requirement</span></span> | <span data-ttu-id="9fbd2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9fbd2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fbd2-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fbd2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9fbd2-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fbd2-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fbd2-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fbd2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9fbd2-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fbd2-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fbd2-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fbd2-135">Namespace</span></span><br/>                | <span data-ttu-id="9fbd2-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9fbd2-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9fbd2-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9fbd2-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fbd2-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fbd2-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fbd2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9fbd2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fbd2-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fbd2-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fbd2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fbd2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fbd2-142">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="9fbd2-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="9fbd2-143">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fbd2-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

