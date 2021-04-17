---
title: WINBIO_PRESENCE_PROPERTIES Union (tipos de WinBio \_ . h)
description: Contém valores biométricos que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- API de Windows Biometric Framework de União de WINBIO_PRESENCE_PROPERTIES
- PWINBIO_PRESENCE_PROPERTIES o ponteiro de União Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454795"
---
# <a name="winbio_presence_properties-union"></a><span data-ttu-id="84478-105">União de propriedades de \_ presença de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="84478-105">WINBIO\_PRESENCE\_PROPERTIES union</span></span>

<span data-ttu-id="84478-106">Contém valores biométricos que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.</span><span class="sxs-lookup"><span data-stu-id="84478-106">Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.</span></span>

## <a name="syntax"></a><span data-ttu-id="84478-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84478-107">Syntax</span></span>


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a><span data-ttu-id="84478-108">Membros</span><span class="sxs-lookup"><span data-stu-id="84478-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="84478-109">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="84478-109">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="84478-110">Valores para o local dos recursos faciais que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.</span><span class="sxs-lookup"><span data-stu-id="84478-110">Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="84478-111">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="84478-111">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="84478-112">A posição dentro do quadro da câmera da face da pessoa, em pixels.</span><span class="sxs-lookup"><span data-stu-id="84478-112">The position within the camera frame of the face of the individual, in pixels.</span></span> <span data-ttu-id="84478-113">O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição.</span><span class="sxs-lookup"><span data-stu-id="84478-113">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="84478-114">Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-114">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="84478-115">Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-115">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame .</span></span>

</dd> <dt>

<span data-ttu-id="84478-116">**Distância**</span><span class="sxs-lookup"><span data-stu-id="84478-116">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="84478-117">A distância entre o local real da face e a distância focal ideal para a face.</span><span class="sxs-lookup"><span data-stu-id="84478-117">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="84478-118">Esse valor varia de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="84478-118">This value ranges from -100 to 100.</span></span> <span data-ttu-id="84478-119">0 indica a distância ideal, os valores positivos indicam que o local real da face está muito distante, e os valores negativos indicam que o local real está muito próximo.</span><span class="sxs-lookup"><span data-stu-id="84478-119">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="84478-120">**Íris**</span><span class="sxs-lookup"><span data-stu-id="84478-120">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="84478-121">Valores para o local da íris que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.</span><span class="sxs-lookup"><span data-stu-id="84478-121">Values for iris location that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="84478-122">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="84478-122">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="84478-123">A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="84478-123">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="84478-124">Se o sistema de reconhecimento de íris estiver monitorando apenas um olho, essa posição será da íris desse olho.</span><span class="sxs-lookup"><span data-stu-id="84478-124">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="84478-125">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será da íris do olho no quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-125">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="84478-126">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho correto do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="84478-126">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="84478-127">O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição.</span><span class="sxs-lookup"><span data-stu-id="84478-127">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="84478-128">Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-128">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="84478-129">Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-129">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="84478-130">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="84478-130">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="84478-131">A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="84478-131">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="84478-132">Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio.</span><span class="sxs-lookup"><span data-stu-id="84478-132">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="84478-133">Se o sistema de reconhecimento de íris estiver monitorando os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho à esquerda do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="84478-133">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="84478-134">O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição.</span><span class="sxs-lookup"><span data-stu-id="84478-134">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="84478-135">Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-135">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="84478-136">Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-136">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="84478-137">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="84478-137">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="84478-138">A posição do centro de um dos Pupils do indivíduo a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="84478-138">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="84478-139">Se o sistema de reconhecimento de íris estiver monitorando apenas um dos olhos, essa posição será do centro da pupilidade desse olho.</span><span class="sxs-lookup"><span data-stu-id="84478-139">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="84478-140">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será do centro da Pupil do olho no quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="84478-140">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="84478-141">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro do Pupil do lado direito do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="84478-141">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="84478-142">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="84478-142">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="84478-143">A posição do centro de um dos Pupils do indivíduo a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="84478-143">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="84478-144">Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio.</span><span class="sxs-lookup"><span data-stu-id="84478-144">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="84478-145">Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro dos Pupil do lado esquerdo do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="84478-145">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="84478-146">**Distância**</span><span class="sxs-lookup"><span data-stu-id="84478-146">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="84478-147">A distância entre o local real da íris e a distância focal ideal para a íris.</span><span class="sxs-lookup"><span data-stu-id="84478-147">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="84478-148">Esse valor varia de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="84478-148">This value ranges from -100 to 100.</span></span> <span data-ttu-id="84478-149">0 indica a distância ideal, os valores positivos indicam que o local real da íris está muito distante, e os valores negativos indicam que o local real está muito próximo.</span><span class="sxs-lookup"><span data-stu-id="84478-149">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84478-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84478-150">Requirements</span></span>



| <span data-ttu-id="84478-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="84478-151">Requirement</span></span> | <span data-ttu-id="84478-152">Valor</span><span class="sxs-lookup"><span data-stu-id="84478-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84478-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84478-153">Minimum supported client</span></span><br/> | <span data-ttu-id="84478-154">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="84478-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="84478-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84478-155">Minimum supported server</span></span><br/> | <span data-ttu-id="84478-156">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="84478-156">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="84478-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84478-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="84478-158"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="84478-158"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





