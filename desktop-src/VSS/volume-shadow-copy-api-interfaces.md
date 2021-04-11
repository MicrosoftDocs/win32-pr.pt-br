---
description: A API do Serviço de Cópias de Sombra de Volume (VSS) fornece interfaces COM e C++ para dar suporte à criação de solicitantes e gravadores.
ms.assetid: 3a0c60df-666c-4e33-a54c-7fa5ddbfde13
title: Interfaces de API de cópia de sombra de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1291f0e63b18530f92d99f9d526202df078fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090448"
---
# <a name="volume-shadow-copy-api-interfaces"></a><span data-ttu-id="c16c6-103">Interfaces de API de cópia de sombra de volume</span><span class="sxs-lookup"><span data-stu-id="c16c6-103">Volume Shadow Copy API Interfaces</span></span>

<span data-ttu-id="c16c6-104">A API do Serviço de Cópias de Sombra de Volume (VSS) fornece interfaces COM e C++ para dar suporte à criação de solicitantes e gravadores.</span><span class="sxs-lookup"><span data-stu-id="c16c6-104">The Volume Shadow Copy Service (VSS) API provides both COM and C++ interfaces to support the creation of requesters and writers.</span></span>

## <a name="vss-requester-specific-interfaces"></a><span data-ttu-id="c16c6-105">Interfaces de Requester-Specific VSS</span><span class="sxs-lookup"><span data-stu-id="c16c6-105">VSS Requester-Specific Interfaces</span></span>

-   [<span data-ttu-id="c16c6-106">**IVssBackupComponents**</span><span class="sxs-lookup"><span data-stu-id="c16c6-106">**IVssBackupComponents**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   [<span data-ttu-id="c16c6-107">**IVssBackupComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="c16c6-107">**IVssBackupComponentsEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex)
-   [<span data-ttu-id="c16c6-108">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="c16c6-108">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
-   [<span data-ttu-id="c16c6-109">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="c16c6-109">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)
-   [<span data-ttu-id="c16c6-110">**IVssExamineWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="c16c6-110">**IVssExamineWriterMetadata**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
-   [<span data-ttu-id="c16c6-111">**IVssExamineWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="c16c6-111">**IVssExamineWriterMetadataEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex)
-   [<span data-ttu-id="c16c6-112">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="c16c6-112">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)
-   [<span data-ttu-id="c16c6-113">**IVssWMComponent**</span><span class="sxs-lookup"><span data-stu-id="c16c6-113">**IVssWMComponent**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
-   [<span data-ttu-id="c16c6-114">**IVssWriterComponentsExt**</span><span class="sxs-lookup"><span data-stu-id="c16c6-114">**IVssWriterComponentsExt**</span></span>](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)

## <a name="vss-writer-specific-interfaces"></a><span data-ttu-id="c16c6-115">Interfaces de Writer-Specific VSS</span><span class="sxs-lookup"><span data-stu-id="c16c6-115">VSS Writer-Specific Interfaces</span></span>

-   [<span data-ttu-id="c16c6-116">**IVssCreateExpressWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="c16c6-116">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)
-   [<span data-ttu-id="c16c6-117">**IVssCreateWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="c16c6-117">**IVssCreateWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
-   [<span data-ttu-id="c16c6-118">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="c16c6-118">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)
-   [<span data-ttu-id="c16c6-119">**IVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="c16c6-119">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)
-   [<span data-ttu-id="c16c6-120">**IVssWriterComponents**</span><span class="sxs-lookup"><span data-stu-id="c16c6-120">**IVssWriterComponents**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

## <a name="vss-hardware-provider-specific-interfaces"></a><span data-ttu-id="c16c6-121">Interfaces de Provider-Specific de hardware do VSS</span><span class="sxs-lookup"><span data-stu-id="c16c6-121">VSS Hardware Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="c16c6-122">**IVssAdmin**</span><span class="sxs-lookup"><span data-stu-id="c16c6-122">**IVssAdmin**</span></span>](/windows/desktop/api/VsAdmin/nn-vsadmin-ivssadmin)
-   [<span data-ttu-id="c16c6-123">**IVssHardwareSnapshotProvider**</span><span class="sxs-lookup"><span data-stu-id="c16c6-123">**IVssHardwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider)
-   [<span data-ttu-id="c16c6-124">**IVssHardwareSnapshotProviderEx**</span><span class="sxs-lookup"><span data-stu-id="c16c6-124">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)
-   [<span data-ttu-id="c16c6-125">**IVssProviderCreateSnapshotSet**</span><span class="sxs-lookup"><span data-stu-id="c16c6-125">**IVssProviderCreateSnapshotSet**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset)
-   [<span data-ttu-id="c16c6-126">**IVssProviderNotifications**</span><span class="sxs-lookup"><span data-stu-id="c16c6-126">**IVssProviderNotifications**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications)

## <a name="vss-software-provider-specific-interfaces"></a><span data-ttu-id="c16c6-127">Interfaces de Provider-Specific de software VSS</span><span class="sxs-lookup"><span data-stu-id="c16c6-127">VSS Software Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="c16c6-128">**IVssSoftwareSnapshotProvider**</span><span class="sxs-lookup"><span data-stu-id="c16c6-128">**IVssSoftwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsssoftwaresnapshotprovider)

## <a name="vss-shared-interfaces"></a><span data-ttu-id="c16c6-129">Interfaces compartilhadas do VSS</span><span class="sxs-lookup"><span data-stu-id="c16c6-129">VSS Shared Interfaces</span></span>

-   [<span data-ttu-id="c16c6-130">**IVssAsync**</span><span class="sxs-lookup"><span data-stu-id="c16c6-130">**IVssAsync**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssasync)
-   [<span data-ttu-id="c16c6-131">**IVssComponent**</span><span class="sxs-lookup"><span data-stu-id="c16c6-131">**IVssComponent**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
-   [<span data-ttu-id="c16c6-132">**IVssComponentEx**</span><span class="sxs-lookup"><span data-stu-id="c16c6-132">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)
-   [<span data-ttu-id="c16c6-133">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="c16c6-133">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)
-   [<span data-ttu-id="c16c6-134">**IVssEnumObject**</span><span class="sxs-lookup"><span data-stu-id="c16c6-134">**IVssEnumObject**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssenumobject)
-   [<span data-ttu-id="c16c6-135">**IVssWMDependency**</span><span class="sxs-lookup"><span data-stu-id="c16c6-135">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)
-   [<span data-ttu-id="c16c6-136">**IVssWMFiledesc**</span><span class="sxs-lookup"><span data-stu-id="c16c6-136">**IVssWMFiledesc**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

## <a name="vss-management-interfaces"></a><span data-ttu-id="c16c6-137">Interfaces de gerenciamento do VSS</span><span class="sxs-lookup"><span data-stu-id="c16c6-137">VSS Management Interfaces</span></span>

-   [<span data-ttu-id="c16c6-138">**IVssDifferentialSoftwareSnapshotMgmt**</span><span class="sxs-lookup"><span data-stu-id="c16c6-138">**IVssDifferentialSoftwareSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt)
-   [<span data-ttu-id="c16c6-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="c16c6-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)
-   [<span data-ttu-id="c16c6-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="c16c6-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)
-   [<span data-ttu-id="c16c6-141">**IVssEnumMgmtObject**</span><span class="sxs-lookup"><span data-stu-id="c16c6-141">**IVssEnumMgmtObject**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssenummgmtobject)
-   [<span data-ttu-id="c16c6-142">**IVssSnapshotMgmt**</span><span class="sxs-lookup"><span data-stu-id="c16c6-142">**IVssSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt)
-   [<span data-ttu-id="c16c6-143">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="c16c6-143">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 
