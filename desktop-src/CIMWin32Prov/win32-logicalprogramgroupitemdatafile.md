---
description: A \_ classe WMI de associação do Win32 LogicalProgramGroupItemDataFile relaciona os itens do grupo de programas do menu iniciar e os arquivos nos quais eles estão armazenados.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupItemDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089655"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a><span data-ttu-id="1bf2c-103">\_Classe Win32 LogicalProgramGroupItemDataFile</span><span class="sxs-lookup"><span data-stu-id="1bf2c-103">Win32\_LogicalProgramGroupItemDataFile class</span></span>

<span data-ttu-id="1bf2c-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ LogicalProgramGroupItemDataFile** relaciona os itens do grupo de programas do menu **Iniciar** e os arquivos nos quais eles estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="1bf2c-104">The **Win32\_LogicalProgramGroupItemDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the program group items of the **Start** menu and the files in which they are stored.</span></span>

<span data-ttu-id="1bf2c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1bf2c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1bf2c-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="1bf2c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf2c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bf2c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1bf2c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1bf2c-108">Members</span></span>

<span data-ttu-id="1bf2c-109">A classe **Win32 \_ LogicalProgramGroupItemDataFile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1bf2c-109">The **Win32\_LogicalProgramGroupItemDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="1bf2c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bf2c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bf2c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bf2c-111">Properties</span></span>

<span data-ttu-id="1bf2c-112">A classe **Win32 \_ LogicalProgramGroupItemDataFile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1bf2c-112">The **Win32\_LogicalProgramGroupItemDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bf2c-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1bf2c-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf2c-114">Tipo de dados: **Win32 \_ LogicalProgramGroupItem**</span><span class="sxs-lookup"><span data-stu-id="1bf2c-114">Data type: **Win32\_LogicalProgramGroupItem**</span></span>
</dt> <dt>

<span data-ttu-id="1bf2c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bf2c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf2c-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroupItem")</span><span class="sxs-lookup"><span data-stu-id="1bf2c-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroupItem")</span></span>
</dt> </dl>

<span data-ttu-id="1bf2c-117">Referência à instância que representa os agrupamentos de programa no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="1bf2c-117">Reference to the instance representing the program groupings in the **Start** menu.</span></span>

</dd> <dt>

<span data-ttu-id="1bf2c-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1bf2c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf2c-119">Tipo de dados **: \_ DataFile do CIM**</span><span class="sxs-lookup"><span data-stu-id="1bf2c-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="1bf2c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bf2c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf2c-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")</span><span class="sxs-lookup"><span data-stu-id="1bf2c-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="1bf2c-122">Referência à instância que representa a classe associada ao grupo de programas.</span><span class="sxs-lookup"><span data-stu-id="1bf2c-122">Reference to the instance representing the class associated with the program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bf2c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bf2c-123">Remarks</span></span>

<span data-ttu-id="1bf2c-124">A classe **Win32 \_ LogicalProgramGroupItemDataFile** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1bf2c-124">The **Win32\_LogicalProgramGroupItemDataFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="1bf2c-125">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="1bf2c-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="1bf2c-126">Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="1bf2c-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="1bf2c-127">Para obter mais informações, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="1bf2c-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf2c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bf2c-128">Requirements</span></span>



| <span data-ttu-id="1bf2c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf2c-129">Requirement</span></span> | <span data-ttu-id="1bf2c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1bf2c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf2c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bf2c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf2c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bf2c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1bf2c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bf2c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf2c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bf2c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1bf2c-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bf2c-135">Namespace</span></span><br/>                | <span data-ttu-id="1bf2c-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1bf2c-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1bf2c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1bf2c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bf2c-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bf2c-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bf2c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1bf2c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bf2c-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bf2c-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf2c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bf2c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf2c-142">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="1bf2c-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="1bf2c-143">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bf2c-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

