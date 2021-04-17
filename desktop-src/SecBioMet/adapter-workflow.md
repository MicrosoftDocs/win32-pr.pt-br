---
title: Fluxo de trabalho do adaptador
description: Esta seção descreve o fluxo de trabalho de registro da perspectiva dos plug-ins do adaptador.
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68f93146e1d6cedd42094876547bfe0c945d6a7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755963"
---
# <a name="adapter-workflow"></a><span data-ttu-id="0c1d3-103">Fluxo de trabalho do adaptador</span><span class="sxs-lookup"><span data-stu-id="0c1d3-103">Adapter Workflow</span></span>

<span data-ttu-id="0c1d3-104">Esta seção descreve o fluxo de trabalho de registro da perspectiva dos plug-ins do adaptador.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-104">This section describes the enrollment workflow from the perspective of the adapter plugins.</span></span>

<span data-ttu-id="0c1d3-105">No Windows 10, nós implementamos uma interface de mecanismo v4 que fornece duas novas funções de adaptador de mecanismo, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) e [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span><span class="sxs-lookup"><span data-stu-id="0c1d3-105">In Windows 10, we ve implemented a V4 engine interface that provides 2 new engine adapter functions, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) and [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span></span> <span data-ttu-id="0c1d3-106">Essas novas funções permitem o suporte para a biometria segura usando o TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-106">These new functions allow support for secure biometrics using TPM 2.0.</span></span> <span data-ttu-id="0c1d3-107">A tabela a seguir mostra o fluxo de trabalho de registro no lado do adaptador.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-107">The following table shows the adapter-side enrollment workflow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c1d3-108">API do cliente</span><span class="sxs-lookup"><span data-stu-id="0c1d3-108">Client API</span></span></td>
<td><span data-ttu-id="0c1d3-109">Métodos de adaptador</span><span class="sxs-lookup"><span data-stu-id="0c1d3-109">Adapter Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c1d3-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENGINE_INFO)</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty(EXTENDED_ENGINE_INFO)</strong></a></span></span></td>
<td><span data-ttu-id="0c1d3-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c1d3-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="0c1d3-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c1d3-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="0c1d3-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong> <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span><span class="sxs-lookup"><span data-stu-id="0c1d3-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span></span></li>
<li><span data-ttu-id="0c1d3-123">Se S_OK ou WINBIO_I_MORE_DATA</span><span class="sxs-lookup"><span data-stu-id="0c1d3-123">If S_OK or WINBIO_I_MORE_DATA</span></span>
<ol>
<li><span data-ttu-id="0c1d3-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-125">[O chamador continua o registro]</span><span class="sxs-lookup"><span data-stu-id="0c1d3-125">[Caller continues enrollment]</span></span></li>
</ol></li>
<li><span data-ttu-id="0c1d3-126">Senão, se WINBIO_E_BAD_CAPTURE [o chamador exibirá comentários rejeitados, continuará o registro]</span><span class="sxs-lookup"><span data-stu-id="0c1d3-126">Else if WINBIO_E_BAD_CAPTURE [Caller displays reject feedback, continues enrollment]</span></span> <br/></li>
<li><span data-ttu-id="0c1d3-127">Caso contrário, se outro erro</span><span class="sxs-lookup"><span data-stu-id="0c1d3-127">Else if other ERROR</span></span>
<ol>
<li><span data-ttu-id="0c1d3-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-130">[O serviço de biografia anula o registro]</span><span class="sxs-lookup"><span data-stu-id="0c1d3-130">[Bio service aborts enrollment]</span></span></li>
</ol></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c1d3-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span></span></td>
<td><span data-ttu-id="0c1d3-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c1d3-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="0c1d3-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-135">Se o banco de dados removível</span><span class="sxs-lookup"><span data-stu-id="0c1d3-135">If REMOVABLE DATABASE</span></span>
<ol>
<li><span data-ttu-id="0c1d3-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span></li>
</ol></li>
<li><span data-ttu-id="0c1d3-138">Senão<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c1d3-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="0c1d3-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="0c1d3-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c1d3-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 





