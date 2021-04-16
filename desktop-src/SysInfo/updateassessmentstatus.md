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
# <a name="updateassessmentstatus-enumeration"></a>Enumeração UpdateAssessmentStatus

Descreve o quão atualizado o sistema operacional em um dispositivo é. **UpdateAssessmentStatus** é usado pelas estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , nos membros **assessmentForCurrent**, **assessmentForUpToDate** e **securityStatus** . Exatamente uma constante é retornada.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Mais recente**
</dt> <dd>

Esse resultado no **assessmentForCurrent** implica que o dispositivo está na última atualização de recursos e atualização de qualidade disponível para esse dispositivo. Em **assessmentForUpToDate**, esse resultado implica que o dispositivo está na atualização de qualidade mais recente para a versão do Windows em execução.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**
</dt> <dd>

A atualização de recursos mais recente não foi instalada devido a uma restrição flexível. Quando uma restrição flexível for colocada em uma atualização, a atualização não será instalada automaticamente; um usuário deve iniciar automaticamente o download dentro da atualização UX. Esse status se aplica somente a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**
</dt> <dd>

A atualização de recursos mais recente não foi instalada devido a uma restrição rígida. Quando uma restrição rígida é colocada em uma atualização, a atualização não é aplicável ao dispositivo. Esse status se aplica somente a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**
</dt> <dd>

O dispositivo não está na atualização mais recente porque a atualização do recurso do dispositivo não é mais suportada pela Microsoft. Quando a Microsoft para de dar suporte a uma versão de recurso, esse status será retornado para **assessmentForCurrent** e **assessmentForUpToDate**.

> [!Note]  
> Quando **UpdateAssessmentStatus \_ NotLatestEndOfSupport** é retornado, o **UpdateImpactLevel** da avaliação é sempre **UpdateImpactLevel \_ alto**.

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**
</dt> <dd>

O dispositivo não está na última atualização de recurso porque o treinamento de serviço do dispositivo limita o dispositivo de atualizar para a atualização de recurso mais recente. Por exemplo: se um dispositivo estiver em Branch Atual para Negócios (CBB) e uma nova atualização de recurso for lançada para Branch Atual (CB), isso será retornado. Esse status se aplica somente a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**
</dt> <dd>

A atualização de recursos mais recente não foi instalada devido à política de adiamento de atualização de recursos de Windows Update do dispositivo para negócios. Determinar o **daysOutOfDate** leva em conta as políticas de adiamento; **daysOutOfDate** não começará a incrementar até que o período de adiamento tenha expirado. Esse status se aplica somente a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**
</dt> <dd>

O dispositivo não está na atualização de qualidade mais recente devido à política de adiamento de Windows Update do dispositivo para a atualização de qualidade comercial. Determinar o **daysOutOfDate** leva em conta as políticas de adiamento; **daysOutOfDate** não começará a incrementar até que o período de adiamento tenha expirado.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**
</dt> <dd>

O dispositivo não está na última atualização de recurso devido ao dispositivo com atualizações de recurso em pausa. Se um dispositivo está em pausa não é acrescentado ao cálculo de **daysOutOfDate**. Esse status se aplica somente a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**
</dt> <dd>

O dispositivo não está na atualização de qualidade mais recente devido ao dispositivo com atualizações de qualidade em pausa. Se um dispositivo está em pausa não é acrescentado ao cálculo de **daysOutOfDate**. **daysOutOfDate** não leva em conta se um dispositivo está pausado em seu cálculo.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**
</dt> <dd>

O dispositivo não está na atualização mais recente porque a aprovação de atualizações não é feita por meio de Windows Update.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**
</dt> <dd>

O dispositivo não está na última atualização devido a um motivo que não pode ser determinado pela avaliação.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**
</dt> <dd>

O dispositivo não está na atualização de recurso mais recente devido à política de versão de destino do Windows Update do dispositivo para a empresa. Esta política está mantendo o dispositivo na versão de lançamento de recurso de destino.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada com mais frequência com as estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , que, por sua vez, são usadas com o método [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) para [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                   |
| INSERI<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




