---
description: Associa o Msvm \_ snapshotcollection aos \_ objetos Msvm VirtualSystemSettingData contidos.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Classe Msvm_CollectedSnapshots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766897"
---
# <a name="msvm_collectedsnapshots-class"></a><span data-ttu-id="82bb7-103">\_Classe Msvm CollectedSnapshots</span><span class="sxs-lookup"><span data-stu-id="82bb7-103">Msvm\_CollectedSnapshots class</span></span>

<span data-ttu-id="82bb7-104">Associa o [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) aos objetos [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) contidos.</span><span class="sxs-lookup"><span data-stu-id="82bb7-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the contained [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) objects.</span></span>

<span data-ttu-id="82bb7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="82bb7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bb7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82bb7-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a><span data-ttu-id="82bb7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="82bb7-107">Members</span></span>

<span data-ttu-id="82bb7-108">A classe **Msvm \_ CollectedSnapshots** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82bb7-108">The **Msvm\_CollectedSnapshots** class has these types of members:</span></span>

-   [<span data-ttu-id="82bb7-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82bb7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82bb7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82bb7-110">Properties</span></span>

<span data-ttu-id="82bb7-111">A classe **Msvm \_ CollectedSnapshots** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="82bb7-111">The **Msvm\_CollectedSnapshots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82bb7-112">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="82bb7-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bb7-113">Tipo de dados: **Msvm \_ snapshotcollection**</span><span class="sxs-lookup"><span data-stu-id="82bb7-113">Data type: **Msvm\_SnapshotCollection**</span></span>
</dt> <dt>

<span data-ttu-id="82bb7-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82bb7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82bb7-115">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("coleção")</span><span class="sxs-lookup"><span data-stu-id="82bb7-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="82bb7-116">Um objeto de agrupamento ou ' recipiente ' do [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) que representa a coleção.</span><span class="sxs-lookup"><span data-stu-id="82bb7-116">An [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="82bb7-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="82bb7-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bb7-118">Tipo de dados: **Msvm \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="82bb7-118">Data type: **Msvm\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="82bb7-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82bb7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82bb7-120">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("membro")</span><span class="sxs-lookup"><span data-stu-id="82bb7-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="82bb7-121">Um [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que contém os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="82bb7-121">An [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82bb7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82bb7-122">Requirements</span></span>



| <span data-ttu-id="82bb7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="82bb7-123">Requirement</span></span> | <span data-ttu-id="82bb7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="82bb7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82bb7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82bb7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82bb7-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="82bb7-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="82bb7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82bb7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82bb7-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82bb7-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="82bb7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="82bb7-129">Namespace</span></span><br/>                | <span data-ttu-id="82bb7-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="82bb7-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="82bb7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="82bb7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82bb7-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82bb7-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82bb7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="82bb7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82bb7-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82bb7-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82bb7-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="82bb7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bb7-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="82bb7-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

