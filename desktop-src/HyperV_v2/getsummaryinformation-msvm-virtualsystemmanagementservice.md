---
description: Retorna informações de resumo da máquina virtual.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Método GetSummaryInformation da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296209"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e0dc1-103">Método GetSummaryInformation da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="e0dc1-103">GetSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e0dc1-104">Retorna informações de resumo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-104">Returns virtual machine summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dc1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0dc1-105">Syntax</span></span>


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="e0dc1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0dc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0dc1-107">*SettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0dc1-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dc1-108">Tipo: **CIM \_ VirtualSystemSettingData \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e0dc1-108">Type: **CIM\_VirtualSystemSettingData\[\]**</span></span>

<span data-ttu-id="e0dc1-109">Uma matriz de [**instâncias \_ VirtualSystemSettingData do CIM**](/previous-versions//cc136954(v=vs.85)) que especificam as máquinas virtuais ou instantâneos para os quais as informações serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-109">An array of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instances that specify the virtual machines or snapshots for which information is to be retrieved.</span></span> <span data-ttu-id="e0dc1-110">Se esse parâmetro for **nulo**, as informações para todas as máquinas virtuais serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-110">If this parameter is **Null**, information for all virtual machines is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="e0dc1-111">*RequestedInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0dc1-111">*RequestedInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dc1-112">Tipo: **UInt32 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e0dc1-112">Type: **uint32\[\]**</span></span>

<span data-ttu-id="e0dc1-113">Uma matriz de valores de enumeração que correspondem às propriedades na classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) , que especificam os dados a serem recuperados para as máquinas virtuais e os instantâneos especificados na matriz *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-113">An array of enumeration values, which correspond to the properties in the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class, that specify the data to retrieve for the virtual machines and snapshots specified in the *SettingData* array.</span></span>

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span data-ttu-id="e0dc1-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome** (0)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-115">Isso corresponde à propriedade **Name** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-115">This corresponds to the **Name** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span data-ttu-id="e0dc1-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nome do elemento** (1)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-117">Isso corresponde à propriedade **ElementName** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-117">This corresponds to the **ElementName** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span data-ttu-id="e0dc1-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Hora de criação** (2)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Creation Time** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-119">Isso corresponde à propriedade **CreationTime** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-119">This corresponds to the **CreationTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span data-ttu-id="e0dc1-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Observações** (3)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notes** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-121">Isso corresponde à propriedade **Notes** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-121">This corresponds to the **Notes** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span data-ttu-id="e0dc1-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Número de processadores** (4)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Number of Processors** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-123">Isso corresponde à propriedade **NumberOfProcessors** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-123">This corresponds to the **NumberOfProcessors** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span data-ttu-id="e0dc1-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Pequena imagem em miniatura (80x60)** (5)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Small Thumbnail Image (80x60)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-125">Isso corresponde à propriedade **ThumbnailImage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-125">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="e0dc1-126">Uma imagem em miniatura com as dimensões de 80 60 será recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-126">A thumbnail image with the dimensions of 80 60 will be retrieved.</span></span>

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span data-ttu-id="e0dc1-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Imagem de miniatura média (160x120)** (6)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Medium Thumbnail Image (160x120)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-128">Isso corresponde à propriedade **ThumbnailImage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-128">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="e0dc1-129">Uma imagem em miniatura com as dimensões de 160 120 será recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-129">A thumbnail image with the dimensions of 160 120 will be retrieved.</span></span>

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span data-ttu-id="e0dc1-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Imagem em miniatura grande (320 x 240)** (7)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Large Thumbnail Image (320x240)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-131">Isso corresponde à propriedade **ThumbnailImage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-131">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="e0dc1-132">Uma imagem em miniatura com as dimensões de 320 240 será recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-132">A thumbnail image with the dimensions of 320 240 will be retrieved.</span></span>

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span data-ttu-id="e0dc1-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-134">Isso corresponde à propriedade **AllocatedGPU** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-134">This corresponds to the **AllocatedGPU** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span data-ttu-id="e0dc1-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span data-ttu-id="e0dc1-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versão** (10)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e0dc1-137">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="e0dc1-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Blindado** (11)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e0dc1-139">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-139">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span data-ttu-id="e0dc1-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**Enabledstate** (100)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-141">Isso corresponde à propriedade **enabledstate** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-141">This corresponds to the **EnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span data-ttu-id="e0dc1-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-143">Isso corresponde à propriedade **ProcessorLoad** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-143">This corresponds to the **ProcessorLoad** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span data-ttu-id="e0dc1-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-145">Isso corresponde à propriedade **ProcessorLoadHistory** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-145">This corresponds to the **ProcessorLoadHistory** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span data-ttu-id="e0dc1-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-147">Isso corresponde à propriedade **MemoryUsage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-147">This corresponds to the **MemoryUsage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span data-ttu-id="e0dc1-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Pulsação** (104)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-149">Isso corresponde à propriedade **Heartbeat** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-149">This corresponds to the **Heartbeat** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span data-ttu-id="e0dc1-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Tempo de atividade** (105)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Uptime** (105)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-151">Isso corresponde à propriedade de **tempo de atividade** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-151">This corresponds to the **UpTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span data-ttu-id="e0dc1-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-153">Isso corresponde à propriedade **GuestOperatingSystem** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-153">This corresponds to the **GuestOperatingSystem** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span data-ttu-id="e0dc1-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Instantâneos** (107)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshots** (107)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-155">Isso corresponde à propriedade **Snapshots** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-155">This corresponds to the **Snapshots** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span data-ttu-id="e0dc1-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-157">Isso corresponde à propriedade **AsynchronousTasks** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-157">This corresponds to the **AsynchronousTasks** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span data-ttu-id="e0dc1-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-159">Isso corresponde à propriedade **HealthState** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-159">This corresponds to the **HealthState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span data-ttu-id="e0dc1-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-161">Isso corresponde à propriedade **OperationalStatus** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-161">This corresponds to the **OperationalStatus** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span data-ttu-id="e0dc1-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-163">Isso corresponde à propriedade **StatusDescriptions** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-163">This corresponds to the **StatusDescriptions** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span data-ttu-id="e0dc1-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-165">Isso corresponde à propriedade **MemoryAvailable** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-165">This corresponds to the **MemoryAvailable** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span data-ttu-id="e0dc1-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-167">Isso corresponde à propriedade **AvailableMemoryBuffer** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-167">This corresponds to the **AvailableMemoryBuffer** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span data-ttu-id="e0dc1-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Modo de replicação** (114)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replication Mode** (114)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-169">Isso corresponde à propriedade **replicationmode** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-169">This corresponds to the **ReplicationMode** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span data-ttu-id="e0dc1-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Estado de replicação** (115)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replication State** (115)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-171">Isso corresponde à propriedade **replicationstate** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-171">This corresponds to the **ReplicationState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span data-ttu-id="e0dc1-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Sistema de réplica HealthTest de replicação** (116)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-173">Isso corresponde à propriedade **ReplicationHealth** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-173">This corresponds to the **ReplicationHealth** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span data-ttu-id="e0dc1-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Integridade do aplicativo** (117)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Application Health** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span data-ttu-id="e0dc1-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-176">Isso corresponde à propriedade **replicationstate** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-176">This corresponds to the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="e0dc1-177">Essa é a matriz para todos os valores de estado de replicação entre as relações primária e estendida.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-177">This is array for all replication state values across primary and extended relationship.</span></span> <span data-ttu-id="e0dc1-178">0 o valor de índice é sempre para a relação primária e, se a replicação estendida estiver habilitada, ela será retornada no índice 1.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-178">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span data-ttu-id="e0dc1-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-180">Isso corresponde à propriedade **ReplicationHealth** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-180">This corresponds to the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="e0dc1-181">Essa é uma matriz para todos os valores de integridade de replicação entre as relações primária e estendida.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-181">This is array for all replication health values across primary and extended relationship.</span></span> <span data-ttu-id="e0dc1-182">0 o valor de índice é sempre para a relação primária e, se a replicação estendida estiver habilitada, ela será retornada no índice 1.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-182">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span data-ttu-id="e0dc1-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-184">Isso corresponde à propriedade **SwapFilesInUse** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-184">This corresponds to the **SwapFilesInUse** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="e0dc1-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span data-ttu-id="e0dc1-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-187">Isso corresponde à propriedade **Name** da classe [**Msvm \_ replicationprovider**](msvm-replicationprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-187">This corresponds to the **Name** property of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class.</span></span>

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span data-ttu-id="e0dc1-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="e0dc1-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-190">Isso corresponde à propriedade **IntegrationServicesVersionState** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-190">This corresponds to the **IntegrationServicesVersionState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span data-ttu-id="e0dc1-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="e0dc1-192">Isso corresponde à propriedade **OtherEnabledState** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-192">This corresponds to the **OtherEnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>



 <span data-ttu-id="e0dc1-193">(133)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-193">(133)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e0dc1-194">*SummaryInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0dc1-194">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dc1-195">Tipo: **[ **Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="e0dc1-195">Type: **[**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span></span>

<span data-ttu-id="e0dc1-196">Uma matriz de instâncias do [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md) que contém as informações solicitadas para as máquinas virtuais e/ou os instantâneos especificados na matriz *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-196">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *SettingData* array.</span></span> <span data-ttu-id="e0dc1-197">Essa matriz terá o mesmo número de elementos que a matriz *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-197">This array will have the same number of elements as the *SettingData* array.</span></span> <span data-ttu-id="e0dc1-198">Cada uma dessas entradas conterá a propriedade **Name** , mesmo que essa propriedade não tenha sido solicitada.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-198">Each of these entries will contain the **Name** property, even if this property was not requested.</span></span> <span data-ttu-id="e0dc1-199">Se a máquina virtual ou o instantâneo não puder ser encontrado ou estiver indisponível, a propriedade **Name** da entrada de informações de resumo correspondente estará vazia.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-199">If the virtual machine or snapshot cannot be found or is unavailable, the **Name** property of the corresponding summary information entry will be empty.</span></span>

<span data-ttu-id="e0dc1-200">As propriedades não especificadas no parâmetro *RequestedInformation* terão um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e0dc1-200">Properties not specified in the *RequestedInformation* parameter will have a **Null** value.</span></span>

> [!Note]  
> <span data-ttu-id="e0dc1-201">Tipo de dados atualizado do no Windows 10, versão 1703 de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="e0dc1-201">Datatype updated from in Windows 10, version 1703 from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0dc1-202">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0dc1-202">Return value</span></span>

<span data-ttu-id="e0dc1-203">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0dc1-203">Type: **uint32**</span></span>

<span data-ttu-id="e0dc1-204">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-204">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e0dc1-205">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-205">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-206">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-206">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-207">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-207">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-208">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-208">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-209">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-209">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-210">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-210">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-211">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-211">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-212">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-212">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-213">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-213">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-214">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-214">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-215">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-215">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-216">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-216">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e0dc1-217">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e0dc1-217">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e0dc1-218">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0dc1-218">Remarks</span></span>

<span data-ttu-id="e0dc1-219">O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-219">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e0dc1-220">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e0dc1-220">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e0dc1-221">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0dc1-221">Examples</span></span>

<span data-ttu-id="e0dc1-222">O exemplo de C# a seguir exibe informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-222">The following C# sample displays summary information.</span></span> <span data-ttu-id="e0dc1-223">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e0dc1-223">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0dc1-224">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="e0dc1-224">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a><span data-ttu-id="e0dc1-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0dc1-225">Requirements</span></span>



| <span data-ttu-id="e0dc1-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0dc1-226">Requirement</span></span> | <span data-ttu-id="e0dc1-227">Valor</span><span class="sxs-lookup"><span data-stu-id="e0dc1-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dc1-228">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0dc1-228">Minimum supported client</span></span><br/> | <span data-ttu-id="e0dc1-229">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e0dc1-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e0dc1-230">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0dc1-230">Minimum supported server</span></span><br/> | <span data-ttu-id="e0dc1-231">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e0dc1-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0dc1-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0dc1-232">Namespace</span></span><br/>                | <span data-ttu-id="e0dc1-233">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e0dc1-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e0dc1-234">MOF</span><span class="sxs-lookup"><span data-stu-id="e0dc1-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0dc1-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0dc1-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0dc1-236">DLL</span><span class="sxs-lookup"><span data-stu-id="e0dc1-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0dc1-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0dc1-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e0dc1-238">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0dc1-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0dc1-239">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="e0dc1-239">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="e0dc1-240">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0dc1-240">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e0dc1-241">**Msvm \_ SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="e0dc1-241">**Msvm\_SummaryInformation**</span></span>](msvm-summaryinformation.md)
</dt> </dl>

 

