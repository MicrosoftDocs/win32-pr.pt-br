---
description: Associa uma unidade de armazenamento à mídia inserida na unidade.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Classe Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837676"
---
# <a name="msvm_mediapresent-class"></a><span data-ttu-id="afffc-103">\_Classe Msvm MediaPresent</span><span class="sxs-lookup"><span data-stu-id="afffc-103">Msvm\_MediaPresent class</span></span>

<span data-ttu-id="afffc-104">Associa uma unidade de armazenamento à mídia inserida na unidade.</span><span class="sxs-lookup"><span data-stu-id="afffc-104">Associates a storage drive with the media inserted into the drive.</span></span> <span data-ttu-id="afffc-105">Essa associação é usada para todos os objetos da unidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="afffc-105">This association is used for all storage drive objects.</span></span>

<span data-ttu-id="afffc-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="afffc-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="afffc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afffc-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="afffc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="afffc-108">Members</span></span>

<span data-ttu-id="afffc-109">A classe **Msvm \_ MediaPresent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="afffc-109">The **Msvm\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="afffc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afffc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afffc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afffc-111">Properties</span></span>

<span data-ttu-id="afffc-112">A classe **Msvm \_ MediaPresent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="afffc-112">The **Msvm\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afffc-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="afffc-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afffc-114">Tipo de dados: **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span><span class="sxs-lookup"><span data-stu-id="afffc-114">Data type: **[**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span></span>
</dt> <dt>

<span data-ttu-id="afffc-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afffc-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afffc-116">A referência ao dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="afffc-116">The reference to the media access device.</span></span> <span data-ttu-id="afffc-117">Essa propriedade é herdada do [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="afffc-117">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="afffc-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="afffc-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afffc-119">Tipo de dados: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="afffc-119">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="afffc-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afffc-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afffc-121">A referência à extensão de armazenamento acessada com o dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="afffc-121">The reference to the storage extent accessed with the media access device.</span></span> <span data-ttu-id="afffc-122">Essa propriedade é herdada do [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="afffc-122">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="afffc-123">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="afffc-123">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afffc-124">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="afffc-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afffc-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afffc-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afffc-126">Indica se a extensão de armazenamento acessada é fixa e não pode ser ejetada.</span><span class="sxs-lookup"><span data-stu-id="afffc-126">Indicates whether the accessed storage extent is fixed and cannot be ejected.</span></span> <span data-ttu-id="afffc-127">O valor é **true** para discos rígidos; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="afffc-127">The value is **True** for hard disks and **False** otherwise.</span></span> <span data-ttu-id="afffc-128">Essa propriedade é herdada do [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="afffc-128">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afffc-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="afffc-129">Remarks</span></span>

<span data-ttu-id="afffc-130">O acesso à classe **Msvm \_ MediaPresent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="afffc-130">Access to the **Msvm\_MediaPresent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="afffc-131">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="afffc-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="afffc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afffc-132">Requirements</span></span>



| <span data-ttu-id="afffc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="afffc-133">Requirement</span></span> | <span data-ttu-id="afffc-134">Valor</span><span class="sxs-lookup"><span data-stu-id="afffc-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afffc-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afffc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="afffc-136">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="afffc-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="afffc-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afffc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="afffc-138">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="afffc-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="afffc-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="afffc-139">Namespace</span></span><br/>                | <span data-ttu-id="afffc-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="afffc-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="afffc-141">MOF</span><span class="sxs-lookup"><span data-stu-id="afffc-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afffc-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afffc-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="afffc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="afffc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afffc-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="afffc-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="afffc-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="afffc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afffc-146">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="afffc-146">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

[<span data-ttu-id="afffc-147">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="afffc-147">**CIM\_MediaPresent**</span></span>](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[<span data-ttu-id="afffc-148">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="afffc-148">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

