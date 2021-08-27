---
title: Fluxo de trabalho do adaptador
description: Esta seção descreve o fluxo de trabalho de registro da perspectiva dos plug-ins do adaptador.
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79d018cfc853e8b92c1e9bd5400526fe0d425c7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466013"
---
# <a name="adapter-workflow"></a>Fluxo de trabalho do adaptador

Esta seção descreve o fluxo de trabalho de registro da perspectiva dos plug-ins do adaptador.

em Windows 10, nós implementamos uma interface de mecanismo V4 que fornece duas novas funções de adaptador de mecanismo, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) e [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn). Essas novas funções permitem o suporte para a biometria segura usando o TPM 2,0. A tabela a seguir mostra o fluxo de trabalho de registro no lado do adaptador.




| | | API do cliente | Métodos de adaptador | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENGINE_INFO)</strong></a>  |  <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></li></ol> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"> <strong>WinBioEnrollCapture</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[- &gt; </strong><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</li><li>Se S_OK ou WINBIO_I_MORE_DATA<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></li><li>[O chamador continua o registro]</li></ol></li><li>Senão, se WINBIO_E_BAD_CAPTURE [o chamador exibirá comentários rejeitados, continuará o registro] <br /></li><li>Caso contrário, se outro erro<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></li><li>[O serviço de biografia anula o registro]</li></ol></li></ol> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a>  |  <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></li><li>Se o banco de dados removível<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></li></ol></li><li>Senão<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a><br /></li></ol> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"> <strong>WinBioEnrollDiscard</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></li></ol> | 




 

 

 





