---
title: Estrutura de WINBIO_EXTENDED_ENROLLMENT_STATUS (WinBio \_ Types. h)
description: Contém informações adicionais sobre o status de um registro em andamento.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_ENROLLMENT_STATUS
- Ponteiro de estrutura de PWINBIO_EXTENDED_ENROLLMENT_STATUS Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085280"
---
# <a name="winbio_extended_enrollment_status-structure"></a><span data-ttu-id="0238d-105">\_Estrutura de \_ status de registro ESTENDIdo WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="0238d-105">WINBIO\_EXTENDED\_ENROLLMENT\_STATUS structure</span></span>

<span data-ttu-id="0238d-106">Contém informações adicionais sobre o status de um registro em andamento.</span><span class="sxs-lookup"><span data-stu-id="0238d-106">Contains additional information about the status of an enrollment that is in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="0238d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0238d-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="0238d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0238d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0238d-109">**TemplateStatus**</span><span class="sxs-lookup"><span data-stu-id="0238d-109">**TemplateStatus**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-110">O status da coleção de exemplo para o modelo de registro.</span><span class="sxs-lookup"><span data-stu-id="0238d-110">The status of sample collection for the enrollment template.</span></span> <span data-ttu-id="0238d-111">Os valores a seguir são possíveis para esse membro.</span><span class="sxs-lookup"><span data-stu-id="0238d-111">The following values are possible for this member.</span></span>



| <span data-ttu-id="0238d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0238d-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="0238d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="0238d-113">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="0238d-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0238d-114"><dt>**S\_OK**</dt></span></span> </dl>                                                                     | <span data-ttu-id="0238d-115">O registro está pronto para ser salvo.</span><span class="sxs-lookup"><span data-stu-id="0238d-115">The enrollment is ready to be saved.</span></span><br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <span data-ttu-id="0238d-116"><dt>**WINBIO \_ E \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0238d-116"><dt>**WINBIO\_E\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0238d-117">Nenhum registro está em andamento.</span><span class="sxs-lookup"><span data-stu-id="0238d-117">No enrollment is in progress.</span></span><br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <span data-ttu-id="0238d-118"><dt>**WINBIO \_ \_ mais \_ dados**</dt></span><span class="sxs-lookup"><span data-stu-id="0238d-118"><dt>**WINBIO\_I\_MORE\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="0238d-119">Mais exemplos são necessários para concluir o modelo.</span><span class="sxs-lookup"><span data-stu-id="0238d-119">More samples are required to complete the template.</span></span><br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <span data-ttu-id="0238d-120"><dt>**\_captura WINBIO E \_ inadequada \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0238d-120"><dt>**WINBIO\_E\_BAD\_CAPTURE**</dt></span></span> </dl>                   | <span data-ttu-id="0238d-121">O exemplo mais recente não é utilizável.</span><span class="sxs-lookup"><span data-stu-id="0238d-121">The most recent sample is not usable.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="0238d-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="0238d-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-123">O motivo pelo qual o exemplo mais recente é inutilizável, se o valor do membro **TemplateStatus** for **WINBIO \_ E uma \_ \_ captura inadequada**.</span><span class="sxs-lookup"><span data-stu-id="0238d-123">The reason that the most recent sample is unusable, if the value of the **TemplateStatus** member is **WINBIO\_E\_BAD\_CAPTURE**.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-124">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="0238d-124">**PercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-125">A melhor estimativa do adaptador do mecanismo para a porcentagem do modelo concluído, como um valor de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="0238d-125">The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-126">**Fator**</span><span class="sxs-lookup"><span data-stu-id="0238d-126">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-127">O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="0238d-127">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="0238d-128">Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de [**\_ \_ \_ informações do mecanismo estendido WINBIO**](winbio-extended-engine-info.md) se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="0238d-128">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-129">**Subfator**</span><span class="sxs-lookup"><span data-stu-id="0238d-129">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-130">Um valor de **\_ \_ subtipo biométrico WINBIO** que fornece informações adicionais sobre o registro.</span><span class="sxs-lookup"><span data-stu-id="0238d-130">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that provides additional information about the enrollment.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-131">**Específicas**</span><span class="sxs-lookup"><span data-stu-id="0238d-131">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-132">Informações sobre o status de um registro que está em andamento para um fator biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="0238d-132">Information about the status of an enrollment that is in progress for a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="0238d-133">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="0238d-133">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-134">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0238d-134">Reserved.</span></span> <span data-ttu-id="0238d-135">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0238d-135">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-136">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="0238d-136">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-137">Informações sobre o status de um registro que está em andamento para os recursos faciais.</span><span class="sxs-lookup"><span data-stu-id="0238d-137">Information about the status of an enrollment that is in progress for facial features.</span></span>

<dl> <dt>

<span data-ttu-id="0238d-138">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="0238d-138">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-139">A posição dentro do quadro da câmera da face do indivíduo a ser registrado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0238d-139">The position within the camera frame of the face of the individual to enroll, in pixels.</span></span> <span data-ttu-id="0238d-140">O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição.</span><span class="sxs-lookup"><span data-stu-id="0238d-140">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="0238d-141">Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-141">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="0238d-142">Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-142">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-143">**Distância**</span><span class="sxs-lookup"><span data-stu-id="0238d-143">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-144">A distância entre o local real da face e a distância focal ideal para a face.</span><span class="sxs-lookup"><span data-stu-id="0238d-144">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="0238d-145">Esse valor varia de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="0238d-145">This value ranges from -100 to 100.</span></span> <span data-ttu-id="0238d-146">0 indica a distância ideal, os valores positivos indicam que o local real da face está muito distante, e os valores negativos indicam que o local real está muito próximo.</span><span class="sxs-lookup"><span data-stu-id="0238d-146">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0238d-147">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="0238d-147">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-148">Informações sobre o status de um registro em andamento para padrões de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="0238d-148">Information about the status of an enrollment that is in progress for fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="0238d-149">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="0238d-149">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-150">O número total de amostras necessárias para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="0238d-150">The total number of samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-151">**Centraliza**</span><span class="sxs-lookup"><span data-stu-id="0238d-151">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-152">O número de amostras para o centro da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="0238d-152">The number of samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-153">**TopEdge**</span><span class="sxs-lookup"><span data-stu-id="0238d-153">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-154">O número de amostras para a borda superior da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="0238d-154">The number of samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-155">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="0238d-155">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-156">O número de amostras para a borda inferior da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="0238d-156">The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-157">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="0238d-157">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-158">O número de amostras para a borda esquerda da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="0238d-158">The number of samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-159">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="0238d-159">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-160">O número de amostras para a borda direita da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="0238d-160">The number of samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0238d-161">**Íris**</span><span class="sxs-lookup"><span data-stu-id="0238d-161">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-162">Informações sobre o status de um registro que está em andamento para padrões de íris.</span><span class="sxs-lookup"><span data-stu-id="0238d-162">Information about the status of an enrollment that is in progress for iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="0238d-163">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0238d-163">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-164">A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0238d-164">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="0238d-165">Se o sistema de reconhecimento de íris estiver monitorando apenas um olho, essa posição será da íris desse olho.</span><span class="sxs-lookup"><span data-stu-id="0238d-165">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="0238d-166">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será da íris do olho no quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-166">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="0238d-167">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho correto do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="0238d-167">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="0238d-168">O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição.</span><span class="sxs-lookup"><span data-stu-id="0238d-168">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="0238d-169">Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-169">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="0238d-170">Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-170">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-171">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0238d-171">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-172">A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0238d-172">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="0238d-173">Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio.</span><span class="sxs-lookup"><span data-stu-id="0238d-173">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="0238d-174">Se o sistema de reconhecimento de íris estiver monitorando os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho à esquerda do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="0238d-174">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="0238d-175">O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição.</span><span class="sxs-lookup"><span data-stu-id="0238d-175">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="0238d-176">Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-176">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="0238d-177">Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-177">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-178">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0238d-178">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-179">A posição do centro de um dos Pupils do indivíduo a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="0238d-179">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="0238d-180">Se o sistema de reconhecimento de íris estiver monitorando apenas um dos olhos, essa posição será do centro da pupilidade desse olho.</span><span class="sxs-lookup"><span data-stu-id="0238d-180">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="0238d-181">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será do centro da Pupil do olho no quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="0238d-181">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="0238d-182">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro do Pupil do lado direito do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="0238d-182">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-183">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0238d-183">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-184">A posição do centro de um dos Pupils do indivíduo a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="0238d-184">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="0238d-185">Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio.</span><span class="sxs-lookup"><span data-stu-id="0238d-185">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="0238d-186">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro dos Pupil do lado esquerdo do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="0238d-186">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="0238d-187">**Distância**</span><span class="sxs-lookup"><span data-stu-id="0238d-187">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-188">A distância entre o local real da íris e a distância focal ideal para a íris.</span><span class="sxs-lookup"><span data-stu-id="0238d-188">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="0238d-189">Esse valor varia de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="0238d-189">This value ranges from -100 to 100.</span></span> <span data-ttu-id="0238d-190">0 indica a distância ideal, os valores positivos indicam que o local real da íris está muito distante, e os valores negativos indicam que o local real está muito próximo.</span><span class="sxs-lookup"><span data-stu-id="0238d-190">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0238d-191">**Voz**</span><span class="sxs-lookup"><span data-stu-id="0238d-191">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-192">Informações sobre o status de um registro que está em andamento para padrões de voz.</span><span class="sxs-lookup"><span data-stu-id="0238d-192">Information about the status of an enrollment that is in progress for voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="0238d-193">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="0238d-193">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="0238d-194">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0238d-194">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0238d-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0238d-195">Requirements</span></span>



| <span data-ttu-id="0238d-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="0238d-196">Requirement</span></span> | <span data-ttu-id="0238d-197">Valor</span><span class="sxs-lookup"><span data-stu-id="0238d-197">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0238d-198">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0238d-198">Minimum supported client</span></span><br/> | <span data-ttu-id="0238d-199">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0238d-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="0238d-200">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0238d-200">Minimum supported server</span></span><br/> | <span data-ttu-id="0238d-201">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="0238d-201">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="0238d-202">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0238d-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="0238d-203"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="0238d-203"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





