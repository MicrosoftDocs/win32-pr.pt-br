---
title: Constantes de WINBIO_OPERATION_TYPE (WinBio \_ Types. h)
description: Especifique o tipo de operação assíncrona que está sendo executada.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086494"
---
# <a name="winbio_operation_type-constants"></a><span data-ttu-id="79c32-103">Constantes do tipo de \_ operação WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="79c32-103">WINBIO\_OPERATION\_TYPE Constants</span></span>

<span data-ttu-id="79c32-104">As constantes a seguir podem ser retornadas pelo Windows Biometric Framework em [**um \_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para especificar o tipo de operação assíncrona que está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="79c32-104">The following constants can be returned by the Windows Biometric Framework in a [**WINBIO\_ASYNC\_RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) to specify the type of asynchronous operation being performed.</span></span>

<dl> <dt>

<span data-ttu-id="79c32-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_operação WINBIO \_ None**</span><span class="sxs-lookup"><span data-stu-id="79c32-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO\_OPERATION\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-106">0</span><span class="sxs-lookup"><span data-stu-id="79c32-106">0</span></span>
</dt> <dt>



<span data-ttu-id="79c32-107">Nenhuma operação foi identificada.</span><span class="sxs-lookup"><span data-stu-id="79c32-107">No operation has been identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_operação WINBIO \_ aberta**</span><span class="sxs-lookup"><span data-stu-id="79c32-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO\_OPERATION\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-109">1</span><span class="sxs-lookup"><span data-stu-id="79c32-109">1</span></span>
</dt> <dt>



<span data-ttu-id="79c32-110">Uma sessão biométrica foi aberta.</span><span class="sxs-lookup"><span data-stu-id="79c32-110">A biometric session was opened.</span></span> <span data-ttu-id="79c32-111">Para obter mais informações, consulte [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span><span class="sxs-lookup"><span data-stu-id="79c32-111">For more information see [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_fechamento da operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO\_OPERATION\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-113">2</span><span class="sxs-lookup"><span data-stu-id="79c32-113">2</span></span>
</dt> <dt>



<span data-ttu-id="79c32-114">Uma sessão biométrica foi fechada.</span><span class="sxs-lookup"><span data-stu-id="79c32-114">A biometric session was closed.</span></span> <span data-ttu-id="79c32-115">Para obter mais informações, consulte [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span><span class="sxs-lookup"><span data-stu-id="79c32-115">For more information, see [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**\_verificação da operação do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO\_OPERATION\_VERIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-117">3</span><span class="sxs-lookup"><span data-stu-id="79c32-117">3</span></span>
</dt> <dt>



<span data-ttu-id="79c32-118">Um exemplo biométrico foi verificado em relação a uma identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="79c32-118">A biometric sample was verified against a user identity.</span></span> <span data-ttu-id="79c32-119">Para obter mais informações, consulte [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span><span class="sxs-lookup"><span data-stu-id="79c32-119">For more information, see [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO de \_ operação de \_ identificação**</span><span class="sxs-lookup"><span data-stu-id="79c32-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO\_OPERATION\_IDENTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-121">4</span><span class="sxs-lookup"><span data-stu-id="79c32-121">4</span></span>
</dt> <dt>



<span data-ttu-id="79c32-122">Um exemplo biométrico foi capturado e comparado a um modelo existente.</span><span class="sxs-lookup"><span data-stu-id="79c32-122">A biometric sample was captured and compared to an existing template.</span></span> <span data-ttu-id="79c32-123">Para obter mais informações, consulte [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span><span class="sxs-lookup"><span data-stu-id="79c32-123">For more information, see [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**\_operação WINBIO \_ localizar \_ sensor**</span><span class="sxs-lookup"><span data-stu-id="79c32-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO\_OPERATION\_LOCATE\_SENSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-125">5</span><span class="sxs-lookup"><span data-stu-id="79c32-125">5</span></span>
</dt> <dt>



<span data-ttu-id="79c32-126">O número de ID de uma unidade biométrica foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="79c32-126">The ID number of a biometric unit was retrieved.</span></span> <span data-ttu-id="79c32-127">Para obter mais informações, consulte [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span><span class="sxs-lookup"><span data-stu-id="79c32-127">For more information, see [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**\_início do \_ registro da operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO\_OPERATION\_ENROLL\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-129">6</span><span class="sxs-lookup"><span data-stu-id="79c32-129">6</span></span>
</dt> <dt>



<span data-ttu-id="79c32-130">Uma sequência de registro biométrica foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="79c32-130">A biometric enrollment sequence was initiated.</span></span> <span data-ttu-id="79c32-131">Para obter mais informações, consulte [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span><span class="sxs-lookup"><span data-stu-id="79c32-131">For more information, see [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**\_captura de \_ registro de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO\_OPERATION\_ENROLL\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-133">7</span><span class="sxs-lookup"><span data-stu-id="79c32-133">7</span></span>
</dt> <dt>



<span data-ttu-id="79c32-134">Um exemplo biométrico foi capturado e adicionado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="79c32-134">A biometric sample was captured and added to the template.</span></span> <span data-ttu-id="79c32-135">Para obter mais informações, consulte [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span><span class="sxs-lookup"><span data-stu-id="79c32-135">For more information, see [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**\_confirmação de \_ registro da operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO\_OPERATION\_ENROLL\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-137">8</span><span class="sxs-lookup"><span data-stu-id="79c32-137">8</span></span>
</dt> <dt>



<span data-ttu-id="79c32-138">Um modelo biométrico pendente foi finalizado.</span><span class="sxs-lookup"><span data-stu-id="79c32-138">A pending biometric template was finalized.</span></span> <span data-ttu-id="79c32-139">Para obter mais informações, consulte [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span><span class="sxs-lookup"><span data-stu-id="79c32-139">For more information, see [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**\_descartar registro de operação WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO\_OPERATION\_ENROLL\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-141">9</span><span class="sxs-lookup"><span data-stu-id="79c32-141">9</span></span>
</dt> <dt>



<span data-ttu-id="79c32-142">Um modelo biométrico pendente foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="79c32-142">A pending biometric template was discarded.</span></span> <span data-ttu-id="79c32-143">Para obter mais informações, consulte [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span><span class="sxs-lookup"><span data-stu-id="79c32-143">For more information, see [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_registros de \_ enumeração de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO\_OPERATION\_ENUM\_ENROLLMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-145">10</span><span class="sxs-lookup"><span data-stu-id="79c32-145">10</span></span>
</dt> <dt>



<span data-ttu-id="79c32-146">Os subfatores para um determinado modelo foram enumerados.</span><span class="sxs-lookup"><span data-stu-id="79c32-146">The sub-factors for a given template were enumerated.</span></span> <span data-ttu-id="79c32-147">Para obter mais informações, consulte [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span><span class="sxs-lookup"><span data-stu-id="79c32-147">For more information, see [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ operação \_ excluir \_ modelo**</span><span class="sxs-lookup"><span data-stu-id="79c32-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO\_OPERATION\_DELETE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-149">11</span><span class="sxs-lookup"><span data-stu-id="79c32-149">11</span></span>
</dt> <dt>



<span data-ttu-id="79c32-150">Um modelo biométrico foi excluído da loja.</span><span class="sxs-lookup"><span data-stu-id="79c32-150">A biometric template was deleted from the store.</span></span> <span data-ttu-id="79c32-151">Para obter mais informações, consulte [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span><span class="sxs-lookup"><span data-stu-id="79c32-151">For more information, see [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_exemplo de \_ captura de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO\_OPERATION\_CAPTURE\_SAMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-153">12</span><span class="sxs-lookup"><span data-stu-id="79c32-153">12</span></span>
</dt> <dt>



<span data-ttu-id="79c32-154">Um exemplo biométrico foi capturado.</span><span class="sxs-lookup"><span data-stu-id="79c32-154">A biometric sample was captured.</span></span> <span data-ttu-id="79c32-155">Para obter mais informações, consulte [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="79c32-155">For more information, see [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**\_propriedade de \_ obtenção de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO\_OPERATION\_GET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-157">13</span><span class="sxs-lookup"><span data-stu-id="79c32-157">13</span></span>
</dt> <dt>



<span data-ttu-id="79c32-158">Uma sessão biométrica, unidade ou propriedade de modelo foi recuperada.</span><span class="sxs-lookup"><span data-stu-id="79c32-158">A biometric session, unit, or template property was retrieved.</span></span> <span data-ttu-id="79c32-159">Para obter mais informações, consulte [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span><span class="sxs-lookup"><span data-stu-id="79c32-159">For more information, see [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_Propriedade do \_ conjunto de operações WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO\_OPERATION\_SET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-161">14</span><span class="sxs-lookup"><span data-stu-id="79c32-161">14</span></span>
</dt> <dt>



<span data-ttu-id="79c32-162">Uma sessão biométrica, unidade, modelo ou propriedade de conta foi definida.</span><span class="sxs-lookup"><span data-stu-id="79c32-162">A biometric session, unit, template, or account property was set.</span></span> <span data-ttu-id="79c32-163">Para obter mais informações, consulte [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span><span class="sxs-lookup"><span data-stu-id="79c32-163">For more information, see [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ evento Get da operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO\_OPERATION\_GET\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-165">15</span><span class="sxs-lookup"><span data-stu-id="79c32-165">15</span></span>
</dt> <dt>



<span data-ttu-id="79c32-166">Não usado.</span><span class="sxs-lookup"><span data-stu-id="79c32-166">Not used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_unidade de \_ bloqueio de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO\_OPERATION\_LOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-168">16</span><span class="sxs-lookup"><span data-stu-id="79c32-168">16</span></span>
</dt> <dt>



<span data-ttu-id="79c32-169">Uma unidade biométrica foi bloqueada para uso exclusivo por uma sessão.</span><span class="sxs-lookup"><span data-stu-id="79c32-169">A biometric unit was locked for exclusive use by a session.</span></span> <span data-ttu-id="79c32-170">Para obter mais informações, consulte [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span><span class="sxs-lookup"><span data-stu-id="79c32-170">For more information, see [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unidade de \_ desbloqueio de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO\_OPERATION\_UNLOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-172">17</span><span class="sxs-lookup"><span data-stu-id="79c32-172">17</span></span>
</dt> <dt>



<span data-ttu-id="79c32-173">O bloqueio de sessão em uma unidade biométrica foi liberado.</span><span class="sxs-lookup"><span data-stu-id="79c32-173">The session lock on a biometric unit was released.</span></span> <span data-ttu-id="79c32-174">Para obter mais informações, consulte [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span><span class="sxs-lookup"><span data-stu-id="79c32-174">For more information, see [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_unidade de \_ controle da operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-176">18</span><span class="sxs-lookup"><span data-stu-id="79c32-176">18</span></span>
</dt> <dt>



<span data-ttu-id="79c32-177">As operações definidas pelo fornecedor foram executadas em uma unidade de controle.</span><span class="sxs-lookup"><span data-stu-id="79c32-177">Vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="79c32-178">Para obter mais informações, consulte [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span><span class="sxs-lookup"><span data-stu-id="79c32-178">For more information, see [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_unidade de controle de operação WINBIO \_ \_ \_ privilegiada**</span><span class="sxs-lookup"><span data-stu-id="79c32-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-180">19</span><span class="sxs-lookup"><span data-stu-id="79c32-180">19</span></span>
</dt> <dt>



<span data-ttu-id="79c32-181">As operações definidas pelo fornecedor com privilégios foram executadas em uma unidade de controle.</span><span class="sxs-lookup"><span data-stu-id="79c32-181">Privileged vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="79c32-182">Para obter mais informações, consulte [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="79c32-182">For more information, see [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ operação \_ abrir \_ estrutura**</span><span class="sxs-lookup"><span data-stu-id="79c32-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO\_OPERATION\_OPEN\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-184">20</span><span class="sxs-lookup"><span data-stu-id="79c32-184">20</span></span>
</dt> <dt>



<span data-ttu-id="79c32-185">Um identificador para a estrutura biométrica foi aberto.</span><span class="sxs-lookup"><span data-stu-id="79c32-185">A handle to the biometric framework was opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**\_estrutura de \_ fechamento da operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO\_OPERATION\_CLOSE\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-187">21</span><span class="sxs-lookup"><span data-stu-id="79c32-187">21</span></span>
</dt> <dt>



<span data-ttu-id="79c32-188">Um identificador para a estrutura biométrica foi fechado.</span><span class="sxs-lookup"><span data-stu-id="79c32-188">A handle to the biometric framework was closed.</span></span> <span data-ttu-id="79c32-189">Para obter mais informações, consulte [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span><span class="sxs-lookup"><span data-stu-id="79c32-189">For more information, see [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_provedores de \_ serviço de enumeração de operação WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO\_OPERATION\_ENUM\_SERVICE\_PROVIDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-191">22</span><span class="sxs-lookup"><span data-stu-id="79c32-191">22</span></span>
</dt> <dt>



<span data-ttu-id="79c32-192">Os provedores de serviços biométricos instalados foram enumerados.</span><span class="sxs-lookup"><span data-stu-id="79c32-192">The installed biometric service providers were enumerated.</span></span> <span data-ttu-id="79c32-193">Para obter mais informações, consulte [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span><span class="sxs-lookup"><span data-stu-id="79c32-193">For more information, see [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ unidades biométricas de enumeração de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO\_OPERATION\_ENUM\_BIOMETRIC\_UNITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-195">23</span><span class="sxs-lookup"><span data-stu-id="79c32-195">23</span></span>
</dt> <dt>



<span data-ttu-id="79c32-196">As unidades biométricas conectadas foram enumeradas.</span><span class="sxs-lookup"><span data-stu-id="79c32-196">The attached biometric units were enumerated.</span></span> <span data-ttu-id="79c32-197">Para obter mais informações, consulte [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span><span class="sxs-lookup"><span data-stu-id="79c32-197">For more information, see [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_banco de \_ dados de enumeração de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO\_OPERATION\_ENUM\_DATABASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-199">24</span><span class="sxs-lookup"><span data-stu-id="79c32-199">24</span></span>
</dt> <dt>



<span data-ttu-id="79c32-200">Os bancos de dados registrados foram enumerados.</span><span class="sxs-lookup"><span data-stu-id="79c32-200">The registered databases were enumerated.</span></span> <span data-ttu-id="79c32-201">Para obter mais informações, consulte [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span><span class="sxs-lookup"><span data-stu-id="79c32-201">For more information, see [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**\_chegada da \_ unidade de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO\_OPERATION\_UNIT\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-203">25</span><span class="sxs-lookup"><span data-stu-id="79c32-203">25</span></span>
</dt> <dt>



<span data-ttu-id="79c32-204">Uma unidade biométrica foi criada.</span><span class="sxs-lookup"><span data-stu-id="79c32-204">A biometric unit was created.</span></span> <span data-ttu-id="79c32-205">Para obter mais informações, consulte [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="79c32-205">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**\_remoção da \_ unidade de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO\_OPERATION\_UNIT\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-207">26</span><span class="sxs-lookup"><span data-stu-id="79c32-207">26</span></span>
</dt> <dt>



<span data-ttu-id="79c32-208">Uma unidade biométrica foi excluída.</span><span class="sxs-lookup"><span data-stu-id="79c32-208">A biometric unit was deleted.</span></span> <span data-ttu-id="79c32-209">Para obter mais informações, consulte [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="79c32-209">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**\_operação WINBIO \_ identificar \_ e \_ liberar o \_ tíquete**</span><span class="sxs-lookup"><span data-stu-id="79c32-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO\_OPERATION\_IDENTIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-211">27</span><span class="sxs-lookup"><span data-stu-id="79c32-211">27</span></span>
</dt> <dt>



<span data-ttu-id="79c32-212">Reservado.</span><span class="sxs-lookup"><span data-stu-id="79c32-212">Reserved.</span></span> <span data-ttu-id="79c32-213">Esse valor tem suporte a partir do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="79c32-213">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_ \_ \_ tíquete de verificação e \_ liberação \_ de operação WINBIO**</span><span class="sxs-lookup"><span data-stu-id="79c32-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO\_OPERATION\_VERIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-215">28</span><span class="sxs-lookup"><span data-stu-id="79c32-215">28</span></span>
</dt> <dt>



<span data-ttu-id="79c32-216">Reservado.</span><span class="sxs-lookup"><span data-stu-id="79c32-216">Reserved.</span></span> <span data-ttu-id="79c32-217">Esse valor tem suporte a partir do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="79c32-217">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_presença do \_ Monitor de operação WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="79c32-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO\_OPERATION\_MONITOR\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-219">29</span><span class="sxs-lookup"><span data-stu-id="79c32-219">29</span></span>
</dt> <dt>



<span data-ttu-id="79c32-220">O mecanismo de reconhecimento facial ou de monitoramento de íris foi ativado.</span><span class="sxs-lookup"><span data-stu-id="79c32-220">The facial recognition or iris monitoring mechanism was turned on.</span></span> <span data-ttu-id="79c32-221">Para obter mais informações, consulte [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span><span class="sxs-lookup"><span data-stu-id="79c32-221">For more information, see [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span></span> <span data-ttu-id="79c32-222">Esse valor tem suporte a partir do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="79c32-222">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79c32-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO \_ de \_ registro de operação \_ Select**</span><span class="sxs-lookup"><span data-stu-id="79c32-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO\_OPERATION\_ENROLL\_SELECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79c32-224">30</span><span class="sxs-lookup"><span data-stu-id="79c32-224">30</span></span>
</dt> <dt>



<span data-ttu-id="79c32-225">Um indivíduo de um grupo de indivíduos que são representados por dados no buffer de exemplo foi especificado como o indivíduo a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="79c32-225">An individual from a group of individuals that are represented by data in the sample buffer was specified as the individual to enroll.</span></span> <span data-ttu-id="79c32-226">Para obter mais informações, consulte [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span><span class="sxs-lookup"><span data-stu-id="79c32-226">For more information, see [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span></span> <span data-ttu-id="79c32-227">Esse valor tem suporte a partir do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="79c32-227">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79c32-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79c32-228">Requirements</span></span>



| <span data-ttu-id="79c32-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="79c32-229">Requirement</span></span> | <span data-ttu-id="79c32-230">Valor</span><span class="sxs-lookup"><span data-stu-id="79c32-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c32-231">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79c32-231">Minimum supported client</span></span><br/> | <span data-ttu-id="79c32-232">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="79c32-232">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="79c32-233">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79c32-233">Minimum supported server</span></span><br/> | <span data-ttu-id="79c32-234">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="79c32-234">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="79c32-235">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79c32-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c32-236"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="79c32-236"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c32-237">Confira também</span><span class="sxs-lookup"><span data-stu-id="79c32-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c32-238">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="79c32-238">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





