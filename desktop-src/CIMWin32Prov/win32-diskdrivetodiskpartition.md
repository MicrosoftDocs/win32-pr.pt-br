---
description: A \_ classe WMI de associação DiskDriveToDiskPartition do Win32 relaciona uma unidade de disco e uma partição existente nela.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Classe Win32_DiskDriveToDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769040"
---
# <a name="win32_diskdrivetodiskpartition-class"></a><span data-ttu-id="d1d87-103">\_Classe Win32 DiskDriveToDiskPartition</span><span class="sxs-lookup"><span data-stu-id="d1d87-103">Win32\_DiskDriveToDiskPartition class</span></span>

<span data-ttu-id="d1d87-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ DiskDriveToDiskPartition do Win32** relaciona uma unidade de disco e uma partição existente nela.</span><span class="sxs-lookup"><span data-stu-id="d1d87-104">The **Win32\_DiskDriveToDiskPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a disk drive and a partition existing on it.</span></span>

<span data-ttu-id="d1d87-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d1d87-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d1d87-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d1d87-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d87-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1d87-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d1d87-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d1d87-108">Members</span></span>

<span data-ttu-id="d1d87-109">A classe **Win32 \_ DiskDriveToDiskPartition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1d87-109">The **Win32\_DiskDriveToDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="d1d87-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1d87-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1d87-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1d87-111">Properties</span></span>

<span data-ttu-id="d1d87-112">A classe **Win32 \_ DiskDriveToDiskPartition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1d87-112">The **Win32\_DiskDriveToDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1d87-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d1d87-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d87-114">Tipo de dados: **Win32 \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="d1d87-114">Data type: **Win32\_DiskDrive**</span></span>
</dt> <dt>

<span data-ttu-id="d1d87-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d87-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d87-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskDrive")</span><span class="sxs-lookup"><span data-stu-id="d1d87-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskDrive")</span></span>
</dt> </dl>

<span data-ttu-id="d1d87-117">Referência à instância que representa as propriedades da unidade de disco onde a partição existe.</span><span class="sxs-lookup"><span data-stu-id="d1d87-117">Reference to the instance representing the properties of the disk drive where the partition exists.</span></span>

</dd> <dt>

<span data-ttu-id="d1d87-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d1d87-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d87-119">Tipo de dados: **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="d1d87-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="d1d87-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1d87-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d87-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="d1d87-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="d1d87-122">Referência à instância que representa a partição de disco que reside na unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="d1d87-122">Reference to the instance representing the disk partition residing on the disk drive.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1d87-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1d87-123">Remarks</span></span>

<span data-ttu-id="d1d87-124">A classe **Win32 \_ DiskDriveToDiskPartition** é derivada de [**CIM \_ MediaPresent**](cim-mediapresent.md).</span><span class="sxs-lookup"><span data-stu-id="d1d87-124">The **Win32\_DiskDriveToDiskPartition** class is derived from [**CIM\_MediaPresent**](cim-mediapresent.md).</span></span>

<span data-ttu-id="d1d87-125">Para obter uma discussão sobre como usar essa classe, consulte [usar o PowerShell para mapear unidades de disco e partições](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) e o artigo [como posso correlacionar unidades lógicas e discos físicos?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog.</span><span class="sxs-lookup"><span data-stu-id="d1d87-125">For a discussion on how to use this class, see the [Use PowerShell to Map Disk Drives and Partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) and the [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog articles.</span></span>

## <a name="examples"></a><span data-ttu-id="d1d87-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1d87-126">Examples</span></span>

<span data-ttu-id="d1d87-127">O exemplo do PowerShell [usar o PowerShell para coletar informações de disco/partição/ponto de montagem](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) usa o **Win32 \_ DiskDriveToDiskPartition** para retornar informações sobre discos/partições locais e pontos de montagem.</span><span class="sxs-lookup"><span data-stu-id="d1d87-127">The [Use Powershell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell sample uses **Win32\_DiskDriveToDiskPartition** to return information about local disks/partitions and mount points.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d87-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d87-128">Requirements</span></span>



| <span data-ttu-id="d1d87-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d87-129">Requirement</span></span> | <span data-ttu-id="d1d87-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d1d87-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d87-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d87-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d87-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1d87-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1d87-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d87-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d87-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1d87-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1d87-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1d87-135">Namespace</span></span><br/>                | <span data-ttu-id="d1d87-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d1d87-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1d87-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d1d87-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1d87-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1d87-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1d87-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d1d87-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1d87-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1d87-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d87-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1d87-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d87-142">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d1d87-142">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

<span data-ttu-id="d1d87-143">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1d87-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d1d87-144">Tarefas do WMI: discos e sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="d1d87-144">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

