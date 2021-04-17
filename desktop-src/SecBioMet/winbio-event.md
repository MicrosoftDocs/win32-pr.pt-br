---
title: Estrutura de WINBIO_EVENT (WinBio \_ Types. h)
description: Contém informações de status enviadas à rotina de retorno de chamada quando um aviso de evento é gerado.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EVENT
- Ponteiro de estrutura de PWINBIO_EVENT Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754611"
---
# <a name="winbio_event-structure"></a><span data-ttu-id="7ac44-105">\_Estrutura de eventos WINBIO</span><span class="sxs-lookup"><span data-stu-id="7ac44-105">WINBIO\_EVENT structure</span></span>

<span data-ttu-id="7ac44-106">A estrutura de **\_ eventos WINBIO** contém informações de status enviadas à rotina de retorno de chamada quando um aviso de evento é gerado.</span><span class="sxs-lookup"><span data-stu-id="7ac44-106">The **WINBIO\_EVENT** structure contains status information sent to the callback routine when an event notice is raised.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac44-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ac44-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a><span data-ttu-id="7ac44-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7ac44-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ac44-109">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7ac44-109">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-110">Um valor que especifica o tipo de aviso de evento do provedor de serviço gerado.</span><span class="sxs-lookup"><span data-stu-id="7ac44-110">A value that specifies the type of service provider event notice raised.</span></span> <span data-ttu-id="7ac44-111">O único provedor com suporte no momento é o sensor de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="7ac44-111">The only provider currently supported is the fingerprint sensor.</span></span> <span data-ttu-id="7ac44-112">Este sensor dá suporte aos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ac44-112">This sensor supports the following flags.</span></span>

<dl> <dt>

<span data-ttu-id="7ac44-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENTO \_ FP não \_ reivindicado** (o sensor detectou um dedo de dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco.</span><span class="sxs-lookup"><span data-stu-id="7ac44-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="7ac44-114">O Windows Biometric Framework chama sua função de retorno de chamada para indicar que um dedo dedo ocorreu, mas não tenta identificar a impressão digital.)</span><span class="sxs-lookup"><span data-stu-id="7ac44-114">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.)</span></span>
</dt> <dt>

<span data-ttu-id="7ac44-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ \_Identificação de FP não \_ reivindicada \_ do evento** (o sensor detectou um dedo dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco.</span><span class="sxs-lookup"><span data-stu-id="7ac44-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="7ac44-116">O Windows Biometric Framework tenta identificar a impressão digital e passa o resultado desse processo para sua função de retorno de chamada.)</span><span class="sxs-lookup"><span data-stu-id="7ac44-116">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="7ac44-117">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="7ac44-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac44-118">**Não reclamado**</span><span class="sxs-lookup"><span data-stu-id="7ac44-118">**Unclaimed**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-119">Estrutura retornada para captura de exemplo biométrica.</span><span class="sxs-lookup"><span data-stu-id="7ac44-119">Structure returned for biometric sample capture.</span></span>

<dl> <dt>

<span data-ttu-id="7ac44-120">**Unidadeid**</span><span class="sxs-lookup"><span data-stu-id="7ac44-120">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-121">A unidade biométrica que gerou o exemplo.</span><span class="sxs-lookup"><span data-stu-id="7ac44-121">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7ac44-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="7ac44-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-123">Um valor **ULONG** que contém informações adicionais sobre a falha ao capturar um exemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="7ac44-123">A **ULONG** value that contains additional information regarding failure to capture a biometric sample.</span></span> <span data-ttu-id="7ac44-124">Se uma captura tiver sido bem-sucedida, esse parâmetro será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="7ac44-124">If a capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="7ac44-125">Os seguintes valores são definidos para captura de impressão digital:</span><span class="sxs-lookup"><span data-stu-id="7ac44-125">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="7ac44-126">\_FP WINBIO \_ muito \_ alto</span><span class="sxs-lookup"><span data-stu-id="7ac44-126">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="7ac44-127">\_FP WINBIO \_ muito \_ baixo</span><span class="sxs-lookup"><span data-stu-id="7ac44-127">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="7ac44-128">\_FP WINBIO \_ muito \_ à esquerda</span><span class="sxs-lookup"><span data-stu-id="7ac44-128">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="7ac44-129">\_FP WINBIO \_ muito \_ à direita</span><span class="sxs-lookup"><span data-stu-id="7ac44-129">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="7ac44-130">\_FP WINBIO \_ muito \_ rápido</span><span class="sxs-lookup"><span data-stu-id="7ac44-130">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="7ac44-131">\_FP WINBIO \_ muito \_ lento</span><span class="sxs-lookup"><span data-stu-id="7ac44-131">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="7ac44-132">\_ \_ qualidade ruim de FP WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="7ac44-132">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="7ac44-133">\_FP WINBIO \_ muito \_ distorcido</span><span class="sxs-lookup"><span data-stu-id="7ac44-133">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="7ac44-134">\_FP WINBIO \_ muito \_ curto</span><span class="sxs-lookup"><span data-stu-id="7ac44-134">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="7ac44-135">\_ \_ falha na mesclagem de FP WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="7ac44-135">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7ac44-136">**UnclaimedIdentify**</span><span class="sxs-lookup"><span data-stu-id="7ac44-136">**UnclaimedIdentify**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-137">Estrutura retornada para captura e identificação biométricas.</span><span class="sxs-lookup"><span data-stu-id="7ac44-137">Structure returned for biometric capture and identification.</span></span> <span data-ttu-id="7ac44-138">A identificação determina se um exemplo pode ser associado a um modelo biométrico existente.</span><span class="sxs-lookup"><span data-stu-id="7ac44-138">Identification determines whether a sample can be associated with an existing biometric template.</span></span>

<dl> <dt>

<span data-ttu-id="7ac44-139">**Unidadeid**</span><span class="sxs-lookup"><span data-stu-id="7ac44-139">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-140">A unidade biométrica que gerou o exemplo.</span><span class="sxs-lookup"><span data-stu-id="7ac44-140">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7ac44-141">**Identidade**</span><span class="sxs-lookup"><span data-stu-id="7ac44-141">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-142">Uma estrutura de [**\_ identidade WINBIO**](winbio-identity.md) que contém o GUID ou o SID do usuário que fornece o exemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="7ac44-142">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that contains the GUID or SID of the user providing the biometric sample.</span></span>

</dd> <dt>

<span data-ttu-id="7ac44-143">**Subfator**</span><span class="sxs-lookup"><span data-stu-id="7ac44-143">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-144">Um valor de [**\_ \_ subtipo biométrico WINBIO**](winbio-biometric-subtype-constants.md) que especifica o subfator associado a um exemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="7ac44-144">A [**WINBIO\_BIOMETRIC\_SUBTYPE**](winbio-biometric-subtype-constants.md) value that specifies the sub-factor associated with a biometric sample.</span></span> <span data-ttu-id="7ac44-145">O Windows Biometric Framework (WBF) atualmente dá suporte apenas à captura de impressão digital e usa as constantes a seguir para representar informações de subtipo.</span><span class="sxs-lookup"><span data-stu-id="7ac44-145">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.</span></span>

-   <span data-ttu-id="7ac44-146">WINBIO \_ ANSI \_ 381 \_ pos \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="7ac44-146">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="7ac44-147">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="7ac44-147">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="7ac44-148">Dedo do índice de RH do WINBIO \_ ANSI \_ 381 \_ pos \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ac44-148">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="7ac44-149">WINBIO \_ ANSI \_ 381 \_ pos \_ \_ meio-dedo central de RH \_</span><span class="sxs-lookup"><span data-stu-id="7ac44-149">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="7ac44-150">WINBIO \_ ANSI \_ 381 \_ pos \_ - \_ anel de RH \_</span><span class="sxs-lookup"><span data-stu-id="7ac44-150">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="7ac44-151">WINBIO \_ ANSI \_ 381 \_ pos \_ \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7ac44-151">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="7ac44-152">WINBIO \_ ANSI \_ 381 \_ pos de \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="7ac44-152">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="7ac44-153">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7ac44-153">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="7ac44-154">WINBIO \_ ANSI \_ 381 \_ pos \_ do \_ meio- \_ dedo médio</span><span class="sxs-lookup"><span data-stu-id="7ac44-154">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="7ac44-155">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Ring \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7ac44-155">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="7ac44-156">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7ac44-156">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="7ac44-157">WINBIO \_ ANSI \_ 381 \_ pos \_ com \_ quatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="7ac44-157">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="7ac44-158">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="7ac44-158">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="7ac44-159">WINBIO \_ ANSI \_ 381 \_ pos \_ dois \_ polegares</span><span class="sxs-lookup"><span data-stu-id="7ac44-159">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="7ac44-160">Não tente validar o valor fornecido para o valor de *subfator* .</span><span class="sxs-lookup"><span data-stu-id="7ac44-160">Do not attempt to validate the value supplied for the *SubFactor* value.</span></span> <span data-ttu-id="7ac44-161">O serviço de biometria do Windows validará o valor fornecido antes de passá-lo para sua implementação.</span><span class="sxs-lookup"><span data-stu-id="7ac44-161">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="7ac44-162">Se o valor for **WINBIO \_ subtipo \_ nenhuma \_ informação** ou **\_ subtipo WINBIO \_**, em seguida, valide quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="7ac44-162">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

</dd> <dt>

<span data-ttu-id="7ac44-163">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="7ac44-163">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-164">Um valor **ULONG** que contém informações adicionais sobre a falha ao capturar um exemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="7ac44-164">A **ULONG** value that contains additional information about the failure to capture a biometric sample.</span></span> <span data-ttu-id="7ac44-165">Se a captura tiver sido bem-sucedida, esse parâmetro será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="7ac44-165">If the capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="7ac44-166">Os seguintes valores são definidos para captura de impressão digital:</span><span class="sxs-lookup"><span data-stu-id="7ac44-166">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="7ac44-167">\_FP WINBIO \_ muito \_ alto</span><span class="sxs-lookup"><span data-stu-id="7ac44-167">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="7ac44-168">\_FP WINBIO \_ muito \_ baixo</span><span class="sxs-lookup"><span data-stu-id="7ac44-168">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="7ac44-169">\_FP WINBIO \_ muito \_ à esquerda</span><span class="sxs-lookup"><span data-stu-id="7ac44-169">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="7ac44-170">\_FP WINBIO \_ muito \_ à direita</span><span class="sxs-lookup"><span data-stu-id="7ac44-170">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="7ac44-171">\_FP WINBIO \_ muito \_ rápido</span><span class="sxs-lookup"><span data-stu-id="7ac44-171">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="7ac44-172">\_FP WINBIO \_ muito \_ lento</span><span class="sxs-lookup"><span data-stu-id="7ac44-172">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="7ac44-173">\_ \_ qualidade ruim de FP WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="7ac44-173">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="7ac44-174">\_FP WINBIO \_ muito \_ distorcido</span><span class="sxs-lookup"><span data-stu-id="7ac44-174">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="7ac44-175">\_FP WINBIO \_ muito \_ curto</span><span class="sxs-lookup"><span data-stu-id="7ac44-175">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="7ac44-176">\_ \_ falha na mesclagem de FP WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="7ac44-176">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7ac44-177">**Erro**</span><span class="sxs-lookup"><span data-stu-id="7ac44-177">**Error**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-178">Estrutura que identifica o êxito ou a falha da operação que está sendo monitorada.</span><span class="sxs-lookup"><span data-stu-id="7ac44-178">Structure that identifies the success or failure of the operation being monitored.</span></span>

<dl> <dt>

<span data-ttu-id="7ac44-179">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7ac44-179">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="7ac44-180">Valor **HRESULT** que contém S \_ OK ou um código de erro que resultou de computações executadas pelo Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="7ac44-180">**HRESULT** value that contains S\_OK or an error code that resulted from computations performed by the Windows Biometric Framework.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ac44-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ac44-181">Remarks</span></span>

<span data-ttu-id="7ac44-182">Chame a função [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para registrar uma rotina de retorno de chamada para receber notificações de eventos da Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="7ac44-182">Call the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to register a callback routine to receive event notifications from the Windows Biometric Framework.</span></span> <span data-ttu-id="7ac44-183">O retorno de chamada é uma função personalizada que você deve definir para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ac44-183">The callback is a custom function that you must define for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac44-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ac44-184">Requirements</span></span>



| <span data-ttu-id="7ac44-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac44-185">Requirement</span></span> | <span data-ttu-id="7ac44-186">Valor</span><span class="sxs-lookup"><span data-stu-id="7ac44-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac44-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ac44-187">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac44-188">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7ac44-188">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7ac44-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ac44-189">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac44-190">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7ac44-190">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7ac44-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ac44-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac44-192"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ac44-192"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac44-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ac44-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac44-194">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="7ac44-194">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="7ac44-195">**WinBioRegisterEventMonitor**</span><span class="sxs-lookup"><span data-stu-id="7ac44-195">**WinBioRegisterEventMonitor**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





