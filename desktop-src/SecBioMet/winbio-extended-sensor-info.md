---
title: Estrutura de WINBIO_EXTENDED_SENSOR_INFO (WinBio \_ Types. h)
description: Contém informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_SENSOR_INFO
- Ponteiro de estrutura de PWINBIO_EXTENDED_SENSOR_INFO Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918095"
---
# <a name="winbio_extended_sensor_info-structure"></a><span data-ttu-id="467f9-105">\_Estrutura de \_ informações do sensor ESTENDIdo WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="467f9-105">WINBIO\_EXTENDED\_SENSOR\_INFO structure</span></span>

<span data-ttu-id="467f9-106">Contém informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="467f9-106">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="467f9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="467f9-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a><span data-ttu-id="467f9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="467f9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="467f9-109">**GenericSensorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="467f9-109">**GenericSensorCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-110">Os recursos genéricos do componente de sensor que está conectado a uma unidade biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="467f9-110">The generic capabilities of the sensor component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="467f9-111">**Fator**</span><span class="sxs-lookup"><span data-stu-id="467f9-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-112">O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador do sensor.</span><span class="sxs-lookup"><span data-stu-id="467f9-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter.</span></span> <span data-ttu-id="467f9-113">Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de **\_ \_ \_ informações do sensor estendido WINBIO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="467f9-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_SENSOR\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="467f9-114">**Específicas**</span><span class="sxs-lookup"><span data-stu-id="467f9-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-115">Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a um fator biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="467f9-115">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="467f9-116">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="467f9-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="467f9-117">Reserved.</span></span> <span data-ttu-id="467f9-118">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="467f9-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="467f9-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="467f9-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-120">Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada aos recursos faciais.</span><span class="sxs-lookup"><span data-stu-id="467f9-120">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="467f9-121">**Quadros**</span><span class="sxs-lookup"><span data-stu-id="467f9-121">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-122">O tamanho do quadro da câmera, indicado como um comprimento e uma largura em pixels pelos membros **direito** e **inferior** da estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="467f9-122">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="467f9-123">O ponto (0, 0) representa o canto superior esquerdo do quadro.</span><span class="sxs-lookup"><span data-stu-id="467f9-123">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="467f9-124">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="467f9-124">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-125">O deslocamento do quadro da câmera para a face da câmera de vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="467f9-125">The offset of the camera frame for the face from the video camera, in pixels.</span></span> <span data-ttu-id="467f9-126">Um valor de (0, 0) indica que o quadro da câmera para a face e a câmera de vídeo se sobrepõem completamente.</span><span class="sxs-lookup"><span data-stu-id="467f9-126">A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="467f9-127">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="467f9-127">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-128">A orientação preferida para a câmera.</span><span class="sxs-lookup"><span data-stu-id="467f9-128">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="467f9-129">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="467f9-129">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-130">Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a padrões de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="467f9-130">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="467f9-131">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="467f9-131">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-132">Reservado.</span><span class="sxs-lookup"><span data-stu-id="467f9-132">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="467f9-133">**Íris**</span><span class="sxs-lookup"><span data-stu-id="467f9-133">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-134">Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a padrões de íris.</span><span class="sxs-lookup"><span data-stu-id="467f9-134">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="467f9-135">**Quadros**</span><span class="sxs-lookup"><span data-stu-id="467f9-135">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-136">O tamanho do quadro da câmera, indicado como um comprimento e uma largura em pixels pelos membros **direito** e **inferior** da estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="467f9-136">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="467f9-137">O ponto (0, 0) representa o canto superior esquerdo do quadro.</span><span class="sxs-lookup"><span data-stu-id="467f9-137">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="467f9-138">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="467f9-138">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-139">O deslocamento do quadro da câmera da íris da câmera de vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="467f9-139">The offset of the camera frame for the iris from the video camera, in pixels.</span></span> <span data-ttu-id="467f9-140">Um valor de (0, 0) indica que o quadro da câmera para a íris e a câmera de vídeo se sobrepõem completamente.</span><span class="sxs-lookup"><span data-stu-id="467f9-140">A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="467f9-141">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="467f9-141">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-142">A orientação preferida para a câmera.</span><span class="sxs-lookup"><span data-stu-id="467f9-142">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="467f9-143">**Voz**</span><span class="sxs-lookup"><span data-stu-id="467f9-143">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-144">Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a padrões de voz.</span><span class="sxs-lookup"><span data-stu-id="467f9-144">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="467f9-145">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="467f9-145">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="467f9-146">Reservado.</span><span class="sxs-lookup"><span data-stu-id="467f9-146">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="467f9-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="467f9-147">Requirements</span></span>



| <span data-ttu-id="467f9-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="467f9-148">Requirement</span></span> | <span data-ttu-id="467f9-149">Valor</span><span class="sxs-lookup"><span data-stu-id="467f9-149">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="467f9-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="467f9-150">Minimum supported client</span></span><br/> | <span data-ttu-id="467f9-151">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="467f9-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="467f9-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="467f9-152">Minimum supported server</span></span><br/> | <span data-ttu-id="467f9-153">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="467f9-153">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="467f9-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="467f9-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="467f9-155"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="467f9-155"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="467f9-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="467f9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467f9-157">**\_Constantes de recurso WINBIO**</span><span class="sxs-lookup"><span data-stu-id="467f9-157">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="467f9-158">**\_Constantes de tipo BIOMÉTRICO WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="467f9-158">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="467f9-159">**Constantes de orientação de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="467f9-159">**WINBIO\_ORIENTATION Constants**</span></span>](winbio-orientation-constants.md)
</dt> </dl>

 

