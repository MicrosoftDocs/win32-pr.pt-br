---
description: Representa uma relação na qual uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: Classe CIM_MediaPresent (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105758989"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a><span data-ttu-id="abac8-103">Classe CIM_MediaPresent (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="abac8-103">CIM_MediaPresent class (Hyper-V management)</span></span>

<span data-ttu-id="abac8-104">Representa uma relação na qual uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="abac8-104">Represents a relationship in which a storage extent must be accessed through a media access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="abac8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abac8-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="abac8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="abac8-106">Members</span></span>

<span data-ttu-id="abac8-107">A classe **CIM \_ MediaPresent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="abac8-107">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="abac8-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="abac8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abac8-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="abac8-109">Properties</span></span>

<span data-ttu-id="abac8-110">A classe **CIM \_ MediaPresent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="abac8-110">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abac8-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="abac8-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abac8-112">Tipo de dados: **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="abac8-112">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="abac8-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abac8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abac8-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="abac8-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="abac8-115">O dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="abac8-115">The media access device.</span></span>

</dd> <dt>

<span data-ttu-id="abac8-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="abac8-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abac8-117">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="abac8-117">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="abac8-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abac8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abac8-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="abac8-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="abac8-120">A extensão de armazenamento que é acessada ao usar o dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="abac8-120">The storage extent that is accessed when using the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="abac8-121">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="abac8-121">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abac8-122">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="abac8-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abac8-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abac8-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abac8-124">**true** se a extensão de armazenamento for fixada no dispositivo de acesso à mídia e não puder ser ejetada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="abac8-124">**true** if the storage extent is fixed in the media access device and can not be ejected; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abac8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abac8-125">Requirements</span></span>



| <span data-ttu-id="abac8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="abac8-126">Requirement</span></span> | <span data-ttu-id="abac8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="abac8-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abac8-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abac8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="abac8-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="abac8-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="abac8-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abac8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="abac8-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abac8-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="abac8-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="abac8-132">Namespace</span></span><br/>                | <span data-ttu-id="abac8-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="abac8-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="abac8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="abac8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abac8-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abac8-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abac8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="abac8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abac8-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abac8-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="abac8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="abac8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abac8-139">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="abac8-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

