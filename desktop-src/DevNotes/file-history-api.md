---
description: API de histórico de arquivo
ms.assetid: 7488BA36-DEBE-42F1-8A12-A2DB1DE8B827
title: API de histórico de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb612a0bbbbd28b703a82bc65c5cd4d33640f760
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920267"
---
# <a name="file-history-api"></a><span data-ttu-id="7403b-103">API de histórico de arquivo</span><span class="sxs-lookup"><span data-stu-id="7403b-103">File History API</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7403b-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7403b-104">In this section</span></span>

-   [<span data-ttu-id="7403b-105">**\_status do backup do FH \_**</span><span class="sxs-lookup"><span data-stu-id="7403b-105">**FH\_BACKUP\_STATUS**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_backup_status)
-   [<span data-ttu-id="7403b-106">**\_resultado da \_ validação do dispositivo FH \_**</span><span class="sxs-lookup"><span data-stu-id="7403b-106">**FH\_DEVICE\_VALIDATION\_RESULT**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_device_validation_result)
-   [<span data-ttu-id="7403b-107">**\_tipo de \_ política \_ local FH**</span><span class="sxs-lookup"><span data-stu-id="7403b-107">**FH\_LOCAL\_POLICY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_local_policy_type)
-   [<span data-ttu-id="7403b-108">**\_categoria de \_ item \_ protegido FH**</span><span class="sxs-lookup"><span data-stu-id="7403b-108">**FH\_PROTECTED\_ITEM\_CATEGORY**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_protected_item_category)
-   [<span data-ttu-id="7403b-109">**\_tipos de retenção FH \_**</span><span class="sxs-lookup"><span data-stu-id="7403b-109">**FH\_RETENTION\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_retention_types)
-   [<span data-ttu-id="7403b-110">**\_tipos de \_ unidade de destino FH \_**</span><span class="sxs-lookup"><span data-stu-id="7403b-110">**FH\_TARGET\_DRIVE\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_drive_types)
-   [<span data-ttu-id="7403b-111">**\_tipo de \_ propriedade de destino FH \_**</span><span class="sxs-lookup"><span data-stu-id="7403b-111">**FH\_TARGET\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_property_type)
-   [<span data-ttu-id="7403b-112">**FhConfigMgr**</span><span class="sxs-lookup"><span data-stu-id="7403b-112">**FhConfigMgr**</span></span>](fhconfigmgr.md)
-   [<span data-ttu-id="7403b-113">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="7403b-113">FhManagew.exe</span></span>](fhmanagew-exe.md)
-   [<span data-ttu-id="7403b-114">**FhReassociation**</span><span class="sxs-lookup"><span data-stu-id="7403b-114">**FhReassociation**</span></span>](fhreassociation.md)
-   [<span data-ttu-id="7403b-115">**FhServiceClosePipe**</span><span class="sxs-lookup"><span data-stu-id="7403b-115">**FhServiceClosePipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceclosepipe)
-   [<span data-ttu-id="7403b-116">**FhServiceOpenPipe**</span><span class="sxs-lookup"><span data-stu-id="7403b-116">**FhServiceOpenPipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceopenpipe)
-   [<span data-ttu-id="7403b-117">**FhServiceReloadConfiguration**</span><span class="sxs-lookup"><span data-stu-id="7403b-117">**FhServiceReloadConfiguration**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicereloadconfiguration)
-   [<span data-ttu-id="7403b-118">**FhServiceBlockBackup**</span><span class="sxs-lookup"><span data-stu-id="7403b-118">**FhServiceBlockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceblockbackup)
-   [<span data-ttu-id="7403b-119">**FhServiceStartBackup**</span><span class="sxs-lookup"><span data-stu-id="7403b-119">**FhServiceStartBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestartbackup)
-   [<span data-ttu-id="7403b-120">**FhServiceStopBackup**</span><span class="sxs-lookup"><span data-stu-id="7403b-120">**FhServiceStopBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestopbackup)
-   [<span data-ttu-id="7403b-121">**FhServiceUnblockBackup**</span><span class="sxs-lookup"><span data-stu-id="7403b-121">**FhServiceUnblockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceunblockbackup)
-   [<span data-ttu-id="7403b-122">**IFhConfigMgr**</span><span class="sxs-lookup"><span data-stu-id="7403b-122">**IFhConfigMgr**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr)
-   [<span data-ttu-id="7403b-123">**IFhReassociation**</span><span class="sxs-lookup"><span data-stu-id="7403b-123">**IFhReassociation**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation)
-   [<span data-ttu-id="7403b-124">**IFhScopeIterator**</span><span class="sxs-lookup"><span data-stu-id="7403b-124">**IFhScopeIterator**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhscopeiterator)
-   [<span data-ttu-id="7403b-125">**IFhTarget**</span><span class="sxs-lookup"><span data-stu-id="7403b-125">**IFhTarget**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhtarget)

 

 



