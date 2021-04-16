---
description: Descreve o quão atualizado o sistema operacional em um dispositivo é.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Enumeração UpdateAssessmentStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751054"
---
# <a name="updateassessmentstatus-enumeration"></a><span data-ttu-id="4262e-103">Enumeração UpdateAssessmentStatus</span><span class="sxs-lookup"><span data-stu-id="4262e-103">UpdateAssessmentStatus enumeration</span></span>

<span data-ttu-id="4262e-104">Descreve o quão atualizado o sistema operacional em um dispositivo é.</span><span class="sxs-lookup"><span data-stu-id="4262e-104">Describes how up-to-date the OS on a device is.</span></span> <span data-ttu-id="4262e-105">**UpdateAssessmentStatus** é usado pelas estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , nos membros **assessmentForCurrent**, **assessmentForUpToDate** e **securityStatus** .</span><span class="sxs-lookup"><span data-stu-id="4262e-105">**UpdateAssessmentStatus** is used by the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, in the **assessmentForCurrent**, **assessmentForUpToDate**, and **securityStatus** members.</span></span> <span data-ttu-id="4262e-106">Exatamente uma constante é retornada.</span><span class="sxs-lookup"><span data-stu-id="4262e-106">Exactly one constant is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="4262e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4262e-107">Syntax</span></span>


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a><span data-ttu-id="4262e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="4262e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4262e-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Mais recente**</span><span class="sxs-lookup"><span data-stu-id="4262e-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span> **UpdateAssessmentStatus\_Latest**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-110">Esse resultado no **assessmentForCurrent** implica que o dispositivo está na última atualização de recursos e atualização de qualidade disponível para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4262e-110">This result within **assessmentForCurrent** implies that the device is on the latest feature update and quality update available for that device.</span></span> <span data-ttu-id="4262e-111">Em **assessmentForUpToDate**, esse resultado implica que o dispositivo está na atualização de qualidade mais recente para a versão do Windows em execução.</span><span class="sxs-lookup"><span data-stu-id="4262e-111">Within **assessmentForUpToDate**, this result implies that the device is on the latest quality update for the release of Windows it is running.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**</span><span class="sxs-lookup"><span data-stu-id="4262e-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestSoftRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-113">A atualização de recursos mais recente não foi instalada devido a uma restrição flexível.</span><span class="sxs-lookup"><span data-stu-id="4262e-113">The latest feature update has not been installed due to a soft restriction.</span></span> <span data-ttu-id="4262e-114">Quando uma restrição flexível for colocada em uma atualização, a atualização não será instalada automaticamente; um usuário deve iniciar automaticamente o download dentro da atualização UX.</span><span class="sxs-lookup"><span data-stu-id="4262e-114">When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX.</span></span> <span data-ttu-id="4262e-115">Esse status se aplica somente a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="4262e-115">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**</span><span class="sxs-lookup"><span data-stu-id="4262e-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestHardRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-117">A atualização de recursos mais recente não foi instalada devido a uma restrição rígida.</span><span class="sxs-lookup"><span data-stu-id="4262e-117">The latest feature update has not been installed due to a hard restriction.</span></span> <span data-ttu-id="4262e-118">Quando uma restrição rígida é colocada em uma atualização, a atualização não é aplicável ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4262e-118">When a hard restriction has been placed on an update, the update is not applicable to the device.</span></span> <span data-ttu-id="4262e-119">Esse status se aplica somente a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="4262e-119">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**</span><span class="sxs-lookup"><span data-stu-id="4262e-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span> **UpdateAssessmentStatus\_NotLatestEndOfSupport**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-121">O dispositivo não está na atualização mais recente porque a atualização do recurso do dispositivo não é mais suportada pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4262e-121">The device is not on the latest update because the device's feature update is no longer supported by Microsoft.</span></span> <span data-ttu-id="4262e-122">Quando a Microsoft para de dar suporte a uma versão de recurso, esse status será retornado para **assessmentForCurrent** e **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="4262e-122">When Microsoft stops supporting a feature release, this status will be returned for both **assessmentForCurrent** and **assessmentForUpToDate**.</span></span>

> [!Note]  
> <span data-ttu-id="4262e-123">Quando **UpdateAssessmentStatus \_ NotLatestEndOfSupport** é retornado, o **UpdateImpactLevel** da avaliação é sempre **UpdateImpactLevel \_ alto**.</span><span class="sxs-lookup"><span data-stu-id="4262e-123">When **UpdateAssessmentStatus\_NotLatestEndOfSupport** is returned, the assessment's **UpdateImpactLevel** is always **UpdateImpactLevel\_High**.</span></span>

 

</dd> <dt>

<span data-ttu-id="4262e-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**</span><span class="sxs-lookup"><span data-stu-id="4262e-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span> **UpdateAssessmentStatus\_NotLatestServicingTrain**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-125">O dispositivo não está na última atualização de recurso porque o treinamento de serviço do dispositivo limita o dispositivo de atualizar para a atualização de recurso mais recente.</span><span class="sxs-lookup"><span data-stu-id="4262e-125">The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update.</span></span> <span data-ttu-id="4262e-126">Por exemplo: se um dispositivo estiver em Branch Atual para Negócios (CBB) e uma nova atualização de recurso for lançada para Branch Atual (CB), isso será retornado.</span><span class="sxs-lookup"><span data-stu-id="4262e-126">For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned.</span></span> <span data-ttu-id="4262e-127">Esse status se aplica somente a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="4262e-127">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**</span><span class="sxs-lookup"><span data-stu-id="4262e-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestDeferredFeature**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-129">A atualização de recursos mais recente não foi instalada devido à política de adiamento de atualização de recursos de Windows Update do dispositivo para negócios.</span><span class="sxs-lookup"><span data-stu-id="4262e-129">The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy.</span></span> <span data-ttu-id="4262e-130">Determinar o **daysOutOfDate** leva em conta as políticas de adiamento; **daysOutOfDate** não começará a incrementar até que o período de adiamento tenha expirado.</span><span class="sxs-lookup"><span data-stu-id="4262e-130">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span> <span data-ttu-id="4262e-131">Esse status se aplica somente a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="4262e-131">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**</span><span class="sxs-lookup"><span data-stu-id="4262e-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestDeferredQuality**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-133">O dispositivo não está na atualização de qualidade mais recente devido à política de adiamento de Windows Update do dispositivo para a atualização de qualidade comercial.</span><span class="sxs-lookup"><span data-stu-id="4262e-133">The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.</span></span> <span data-ttu-id="4262e-134">Determinar o **daysOutOfDate** leva em conta as políticas de adiamento; **daysOutOfDate** não começará a incrementar até que o período de adiamento tenha expirado.</span><span class="sxs-lookup"><span data-stu-id="4262e-134">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**</span><span class="sxs-lookup"><span data-stu-id="4262e-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestPausedFeature**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-136">O dispositivo não está na última atualização de recurso devido ao dispositivo com atualizações de recurso em pausa.</span><span class="sxs-lookup"><span data-stu-id="4262e-136">The device is not on the latest feature update due to the device having paused Feature Updates.</span></span> <span data-ttu-id="4262e-137">Se um dispositivo está em pausa não é acrescentado ao cálculo de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="4262e-137">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="4262e-138">Esse status se aplica somente a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="4262e-138">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**</span><span class="sxs-lookup"><span data-stu-id="4262e-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestPausedQuality**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-140">O dispositivo não está na atualização de qualidade mais recente devido ao dispositivo com atualizações de qualidade em pausa.</span><span class="sxs-lookup"><span data-stu-id="4262e-140">The device is not on the latest quality update due to the device having paused Quality Updates.</span></span> <span data-ttu-id="4262e-141">Se um dispositivo está em pausa não é acrescentado ao cálculo de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="4262e-141">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="4262e-142">**daysOutOfDate** não leva em conta se um dispositivo está pausado em seu cálculo.</span><span class="sxs-lookup"><span data-stu-id="4262e-142">**daysOutOfDate** does not factor whether a device is paused into its calculation.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**</span><span class="sxs-lookup"><span data-stu-id="4262e-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span> **UpdateAssessmentStatus\_NotLatestManaged**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-144">O dispositivo não está na atualização mais recente porque a aprovação de atualizações não é feita por meio de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="4262e-144">The device is not on the latest update because the approval of updates is not done through Windows Update.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**</span><span class="sxs-lookup"><span data-stu-id="4262e-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span> **UpdateAssessmentStatus\_NotLatestUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-146">O dispositivo não está na última atualização devido a um motivo que não pode ser determinado pela avaliação.</span><span class="sxs-lookup"><span data-stu-id="4262e-146">The device is not on the latest update due to a reason that cannot be determined by the assessment.</span></span>

</dd> <dt>

<span data-ttu-id="4262e-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**</span><span class="sxs-lookup"><span data-stu-id="4262e-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span> **UpdateAssessmentStatus\_NotLatestTargetedVersion**</span></span>
</dt> <dd>

<span data-ttu-id="4262e-148">O dispositivo não está na atualização de recurso mais recente devido à política de versão de destino do Windows Update do dispositivo para a empresa.</span><span class="sxs-lookup"><span data-stu-id="4262e-148">The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy.</span></span> <span data-ttu-id="4262e-149">Esta política está mantendo o dispositivo na versão de lançamento de recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="4262e-149">This policy is keeping the device on the targeted feature release version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4262e-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="4262e-150">Remarks</span></span>

<span data-ttu-id="4262e-151">Essa enumeração é usada com mais frequência com as estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , que, por sua vez, são usadas com o método [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) para [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span><span class="sxs-lookup"><span data-stu-id="4262e-151">This enumeration is used most often with the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, which are in turn used with the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method for [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span></span>

## <a name="requirements"></a><span data-ttu-id="4262e-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4262e-152">Requirements</span></span>



| <span data-ttu-id="4262e-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="4262e-153">Requirement</span></span> | <span data-ttu-id="4262e-154">Valor</span><span class="sxs-lookup"><span data-stu-id="4262e-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4262e-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4262e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4262e-156">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="4262e-156">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4262e-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4262e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4262e-158">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="4262e-158">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4262e-159">INSERI</span><span class="sxs-lookup"><span data-stu-id="4262e-159">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4262e-160"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4262e-160"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




