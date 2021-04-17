---
description: Representa uma unidade de DVD.
ms.assetid: 6127b58d-c70f-47c7-9eeb-6aff819f672e
title: Classe CIM_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DVDDrive
- CIM_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44c69cfe537257076623e472f4bb1406f8bf7665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780542"
---
# <a name="cim_dvddrive-class"></a><span data-ttu-id="226a3-103">\_Classe CIM DVDDrive</span><span class="sxs-lookup"><span data-stu-id="226a3-103">CIM\_DVDDrive class</span></span>

<span data-ttu-id="226a3-104">Representa uma unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="226a3-104">Represents a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="226a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="226a3-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_DVDDrive : CIM_MediaAccessDevice
{
  uint16 FormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="226a3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="226a3-106">Members</span></span>

<span data-ttu-id="226a3-107">A classe **CIM \_ DVDDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="226a3-107">The **CIM\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="226a3-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="226a3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="226a3-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="226a3-109">Properties</span></span>

<span data-ttu-id="226a3-110">A classe **CIM \_ DVDDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="226a3-110">The **CIM\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="226a3-111">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="226a3-111">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="226a3-112">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="226a3-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="226a3-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="226a3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="226a3-114">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalMedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**MediaType**")</span><span class="sxs-lookup"><span data-stu-id="226a3-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="226a3-115">Os formatos de CD e DVD com suporte no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="226a3-115">The CD and DVD formats that are supported by the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="226a3-116">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="226a3-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="226a3-117">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="226a3-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="226a3-118">**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="226a3-118">**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="226a3-119">**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="226a3-119">**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="226a3-120">**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="226a3-120">**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="226a3-121">**CD gravável** (19)</span><span class="sxs-lookup"><span data-stu-id="226a3-121">**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="226a3-122">**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="226a3-122">**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>

<span data-ttu-id="226a3-123">**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="226a3-123">**DVD-RW+** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="226a3-124">**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="226a3-124">**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="226a3-125">**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="226a3-125">**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="226a3-126">**DVD-vídeo** (26)</span><span class="sxs-lookup"><span data-stu-id="226a3-126">**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="226a3-127">**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="226a3-127">**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="226a3-128">**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="226a3-128">**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="226a3-129">**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="226a3-129">**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="226a3-130">**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="226a3-130">**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="226a3-131">**DVD gravável** (36)</span><span class="sxs-lookup"><span data-stu-id="226a3-131">**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="226a3-132">**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="226a3-132">**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="226a3-133">**DVD-áudio** (38)</span><span class="sxs-lookup"><span data-stu-id="226a3-133">**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="226a3-134">**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="226a3-134">**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="226a3-135">**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="226a3-135">**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="226a3-136">**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="226a3-136">**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="226a3-137">**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="226a3-137">**DVD-18** (42)</span></span>


<span data-ttu-id="226a3-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="226a3-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="226a3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="226a3-139">Requirements</span></span>



| <span data-ttu-id="226a3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="226a3-140">Requirement</span></span> | <span data-ttu-id="226a3-141">Valor</span><span class="sxs-lookup"><span data-stu-id="226a3-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="226a3-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="226a3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="226a3-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="226a3-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="226a3-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="226a3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="226a3-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="226a3-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="226a3-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="226a3-146">Namespace</span></span><br/>                | <span data-ttu-id="226a3-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="226a3-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="226a3-148">MOF</span><span class="sxs-lookup"><span data-stu-id="226a3-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="226a3-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="226a3-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="226a3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="226a3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="226a3-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="226a3-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="226a3-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="226a3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226a3-153">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="226a3-153">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

